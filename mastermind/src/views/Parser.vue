<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800 relative overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute inset-0 opacity-20">
        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-r from-indigo-500/8 via-purple-500/8 to-blue-500/8"></div>
      </div>
      
      <!-- Floating Elements -->
      <div class="absolute inset-0">
        <div class="absolute top-[12%] left-[8%] w-20 h-20 bg-gradient-to-br from-indigo-400/15 to-purple-600/15 rounded-2xl opacity-40 animate-float transform rotate-12"></div>
        <div class="absolute top-[35%] right-[10%] w-16 h-16 bg-gradient-to-br from-purple-400/15 to-pink-600/15 rounded-full opacity-30 animate-float-delay"></div>
        <div class="absolute bottom-[20%] left-[15%] w-24 h-24 bg-gradient-to-br from-pink-400/15 to-blue-600/15 rounded-xl opacity-25 animate-float"></div>
      </div>
    </div>

    <div class="relative z-10 min-h-screen grid grid-rows-[auto_1fr_auto] gap-0">
      <!-- Content Container -->
      <div class="grid place-items-center gap-16 px-6 py-12">
        
        <!-- Header Section -->
        <div class="grid place-items-center gap-8 text-center max-w-4xl">
          <div class="inline-flex items-center px-5 py-2.5 rounded-full bg-white/90 dark:bg-gray-800/90 backdrop-blur-xl border border-gray-200/60 dark:border-gray-700/60 shadow-lg">
            <div class="w-1.5 h-1.5 bg-gradient-to-r from-indigo-500 to-purple-500 rounded-full animate-pulse mr-2.5"></div>
            <span class="text-xs font-medium text-gray-700 dark:text-gray-300 tracking-wide">MATHEMATICAL COMPUTATION</span>
          </div>
          
          <h1 class="text-5xl sm:text-6xl lg:text-7xl font-black leading-[0.9] tracking-tight">
            <span class="block bg-gradient-to-r from-gray-900 via-indigo-800 to-purple-900 dark:from-white dark:via-indigo-200 dark:to-purple-200 bg-clip-text text-transparent">
              Expression
            </span>
            <span class="block bg-gradient-to-r from-purple-800 via-pink-800 to-indigo-900 dark:from-purple-200 dark:via-pink-200 dark:to-indigo-200 bg-clip-text text-transparent">
              Calculator
            </span>
          </h1>
          
          <p class="text-xl sm:text-2xl leading-[1.6] font-light text-gray-600 dark:text-gray-300">
            Advanced <span class="font-semibold text-indigo-600 dark:text-indigo-400">mathematical parser</span> with 
            <span class="font-semibold text-purple-600 dark:text-purple-400">smart evaluation</span> 
            and proper order of operations.
          </p>
        </div>

        <!-- Calculator Interface -->
        <div class="grid place-items-center gap-12 w-full max-w-4xl">
          
          <!-- Main Calculator -->
          <div class="grid gap-8 w-full max-w-2xl">
            <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 shadow-xl p-8">
              <div class="grid gap-8">
                <!-- Input Section -->
                <div class="grid gap-4">
                  <label class="text-lg font-semibold text-gray-900 dark:text-white">Mathematical Expression</label>
                  <div class="relative">
                    <input
                      v-model="expression"
                      type="text"
                      placeholder="Enter expression (e.g., 2 + 3 * (4 - 1))"
                      class="w-full px-6 py-4 text-lg bg-white/90 dark:bg-gray-700/90 border border-gray-300 dark:border-gray-600 rounded-xl focus:ring-4 focus:ring-indigo-500/50 focus:border-indigo-500 dark:focus:border-indigo-400 transition-all duration-200 placeholder-gray-500 dark:placeholder-gray-400 text-gray-900 dark:text-white"
                      @keyup.enter="calculateExpression"
                    />
                    <div class="absolute right-4 top-1/2 -translate-y-1/2">
                      <IconEqual class="w-5 h-5 text-gray-400" />
                    </div>
                  </div>
                </div>

                <!-- Result Section -->
                <div class="grid gap-4">
                  <label class="text-lg font-semibold text-gray-900 dark:text-white">Result</label>
                  <div class="relative">
                    <div 
                      class="w-full px-6 py-4 text-lg bg-gray-100/90 dark:bg-gray-600/90 border border-gray-300 dark:border-gray-600 rounded-xl text-gray-900 dark:text-white font-mono"
                      :class="result ? 'text-indigo-700 dark:text-indigo-300' : 'text-gray-500 dark:text-gray-400'"
                    >
                      {{ result || 'Enter an expression to see the result' }}
                    </div>
                    <div class="absolute right-4 top-1/2 -translate-y-1/2">
                      <IconCheck v-if="result && !error" class="w-5 h-5 text-green-500" />
                      <IconX v-if="error" class="w-5 h-5 text-red-500" />
                    </div>
                  </div>
                </div>

                <!-- Action Buttons -->
                <div class="grid grid-cols-2 gap-4">
                  <button
                    @click="calculateExpression"
                    :disabled="!expression.trim()"
                    class="group relative px-6 py-3 bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-700 hover:to-purple-700 disabled:from-gray-400 disabled:to-gray-500 text-white font-semibold rounded-xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-lg disabled:transform-none disabled:shadow-none focus:outline-none focus:ring-4 focus:ring-indigo-500/50"
                  >
                    <span class="relative z-10 grid grid-cols-[auto_auto] gap-2 items-center justify-center">
                      <IconCalculator class="w-5 h-5" />
                      <span>Calculate</span>
                    </span>
                    <div class="absolute inset-0 rounded-xl bg-gradient-to-r from-white/20 to-white/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                  </button>
                  
                  <button
                    @click="clearAll"
                    class="group relative px-6 py-3 bg-gradient-to-r from-gray-600 to-slate-600 hover:from-gray-700 hover:to-slate-700 text-white font-semibold rounded-xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-lg focus:outline-none focus:ring-4 focus:ring-gray-500/50"
                  >
                    <span class="relative z-10 grid grid-cols-[auto_auto] gap-2 items-center justify-center">
                      <IconTrash class="w-5 h-5" />
                      <span>Clear</span>
                    </span>
                    <div class="absolute inset-0 rounded-xl bg-gradient-to-r from-white/20 to-white/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- Examples Section -->
          <div class="grid gap-8 w-full">
            <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white text-center">Example Expressions</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
              <div 
                v-for="example in examples" 
                :key="example.expression"
                @click="setExample(example.expression)"
                class="group cursor-pointer"
              >
                <div class="bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                  <div class="grid gap-4">
                    <div class="grid gap-2">
                      <h3 class="font-bold text-gray-900 dark:text-white">{{ example.title }}</h3>
                      <p class="text-sm text-gray-600 dark:text-gray-300">{{ example.description }}</p>
                    </div>
                    
                    <div class="grid gap-2">
                      <div class="font-mono text-sm bg-gray-100 dark:bg-gray-700 rounded-lg p-3 text-indigo-700 dark:text-indigo-300">
                        {{ example.expression }}
                      </div>
                      <div class="font-mono text-sm text-gray-600 dark:text-gray-400">
                        = {{ example.result }}
                      </div>
                    </div>
                    
                    <div class="grid grid-cols-[auto_1fr] gap-2 items-center">
                      <IconClick class="w-4 h-4 text-gray-400" />
                      <span class="text-xs text-gray-500 dark:text-gray-400">Click to try</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Features Section -->
          <div class="grid gap-8 w-full max-w-4xl">
            <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white text-center">Parser Features</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div class="grid gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-8 border border-gray-200/40 dark:border-gray-700/40 shadow-md">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white grid grid-cols-[auto_1fr] gap-3 items-center">
                  <IconMathSymbols class="w-6 h-6 text-indigo-600 dark:text-indigo-400" />
                  <span>Supported Operations</span>
                </h3>
                <div class="grid gap-3 text-sm text-gray-600 dark:text-gray-300">
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                    <span class="font-mono bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-indigo-700 dark:text-indigo-300">+</span>
                    <span>Addition</span>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                    <span class="font-mono bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-indigo-700 dark:text-indigo-300">-</span>
                    <span>Subtraction</span>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                    <span class="font-mono bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-indigo-700 dark:text-indigo-300">*</span>
                    <span>Multiplication</span>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                    <span class="font-mono bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-indigo-700 dark:text-indigo-300">/</span>
                    <span>Division</span>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                    <span class="font-mono bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-indigo-700 dark:text-indigo-300">( )</span>
                    <span>Parentheses for grouping</span>
                  </div>
                </div>
              </div>
              
              <div class="grid gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-8 border border-gray-200/40 dark:border-gray-700/40 shadow-md">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white grid grid-cols-[auto_1fr] gap-3 items-center">
                  <IconBrain class="w-6 h-6 text-purple-600 dark:text-purple-400" />
                  <span>Smart Features</span>
                </h3>
                <div class="grid gap-3 text-sm text-gray-600 dark:text-gray-300">
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-start">
                    <IconCheck class="w-4 h-4 text-green-500 mt-0.5" />
                    <span>Proper order of operations (PEMDAS/BODMAS)</span>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-start">
                    <IconCheck class="w-4 h-4 text-green-500 mt-0.5" />
                    <span>Nested parentheses support</span>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-start">
                    <IconCheck class="w-4 h-4 text-green-500 mt-0.5" />
                    <span>Decimal number precision</span>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-start">
                    <IconCheck class="w-4 h-4 text-green-500 mt-0.5" />
                    <span>Error handling and validation</span>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-start">
                    <IconCheck class="w-4 h-4 text-green-500 mt-0.5" />
                    <span>Real-time calculation</span>
                  </div>
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
import { 
  IconCalculator, 
  IconTrash, 
  IconEqual, 
  IconCheck, 
  IconX, 
  IconClick,
  IconMathSymbols,
  IconBrain
} from '@tabler/icons-vue'

