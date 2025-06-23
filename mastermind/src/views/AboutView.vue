<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800 relative overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute inset-0 opacity-20">
        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-r from-blue-500/8 via-indigo-500/8 to-purple-500/8"></div>
      </div>
      
      <!-- Floating Elements -->
      <div class="absolute inset-0">
        <div class="absolute top-[15%] left-[10%] w-20 h-20 bg-gradient-to-br from-blue-400/15 to-indigo-600/15 rounded-2xl opacity-40 animate-float transform rotate-12"></div>
        <div class="absolute top-[30%] right-[12%] w-16 h-16 bg-gradient-to-br from-indigo-400/15 to-purple-600/15 rounded-full opacity-30 animate-float-delay"></div>
        <div class="absolute bottom-[25%] left-[20%] w-24 h-24 bg-gradient-to-br from-purple-400/15 to-pink-600/15 rounded-xl opacity-25 animate-float"></div>
      </div>
    </div>

    <div class="relative z-10 min-h-screen grid grid-rows-[auto_1fr_auto] gap-0">
      <!-- Content Container -->
      <div class="grid place-items-center gap-16 px-6 py-16">
        
        <!-- Header Section -->
        <div class="grid place-items-center gap-8 text-center max-w-4xl">
          <div class="inline-flex items-center px-5 py-2.5 rounded-full bg-white/90 dark:bg-gray-800/90 backdrop-blur-xl border border-gray-200/60 dark:border-gray-700/60 shadow-lg">
            <div class="w-1.5 h-1.5 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-full animate-pulse mr-2.5"></div>
            <span class="text-xs font-medium text-gray-700 dark:text-gray-300 tracking-wide">ABOUT PROJECT SHOWCASE</span>
          </div>
          
          <h1 class="text-5xl sm:text-6xl lg:text-7xl font-black leading-[0.9] tracking-tight">
            <span class="block bg-gradient-to-r from-gray-900 via-blue-800 to-indigo-900 dark:from-white dark:via-blue-200 dark:to-indigo-200 bg-clip-text text-transparent">
              About Our
            </span>
            <span class="block bg-gradient-to-r from-indigo-800 via-purple-800 to-blue-900 dark:from-indigo-200 dark:via-purple-200 dark:to-blue-200 bg-clip-text text-transparent">
              Platform
            </span>
          </h1>
          
          <p class="text-xl sm:text-2xl leading-[1.6] font-light text-gray-600 dark:text-gray-300">
            A collection of <span class="font-semibold text-blue-600 dark:text-blue-400">interactive applications</span> and 
            <span class="font-semibold text-indigo-600 dark:text-indigo-400">problem-solving tools</span> 
            built with modern web technologies.
          </p>
        </div>

        <!-- Applications Section -->
        <div class="grid place-items-center gap-12 w-full max-w-6xl">
          <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white">Featured Applications</h2>
          
          <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 w-full">
            <!-- Mastermind Game -->
            <div class="group">
              <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 overflow-hidden shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
                <div class="relative h-32 bg-gradient-to-br from-blue-500 via-indigo-600 to-purple-600 overflow-hidden">
                  <div class="absolute inset-0 opacity-20">
                    <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 20px 20px;"></div>
                  </div>
                  <div class="absolute inset-0 grid place-items-center">
                    <IconPuzzle class="w-12 h-12 text-white opacity-80" />
                  </div>
                </div>
                
                <div class="grid gap-6 p-8">
                  <h3 class="text-2xl font-bold text-gray-900 dark:text-white">Mastermind Game</h3>
                  <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                    A digital implementation of the classic Mastermind board game. Challenge your deductive reasoning 
                    by trying to guess the secret color combination within 10 attempts.
                  </p>
                  <div class="grid grid-flow-col gap-2 justify-start">
                    <span class="px-3 py-1.5 bg-blue-100 dark:bg-blue-900/30 text-blue-700 dark:text-blue-300 rounded-full text-sm font-medium">Logic Puzzle</span>
                    <span class="px-3 py-1.5 bg-indigo-100 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 rounded-full text-sm font-medium">Deductive Reasoning</span>
                    <span class="px-3 py-1.5 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 rounded-full text-sm font-medium">Interactive</span>
                  </div>
                </div>
              </div>
            </div>

            <!-- Math Parser Calculator -->
            <div class="group">
              <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 overflow-hidden shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
                <div class="relative h-32 bg-gradient-to-br from-indigo-500 via-purple-600 to-pink-600 overflow-hidden">
                  <div class="absolute inset-0 opacity-20">
                    <div class="absolute inset-0" style="background-image: linear-gradient(45deg, transparent 35%, white 35%, white 65%, transparent 65%), linear-gradient(-45deg, transparent 35%, white 35%, white 65%, transparent 65%); background-size: 16px 16px;"></div>
                  </div>
                  <div class="absolute inset-0 grid place-items-center">
                    <IconCalculator class="w-12 h-12 text-white opacity-80" />
                  </div>
                </div>
                
                <div class="grid gap-6 p-8">
                  <h3 class="text-2xl font-bold text-gray-900 dark:text-white">Math Parser Calculator</h3>
                  <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                    An advanced mathematical expression parser that supports complex equations with 
                    parentheses, multiple operators, and proper order of operations.
                  </p>
                  <div class="grid grid-flow-col gap-2 justify-start">
                    <span class="px-3 py-1.5 bg-indigo-100 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 rounded-full text-sm font-medium">Parser</span>
                    <span class="px-3 py-1.5 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 rounded-full text-sm font-medium">Algorithms</span>
                    <span class="px-3 py-1.5 bg-pink-100 dark:bg-pink-900/30 text-pink-700 dark:text-pink-300 rounded-full text-sm font-medium">Real-time</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Technology Stack -->
        <div class="grid place-items-center gap-12 w-full max-w-6xl">
          <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white">Built With Modern Technologies</h2>
          
          <div class="grid grid-cols-2 md:grid-cols-3 gap-6 w-full">
            <div class="group">
              <div class="grid place-items-center gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div class="relative w-16 h-16">
                  <div class="absolute inset-0 bg-gradient-to-r from-emerald-500 to-blue-500 rounded-xl rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                  <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full grid place-items-center border border-emerald-100 dark:border-emerald-800">
                    <IconBrandVue class="w-8 h-8 text-emerald-600 dark:text-emerald-400" />
                  </div>
                </div>
                <div class="grid place-items-center gap-2 text-center">
                  <h3 class="font-bold text-gray-900 dark:text-white">Vue 3</h3>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Progressive JavaScript framework with Composition API</p>
                </div>
              </div>
            </div>
            
            <div class="group">
              <div class="grid place-items-center gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div class="relative w-16 h-16">
                  <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-xl rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                  <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full grid place-items-center border border-blue-100 dark:border-blue-800">
                    <IconBrandTypescript class="w-8 h-8 text-blue-600 dark:text-blue-400" />
                  </div>
                </div>
                <div class="grid place-items-center gap-2 text-center">
                  <h3 class="font-bold text-gray-900 dark:text-white">TypeScript</h3>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Type-safe JavaScript for better development experience</p>
                </div>
              </div>
            </div>
            
            <div class="group">
              <div class="grid place-items-center gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div class="relative w-16 h-16">
                  <div class="absolute inset-0 bg-gradient-to-r from-cyan-500 to-blue-500 rounded-xl rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                  <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full grid place-items-center border border-cyan-100 dark:border-cyan-800">
                    <IconBrandTailwind class="w-8 h-8 text-cyan-600 dark:text-cyan-400" />
                  </div>
                </div>
                <div class="grid place-items-center gap-2 text-center">
                  <h3 class="font-bold text-gray-900 dark:text-white">Tailwind CSS</h3>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Utility-first CSS framework for rapid UI development</p>
                </div>
              </div>
            </div>
            
            <div class="group">
              <div class="grid place-items-center gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div class="relative w-16 h-16">
                  <div class="absolute inset-0 bg-gradient-to-r from-purple-500 to-pink-500 rounded-xl rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                  <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full grid place-items-center border border-purple-100 dark:border-purple-800">
                    <IconComponents class="w-8 h-8 text-purple-600 dark:text-purple-400" />
                  </div>
                </div>
                <div class="grid place-items-center gap-2 text-center">
                  <h3 class="font-bold text-gray-900 dark:text-white">Headless UI</h3>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Unstyled, accessible UI components</p>
                </div>
              </div>
            </div>
            
            <div class="group">
              <div class="grid place-items-center gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div class="relative w-16 h-16">
                  <div class="absolute inset-0 bg-gradient-to-r from-orange-500 to-red-500 rounded-xl rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                  <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full grid place-items-center border border-orange-100 dark:border-orange-800">
                    <IconBrandVite class="w-8 h-8 text-orange-600 dark:text-orange-400" />
                  </div>
                </div>
                <div class="grid place-items-center gap-2 text-center">
                  <h3 class="font-bold text-gray-900 dark:text-white">Vite</h3>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Next generation frontend build tool</p>
                </div>
              </div>
            </div>
            
            <div class="group">
              <div class="grid place-items-center gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-1">
                <div class="relative w-16 h-16">
                  <div class="absolute inset-0 bg-gradient-to-r from-gray-500 to-slate-500 rounded-xl rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                  <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full grid place-items-center border border-gray-100 dark:border-gray-700">
                    <IconIcons class="w-8 h-8 text-gray-600 dark:text-gray-400" />
                  </div>
                </div>
                <div class="grid place-items-center gap-2 text-center">
                  <h3 class="font-bold text-gray-900 dark:text-white">Tabler Icons</h3>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Beautiful SVG icons for modern interfaces</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Features -->
        <div class="grid place-items-center gap-12 w-full max-w-4xl">
          <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white">Key Features</h2>
          
          <div class="grid grid-cols-1 md:grid-cols-2 gap-8 w-full">
            <div class="grid gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-8 border border-gray-200/40 dark:border-gray-700/40 shadow-md">
              <div class="grid grid-cols-[auto_1fr] gap-4 items-start">
                <div class="w-8 h-8 bg-gradient-to-r from-green-500 to-emerald-500 rounded-lg grid place-items-center">
                  <IconCheck class="w-5 h-5 text-white" />
                </div>
                <div class="grid gap-1">
                  <h4 class="font-bold text-gray-900 dark:text-white">Responsive Design</h4>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Optimized for all screen sizes and devices</p>
                </div>
              </div>
              
              <div class="grid grid-cols-[auto_1fr] gap-4 items-start">
                <div class="w-8 h-8 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-lg grid place-items-center">
                  <IconCheck class="w-5 h-5 text-white" />
                </div>
                <div class="grid gap-1">
                  <h4 class="font-bold text-gray-900 dark:text-white">Dark Mode Support</h4>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Beautiful interface in both light and dark themes</p>
                </div>
              </div>
              
              <div class="grid grid-cols-[auto_1fr] gap-4 items-start">
                <div class="w-8 h-8 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg grid place-items-center">
                  <IconCheck class="w-5 h-5 text-white" />
                </div>
                <div class="grid gap-1">
                  <h4 class="font-bold text-gray-900 dark:text-white">Fast Performance</h4>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Built with modern tools for optimal speed</p>
                </div>
              </div>
            </div>
            
            <div class="grid gap-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-8 border border-gray-200/40 dark:border-gray-700/40 shadow-md">
              <div class="grid grid-cols-[auto_1fr] gap-4 items-start">
                <div class="w-8 h-8 bg-gradient-to-r from-orange-500 to-red-500 rounded-lg grid place-items-center">
                  <IconCheck class="w-5 h-5 text-white" />
                </div>
                <div class="grid gap-1">
                  <h4 class="font-bold text-gray-900 dark:text-white">Type Safety</h4>
                  <p class="text-sm text-gray-600 dark:text-gray-300">TypeScript ensures reliable code quality</p>
                </div>
              </div>
              
              <div class="grid grid-cols-[auto_1fr] gap-4 items-start">
                <div class="w-8 h-8 bg-gradient-to-r from-cyan-500 to-blue-500 rounded-lg grid place-items-center">
                  <IconCheck class="w-5 h-5 text-white" />
                </div>
                <div class="grid gap-1">
                  <h4 class="font-bold text-gray-900 dark:text-white">Accessible UI</h4>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Built with accessibility best practices</p>
                </div>
              </div>
              
              <div class="grid grid-cols-[auto_1fr] gap-4 items-start">
                <div class="w-8 h-8 bg-gradient-to-r from-indigo-500 to-purple-500 rounded-lg grid place-items-center">
                  <IconCheck class="w-5 h-5 text-white" />
                </div>
                <div class="grid gap-1">
                  <h4 class="font-bold text-gray-900 dark:text-white">Smooth Animations</h4>
                  <p class="text-sm text-gray-600 dark:text-gray-300">Delightful transitions and hover effects</p>
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
/* Animations */
@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(12deg); }
  50% { transform: translateY(-6px) rotate(12deg); }
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
