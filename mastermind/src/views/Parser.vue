<template>
  <div class="w-full mx-auto p-5 pt-32 text-center flex flex-col items-center">
    <h1 class="text-2xl font-bold mb-8 text-gray-800">Math Equation Parser</h1>
    <div class="flex gap-3 mb-5">
      <input 
        v-model="equation" 
        type="text"
        placeholder="Enter a math equation (e.g. 2 * 3 + 6)" 
        @keyup.enter="calculateResult"
        class="flex-1 p-3 text-base border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-green-500 focus:border-transparent"
      />
      <button 
        @click="calculateResult"
        class="px-5 py-3 bg-green-600 text-white border-none rounded-md cursor-pointer text-base transition-colors hover:bg-green-700 focus:outline-none focus:ring-2 focus:ring-green-500 focus:ring-offset-2"
      >
        Calculate
      </button>
    </div>
    <div v-if="result !== null" class="mt-5 p-4 bg-gray-100 rounded-md shadow-sm">
      <p class="text-lg font-semibold m-0">{{ equation }} = {{ result }}</p>
    </div>
    <div v-if="errorMessage" class="text-red-600 mt-3">
      <p>{{ errorMessage }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const equation = ref('')
const result = ref<number | null>(null)
const errorMessage = ref('')

/**
 * Tokenizes the input equation string into numbers and operators
 */
function tokenize(expr: string): string[] {
  // Replace all whitespace
  expr = expr.replace(/\s+/g, '')
  
  // Add spaces around operators and parentheses for easier splitting
  expr = expr.replace(/([+\-*/()^])/g, ' $1 ')
  
  // Split by spaces and filter out empty strings
  return expr.split(' ').filter(token => token.length > 0)
}

/**
 * Determines if a token is an operator
 */
function isOperator(token: string): boolean {
  return ['+', '-', '*', '/', '^'].includes(token)
}

/**
 * Returns the precedence of an operator
 */
function getPrecedence(operator: string): number {
  if (operator === '+' || operator === '-') return 1
  if (operator === '*' || operator === '/') return 2
  if (operator === '^') return 3
  return 0
}

/**
 * Converts infix notation to postfix (Reverse Polish Notation)
 */
function infixToPostfix(tokens: string[]): string[] {
  const output: string[] = []
  const operatorStack: string[] = []

  for (const token of tokens) {
    if (!isNaN(Number(token))) {
      // If token is a number, add to output
      output.push(token)
    } else if (token === '(') {
      // If token is an opening parenthesis, push to stack
      operatorStack.push(token)
    } else if (token === ')') {
      // If token is a closing parenthesis, pop operators from stack and add to output until matching opening parenthesis
      while (operatorStack.length > 0 && operatorStack[operatorStack.length - 1] !== '(') {
        output.push(operatorStack.pop()!)
      }
      // Remove the opening parenthesis
      operatorStack.pop()
    } else if (isOperator(token)) {
      // If token is an operator
      while (
        operatorStack.length > 0 &&
        operatorStack[operatorStack.length - 1] !== '(' &&
        getPrecedence(operatorStack[operatorStack.length - 1]) >= getPrecedence(token)
      ) {
        output.push(operatorStack.pop()!)
      }
      operatorStack.push(token)
    }
  }

  // Pop any remaining operators from the stack and add to output
  while (operatorStack.length > 0) {
    output.push(operatorStack.pop()!)
  }

  return output
}

/**
 * Evaluates a postfix expression
 */
function evaluatePostfix(postfix: string[]): number {
  const stack: number[] = []

  for (const token of postfix) {
    if (!isNaN(Number(token))) {
      // If token is a number, push to stack
      stack.push(Number(token))
    } else if (isOperator(token)) {
      // If token is an operator, pop two values from stack, apply operator, and push result back
      const b = stack.pop()!
      const a = stack.pop()!
      
      switch (token) {
        case '+': stack.push(a + b); break
        case '-': stack.push(a - b); break
        case '*': stack.push(a * b); break
        case '/': stack.push(a / b); break
        case '^': stack.push(Math.pow(a, b)); break
      }
    }
  }

  // The final result should be the only item in the stack
  return stack[0]
}

/**
 * Validates the input equation
 */
function validateEquation(eq: string): boolean {
  // Basic validation to ensure balanced parentheses and valid operators
  if (!eq.trim()) return false
  
  // Check for balanced parentheses
  let parenCount = 0
  for (const char of eq) {
    if (char === '(') parenCount++
    if (char === ')') parenCount--
    if (parenCount < 0) return false // Unbalanced closing parenthesis
  }
  if (parenCount !== 0) return false // Unbalanced opening parenthesis
  
  // Check for invalid character sequences like consecutive operators
  if (/[+\-*/^]{2,}/.test(eq.replace(/\s+/g, ''))) return false
  
  return true
}

/**
 * Calculates the result of the equation
 */
function calculateResult(): void {
  errorMessage.value = ''
  
  if (!equation.value.trim()) {
    errorMessage.value = 'Please enter an equation'
    result.value = null
    return
  }

  try {
    if (!validateEquation(equation.value)) {
      errorMessage.value = 'Invalid equation format'
      result.value = null
      return
    }
    
    const tokens = tokenize(equation.value)
    const postfix = infixToPostfix(tokens)
    result.value = evaluatePostfix(postfix)
    
    // Check for invalid results
    if (isNaN(result.value) || !isFinite(result.value)) {
      errorMessage.value = 'Calculation resulted in an invalid value'
      result.value = null
    }
  } catch (error) {
    errorMessage.value = 'Error calculating result: ' + (error as Error).message
    result.value = null
  }
}
</script>