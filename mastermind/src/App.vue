<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { IconHome, IconPuzzle, IconCalculator, IconInfoCircle } from '@tabler/icons-vue'
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800 relative">
    <!-- Enhanced Professional Navigation -->
    <header class="sticky top-0 z-50 bg-white/95 dark:bg-gray-900/95 backdrop-blur-xl border-b border-gray-200/60 dark:border-gray-700/60 shadow-lg">
      <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12">
        <div class="flex items-center justify-between h-24">
          
          <!-- Enhanced Logo Section -->
          <div class="flex items-center space-x-5">
            <div class="relative group">
              <div class="absolute inset-0 bg-gradient-to-br from-blue-600 via-indigo-600 to-purple-600 rounded-2xl blur-sm opacity-20 group-hover:opacity-40 transition-opacity duration-300"></div>
              <div class="relative w-14 h-14 bg-gradient-to-br from-blue-600 via-indigo-600 to-purple-600 rounded-2xl flex items-center justify-center transform hover:scale-105 transition-all duration-300 shadow-xl hover:shadow-2xl">
                <span class="text-white font-bold text-xl">PS</span>
              </div>
            </div>
            
            <div class="hidden sm:block">
              <h1 class="text-2xl font-bold bg-gradient-to-r from-gray-900 via-blue-800 to-indigo-900 dark:from-white dark:via-blue-200 dark:to-indigo-200 bg-clip-text text-transparent">
                Project Showcase
              </h1>
              <p class="text-sm text-gray-600 dark:text-gray-400 font-medium mt-0.5">Interactive Portfolio</p>
            </div>
          </div>
          
          <!-- Enhanced Navigation Buttons -->
          <nav class="flex items-center space-x-3">
            
            <RouterLink 
              to="/" 
              class="nav-button group"
              active-class="nav-button-active nav-button-home-active"
            >
              <div class="nav-icon-wrapper">
                <IconHome class="w-5 h-5 transition-all duration-300 group-hover:scale-110" />
              </div>
              <span class="nav-text">Home</span>
            </RouterLink>
            
            <RouterLink 
              to="/mastermind" 
              class="nav-button group"
              active-class="nav-button-active nav-button-logic-active"
            >
              <div class="nav-icon-wrapper">
                <IconPuzzle class="w-5 h-5 transition-all duration-300 group-hover:scale-110 group-hover:rotate-12" />
              </div>
              <span class="nav-text">Logic Game</span>
            </RouterLink>
            
            <RouterLink 
              to="/parser" 
              class="nav-button group"
              active-class="nav-button-active nav-button-calc-active"
            >
              <div class="nav-icon-wrapper">
                <IconCalculator class="w-5 h-5 transition-all duration-300 group-hover:scale-110" />
              </div>
              <span class="nav-text">Calculator</span>
            </RouterLink>
            
            <RouterLink 
              to="/about" 
              class="nav-button group"
              active-class="nav-button-active nav-button-about-active"
            >
              <div class="nav-icon-wrapper">
                <IconInfoCircle class="w-5 h-5 transition-all duration-300 group-hover:scale-110" />
              </div>
              <span class="nav-text">About</span>
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
/* Enhanced Navigation Buttons */
.nav-button {
  position: relative;
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.875rem 1.25rem;
  border-radius: 1rem;
  font-size: 0.875rem;
  font-weight: 600;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  color: rgb(55 65 81);
  background: rgba(249 250 251 / 0.5);
  border: 1px solid transparent;
  box-shadow: 0 1px 2px 0 rgba(0 0 0 / 0.05);
  backdrop-filter: blur(8px);
  transform: translateY(0);
}

.dark .nav-button {
  color: rgb(209 213 219);
  background: rgba(31 41 55 / 0.5);
}

.nav-button:hover {
  color: rgb(17 24 39);
  background: white;
  border-color: rgba(229 231 235 / 0.6);
  box-shadow: 0 10px 15px -3px rgba(0 0 0 / 0.1);
  transform: translateY(-2px);
}

.dark .nav-button:hover {
  color: white;
  background: rgb(55 65 81);
  border-color: rgba(75 85 99 / 0.6);
}

