<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { IconHome, IconPuzzle, IconCalculator, IconInfoCircle } from '@tabler/icons-vue'
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-blue-50 to-indigo-100 dark:from-gray-950 dark:via-slate-900 dark:to-gray-900">
    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 bg-white/80 dark:bg-gray-900/80 backdrop-blur-xl border-b border-gray-200/50 dark:border-gray-700/50 shadow-sm">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-20">
          <!-- Logo and Title -->
          <div class="flex items-center space-x-4">
            <div class="relative">
              <div class="w-12 h-12 bg-gradient-to-br from-purple-500 via-pink-500 to-indigo-600 rounded-2xl flex items-center justify-center transform rotate-3 hover:rotate-6 transition-transform duration-300 shadow-lg">
                <span class="text-white font-black text-lg">GH</span>
              </div>
              <div class="absolute -top-1 -right-1 w-4 h-4 bg-green-400 rounded-full border-2 border-white dark:border-gray-900 animate-pulse"></div>
            </div>
            <div class="hidden sm:block">
              <h1 class="text-2xl font-black bg-gradient-to-r from-gray-900 via-purple-700 to-indigo-700 dark:from-white dark:via-purple-300 dark:to-blue-300 bg-clip-text text-transparent">
                Gaming Hub
              </h1>
              <p class="text-xs text-gray-500 dark:text-gray-400 font-medium">Interactive Experience</p>
            </div>
          </div>
          
          <!-- Navigation Links -->
          <nav class="flex items-center space-x-2">
            <RouterLink 
              to="/" 
              class="group relative flex items-center space-x-3 px-4 py-3 rounded-2xl text-sm font-semibold transition-all duration-300 hover:bg-gray-100/80 dark:hover:bg-gray-800/80 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-gradient-to-r from-purple-100 to-pink-100 dark:from-purple-900/40 dark:to-pink-900/40 text-purple-700 dark:text-purple-300 shadow-lg ring-1 ring-purple-200/50 dark:ring-purple-700/50"
            >
              <div class="relative">
                <IconHome class="w-5 h-5 transition-transform group-hover:scale-110" />
                <div class="absolute inset-0 bg-purple-400/20 rounded-full blur-sm opacity-0 group-hover:opacity-100 transition-opacity"></div>
              </div>
              <span class="hidden md:inline">Home</span>
              <div class="absolute inset-0 rounded-2xl bg-gradient-to-r from-purple-500/5 to-pink-500/5 opacity-0 group-hover:opacity-100 transition-opacity"></div>
            </RouterLink>
            
            <RouterLink 
              to="/mastermind" 
              class="group relative flex items-center space-x-3 px-4 py-3 rounded-2xl text-sm font-semibold transition-all duration-300 hover:bg-gray-100/80 dark:hover:bg-gray-800/80 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-gradient-to-r from-purple-100 to-pink-100 dark:from-purple-900/40 dark:to-pink-900/40 text-purple-700 dark:text-purple-300 shadow-lg ring-1 ring-purple-200/50 dark:ring-purple-700/50"
            >
              <div class="relative">
                <IconPuzzle class="w-5 h-5 transition-transform group-hover:scale-110" />
                <div class="absolute inset-0 bg-purple-400/20 rounded-full blur-sm opacity-0 group-hover:opacity-100 transition-opacity"></div>
              </div>
              <span class="hidden md:inline">Mastermind</span>
              <div class="absolute inset-0 rounded-2xl bg-gradient-to-r from-purple-500/5 to-pink-500/5 opacity-0 group-hover:opacity-100 transition-opacity"></div>
            </RouterLink>
            
            <RouterLink 
              to="/parser" 
              class="group relative flex items-center space-x-3 px-4 py-3 rounded-2xl text-sm font-semibold transition-all duration-300 hover:bg-gray-100/80 dark:hover:bg-gray-800/80 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-gradient-to-r from-green-100 to-blue-100 dark:from-green-900/40 dark:to-blue-900/40 text-green-700 dark:text-green-300 shadow-lg ring-1 ring-green-200/50 dark:ring-green-700/50"
            >
              <div class="relative">
                <IconCalculator class="w-5 h-5 transition-transform group-hover:scale-110" />
                <div class="absolute inset-0 bg-green-400/20 rounded-full blur-sm opacity-0 group-hover:opacity-100 transition-opacity"></div>
              </div>
              <span class="hidden md:inline">Calculator</span>
              <div class="absolute inset-0 rounded-2xl bg-gradient-to-r from-green-500/5 to-blue-500/5 opacity-0 group-hover:opacity-100 transition-opacity"></div>
            </RouterLink>
            
            <RouterLink 
              to="/about" 
              class="group relative flex items-center space-x-3 px-4 py-3 rounded-2xl text-sm font-semibold transition-all duration-300 hover:bg-gray-100/80 dark:hover:bg-gray-800/80 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-gradient-to-r from-blue-100 to-indigo-100 dark:from-blue-900/40 dark:to-indigo-900/40 text-blue-700 dark:text-blue-300 shadow-lg ring-1 ring-blue-200/50 dark:ring-blue-700/50"
            >
              <div class="relative">
                <IconInfoCircle class="w-5 h-5 transition-transform group-hover:scale-110" />
                <div class="absolute inset-0 bg-blue-400/20 rounded-full blur-sm opacity-0 group-hover:opacity-100 transition-opacity"></div>
              </div>
              <span class="hidden md:inline">About</span>
              <div class="absolute inset-0 rounded-2xl bg-gradient-to-r from-blue-500/5 to-indigo-500/5 opacity-0 group-hover:opacity-100 transition-opacity"></div>
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
/* Enhanced hover effects */
.router-link-active {
  transform: translateY(-1px);
}

/* Custom backdrop blur fallback */
@supports not (backdrop-filter: blur(12px)) {
  header {
    background-color: rgba(255, 255, 255, 0.95);
  }
  
  .dark header {
    background-color: rgba(17, 24, 39, 0.95);
  }
}
</style>
