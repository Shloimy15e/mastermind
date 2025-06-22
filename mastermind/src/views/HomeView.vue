<template>
  <div class="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100 dark:from-gray-900 dark:to-gray-800">
    <div class="container mx-auto px-4 py-12">
      <!-- Header Section -->
      <div class="text-center mb-16">
        <h1 class="text-5xl font-bold text-gray-900 dark:text-white mb-4">
          Welcome to Gaming Hub
        </h1>
        <p class="text-xl text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">
          Explore our collection of interactive games and tools. Challenge your mind with puzzles 
          and calculations in a beautifully designed interface.
        </p>
      </div>

      <!-- Applications Grid -->
      <div class="grid md:grid-cols-2 gap-8 max-w-6xl mx-auto">
        
        <!-- Mastermind Game Card -->
        <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-xl overflow-hidden transform hover:scale-105 transition-all duration-300 hover:shadow-2xl">
          <div class="h-48 bg-gradient-to-br from-purple-400 to-pink-400 relative overflow-hidden">
            <div class="absolute inset-0 flex items-center justify-center">
              <!-- Visual representation of mastermind -->
              <div class="flex space-x-2">
                <div class="w-8 h-8 rounded-full bg-red-500 shadow-lg"></div>
                <div class="w-8 h-8 rounded-full bg-blue-500 shadow-lg"></div>
                <div class="w-8 h-8 rounded-full bg-green-500 shadow-lg"></div>
                <div class="w-8 h-8 rounded-full bg-yellow-500 shadow-lg"></div>
              </div>
            </div>
            <div class="absolute top-4 right-4">
              <IconPuzzle class="w-8 h-8 text-white/80" />
            </div>
          </div>
          
          <div class="p-6">
            <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-3">
              Mastermind Game
            </h2>
            <p class="text-gray-600 dark:text-gray-300 mb-4">
              Test your deductive reasoning skills! Guess the secret color combination within 10 attempts. 
              Get feedback on each guess to help narrow down the solution.
            </p>
            
            <div class="flex items-center justify-between">
              <div class="flex items-center space-x-4 text-sm text-gray-500 dark:text-gray-400">
                <span class="flex items-center">
                  <IconTarget class="w-4 h-4 mr-1" />
                  Logic Puzzle
                </span>
                <span class="flex items-center">
                  <IconClock class="w-4 h-4 mr-1" />
                  5-15 min
                </span>
              </div>
              
              <router-link 
                to="/mastermind"
                class="bg-purple-600 hover:bg-purple-700 text-white px-6 py-2 rounded-lg font-medium transition-colors duration-200 flex items-center space-x-2 group"
              >
                <span>Play Game</span>
                <IconArrowRight class="w-4 h-4 group-hover:translate-x-1 transition-transform" />
              </router-link>
            </div>
          </div>
        </div>

        <!-- Parser Calculator Card -->
        <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-xl overflow-hidden transform hover:scale-105 transition-all duration-300 hover:shadow-2xl">
          <div class="h-48 bg-gradient-to-br from-green-400 to-blue-500 relative overflow-hidden">
            <div class="absolute inset-0 flex items-center justify-center">
              <!-- Visual representation of calculator -->
              <div class="text-white font-mono text-2xl">
                2 × 3 + 6 = 12
              </div>
            </div>
            <div class="absolute top-4 right-4">
              <IconCalculator class="w-8 h-8 text-white/80" />
            </div>
          </div>
          
          <div class="p-6">
            <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-3">
              Math Parser Calculator
            </h2>
            <p class="text-gray-600 dark:text-gray-300 mb-4">
              Advanced mathematical expression parser and calculator. Supports complex equations with 
              parentheses, multiple operators, and proper order of operations.
            </p>
            
            <div class="flex items-center justify-between">
              <div class="flex items-center space-x-4 text-sm text-gray-500 dark:text-gray-400">
                <span class="flex items-center">
                  <IconMath class="w-4 h-4 mr-1" />
                  Calculator
                </span>
                <span class="flex items-center">
                  <IconBolt class="w-4 h-4 mr-1" />
                  Instant
                </span>
              </div>
              
              <router-link 
                to="/parser"
                class="bg-green-600 hover:bg-green-700 text-white px-6 py-2 rounded-lg font-medium transition-colors duration-200 flex items-center space-x-2 group"
              >
                <span>Try Calculator</span>
                <IconArrowRight class="w-4 h-4 group-hover:translate-x-1 transition-transform" />
              </router-link>
            </div>
          </div>
        </div>

      </div>

      <!-- Features Section -->
      <div class="mt-16 text-center">
        <h2 class="text-3xl font-bold text-gray-900 dark:text-white mb-8">Features</h2>
        <div class="grid md:grid-cols-3 gap-6 max-w-4xl mx-auto">
          <div class="p-6">
            <div class="w-12 h-12 bg-blue-100 dark:bg-blue-900 rounded-lg flex items-center justify-center mx-auto mb-4">
              <IconDeviceDesktop class="w-6 h-6 text-blue-600 dark:text-blue-400" />
            </div>
            <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-2">Responsive Design</h3>
            <p class="text-gray-600 dark:text-gray-300">Works perfectly on desktop, tablet, and mobile devices</p>
          </div>
          
          <div class="p-6">
            <div class="w-12 h-12 bg-purple-100 dark:bg-purple-900 rounded-lg flex items-center justify-center mx-auto mb-4">
              <IconPalette class="w-6 h-6 text-purple-600 dark:text-purple-400" />
            </div>
            <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-2">Beautiful UI</h3>
            <p class="text-gray-600 dark:text-gray-300">Clean, modern interface with smooth animations</p>
          </div>
          
          <div class="p-6">
            <div class="w-12 h-12 bg-green-100 dark:bg-green-900 rounded-lg flex items-center justify-center mx-auto mb-4">
              <IconRocket class="w-6 h-6 text-green-600 dark:text-green-400" />
            </div>
            <h3 class="text-lg font-semibold text-gray-900 dark:text-white mb-2">Fast & Efficient</h3>
            <p class="text-gray-600 dark:text-gray-300">Built with Vue 3 and optimized for performance</p>
          </div>
        </div>
      </div>

      <!-- Footer -->
      <div class="mt-16 text-center text-gray-500 dark:text-gray-400">
        <p>Built with Vue 3, TypeScript, and Tailwind CSS</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { 
  IconPuzzle, 
  IconCalculator, 
  IconTarget, 
  IconClock, 
  IconArrowRight, 
  IconMath, 
  IconBolt,
  IconDeviceDesktop,
  IconPalette,
  IconRocket
} from '@tabler/icons-vue'
</script>

<style scoped>
/* Add any additional custom styles if needed */
</style>