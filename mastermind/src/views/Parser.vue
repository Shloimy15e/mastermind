<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800 relative overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute inset-0 opacity-20">
        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-r from-purple-500/8 via-blue-500/8 to-indigo-500/8"></div>
      </div>
      
      <!-- Floating Elements -->
      <div class="absolute inset-0">
        <div class="absolute top-[20%] left-[8%] w-16 h-16 bg-gradient-to-br from-blue-400/15 to-indigo-600/15 rounded-xl opacity-40 animate-float transform rotate-45"></div>
        <div class="absolute top-[40%] right-[15%] w-20 h-20 bg-gradient-to-br from-indigo-400/15 to-purple-600/15 rounded-2xl opacity-30 animate-float-delay"></div>
        <div class="absolute bottom-[30%] left-[20%] w-12 h-12 bg-gradient-to-br from-purple-400/15 to-pink-600/15 rounded-full opacity-25 animate-float"></div>
        <div class="absolute top-[10%] right-[25%] w-14 h-14 bg-gradient-to-br from-indigo-400/10 to-blue-600/10 rounded-lg opacity-20 animate-float-delay"></div>
      </div>
    </div>

    <div class="relative z-10 flex flex-col min-h-screen">
      <!-- Content Container -->
      <div class="flex-1 flex flex-col items-center justify-start gap-16 px-6 py-20">
        
        <!-- Header Section -->
        <div class="flex flex-col items-center gap-8 text-center max-w-3xl">
          <div class="inline-flex items-center px-5 py-2.5 rounded-full bg-white/90 dark:bg-gray-800/90 backdrop-blur-xl border border-gray-200/60 dark:border-gray-700/60 shadow-lg">
            <div class="w-1.5 h-1.5 bg-gradient-to-r from-indigo-500 to-purple-500 rounded-full animate-pulse mr-2.5"></div>
            <span class="text-xs font-medium text-gray-700 dark:text-gray-300 tracking-wide">MATH PARSER ENGINE</span>
          </div>
          
          <h1 class="text-4xl sm:text-5xl lg:text-6xl font-black leading-[0.9] tracking-tight">
            <span class="block bg-gradient-to-r from-gray-900 via-indigo-800 to-purple-900 dark:from-white dark:via-indigo-200 dark:to-purple-200 bg-clip-text text-transparent">
              Advanced Math
            </span>
            <span class="block bg-gradient-to-r from-indigo-800 via-purple-800 to-pink-900 dark:from-indigo-200 dark:via-purple-200 dark:to-pink-200 bg-clip-text text-transparent">
              Calculator
            </span>
          </h1>
          
          <p class="text-lg sm:text-xl leading-[1.6] font-light text-gray-600 dark:text-gray-300">
            Parse and evaluate complex mathematical expressions with 
            <span class="font-semibold text-indigo-600 dark:text-indigo-400">operator precedence</span> and 
            <span class="font-semibold text-purple-600 dark:text-purple-400">parentheses support</span>
          </p>
        </div>

        <!-- Main Calculator Interface -->
        <div class="w-full max-w-3xl">
          <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 shadow-xl p-8">
            <!-- Input Section -->
            <div class="flex flex-col gap-8">
              <div class="flex flex-col gap-3">
                <label class="text-sm font-semibold text-gray-700 dark:text-gray-300">
                  Enter Mathematical Expression
                </label>
                <div class="flex gap-4">
                  <div class="flex-1 relative">
                    <input 
                      v-model="equation" 
                      type="text"
                      placeholder="e.g., 2 * 3 + 6 * (4 - 1)" 
                      @keyup.enter="calculateResult"
                      class="w-full px-4 py-4 text-lg bg-white/90 dark:bg-gray-900/90 border-2 border-gray-200/60 dark:border-gray-600/60 rounded-xl focus:outline-none focus:border-indigo-500 dark:focus:border-indigo-400 focus:ring-4 focus:ring-indigo-500/20 transition-all duration-300 text-gray-900 dark:text-white placeholder-gray-500 dark:placeholder-gray-400"
                    />
                    <div class="absolute inset-0 rounded-xl bg-gradient-to-r from-indigo-500/5 to-purple-500/5 pointer-events-none"></div>
                  </div>
                  <button 
                    @click="calculateResult"
                    class="group relative px-8 py-4 bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-700 hover:to-purple-700 text-white font-semibold rounded-xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-lg focus:outline-none focus:ring-4 focus:ring-indigo-500/50"
                  >
                    <span class="relative z-10">Calculate</span>
                    <div class="absolute inset-0 rounded-xl bg-gradient-to-r from-white/20 to-white/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                  </button>
                </div>
              </div>

              <!-- Result Section -->
              <div v-if="result !== null">
                <div class="bg-gradient-to-r from-green-50 to-emerald-50 dark:from-green-900/20 dark:to-emerald-900/20 rounded-xl p-6 border border-green-200/50 dark:border-green-700/50">
                  <div class="flex items-center justify-between">
                    <div class="flex items-center gap-3">
                      <div class="w-8 h-8 bg-gradient-to-r from-green-500 to-emerald-500 rounded-lg flex items-center justify-center">
                        <svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 20 20">
                          <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                        </svg>
                      </div>
                      <span class="text-sm font-medium text-green-700 dark:text-green-300">Result</span>
                    </div>
                  </div>
                  <div class="mt-4">
                    <p class="text-2xl font-bold text-green-800 dark:text-green-200 font-mono">
                      {{ equation }} = {{ result }}
                    </p>
                  </div>
                </div>
              </div>

              <!-- Error Section -->
              <div v-if="errorMessage">
                <div class="bg-gradient-to-r from-red-50 to-pink-50 dark:from-red-900/20 dark:to-pink-900/20 rounded-xl p-6 border border-red-200/50 dark:border-red-700/50">
                  <div class="flex items-center gap-3">
                    <div class="w-8 h-8 bg-gradient-to-r from-red-500 to-pink-500 rounded-lg flex items-center justify-center">
                      <svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7 4a1 1 0 11-2 0 1 1 0 012 0zm-1-9a1 1 0 00-1 1v4a1 1 0 102 0V6a1 1 0 00-1-1z" clip-rule="evenodd"/>
                      </svg>
                    </div>
                    <span class="text-sm font-medium text-red-700 dark:text-red-300">Error</span>
                  </div>
                  <div class="mt-3">
                    <p class="text-red-800 dark:text-red-200">{{ errorMessage }}</p>
                  </div>
                </div>
              </div>

              <!-- Examples Section -->
              <div class="flex flex-col gap-4">
                <h3 class="text-lg font-semibold text-gray-800 dark:text-gray-200">Try these examples:</h3>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                  <button 
                    v-for="example in examples" 
                    :key="example"
                    @click="equation = example"
                    class="group text-left p-4 bg-gray-50/80 dark:bg-gray-700/50 rounded-lg border border-gray-200/50 dark:border-gray-600/50 hover:bg-indigo-50/80 dark:hover:bg-indigo-900/20 hover:border-indigo-300/50 dark:hover:border-indigo-600/50 transition-all duration-300"
                  >
                    <code class="text-sm font-mono text-gray-700 dark:text-gray-300 group-hover:text-indigo-700 dark:group-hover:text-indigo-300">{{ example }}</code>
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Features Section -->
        <div class="flex flex-col items-center gap-12 w-full max-w-4xl">
          <h2 class="text-3xl font-bold text-gray-900 dark:text-white">Parser Features</h2>
          
          <div class="grid grid-cols-2 md:grid-cols-4 gap-6 w-full">
            <div class="group">
              <div class="flex flex-col items-center gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div class="relative w-12 h-12">
                  <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-xl rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                  <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full flex items-center justify-center">
                    <span class="text-xl font-bold text-blue-600 dark:text-blue-400">( )</span>
                  </div>
                </div>
                <div class="flex flex-col items-center gap-2 text-center">
                  <h3 class="font-bold text-gray-900 dark:text-white">Parentheses</h3>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Supports nested parentheses for complex expressions</p>
                </div>
              </div>
            </div>

            <div class="group">
              <div class="flex flex-col items-center gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div class="relative w-12 h-12">
                  <div class="absolute inset-0 bg-gradient-to-r from-indigo-500 to-purple-500 rounded-xl rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                  <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full flex items-center justify-center">
                    <span class="text-xl font-bold text-indigo-600 dark:text-indigo-400">+-*/</span>
                  </div>
                </div>
                <div class="flex flex-col items-center gap-2 text-center">
                  <h3 class="font-bold text-gray-900 dark:text-white">Basic Operations</h3>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Add, subtract, multiply, and divide with precision</p>
                </div>
              </div>
            </div>

            <div class="group">
              <div class="flex flex-col items-center gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div class="relative w-12 h-12">
                  <div class="absolute inset-0 bg-gradient-to-r from-purple-500 to-pink-500 rounded-xl rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                  <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full flex items-center justify-center">
                    <span class="text-xl font-bold text-purple-600 dark:text-purple-400">^</span>
                  </div>
                </div>
                <div class="flex flex-col items-center gap-2 text-center">
                  <h3 class="font-bold text-gray-900 dark:text-white">Exponents</h3>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Power operations with proper precedence</p>
                </div>
              </div>
            </div>

            <div class="group">
              <div class="flex flex-col items-center gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div class="relative w-12 h-12">
                  <div class="absolute inset-0 bg-gradient-to-r from-green-500 to-emerald-500 rounded-xl rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                  <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full flex items-center justify-center">
                    <span class="text-lg font-bold text-green-600 dark:text-green-400">RPN</span>
                  </div>
                </div>
                <div class="flex flex-col items-center gap-2 text-center">
                  <h3 class="font-bold text-gray-900 dark:text-white">Algorithm</h3>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Uses shunting-yard algorithm for accuracy</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const equation = ref('')
const result = ref<number | null>(null)
const errorMessage = ref('')

// Example equations for users to try
const examples = ref([
  '2 + 3 * 4',
  '(2 + 3) * 4',
  '2 ^ 3 + 1',
  '10 / (2 + 3)'
])

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

<style scoped>
/* Animations */
@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(45deg); }
  50% { transform: translateY(-6px) rotate(45deg); }
}

@keyframes float-delay {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-8px); }
}

.animate-float {
  animation: float 3.5s ease-in-out infinite;
}

.animate-float-delay {
  animation: float-delay 4.2s ease-in-out infinite;
}

/* Smooth Transitions */
* {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}
</style>