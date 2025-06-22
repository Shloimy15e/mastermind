<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { IconHome, IconPuzzle, IconCalculator, IconInfoCircle } from '@tabler/icons-vue'
</script>

<template>
  <div class="min-h-screen bg-gray-50 dark:bg-gray-900">
    <!-- Navigation Header -->
    <header class="bg-white dark:bg-gray-800 shadow-sm border-b border-gray-200 dark:border-gray-700">
      <div class="container mx-auto px-4">
        <div class="flex items-center justify-between h-16">
          <!-- Logo and Title -->
          <div class="flex items-center space-x-3">
            <div class="w-8 h-8 bg-gradient-to-br from-purple-500 to-pink-500 rounded-lg flex items-center justify-center">
              <span class="text-white font-bold text-sm">GH</span>
            </div>
            <h1 class="text-xl font-bold text-gray-900 dark:text-white">Gaming Hub</h1>
          </div>
          
          <!-- Navigation Links -->
          <nav class="flex items-center space-x-1">
            <RouterLink 
              to="/" 
              class="flex items-center space-x-2 px-3 py-2 rounded-lg text-sm font-medium transition-colors duration-200 hover:bg-gray-100 dark:hover:bg-gray-700 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-purple-100 dark:bg-purple-900 text-purple-700 dark:text-purple-300"
            >
              <IconHome class="w-4 h-4" />
              <span class="hidden sm:inline">Home</span>
            </RouterLink>
            
            <RouterLink 
              to="/mastermind" 
              class="flex items-center space-x-2 px-3 py-2 rounded-lg text-sm font-medium transition-colors duration-200 hover:bg-gray-100 dark:hover:bg-gray-700 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-purple-100 dark:bg-purple-900 text-purple-700 dark:text-purple-300"
            >
              <IconPuzzle class="w-4 h-4" />
              <span class="hidden sm:inline">Mastermind</span>
            </RouterLink>
            
            <RouterLink 
              to="/parser" 
              class="flex items-center space-x-2 px-3 py-2 rounded-lg text-sm font-medium transition-colors duration-200 hover:bg-gray-100 dark:hover:bg-gray-700 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-green-100 dark:bg-green-900 text-green-700 dark:text-green-300"
            >
              <IconCalculator class="w-4 h-4" />
              <span class="hidden sm:inline">Calculator</span>
            </RouterLink>
            
            <RouterLink 
              to="/about" 
              class="flex items-center space-x-2 px-3 py-2 rounded-lg text-sm font-medium transition-colors duration-200 hover:bg-gray-100 dark:hover:bg-gray-700 text-gray-700 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white"
              active-class="bg-blue-100 dark:bg-blue-900 text-blue-700 dark:text-blue-300"
            >
              <IconInfoCircle class="w-4 h-4" />
              <span class="hidden sm:inline">About</span>
            </RouterLink>
          </nav>
        </div>
      </div>
    </header>

    <!-- Main Content -->
    <main class="pt-0">
      <RouterView />
    </main>
  </div>
</template>

<style scoped>
/* Custom styles if needed */
</style>