.nav-button::before {
  content: '';
  position: absolute;
  inset: 0;
  border-radius: 1rem;
  opacity: 0;
  transition: opacity 0.3s;
  background: linear-gradient(135deg, rgba(255, 255, 255, 0.1) 0%, rgba(255, 255, 255, 0.05) 100%);
}

.nav-button:hover::before {
  opacity: 1;
}

.nav-icon-wrapper {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

.nav-text {
  font-weight: 500;
  letter-spacing: 0.025em;
}

@media (max-width: 768px) {
  .nav-text {
    display: none;
  }
}

/* Enhanced Active States */
.nav-button-active {
  transform: translateY(-2px);
  box-shadow: 0 10px 15px -3px rgba(0 0 0 / 0.1);
  border-style: solid;
  backdrop-filter: blur(12px);
}

.nav-button-home-active {
  background: linear-gradient(to right, rgb(239 246 255), rgb(238 242 255));
  color: rgb(29 78 216);
  border-color: rgba(147 197 253 / 0.8);
  box-shadow: 0 8px 25px -8px rgba(59, 130, 246, 0.3);
}

.dark .nav-button-home-active {
  background: linear-gradient(to right, rgba(30 58 138 / 0.4), rgba(49 46 129 / 0.4));
  color: rgb(147 197 253);
  border-color: rgba(29 78 216 / 0.8);
}

.nav-button-logic-active {
  background: linear-gradient(to right, rgb(238 242 255), rgb(250 245 255));
  color: rgb(67 56 202);
  border-color: rgba(165 180 252 / 0.8);
  box-shadow: 0 8px 25px -8px rgba(99, 102, 241, 0.3);
}

.dark .nav-button-logic-active {
  background: linear-gradient(to right, rgba(49 46 129 / 0.4), rgba(88 28 135 / 0.4));
  color: rgb(165 180 252);
  border-color: rgba(67 56 202 / 0.8);
}

.nav-button-calc-active {
  background: linear-gradient(to right, rgb(250 245 255), rgb(253 242 248));
  color: rgb(126 34 206);
  border-color: rgba(196 181 253 / 0.8);
  box-shadow: 0 8px 25px -8px rgba(147, 51, 234, 0.3);
}

.dark .nav-button-calc-active {
  background: linear-gradient(to right, rgba(88 28 135 / 0.4), rgba(157 23 77 / 0.4));
  color: rgb(196 181 253);
  border-color: rgba(126 34 206 / 0.8);
}

.nav-button-about-active {
  background: linear-gradient(to right, rgb(249 250 251), rgb(248 250 252));
  color: rgb(55 65 81);
  border-color: rgba(229 231 235 / 0.8);
  box-shadow: 0 8px 25px -8px rgba(107, 114, 128, 0.3);
}

.dark .nav-button-about-active {
  background: linear-gradient(to right, rgba(31 41 55 / 0.6), rgba(30 41 59 / 0.6));
  color: rgb(209 213 219);
  border-color: rgba(75 85 99 / 0.8);
}

/* Enhanced Hover Effects */
.nav-button-active:hover {
  transform: translateY(-3px);
}

/* Focus States for Accessibility */
.nav-button:focus {
  outline: none;
  box-shadow: 0 0 0 2px white, 0 0 0 4px rgba(59 130 246 / 0.5);
}

.dark .nav-button:focus {
  box-shadow: 0 0 0 2px rgb(17 24 39), 0 0 0 4px rgba(59 130 246 / 0.5);
}

/* Enhanced Transitions */
* {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}

/* Backdrop Blur Fallbacks */
@supports not (backdrop-filter: blur(12px)) {
  header {
    background-color: rgba(255, 255, 255, 0.98);
  }
  
  .dark header {
    background-color: rgba(17, 24, 39, 0.98);
  }
  
  .nav-button {
    background-color: rgba(249, 250, 251, 0.8);
  }
  
  .dark .nav-button {
    background-color: rgba(31, 41, 55, 0.8);
  }
}

/* Mobile Responsive Adjustments */
@media (max-width: 768px) {
  header .max-w-7xl {
    padding-left: 1rem;
    padding-right: 1rem;
  }
  
  header .flex.justify-between {
    height: 5rem;
  }
  
  .nav-button {
    padding: 0.75rem 1rem;
  }
}
</style>
