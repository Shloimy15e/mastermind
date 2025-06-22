<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { IconHome, IconPuzzle, IconCalculator, IconInfoCircle } from '@tabler/icons-vue'
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 relative">
    <!-- Ultra Premium Navigation -->
    <header class="fixed top-0 left-0 right-0 z-50 bg-black/20 backdrop-blur-2xl border-b border-white/10 shadow-2xl">
      <!-- Animated Background -->
      <div class="absolute inset-0 bg-gradient-to-r from-purple-600/10 via-transparent to-pink-600/10 animate-pulse"></div>
      
      <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between h-24">
          
          <!-- Ultra Premium Logo -->
          <div class="flex items-center space-x-6">
            <div class="relative group">
              <!-- Logo Glow Effect -->
              <div class="absolute inset-0 bg-gradient-to-r from-purple-500 to-pink-500 rounded-3xl blur-lg opacity-75 group-hover:opacity-100 transition-opacity duration-500 scale-110"></div>
              
              <!-- Main Logo -->
              <div class="relative w-16 h-16 bg-gradient-to-br from-purple-600 via-pink-600 to-indigo-600 rounded-3xl flex items-center justify-center transform rotate-6 group-hover:rotate-12 group-hover:scale-110 transition-all duration-500 shadow-2xl">
                <span class="text-white font-black text-2xl">GH</span>
                
                <!-- Holographic Sweep -->
                <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/30 to-transparent skew-x-12 transform -translate-x-full group-hover:translate-x-full transition-transform duration-1000 rounded-3xl"></div>
              </div>
              
              <!-- Status Indicator -->
              <div class="absolute -top-2 -right-2 w-6 h-6 bg-gradient-to-r from-green-400 to-emerald-400 rounded-full border-2 border-black shadow-lg animate-pulse"></div>
            </div>
            
            <div class="hidden sm:block">
              <h1 class="text-3xl font-black bg-gradient-to-r from-white via-purple-200 to-pink-200 bg-clip-text text-transparent transform hover:scale-105 transition-transform duration-500">
                GAMING HUB
              </h1>
              <p class="text-xs text-gray-400 font-bold tracking-wider uppercase">Next-Gen Experience</p>
            </div>
          </div>
          
          <!-- Revolutionary Navigation -->
          <nav class="flex items-center space-x-3">
            
            <!-- Home -->
            <RouterLink 
              to="/" 
              class="group relative flex items-center space-x-4 px-6 py-4 rounded-2xl font-bold text-sm transition-all duration-500 hover:bg-white/10 text-gray-300 hover:text-white transform hover:scale-105 hover:-translate-y-1"
              active-class="bg-gradient-to-r from-purple-600/30 to-pink-600/30 text-white border border-purple-500/50 shadow-lg shadow-purple-500/25"
            >
              <!-- Icon Container with 3D Effects -->
              <div class="relative">
                <div class="absolute inset-0 bg-purple-400/30 rounded-xl blur-sm opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                <div class="relative w-10 h-10 bg-gradient-to-br from-purple-500/20 to-pink-500/20 rounded-xl flex items-center justify-center border border-purple-500/30 group-hover:border-purple-400/60 transition-all duration-500">
                  <IconHome class="w-5 h-5 group-hover:scale-125 group-hover:rotate-12 transition-all duration-500" />
                </div>
              </div>
              
              <span class="hidden lg:inline group-hover:text-purple-300 transition-colors duration-500">HOME</span>
              
              <!-- Hover Glow -->
              <div class="absolute inset-0 rounded-2xl bg-gradient-to-r from-purple-500/0 via-purple-500/20 to-purple-500/0 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            </RouterLink>
            
            <!-- Mastermind -->
            <RouterLink 
              to="/mastermind" 
              class="group relative flex items-center space-x-4 px-6 py-4 rounded-2xl font-bold text-sm transition-all duration-500 hover:bg-white/10 text-gray-300 hover:text-white transform hover:scale-105 hover:-translate-y-1"
              active-class="bg-gradient-to-r from-purple-600/30 to-pink-600/30 text-white border border-purple-500/50 shadow-lg shadow-purple-500/25"
            >
              <div class="relative">
                <div class="absolute inset-0 bg-purple-400/30 rounded-xl blur-sm opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                <div class="relative w-10 h-10 bg-gradient-to-br from-purple-500/20 to-pink-500/20 rounded-xl flex items-center justify-center border border-purple-500/30 group-hover:border-purple-400/60 transition-all duration-500">
                  <IconPuzzle class="w-5 h-5 group-hover:scale-125 group-hover:rotate-180 transition-all duration-700" />
                </div>
              </div>
              
              <span class="hidden lg:inline group-hover:text-purple-300 transition-colors duration-500">MASTERMIND</span>
              
              <div class="absolute inset-0 rounded-2xl bg-gradient-to-r from-purple-500/0 via-purple-500/20 to-purple-500/0 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            </RouterLink>
            
            <!-- Calculator -->
            <RouterLink 
              to="/parser" 
              class="group relative flex items-center space-x-4 px-6 py-4 rounded-2xl font-bold text-sm transition-all duration-500 hover:bg-white/10 text-gray-300 hover:text-white transform hover:scale-105 hover:-translate-y-1"
              active-class="bg-gradient-to-r from-emerald-600/30 to-cyan-600/30 text-white border border-emerald-500/50 shadow-lg shadow-emerald-500/25"
            >
              <div class="relative">
                <div class="absolute inset-0 bg-emerald-400/30 rounded-xl blur-sm opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                <div class="relative w-10 h-10 bg-gradient-to-br from-emerald-500/20 to-cyan-500/20 rounded-xl flex items-center justify-center border border-emerald-500/30 group-hover:border-emerald-400/60 transition-all duration-500">
                  <IconCalculator class="w-5 h-5 group-hover:scale-125 group-hover:rotate-180 transition-all duration-700" />
                </div>
              </div>
              
              <span class="hidden lg:inline group-hover:text-emerald-300 transition-colors duration-500">CALCULATOR</span>
              
              <div class="absolute inset-0 rounded-2xl bg-gradient-to-r from-emerald-500/0 via-emerald-500/20 to-emerald-500/0 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            </RouterLink>
            
            <!-- About -->
            <RouterLink 
              to="/about" 
              class="group relative flex items-center space-x-4 px-6 py-4 rounded-2xl font-bold text-sm transition-all duration-500 hover:bg-white/10 text-gray-300 hover:text-white transform hover:scale-105 hover:-translate-y-1"
              active-class="bg-gradient-to-r from-blue-600/30 to-indigo-600/30 text-white border border-blue-500/50 shadow-lg shadow-blue-500/25"
            >
              <div class="relative">
                <div class="absolute inset-0 bg-blue-400/30 rounded-xl blur-sm opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                <div class="relative w-10 h-10 bg-gradient-to-br from-blue-500/20 to-indigo-500/20 rounded-xl flex items-center justify-center border border-blue-500/30 group-hover:border-blue-400/60 transition-all duration-500">
                  <IconInfoCircle class="w-5 h-5 group-hover:scale-125 group-hover:rotate-12 transition-all duration-500" />
                </div>
              </div>
              
              <span class="hidden lg:inline group-hover:text-blue-300 transition-colors duration-500">ABOUT</span>
              
              <div class="absolute inset-0 rounded-2xl bg-gradient-to-r from-blue-500/0 via-blue-500/20 to-blue-500/0 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            </RouterLink>
          </nav>
        </div>
      </div>
      
      <!-- Bottom Glow Line -->
      <div class="absolute bottom-0 left-0 right-0 h-px bg-gradient-to-r from-transparent via-purple-500/50 to-transparent"></div>
    </header>

    <!-- Main Content with Padding for Fixed Header -->
    <main class="relative min-h-screen pt-24">
      <RouterView />
    </main>
  </div>
</template>

<style scoped>
/* Enhanced 3D Effects */
.transform-gpu {
  transform: translateZ(0);
  backface-visibility: hidden;
}

/* Router Link Active State Enhancements */
.router-link-active {
  transform: translateY(-2px) scale(1.05);
  box-shadow: 0 10px 25px -5px rgba(147, 51, 234, 0.4);
}

/* Custom Hover Effects */
.group:hover .transform {
  transform: translateY(-2px) scale(1.05);
}

/* Backdrop Blur Fallback */
@supports not (backdrop-filter: blur(32px)) {
  header {
    background-color: rgba(0, 0, 0, 0.9);
  }
}

/* Advanced Animation Timing */
* {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}

/* Holographic Effect */
@keyframes holographic {
  0% { transform: translateX(-100%) skewX(-12deg); }
  100% { transform: translateX(200%) skewX(-12deg); }
}

.group:hover .holographic {
  animation: holographic 1s ease-out;
}
</style>
