<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800">
    <div class="min-h-screen grid grid-rows-[auto_1fr] gap-0">
      
      <!-- Hero Section -->
      <div class="grid place-items-center gap-12 px-6 py-16">
        <div class="grid place-items-center gap-8 text-center max-w-4xl">
          <div class="inline-flex items-center px-4 py-2 rounded-full bg-white/90 dark:bg-gray-800/90 backdrop-blur-xl border border-gray-200/60 dark:border-gray-700/60 shadow-lg">
            <div class="w-2 h-2 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-full animate-pulse mr-3"></div>
            <span class="text-sm font-medium text-gray-700 dark:text-gray-300 tracking-wide">INTERACTIVE APPLICATIONS</span>
          </div>
          
          <h1 class="text-5xl sm:text-6xl lg:text-7xl font-black leading-tight tracking-tight">
            <span class="block bg-gradient-to-r from-gray-900 via-blue-800 to-indigo-900 dark:from-white dark:via-blue-200 dark:to-indigo-200 bg-clip-text text-transparent">
              Welcome to
            </span>
            <span class="block bg-gradient-to-r from-indigo-800 via-purple-800 to-blue-900 dark:from-indigo-200 dark:via-purple-200 dark:to-blue-200 bg-clip-text text-transparent">
              My Showcase
            </span>
          </h1>
          
          <p class="text-xl sm:text-2xl leading-relaxed font-light text-gray-600 dark:text-gray-300 max-w-3xl">
            Explore two interactive applications: a challenging logic puzzle game and a powerful mathematical calculator.
          </p>
        </div>
      </div>

      <!-- Applications Showcase -->
      <div class="grid place-items-center gap-16 px-6 pb-20">
        <div class="grid gap-16 w-full max-w-7xl">
          
          <!-- Mastermind Game Section -->
          <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            
            <!-- App Preview -->
            <div class="order-2 lg:order-1">
              <div class="relative group">
                <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-3xl opacity-20 blur-xl group-hover:opacity-30 transition-opacity duration-500"></div>
                <div class="relative bg-white/90 dark:bg-gray-800/90 backdrop-blur-xl rounded-3xl border border-gray-200/50 dark:border-gray-700/50 shadow-2xl overflow-hidden">
                  
                  <!-- Mock Browser Header -->
                  <div class="grid grid-cols-[auto_1fr_auto] gap-3 items-center px-6 py-4 bg-gray-100/80 dark:bg-gray-700/80 border-b border-gray-200/50 dark:border-gray-600/50">
                    <div class="grid grid-cols-3 gap-2">
                      <div class="w-3 h-3 bg-red-400 rounded-full"></div>
                      <div class="w-3 h-3 bg-yellow-400 rounded-full"></div>
                      <div class="w-3 h-3 bg-green-400 rounded-full"></div>
                    </div>
                    <div class="text-center text-sm text-gray-500 dark:text-gray-400 font-mono">mastermind-game.app</div>
                    <div class="w-16"></div>
                  </div>
                  
                  <!-- Mastermind Game Preview -->
                  <div class="p-8 bg-gradient-to-br from-blue-50 to-indigo-50 dark:from-blue-900/20 dark:to-indigo-900/20">
                    <div class="grid place-items-center gap-6">
                      <!-- Game Title -->
                      <div class="grid place-items-center gap-3">
                        <h3 class="text-2xl font-bold text-gray-900 dark:text-white">Mastermind Challenge</h3>
                        <div class="grid grid-cols-2 gap-3 text-sm">
                          <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900/30 text-blue-700 dark:text-blue-300 rounded-full text-center">Round 1</span>
                          <span class="px-3 py-1 bg-indigo-100 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 rounded-full text-center">8 attempts left</span>
                        </div>
                      </div>
                      
                      <!-- Game Board Mock -->
                      <div class="grid gap-3 w-full max-w-md">
                        <!-- Current guess row -->
                        <div class="grid grid-cols-[auto_1fr_auto] gap-4 items-center p-3 bg-blue-100/80 dark:bg-blue-900/30 rounded-xl border border-blue-200 dark:border-blue-700">
                          <span class="text-sm font-medium text-gray-700 dark:text-gray-300">1.</span>
                          <div class="grid grid-cols-4 gap-2 justify-items-center">
                            <div class="w-8 h-8 bg-red-500 rounded-lg border-2 border-white/60 shadow-sm"></div>
                            <div class="w-8 h-8 bg-yellow-500 rounded-lg border-2 border-white/60 shadow-sm"></div>
                            <div class="w-8 h-8 bg-green-500 rounded-lg border-2 border-white/60 shadow-sm"></div>
                            <div class="w-8 h-8 bg-blue-500 rounded-lg border-2 border-white/60 shadow-sm"></div>
                          </div>
                          <button class="px-4 py-2 bg-emerald-500 hover:bg-emerald-600 text-white text-sm font-medium rounded-lg transition-colors duration-200">
                            Submit
                          </button>
                        </div>
                        
                        <!-- Previous guesses -->
                        <div class="grid grid-cols-[auto_1fr_auto] gap-4 items-center p-3 bg-gray-50/80 dark:bg-gray-700/30 rounded-xl">
                          <span class="text-sm font-medium text-gray-500 dark:text-gray-400">2.</span>
                          <div class="grid grid-cols-4 gap-2 justify-items-center">
                            <div class="w-8 h-8 bg-gray-300 dark:bg-gray-600 rounded-lg border-2 border-white/40"></div>
                            <div class="w-8 h-8 bg-gray-300 dark:bg-gray-600 rounded-lg border-2 border-white/40"></div>
                            <div class="w-8 h-8 bg-gray-300 dark:bg-gray-600 rounded-lg border-2 border-white/40"></div>
                            <div class="w-8 h-8 bg-gray-300 dark:bg-gray-600 rounded-lg border-2 border-white/40"></div>
                          </div>
                          <div class="w-16"></div>
                        </div>
                        
                        <div class="grid grid-cols-[auto_1fr_auto] gap-4 items-center p-3 bg-gray-50/80 dark:bg-gray-700/30 rounded-xl">
                          <span class="text-sm font-medium text-gray-500 dark:text-gray-400">3.</span>
                          <div class="grid grid-cols-4 gap-2 justify-items-center">
                            <div class="w-8 h-8 bg-gray-300 dark:bg-gray-600 rounded-lg border-2 border-white/40"></div>
                            <div class="w-8 h-8 bg-gray-300 dark:bg-gray-600 rounded-lg border-2 border-white/40"></div>
                            <div class="w-8 h-8 bg-gray-300 dark:bg-gray-600 rounded-lg border-2 border-white/40"></div>
                            <div class="w-8 h-8 bg-gray-300 dark:bg-gray-600 rounded-lg border-2 border-white/40"></div>
                          </div>
                          <div class="w-16"></div>
                        </div>
                      </div>
                      
                      <!-- Feedback Legend -->
                      <div class="grid grid-cols-2 gap-4 text-xs text-gray-600 dark:text-gray-400">
                        <div class="grid grid-cols-[auto_1fr] gap-2 items-center">
                          <div class="w-3 h-3 bg-emerald-500 rounded-full"></div>
                          <span>Perfect match</span>
                        </div>
                        <div class="grid grid-cols-[auto_1fr] gap-2 items-center">
                          <div class="w-3 h-3 bg-amber-500 rounded-full"></div>
                          <span>Right color</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            
            <!-- App Description -->
            <div class="order-1 lg:order-2 grid gap-8">
              <div class="grid gap-6">
                <div class="grid gap-3">
                  <h2 class="text-4xl sm:text-5xl font-bold text-gray-900 dark:text-white leading-tight">
                    Mastermind Game
                  </h2>
                  <p class="text-xl text-gray-600 dark:text-gray-300 leading-relaxed">
                    Test your logical thinking with this classic code-breaking puzzle. Crack the secret color combination using deductive reasoning and strategic guessing.
                  </p>
                </div>
                
                <div class="grid gap-4">
                  <h3 class="text-lg font-semibold text-gray-900 dark:text-white">Game Features:</h3>
                  <div class="grid gap-3">
                    <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                      <IconCheck class="w-5 h-5 text-emerald-500" />
                      <span class="text-gray-600 dark:text-gray-300">Challenge yourself with 10 attempts to solve each puzzle</span>
                    </div>
                    <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                      <IconCheck class="w-5 h-5 text-emerald-500" />
                      <span class="text-gray-600 dark:text-gray-300">Visual feedback system guides your deductive process</span>
                    </div>
                    <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                      <IconCheck class="w-5 h-5 text-emerald-500" />
                      <span class="text-gray-600 dark:text-gray-300">Clean, intuitive interface built with Vue 3 and TypeScript</span>
                    </div>
                  </div>
                </div>
              </div>
              
              <router-link
                to="/mastermind"
                class="group inline-flex items-center justify-center gap-3 px-8 py-4 bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-semibold rounded-2xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-xl focus:outline-none focus:ring-4 focus:ring-blue-500/50"
              >
                <IconPlayerPlay class="w-6 h-6 transition-transform duration-300 group-hover:scale-110" />
                <span class="text-lg">Play Mastermind Game</span>
              </router-link>
            </div>
          </div>

          <!-- Parser Calculator Section -->
          <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            
            <!-- App Description -->
            <div class="grid gap-8">
              <div class="grid gap-6">
                <div class="grid gap-3">
                  <h2 class="text-4xl sm:text-5xl font-bold text-gray-900 dark:text-white leading-tight">
                    Expression Calculator
                  </h2>
                  <p class="text-xl text-gray-600 dark:text-gray-300 leading-relaxed">
                    A powerful mathematical expression parser that handles complex equations with proper order of operations, nested parentheses, and real-time validation.
                  </p>
                </div>
                
                <div class="grid gap-4">
                  <h3 class="text-lg font-semibold text-gray-900 dark:text-white">Calculator Features:</h3>
                  <div class="grid gap-3">
                    <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                      <IconCheck class="w-5 h-5 text-emerald-500" />
                      <span class="text-gray-600 dark:text-gray-300">Supports complex nested expressions with proper PEMDAS order</span>
                    </div>
                    <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                      <IconCheck class="w-5 h-5 text-emerald-500" />
                      <span class="text-gray-600 dark:text-gray-300">Real-time expression validation and error handling</span>
                    </div>
                    <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                      <IconCheck class="w-5 h-5 text-emerald-500" />
                      <span class="text-gray-600 dark:text-gray-300">Clean interface with example expressions to get started</span>
                    </div>
                  </div>
                </div>
              </div>
              
              <router-link
                to="/parser"
                class="group inline-flex items-center justify-center gap-3 px-8 py-4 bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-700 hover:to-purple-700 text-white font-semibold rounded-2xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-xl focus:outline-none focus:ring-4 focus:ring-indigo-500/50"
              >
                <IconCalculator class="w-6 h-6 transition-transform duration-300 group-hover:scale-110" />
                <span class="text-lg">Try Expression Calculator</span>
              </router-link>
            </div>
            
            <!-- App Preview -->
            <div class="relative group">
              <div class="absolute inset-0 bg-gradient-to-r from-indigo-500 to-purple-500 rounded-3xl opacity-20 blur-xl group-hover:opacity-30 transition-opacity duration-500"></div>
              <div class="relative bg-white/90 dark:bg-gray-800/90 backdrop-blur-xl rounded-3xl border border-gray-200/50 dark:border-gray-700/50 shadow-2xl overflow-hidden">
                
                <!-- Mock Browser Header -->
                <div class="grid grid-cols-[auto_1fr_auto] gap-3 items-center px-6 py-4 bg-gray-100/80 dark:bg-gray-700/80 border-b border-gray-200/50 dark:border-gray-600/50">
                  <div class="grid grid-cols-3 gap-2">
                    <div class="w-3 h-3 bg-red-400 rounded-full"></div>
                    <div class="w-3 h-3 bg-yellow-400 rounded-full"></div>
                    <div class="w-3 h-3 bg-green-400 rounded-full"></div>
                  </div>
                  <div class="text-center text-sm text-gray-500 dark:text-gray-400 font-mono">expression-calculator.app</div>
                  <div class="w-16"></div>
                </div>
                
                <!-- Calculator Preview -->
                <div class="p-8 bg-gradient-to-br from-indigo-50 to-purple-50 dark:from-indigo-900/20 dark:to-purple-900/20">
                  <div class="grid gap-6">
                    <!-- Calculator Title -->
                    <div class="text-center">
                      <h3 class="text-2xl font-bold text-gray-900 dark:text-white">Expression Calculator</h3>
                      <p class="text-sm text-gray-600 dark:text-gray-400 mt-2">Advanced mathematical parser</p>
                    </div>
                    
                    <!-- Input Field Mock -->
                    <div class="grid gap-4">
                      <div class="grid gap-2">
                        <label class="text-sm font-medium text-gray-700 dark:text-gray-300">Mathematical Expression</label>
                        <div class="relative">
                          <input 
                            type="text" 
                            value="2 + 3 * (4 - 1)" 
                            readonly
                            class="w-full px-4 py-3 bg-white/90 dark:bg-gray-700/90 border border-gray-300 dark:border-gray-600 rounded-xl text-gray-900 dark:text-white font-mono"
                          />
                          <IconEqual class="absolute right-4 top-1/2 -translate-y-1/2 w-5 h-5 text-gray-400" />
                        </div>
                      </div>
                      
                      <div class="grid gap-2">
                        <label class="text-sm font-medium text-gray-700 dark:text-gray-300">Result</label>
                        <div class="relative">
                          <div class="w-full px-4 py-3 bg-green-100/90 dark:bg-green-900/30 border border-green-300 dark:border-green-600 rounded-xl text-green-700 dark:text-green-300 font-mono text-lg font-semibold">
                            11
                          </div>
                          <IconCheck class="absolute right-4 top-1/2 -translate-y-1/2 w-5 h-5 text-green-500" />
                        </div>
                      </div>
                    </div>
                    
                    <!-- Action Buttons Mock -->
                    <div class="grid grid-cols-2 gap-3">
                      <button class="px-4 py-2 bg-indigo-500 hover:bg-indigo-600 text-white rounded-lg font-medium transition-colors duration-200">
                        Calculate
                      </button>
                      <button class="px-4 py-2 bg-gray-500 hover:bg-gray-600 text-white rounded-lg font-medium transition-colors duration-200">
                        Clear
                      </button>
                    </div>
                    
                    <!-- Example expressions -->
                    <div class="grid gap-3">
                      <h4 class="text-sm font-medium text-gray-700 dark:text-gray-300">Example Expressions:</h4>
                      <div class="grid gap-2 text-sm">
                        <div class="px-3 py-2 bg-white/60 dark:bg-gray-700/60 rounded-lg">
                          <span class="font-mono text-indigo-600 dark:text-indigo-400">10 * (5 + 3) / (4 - 2)</span>
                          <span class="text-gray-500 dark:text-gray-400 ml-2">= 40</span>
                        </div>
                        <div class="px-3 py-2 bg-white/60 dark:bg-gray-700/60 rounded-lg">
                          <span class="font-mono text-indigo-600 dark:text-indigo-400">((2 + 3) * (4 + 1)) / 5</span>
                          <span class="text-gray-500 dark:text-gray-400 ml-2">= 5</span>
                        </div>
                      </div>
                    </div>
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
import { IconPlayerPlay, IconCalculator, IconCheck, IconEqual } from '@tabler/icons-vue'
</script>

<style scoped>
/* Smooth Transitions */
* {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}
</style>