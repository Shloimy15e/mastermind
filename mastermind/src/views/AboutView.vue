<template>
  <div class="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100 dark:from-gray-900 dark:to-gray-800">
    <div class="container mx-auto px-4 py-12">
      <!-- Header Section -->
      <div class="text-center mb-12">
        <h1 class="text-4xl font-bold text-gray-900 dark:text-white mb-4">
          About Gaming Hub
        </h1>
        <p class="text-lg text-gray-600 dark:text-gray-300 max-w-3xl mx-auto">
          A collection of interactive games and tools built with modern web technologies. 
          Designed to challenge your mind and provide useful utilities in an elegant interface.
        </p>
      </div>

      <!-- Applications Section -->
      <div class="max-w-4xl mx-auto mb-16">
        <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-8 text-center">Our Applications</h2>
        
        <div class="space-y-8">
          <!-- Mastermind Game -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg p-8">
            <div class="flex items-start space-x-6">
              <div class="w-16 h-16 bg-gradient-to-br from-purple-400 to-pink-400 rounded-xl flex items-center justify-center flex-shrink-0">
                <IconPuzzle class="w-8 h-8 text-white" />
              </div>
              <div class="flex-1">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-3">Mastermind Game</h3>
                <p class="text-gray-600 dark:text-gray-300 mb-4">
                  A digital implementation of the classic Mastermind board game. Challenge your deductive reasoning 
                  by trying to guess the secret color combination within 10 attempts. Each guess provides valuable 
                  feedback to help you narrow down the solution.
                </p>
                <div class="flex flex-wrap gap-2">
                  <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900 text-purple-800 dark:text-purple-200 rounded-full text-sm">Logic Puzzle</span>
                  <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900 text-purple-800 dark:text-purple-200 rounded-full text-sm">Deductive Reasoning</span>
                  <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900 text-purple-800 dark:text-purple-200 rounded-full text-sm">Color Recognition</span>
                </div>
              </div>
            </div>
          </div>

          <!-- Math Parser Calculator -->
          <div class="bg-white dark:bg-gray-800 rounded-xl shadow-lg p-8">
            <div class="flex items-start space-x-6">
              <div class="w-16 h-16 bg-gradient-to-br from-green-400 to-blue-500 rounded-xl flex items-center justify-center flex-shrink-0">
                <IconCalculator class="w-8 h-8 text-white" />
              </div>
              <div class="flex-1">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-3">Math Parser Calculator</h3>
                <p class="text-gray-600 dark:text-gray-300 mb-4">
                  An advanced mathematical expression parser and calculator that supports complex equations with 
                  parentheses, multiple operators, and proper order of operations. Built with custom parsing algorithms 
                  for accurate and reliable calculations.
                </p>
                <div class="flex flex-wrap gap-2">
                  <span class="px-3 py-1 bg-green-100 dark:bg-green-900 text-green-800 dark:text-green-200 rounded-full text-sm">Mathematical Parser</span>
                  <span class="px-3 py-1 bg-green-100 dark:bg-green-900 text-green-800 dark:text-green-200 rounded-full text-sm">Expression Evaluation</span>
                  <span class="px-3 py-1 bg-green-100 dark:bg-green-900 text-green-800 dark:text-green-200 rounded-full text-sm">Algorithm Implementation</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Technology Stack -->
      <div class="max-w-4xl mx-auto mb-16">
        <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-8 text-center">Built With</h2>
        
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
          <div class="bg-white dark:bg-gray-800 rounded-lg p-6 text-center">
            <div class="w-12 h-12 bg-green-100 dark:bg-green-900 rounded-lg flex items-center justify-center mx-auto mb-4">
              <IconBrandVue class="w-6 h-6 text-green-600 dark:text-green-400" />
            </div>
            <h3 class="font-semibold text-gray-900 dark:text-white mb-2">Vue 3</h3>
            <p class="text-sm text-gray-600 dark:text-gray-300">Progressive JavaScript framework with Composition API</p>
          </div>
          
          <div class="bg-white dark:bg-gray-800 rounded-lg p-6 text-center">
            <div class="w-12 h-12 bg-blue-100 dark:bg-blue-900 rounded-lg flex items-center justify-center mx-auto mb-4">
              <IconBrandTypescript class="w-6 h-6 text-blue-600 dark:text-blue-400" />
            </div>
            <h3 class="font-semibold text-gray-900 dark:text-white mb-2">TypeScript</h3>
            <p class="text-sm text-gray-600 dark:text-gray-300">Type-safe JavaScript for better development experience</p>
          </div>
          
          <div class="bg-white dark:bg-gray-800 rounded-lg p-6 text-center">
            <div class="w-12 h-12 bg-cyan-100 dark:bg-cyan-900 rounded-lg flex items-center justify-center mx-auto mb-4">
              <IconBrandTailwind class="w-6 h-6 text-cyan-600 dark:text-cyan-400" />
            </div>
            <h3 class="font-semibold text-gray-900 dark:text-white mb-2">Tailwind CSS</h3>
            <p class="text-sm text-gray-600 dark:text-gray-300">Utility-first CSS framework for rapid UI development</p>
          </div>
          
          <div class="bg-white dark:bg-gray-800 rounded-lg p-6 text-center">
            <div class="w-12 h-12 bg-purple-100 dark:bg-purple-900 rounded-lg flex items-center justify-center mx-auto mb-4">
              <IconComponents class="w-6 h-6 text-purple-600 dark:text-purple-400" />
            </div>
            <h3 class="font-semibold text-gray-900 dark:text-white mb-2">Headless UI</h3>
            <p class="text-sm text-gray-600 dark:text-gray-300">Unstyled, accessible UI components</p>
          </div>
          
          <div class="bg-white dark:bg-gray-800 rounded-lg p-6 text-center">
            <div class="w-12 h-12 bg-orange-100 dark:bg-orange-900 rounded-lg flex items-center justify-center mx-auto mb-4">
              <IconBrandVite class="w-6 h-6 text-orange-600 dark:text-orange-400" />
            </div>
            <h3 class="font-semibold text-gray-900 dark:text-white mb-2">Vite</h3>
            <p class="text-sm text-gray-600 dark:text-gray-300">Next generation frontend build tool</p>
          </div>
          
          <div class="bg-white dark:bg-gray-800 rounded-lg p-6 text-center">
            <div class="w-12 h-12 bg-gray-100 dark:bg-gray-700 rounded-lg flex items-center justify-center mx-auto mb-4">
              <IconIcons class="w-6 h-6 text-gray-600 dark:text-gray-300" />
            </div>
            <h3 class="font-semibold text-gray-900 dark:text-white mb-2">Tabler Icons</h3>
            <p class="text-sm text-gray-600 dark:text-gray-300">Beautiful SVG icons for modern interfaces</p>
          </div>
        </div>
      </div>

      <!-- Features -->
      <div class="max-w-4xl mx-auto">
        <h2 class="text-2xl font-bold text-gray-900 dark:text-white mb-8 text-center">Key Features</h2>
        
        <div class="grid md:grid-cols-2 gap-8">
          <div class="space-y-4">
            <div class="flex items-start space-x-3">
              <IconCheck class="w-5 h-5 text-green-500 mt-1 flex-shrink-0" />
              <div>
                <h4 class="font-semibold text-gray-900 dark:text-white">Responsive Design</h4>
                <p class="text-sm text-gray-600 dark:text-gray-300">Optimized for all screen sizes and devices</p>
              </div>
            </div>
            
            <div class="flex items-start space-x-3">
              <IconCheck class="w-5 h-5 text-green-500 mt-1 flex-shrink-0" />
              <div>
                <h4 class="font-semibold text-gray-900 dark:text-white">Dark Mode Support</h4>
                <p class="text-sm text-gray-600 dark:text-gray-300">Beautiful interface in both light and dark themes</p>
              </div>
            </div>
            
            <div class="flex items-start space-x-3">
              <IconCheck class="w-5 h-5 text-green-500 mt-1 flex-shrink-0" />
              <div>
                <h4 class="font-semibold text-gray-900 dark:text-white">Fast Performance</h4>
                <p class="text-sm text-gray-600 dark:text-gray-300">Built with modern tools for optimal speed</p>
              </div>
            </div>
          </div>
          
          <div class="space-y-4">
            <div class="flex items-start space-x-3">
              <IconCheck class="w-5 h-5 text-green-500 mt-1 flex-shrink-0" />
              <div>
                <h4 class="font-semibold text-gray-900 dark:text-white">Type Safety</h4>
                <p class="text-sm text-gray-600 dark:text-gray-300">TypeScript ensures reliable code quality</p>
              </div>
            </div>
            
            <div class="flex items-start space-x-3">
              <IconCheck class="w-5 h-5 text-green-500 mt-1 flex-shrink-0" />
              <div>
                <h4 class="font-semibold text-gray-900 dark:text-white">Accessible UI</h4>
                <p class="text-sm text-gray-600 dark:text-gray-300">Built with accessibility best practices</p>
              </div>
            </div>
            
            <div class="flex items-start space-x-3">
              <IconCheck class="w-5 h-5 text-green-500 mt-1 flex-shrink-0" />
              <div>
                <h4 class="font-semibold text-gray-900 dark:text-white">Smooth Animations</h4>
                <p class="text-sm text-gray-600 dark:text-gray-300">Delightful transitions and hover effects</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { 
  IconPuzzle,
  IconCalculator,
  IconBrandVue,
  IconBrandTypescript,
  IconBrandTailwind,
  IconBrandVite,
  IconComponents,
  IconIcons,
  IconCheck
} from '@tabler/icons-vue'
</script>

<style scoped>
/* Add any additional custom styles if needed */
</style>
