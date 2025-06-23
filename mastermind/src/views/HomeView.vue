<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800 relative overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute inset-0 opacity-30">
        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-r from-blue-600/10 via-indigo-600/10 to-purple-600/10"></div>
      </div>
      
      <!-- Radial gradient overlays -->
      <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-gradient-radial from-blue-400/20 to-transparent rounded-full blur-3xl"></div>
      <div class="absolute bottom-1/4 right-1/4 w-96 h-96 bg-gradient-radial from-indigo-400/20 to-transparent rounded-full blur-3xl"></div>
    </div>

    <div class="relative z-10 flex flex-col min-h-screen">
      <!-- Content Container -->
      <div class="flex-1 flex flex-col items-center justify-center gap-20 px-6 py-16">
        
        <!-- Hero Section -->
        <div class="flex flex-col items-center gap-12 text-center max-w-5xl">
          <div class="inline-flex items-center px-6 py-3 rounded-full bg-white/90 dark:bg-gray-800/90 backdrop-blur-xl border border-gray-200/60 dark:border-gray-700/60 shadow-lg">
            <div class="w-2 h-2 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-full animate-pulse mr-3"></div>
            <span class="text-sm font-medium text-gray-700 dark:text-gray-300 tracking-wide">INTERACTIVE PROJECT SHOWCASE</span>
          </div>
          
          <h1 class="text-6xl sm:text-7xl lg:text-8xl font-black leading-[0.85] tracking-tighter">
            <span class="block bg-gradient-to-r from-gray-900 via-blue-800 to-indigo-900 dark:from-white dark:via-blue-200 dark:to-indigo-200 bg-clip-text text-transparent">
              Project
            </span>
            <span class="block bg-gradient-to-r from-indigo-800 via-purple-800 to-blue-900 dark:from-indigo-200 dark:via-purple-200 dark:to-blue-200 bg-clip-text text-transparent">
              Showcase
            </span>
          </h1>
          
          <p class="text-xl sm:text-2xl leading-[1.6] font-light text-gray-600 dark:text-gray-300 max-w-4xl">
            Explore interactive tools designed to challenge your mind and solve complex problems with 
            <span class="font-semibold text-blue-600 dark:text-blue-400">elegant solutions</span>
          </p>

          <!-- Navigation Links -->
          <div class="flex flex-col sm:flex-row items-center gap-6">
            <RouterLink 
              to="/mastermind" 
              class="group flex items-center gap-4 px-8 py-4 bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white rounded-2xl transition-all duration-300 transform hover:-translate-y-2 hover:shadow-xl backdrop-blur-xl"
            >
              <IconPlayerPlay class="w-6 h-6 transition-transform duration-300 group-hover:scale-110" />
              <span class="font-semibold text-lg">Play Mastermind</span>
            </RouterLink>
            
            <RouterLink 
              to="/parser" 
              class="group flex items-center gap-4 px-8 py-4 bg-white/80 dark:bg-gray-800/80 hover:bg-white dark:hover:bg-gray-700 text-gray-900 dark:text-white rounded-2xl transition-all duration-300 transform hover:-translate-y-2 hover:shadow-xl backdrop-blur-xl border border-gray-200/50 dark:border-gray-700/50"
            >
              <IconMath class="w-6 h-6 transition-transform duration-300 group-hover:scale-110" />
              <span class="font-semibold text-lg">Try Calculator</span>
            </RouterLink>
          </div>
        </div>

        <!-- Preview Cards -->
        <div class="flex flex-col lg:flex-row items-stretch gap-8 w-full max-w-6xl">
          <!-- Mastermind Preview -->
          <div class="flex-1 group">
            <div class="h-full bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 overflow-hidden shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
              <div class="relative h-48 bg-gradient-to-br from-blue-500 via-indigo-600 to-purple-600 overflow-hidden">
                <div class="absolute inset-0 opacity-20">
                  <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 20px 20px;"></div>
                </div>
                <div class="absolute inset-0 flex items-center justify-center">
                  <div class="flex gap-2">
                    <div class="w-6 h-6 bg-red-400 rounded-full opacity-80"></div>
                    <div class="w-6 h-6 bg-blue-400 rounded-full opacity-80"></div>
                    <div class="w-6 h-6 bg-green-400 rounded-full opacity-80"></div>
                    <div class="w-6 h-6 bg-yellow-400 rounded-full opacity-80"></div>
                  </div>
                </div>
              </div>
              
              <div class="flex flex-col gap-6 p-8">
                <div class="flex flex-col gap-3">
                  <h2 class="text-2xl font-bold text-gray-900 dark:text-white">Mastermind Logic Game</h2>
                  <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                    Challenge your deductive reasoning with this classic code-breaking game featuring colorful combinations and strategic thinking.
                  </p>
                </div>
                
                <div class="flex flex-col gap-3">
                  <h3 class="font-semibold text-gray-900 dark:text-white">Features:</h3>
                  <div class="flex flex-col gap-2">
                    <div class="flex items-center gap-3">
                      <IconCheck class="w-4 h-4 text-emerald-500 flex-shrink-0" />
                      <span class="text-sm text-gray-600 dark:text-gray-300">10 attempts to crack the code</span>
                    </div>
                    <div class="flex items-center gap-3">
                      <IconCheck class="w-4 h-4 text-emerald-500 flex-shrink-0" />
                      <span class="text-sm text-gray-600 dark:text-gray-300">Visual feedback system</span>
                    </div>
                    <div class="flex items-center gap-3">
                      <IconCheck class="w-4 h-4 text-emerald-500 flex-shrink-0" />
                      <span class="text-sm text-gray-600 dark:text-gray-300">Multiple difficulty levels</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Calculator Preview -->
          <div class="flex-1 group">
            <div class="h-full bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 overflow-hidden shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
              <div class="relative h-48 bg-gradient-to-br from-indigo-500 via-purple-600 to-pink-600 overflow-hidden">
                <div class="absolute inset-0 opacity-20">
                  <div class="absolute inset-0" style="background-image: linear-gradient(45deg, transparent 35%, white 35%, white 65%, transparent 65%), linear-gradient(-45deg, transparent 35%, white 35%, white 65%, transparent 65%); background-size: 16px 16px;"></div>
                </div>
                <div class="absolute inset-0 flex items-center justify-center">
                  <div class="text-white opacity-80 text-lg font-mono">
                    (2 + 3) × 4 = 20
                  </div>
                </div>
              </div>
              
              <div class="flex flex-col gap-6 p-8">
                <div class="flex flex-col gap-3">
                  <h2 class="text-2xl font-bold text-gray-900 dark:text-white">Advanced Math Parser</h2>
                  <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                    Parse and evaluate complex mathematical expressions with full operator precedence and parentheses support.
                  </p>
                </div>
                
                <div class="flex flex-col gap-3">
                  <h3 class="font-semibold text-gray-900 dark:text-white">Capabilities:</h3>
                  <div class="flex flex-col gap-2">
                    <div class="flex items-center gap-3">
                      <IconCheck class="w-4 h-4 text-emerald-500 flex-shrink-0" />
                      <span class="text-sm text-gray-600 dark:text-gray-300">Complex nested expressions</span>
                    </div>
                    <div class="flex items-center gap-3">
                      <IconCheck class="w-4 h-4 text-emerald-500 flex-shrink-0" />
                      <span class="text-sm text-gray-600 dark:text-gray-300">Operator precedence handling</span>
                    </div>
                    <div class="flex items-center gap-3">
                      <IconCheck class="w-4 h-4 text-emerald-500 flex-shrink-0" />
                      <span class="text-sm text-gray-600 dark:text-gray-300">Real-time calculation</span>
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
import { IconPlayerPlay, IconMath, IconCheck } from '@tabler/icons-vue'
</script>

<style scoped>
/* Gradient utilities for background */
.bg-gradient-radial {
  background: radial-gradient(circle, var(--tw-gradient-stops));
}

/* Smooth transitions */
* {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}
</style>