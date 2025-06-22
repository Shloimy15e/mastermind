<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { IconHome, IconPuzzle, IconCalculator, IconInfoCircle } from '@tabler/icons-vue'
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800 relative">
    <!-- Professional Navigation -->
    <header class="sticky top-0 z-50 bg-white/90 dark:bg-gray-900/90 backdrop-blur-xl border-b border-gray-200/50 dark:border-gray-700/50 shadow-sm">
      <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-20">
          
          <!-- Professional Logo -->
          <div class="flex items-center space-x-4">
            <div class="relative group">
              <div class="w-12 h-12 bg-gradient-to-br from-blue-600 via-indigo-600 to-purple-600 rounded-xl flex items-center justify-center transform hover:scale-105 transition-all duration-300 shadow-lg">
                <span class="text-white font-bold text-lg">PS</span>
              </div>
            </div>
            
            <div class="hidden sm:block">
              <h1 class="text-xl font-bold text-gray-900 dark:text-white">
                Project Showcase
              </h1>
              <p class="text-xs text-gray-500 dark:text-gray-400 font-medium">Interactive Portfolio</p>
            </div>
          </div>
          
          <!-- Professional Navigation -->
          <nav class="flex items-center space-x-2">
            
            <RouterLink 
              to="/" 
              class="group flex items-center space-x-3 px-4 py-3 rounded-xl text-sm font-semibold transition-all duration-300 hover:bg-gray-100 dark:hover:bg-gray-800 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-blue-50 dark:bg-blue-900/30 text-blue-700 dark:text-blue-300 border border-blue-200/50 dark:border-blue-700/50"
            >
              <div class="relative">
                <IconHome class="w-5 h-5 transition-transform group-hover:scale-110 duration-300" />
              </div>
              <span class="hidden md:inline">Home</span>
            </RouterLink>
            
            <RouterLink 
              to="/mastermind" 
              class="group flex items-center space-x-3 px-4 py-3 rounded-xl text-sm font-semibold transition-all duration-300 hover:bg-gray-100 dark:hover:bg-gray-800 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-indigo-50 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 border border-indigo-200/50 dark:border-indigo-700/50"
            >
              <div class="relative">
                <IconPuzzle class="w-5 h-5 transition-transform group-hover:scale-110 duration-300" />
              </div>
              <span class="hidden md:inline">Logic Game</span>
            </RouterLink>
            
            <RouterLink 
              to="/parser" 
              class="group flex items-center space-x-3 px-4 py-3 rounded-xl text-sm font-semibold transition-all duration-300 hover:bg-gray-100 dark:hover:bg-gray-800 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-purple-50 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 border border-purple-200/50 dark:border-purple-700/50"
            >
              <div class="relative">
                <IconCalculator class="w-5 h-5 transition-transform group-hover:scale-110 duration-300" />
              </div>
              <span class="hidden md:inline">Calculator</span>
            </RouterLink>
            
            <RouterLink 
              to="/about" 
              class="group flex items-center space-x-3 px-4 py-3 rounded-xl text-sm font-semibold transition-all duration-300 hover:bg-gray-100 dark:hover:bg-gray-800 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-gray-50 dark:bg-gray-800/50 text-gray-700 dark:text-gray-300 border border-gray-200/50 dark:border-gray-700/50"
            >
              <div class="relative">
                <IconInfoCircle class="w-5 h-5 transition-transform group-hover:scale-110 duration-300" />
              </div>
              <span class="hidden md:inline">About</span>
            </RouterLink>
          </nav>
        </div>
      </div>
    </header>

    <!-- Main Content -->
    <main class="relative min-h-screen">
      <RouterView />
    </main>
  </div>
</template>

<style scoped>
/* Professional Styling */
.router-link-active {
  transform: translateY(-1px);
  box-shadow: 0 4px 12px -2px rgba(0, 0, 0, 0.1);
}

/* Smooth Transitions */
* {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}

/* Backdrop Blur Support */
@supports not (backdrop-filter: blur(12px)) {
  header {
    background-color: rgba(255, 255, 255, 0.95);
  }
  
  .dark header {
    background-color: rgba(17, 24, 39, 0.95);
  }
}
</style>