const expression = ref('')
const result = ref('')
const error = ref(false)

const examples = [
  {
    title: "Basic Arithmetic",
    description: "Simple addition and multiplication",
    expression: "2 + 3 * 4",
    result: "14"
  },
  {
    title: "Parentheses Grouping",
    description: "Changing order with parentheses",
    expression: "(2 + 3) * 4",
    result: "20"
  },
  {
    title: "Complex Expression",
    description: "Nested operations",
    expression: "10 * (5 + 3) / (4 - 2)",
    result: "40"
  },
  {
    title: "Decimal Numbers",
    description: "Working with decimals",
    expression: "3.14 * 2 + 1.5",
    result: "7.78"
  },
  {
    title: "Division with Precision",
    description: "Accurate division results",
    expression: "22 / 7",
    result: "3.142857142857143"
  },
  {
    title: "Nested Parentheses",
    description: "Multiple levels of grouping",
    expression: "((2 + 3) * (4 + 1)) / 5",
    result: "5"
  }
]

const setExample = (expr: string) => {
  expression.value = expr
  calculateExpression()
}

const clearAll = () => {
  expression.value = ''
  result.value = ''
  error.value = false
}

const calculateExpression = () => {
  if (!expression.value.trim()) {
    result.value = ''
    error.value = false
    return
  }

  try {
    // Basic expression parser
    const sanitized = expression.value.replace(/[^0-9+\-*/().\s]/g, '')
    
    if (!sanitized.trim()) {
      throw new Error('Invalid characters in expression')
    }
    
    // Check for balanced parentheses
    let parenCount = 0
    for (const char of sanitized) {
      if (char === '(') parenCount++
      if (char === ')') parenCount--
      if (parenCount < 0) throw new Error('Unmatched parentheses')
    }
    if (parenCount !== 0) throw new Error('Unmatched parentheses')
    
    // Use Function constructor for safe evaluation (better than eval)
    const func = new Function('return ' + sanitized)
    const resultValue = func()
    
    if (typeof resultValue !== 'number' || !isFinite(resultValue)) {
      throw new Error('Invalid result')
    }
    
    result.value = resultValue.toString()
    error.value = false
  } catch (err) {
    result.value = 'Error: Invalid expression'
    error.value = true
  }
}
</script>

<style scoped>
/* Animations */
@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(12deg); }
  50% { transform: translateY(-6px) rotate(12deg); }
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