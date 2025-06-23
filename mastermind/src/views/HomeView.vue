<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800 relative overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute inset-0 opacity-20">
        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-r from-blue-500/8 via-indigo-500/8 to-purple-500/8"></div>
      </div>
      
      <!-- Floating Elements -->
      <div class="absolute inset-0">
        <div class="absolute top-[20%] left-[8%] w-16 h-16 bg-gradient-to-br from-blue-400/15 to-indigo-600/15 rounded-xl opacity-40 animate-float transform rotate-45"></div>
        <div class="absolute top-[40%] right-[15%] w-20 h-20 bg-gradient-to-br from-indigo-400/15 to-purple-600/15 rounded-2xl opacity-30 animate-float-delay"></div>
        <div class="absolute bottom-[30%] left-[20%] w-12 h-12 bg-gradient-to-br from-purple-400/15 to-pink-600/15 rounded-full opacity-25 animate-float"></div>
        <div class="absolute top-[10%] right-[25%] w-14 h-14 bg-gradient-to-br from-indigo-400/10 to-blue-600/10 rounded-lg opacity-20 animate-float-delay"></div>
      </div>
    </div>

    <div class="relative z-10 min-h-screen grid grid-rows-[auto_1fr_auto] gap-0">
      <!-- Content Container -->
      <div class="grid place-items-center gap-20 px-6 py-20">
        
        <!-- Hero Section -->
        <div class="grid place-items-center gap-12 text-center max-w-4xl">
          <!-- Badge -->
          <div class="inline-flex items-center px-5 py-2.5 rounded-full bg-white/90 dark:bg-gray-800/90 backdrop-blur-xl border border-gray-200/60 dark:border-gray-700/60 shadow-lg">
            <div class="w-1.5 h-1.5 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-full animate-pulse mr-2.5"></div>
            <span class="text-xs font-medium text-gray-700 dark:text-gray-300 tracking-wide">PROJECT SHOWCASE</span>
          </div>
          
          <!-- Title -->
          <h1 class="text-6xl sm:text-7xl lg:text-8xl font-black leading-[0.85] tracking-tighter">
            <span class="block bg-gradient-to-r from-gray-900 via-blue-800 to-indigo-900 dark:from-white dark:via-blue-200 dark:to-indigo-200 bg-clip-text text-transparent">
              Interactive
            </span>
            <span class="block bg-gradient-to-r from-indigo-800 via-purple-800 to-blue-900 dark:from-indigo-200 dark:via-purple-200 dark:to-blue-200 bg-clip-text text-transparent -mt-4">
              Applications
            </span>
          </h1>
          
          <!-- Subtitle -->
          <p class="text-xl sm:text-2xl leading-[1.6] font-light text-gray-600 dark:text-gray-300 max-w-3xl">
            Explore our collection of <span class="font-semibold text-blue-600 dark:text-blue-400">interactive tools</span> and 
            <span class="font-semibold text-indigo-600 dark:text-indigo-400">problem-solving applications</span> 
            built with modern web technologies.
          </p>

          <!-- Navigation Links -->
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 w-full max-w-xl">
            <router-link
              to="/mastermind"
              class="group relative px-8 py-4 bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-semibold rounded-xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-xl focus:outline-none focus:ring-4 focus:ring-blue-500/50"
            >
              <span class="relative z-10 grid grid-cols-[auto_1fr] gap-3 items-center justify-center">
                <IconPlayerPlay class="w-6 h-6" />
                <span>Play Mastermind</span>
              </span>
              <div class="absolute inset-0 rounded-xl bg-gradient-to-r from-white/20 to-white/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
            </router-link>
            
            <router-link
              to="/parser"
              class="group relative px-8 py-4 bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-700 hover:to-purple-700 text-white font-semibold rounded-xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-xl focus:outline-none focus:ring-4 focus:ring-indigo-500/50"
            >
              <span class="relative z-10 grid grid-cols-[auto_1fr] gap-3 items-center justify-center">
                <IconMath class="w-6 h-6" />
                <span>Try Calculator</span>
              </span>
              <div class="absolute inset-0 rounded-xl bg-gradient-to-r from-white/20 to-white/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
            </router-link>
          </div>
        </div>

        <!-- App Previews -->
        <div class="grid place-items-center gap-16 w-full max-w-6xl">
          <h2 class="text-4xl sm:text-5xl font-bold text-gray-900 dark:text-white">Featured Applications</h2>
          
          <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
            
            <!-- Mastermind Preview -->
            <div class="group">
              <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-3xl border border-gray-200/50 dark:border-gray-700/50 overflow-hidden shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
                
                <!-- Header -->
                <div class="relative h-48 bg-gradient-to-br from-blue-500 via-indigo-600 to-purple-600 overflow-hidden">
                  <div class="absolute inset-0 opacity-20">
                    <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 20px 20px;"></div>
                  </div>
                  <div class="absolute inset-0 grid place-items-center">
                    <div class="grid place-items-center gap-6">
                      <IconPuzzle class="w-16 h-16 text-white opacity-90" />
                      <div class="grid place-items-center gap-2">
                        <h3 class="text-2xl font-bold text-white">Mastermind Game</h3>
                        <p class="text-blue-100 text-center px-4">Logic puzzle & deductive reasoning</p>
                      </div>
                    </div>
                  </div>
                  
                  <!-- Preview Elements -->
                  <div class="absolute bottom-4 left-4 grid grid-cols-4 gap-2">
                    <div class="w-8 h-8 bg-red-500 rounded-lg border-2 border-white/40"></div>
                    <div class="w-8 h-8 bg-yellow-500 rounded-lg border-2 border-white/40"></div>
                    <div class="w-8 h-8 bg-green-500 rounded-lg border-2 border-white/40"></div>
                    <div class="w-8 h-8 bg-blue-500 rounded-lg border-2 border-white/40"></div>
                  </div>
                  
                  <div class="absolute bottom-4 right-4 grid grid-cols-2 gap-1">
                    <div class="w-3 h-3 bg-emerald-400 rounded-full"></div>
                    <div class="w-3 h-3 bg-amber-400 rounded-full"></div>
                  </div>
                </div>
                
                <!-- Content -->
                <div class="grid gap-8 p-8">
                  <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                    Challenge yourself with this classic code-breaking game. Use deductive reasoning to crack the 
                    secret color combination within 10 attempts.
                  </p>
                  
                  <div class="grid gap-4">
                    <h4 class="font-semibold text-gray-900 dark:text-white">Key Features:</h4>
                    <div class="grid gap-3">
                      <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                        <IconCheck class="w-5 h-5 text-green-500" />
                        <span class="text-sm text-gray-600 dark:text-gray-300">10 attempts to solve the puzzle</span>
                      </div>
                      <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                        <IconCheck class="w-5 h-5 text-green-500" />
                        <span class="text-sm text-gray-600 dark:text-gray-300">Visual feedback system</span>
                      </div>
                      <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                        <IconCheck class="w-5 h-5 text-green-500" />
                        <span class="text-sm text-gray-600 dark:text-gray-300">6 different colors to choose from</span>
                      </div>
                    </div>
                  </div>
                  
                  <div class="grid grid-flow-col gap-2 justify-start">
                    <span class="px-3 py-1.5 bg-blue-100 dark:bg-blue-900/30 text-blue-700 dark:text-blue-300 rounded-full text-sm font-medium">Vue 3</span>
                    <span class="px-3 py-1.5 bg-indigo-100 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 rounded-full text-sm font-medium">TypeScript</span>
                    <span class="px-3 py-1.5 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 rounded-full text-sm font-medium">Tailwind</span>
                  </div>
                </div>
              </div>
            </div>

            <!-- Parser Calculator Preview -->
            <div class="group">
              <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-3xl border border-gray-200/50 dark:border-gray-700/50 overflow-hidden shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
                
                <!-- Header -->
                <div class="relative h-48 bg-gradient-to-br from-indigo-500 via-purple-600 to-pink-600 overflow-hidden">
                  <div class="absolute inset-0 opacity-20">
                    <div class="absolute inset-0" style="background-image: linear-gradient(45deg, transparent 35%, white 35%, white 65%, transparent 65%), linear-gradient(-45deg, transparent 35%, white 35%, white 65%, transparent 65%); background-size: 16px 16px;"></div>
                  </div>
                  <div class="absolute inset-0 grid place-items-center">
                    <div class="grid place-items-center gap-6">
                      <IconCalculator class="w-16 h-16 text-white opacity-90" />
                      <div class="grid place-items-center gap-2">
                        <h3 class="text-2xl font-bold text-white">Expression Parser</h3>
                        <p class="text-indigo-100 text-center px-4">Advanced mathematical calculator</p>
                      </div>
                    </div>
                  </div>
                  
                  <!-- Preview Elements -->
                  <div class="absolute bottom-4 left-4 bg-white/20 backdrop-blur-sm rounded-lg px-3 py-2">
                    <span class="text-white font-mono text-sm">2 + 3 * (4 - 1)</span>
                  </div>
                  
                  <div class="absolute bottom-4 right-4 bg-emerald-400/90 backdrop-blur-sm rounded-lg px-3 py-2">
                    <span class="text-emerald-900 font-mono text-sm font-bold">= 11</span>
                  </div>
                </div>
                
                <!-- Content -->
                <div class="grid gap-8 p-8">
                  <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                    Powerful mathematical expression parser with support for complex equations, 
                    parentheses, and proper order of operations.
                  </p>
                  
                  <div class="grid gap-4">
                    <h4 class="font-semibold text-gray-900 dark:text-white">Key Features:</h4>
                    <div class="grid gap-3">
                      <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                        <IconCheck class="w-5 h-5 text-green-500" />
                        <span class="text-sm text-gray-600 dark:text-gray-300">PEMDAS order of operations</span>
                      </div>
                      <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                        <IconCheck class="w-5 h-5 text-green-500" />
                        <span class="text-sm text-gray-600 dark:text-gray-300">Nested parentheses support</span>
                      </div>
                      <div class="grid grid-cols-[auto_1fr] gap-3 items-center">
                        <IconCheck class="w-5 h-5 text-green-500" />
                        <span class="text-sm text-gray-600 dark:text-gray-300">Real-time expression validation</span>
                      </div>
                    </div>
                  </div>
                  
                  <div class="grid grid-flow-col gap-2 justify-start">
                    <span class="px-3 py-1.5 bg-indigo-100 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 rounded-full text-sm font-medium">Parsing</span>
                    <span class="px-3 py-1.5 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 rounded-full text-sm font-medium">Algorithms</span>
                    <span class="px-3 py-1.5 bg-pink-100 dark:bg-pink-900/30 text-pink-700 dark:text-pink-300 rounded-full text-sm font-medium">Math</span>
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
import { IconPlayerPlay, IconMath, IconPuzzle, IconCalculator, IconCheck } from '@tabler/icons-vue'
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