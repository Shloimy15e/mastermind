<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800 relative overflow-hidden">
    <!-- Subtle Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <!-- Refined Gradient Overlay -->
      <div class="absolute inset-0 opacity-30">
        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-r from-blue-500/10 via-indigo-500/10 to-purple-500/10"></div>
      </div>
      
      <!-- Minimal Floating Elements -->
      <div class="absolute inset-0">
        <div class="absolute top-20 left-20 w-24 h-24 bg-gradient-to-br from-blue-400/20 to-indigo-600/20 rounded-2xl opacity-40 animate-float transform rotate-12"></div>
        <div class="absolute top-40 right-32 w-20 h-20 bg-gradient-to-br from-indigo-400/20 to-purple-600/20 rounded-full opacity-30 animate-float-delay"></div>
        <div class="absolute bottom-32 left-40 w-28 h-28 bg-gradient-to-br from-purple-400/20 to-pink-600/20 rounded-xl opacity-25 animate-float"></div>
      </div>
    </div>

    <div class="relative z-10">
      <!-- Hero Section -->
      <section class="px-4 pt-32 pb-24 sm:px-6 lg:px-8">
        <div class="max-w-6xl mx-auto">
          <div class="text-center space-y-12">
            
            <!-- Professional Badge -->
            <div class="inline-flex items-center px-6 py-3 rounded-full bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl border border-gray-200/50 dark:border-gray-700/50 shadow-lg">
              <div class="w-2 h-2 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-full animate-pulse mr-3"></div>
              <span class="text-sm font-semibold text-gray-700 dark:text-gray-300">Portfolio of Interactive Projects</span>
            </div>
            
            <!-- Main Title -->
            <div class="space-y-8">
              <h1 class="text-5xl sm:text-7xl lg:text-8xl font-black leading-tight">
                <span class="block bg-gradient-to-r from-gray-900 via-blue-800 to-indigo-900 dark:from-white dark:via-blue-200 dark:to-indigo-200 bg-clip-text text-transparent">
                  Project
                </span>
                <span class="block bg-gradient-to-r from-indigo-800 via-purple-800 to-blue-900 dark:from-indigo-200 dark:via-purple-200 dark:to-blue-200 bg-clip-text text-transparent mt-2">
                  Showcase
                </span>
              </h1>
              
              <div class="max-w-4xl mx-auto space-y-8">
                <p class="text-xl sm:text-2xl text-gray-600 dark:text-gray-300 leading-relaxed font-light">
                  A curated collection of 
                  <span class="font-semibold text-blue-600 dark:text-blue-400">interactive tools</span> and 
                  <span class="font-semibold text-indigo-600 dark:text-indigo-400">problem-solving applications</span> 
                  built with modern web technologies.
                </p>
                
                <!-- Professional CTA Buttons -->
                <div class="flex flex-col sm:flex-row gap-4 justify-center items-center pt-8">
                  <router-link 
                    to="/mastermind"
                    class="group inline-flex items-center px-8 py-4 bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-semibold rounded-xl shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105"
                  >
                    <IconPuzzle class="w-5 h-5 mr-3 group-hover:rotate-12 transition-transform duration-300" />
                    <span>Explore Logic Puzzle</span>
                    <IconArrowRight class="w-5 h-5 ml-3 group-hover:translate-x-1 transition-transform duration-300" />
                  </router-link>
                  
                  <router-link 
                    to="/parser"
                    class="group inline-flex items-center px-8 py-4 bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-700 hover:to-purple-700 text-white font-semibold rounded-xl shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105"
                  >
                    <IconCalculator class="w-5 h-5 mr-3 group-hover:rotate-12 transition-transform duration-300" />
                    <span>Try Math Parser</span>
                    <IconArrowRight class="w-5 h-5 ml-3 group-hover:translate-x-1 transition-transform duration-300" />
                  </router-link>
                </div>
              </div>
            </div>

            <!-- Professional Stats -->
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-8 pt-16 max-w-4xl mx-auto">
              <div class="text-center p-6 bg-white/60 dark:bg-gray-800/60 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-1">
                <div class="text-3xl sm:text-4xl font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent mb-2">2</div>
                <div class="text-gray-700 dark:text-gray-300 font-semibold text-sm mb-1">Active Projects</div>
                <div class="text-gray-500 dark:text-gray-400 text-xs">Interactive applications</div>
              </div>
              
              <div class="text-center p-6 bg-white/60 dark:bg-gray-800/60 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-1">
                <div class="text-3xl sm:text-4xl font-bold bg-gradient-to-r from-indigo-600 to-purple-600 bg-clip-text text-transparent mb-2">100%</div>
                <div class="text-gray-700 dark:text-gray-300 font-semibold text-sm mb-1">Open Source</div>
                <div class="text-gray-500 dark:text-gray-400 text-xs">MIT Licensed</div>
              </div>
              
              <div class="text-center p-6 bg-white/60 dark:bg-gray-800/60 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 shadow-lg hover:shadow-xl transition-all duration-300 transform hover:-translate-y-1">
                <div class="text-3xl sm:text-4xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent mb-2">Vue 3</div>
                <div class="text-gray-700 dark:text-gray-300 font-semibold text-sm mb-1">Technology</div>
                <div class="text-gray-500 dark:text-gray-400 text-xs">Modern framework</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Projects Section -->
      <section class="px-4 py-24 sm:px-6 lg:px-8">
        <div class="max-w-6xl mx-auto">
          
          <div class="text-center mb-16">
            <h2 class="text-4xl sm:text-5xl font-bold text-gray-900 dark:text-white mb-6">
              Featured Projects
            </h2>
            <p class="text-lg text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">
              Each project demonstrates different aspects of modern web development and user interaction design
            </p>
          </div>

          <div class="grid lg:grid-cols-2 gap-12 items-center">
            
            <!-- Mastermind Project -->
            <div class="group">
              <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 overflow-hidden shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
                
                <!-- Project Header -->
                <div class="relative h-64 bg-gradient-to-br from-blue-500 via-indigo-600 to-purple-600 overflow-hidden">
                  <!-- Professional Pattern -->
                  <div class="absolute inset-0 opacity-20">
                    <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 24px 24px;"></div>
                  </div>
                  
                  <!-- Project Visualization -->
                  <div class="absolute inset-0 flex items-center justify-center">
                    <div class="relative">
                      <div class="flex items-center space-x-3">
                        <div class="w-12 h-12 rounded-full bg-red-400 shadow-lg animate-float"></div>
                        <div class="w-12 h-12 rounded-full bg-blue-400 shadow-lg animate-float" style="animation-delay: 0.3s;"></div>
                        <div class="w-12 h-12 rounded-full bg-green-400 shadow-lg animate-float" style="animation-delay: 0.6s;"></div>
                        <div class="w-12 h-12 rounded-full bg-yellow-400 shadow-lg animate-float" style="animation-delay: 0.9s;"></div>
                      </div>
                    </div>
                  </div>

                  <!-- Project Type Badge -->
                  <div class="absolute top-6 right-6">
                    <div class="px-3 py-1 bg-white/20 backdrop-blur-lg rounded-full border border-white/30">
                      <span class="text-white text-sm font-semibold">Logic Game</span>
                    </div>
                  </div>

                  <!-- Difficulty Indicator -->
                  <div class="absolute bottom-6 left-6">
                    <div class="flex items-center space-x-2 px-3 py-1 bg-white/20 backdrop-blur-lg rounded-full border border-white/30">
                      <div class="w-2 h-2 bg-yellow-400 rounded-full"></div>
                      <span class="text-white text-sm font-semibold">Intermediate</span>
                    </div>
                  </div>
                </div>

                <!-- Project Content -->
                <div class="p-8 space-y-6">
                  <div class="space-y-4">
                    <h3 class="text-2xl font-bold text-gray-900 dark:text-white">
                      Mastermind Logic Game
                    </h3>
                    <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                      A digital implementation of the classic Mastermind puzzle. Test your deductive reasoning skills by solving color-based logic problems with intelligent feedback systems.
                    </p>
                  </div>

                  <!-- Tech Stack -->
                  <div class="flex flex-wrap gap-2">
                    <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900/30 text-blue-700 dark:text-blue-300 rounded-full text-sm font-medium">Vue 3</span>
                    <span class="px-3 py-1 bg-indigo-100 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 rounded-full text-sm font-medium">TypeScript</span>
                    <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 rounded-full text-sm font-medium">Logic Design</span>
                  </div>

                  <!-- Project Stats -->
                  <div class="grid grid-cols-2 gap-4 pt-4 border-t border-gray-200 dark:border-gray-700">
                    <div class="text-center">
                      <div class="text-2xl font-bold text-gray-900 dark:text-white mb-1">10</div>
                      <span class="text-sm text-gray-500 dark:text-gray-400">Max Attempts</span>
                    </div>
                    <div class="text-center">
                      <div class="text-2xl font-bold text-gray-900 dark:text-white mb-1">6</div>
                      <span class="text-sm text-gray-500 dark:text-gray-400">Color Options</span>
                    </div>
                  </div>

                  <!-- Action Button -->
                  <router-link 
                    to="/mastermind"
                    class="w-full inline-flex items-center justify-center px-6 py-3 bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-semibold rounded-xl transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl"
                  >
                    <span class="mr-2">View Project</span>
                    <IconArrowRight class="w-4 h-4 group-hover:translate-x-1 transition-transform" />
                  </router-link>
                </div>
              </div>
            </div>

            <!-- Math Parser Project -->
            <div class="group">
              <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 overflow-hidden shadow-xl hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
                
                <!-- Project Header -->
                <div class="relative h-64 bg-gradient-to-br from-indigo-500 via-purple-600 to-pink-600 overflow-hidden">
                  <!-- Professional Pattern -->
                  <div class="absolute inset-0 opacity-20">
                    <div class="absolute inset-0" style="background-image: linear-gradient(45deg, transparent 35%, white 35%, white 65%, transparent 65%), linear-gradient(-45deg, transparent 35%, white 35%, white 65%, transparent 65%); background-size: 20px 20px;"></div>
                  </div>
                  
                  <!-- Mathematical Visualization -->
                  <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center space-y-3">
                      <div class="text-2xl font-bold text-white animate-pulse">
                        (2 + 3) × 4 = 20
                      </div>
                      <div class="text-lg text-white/80">
                        √(16) + 3² = 13
                      </div>
                      <div class="text-sm text-white/60">
                        Complex expressions supported
                      </div>
                    </div>
                  </div>

                  <!-- Project Type Badge -->
                  <div class="absolute top-6 right-6">
                    <div class="px-3 py-1 bg-white/20 backdrop-blur-lg rounded-full border border-white/30">
                      <span class="text-white text-sm font-semibold">Calculator</span>
                    </div>
                  </div>

                  <!-- Performance Badge -->
                  <div class="absolute bottom-6 left-6">
                    <div class="flex items-center space-x-2 px-3 py-1 bg-white/20 backdrop-blur-lg rounded-full border border-white/30">
                      <div class="w-2 h-2 bg-green-400 rounded-full animate-pulse"></div>
                      <span class="text-white text-sm font-semibold">Real-time</span>
                    </div>
                  </div>
                </div>

                <!-- Project Content -->
                <div class="p-8 space-y-6">
                  <div class="space-y-4">
                    <h3 class="text-2xl font-bold text-gray-900 dark:text-white">
                      Mathematical Expression Parser
                    </h3>
                    <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                      An advanced calculator that parses and evaluates complex mathematical expressions. Features operator precedence, parentheses support, and comprehensive error handling.
                    </p>
                  </div>

                  <!-- Tech Stack -->
                  <div class="flex flex-wrap gap-2">
                    <span class="px-3 py-1 bg-indigo-100 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 rounded-full text-sm font-medium">Parsing Algorithms</span>
                    <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 rounded-full text-sm font-medium">Real-time</span>
                    <span class="px-3 py-1 bg-pink-100 dark:bg-pink-900/30 text-pink-700 dark:text-pink-300 rounded-full text-sm font-medium">Error Handling</span>
                  </div>

                  <!-- Project Stats -->
                  <div class="grid grid-cols-2 gap-4 pt-4 border-t border-gray-200 dark:border-gray-700">
                    <div class="text-center">
                      <div class="text-2xl font-bold text-gray-900 dark:text-white mb-1">∞</div>
                      <span class="text-sm text-gray-500 dark:text-gray-400">Operations</span>
                    </div>
                    <div class="text-center">
                      <div class="text-2xl font-bold text-gray-900 dark:text-white mb-1">100%</div>
                      <span class="text-sm text-gray-500 dark:text-gray-400">Accuracy</span>
                    </div>
                  </div>

                  <!-- Action Button -->
                  <router-link 
                    to="/parser"
                    class="w-full inline-flex items-center justify-center px-6 py-3 bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-700 hover:to-purple-700 text-white font-semibold rounded-xl transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl"
                  >
                    <span class="mr-2">View Project</span>
                    <IconArrowRight class="w-4 h-4 group-hover:translate-x-1 transition-transform" />
                  </router-link>
                </div>
              </div>
            </div>

          </div>
        </div>
      </section>

      <!-- Technologies Section -->
      <section class="px-4 py-24 sm:px-6 lg:px-8 bg-white/50 dark:bg-gray-900/50 backdrop-blur-xl">
        <div class="max-w-6xl mx-auto">
          <div class="text-center mb-16">
            <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white mb-4">
              Built With Modern Technologies
            </h2>
            <p class="text-lg text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">
              These projects showcase best practices in modern web development
            </p>
          </div>

          <div class="grid md:grid-cols-3 gap-8">
            <div class="text-center group">
              <div class="relative mx-auto w-16 h-16 mb-6">
                <div class="absolute inset-0 bg-gradient-to-r from-emerald-500 to-blue-500 rounded-xl rotate-3 group-hover:rotate-6 transition-transform duration-300"></div>
                <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full flex items-center justify-center border-2 border-emerald-100 dark:border-emerald-800">
                  <IconCode class="w-6 h-6 text-emerald-600 dark:text-emerald-400" />
                </div>
              </div>
              <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-3">Vue 3 Composition API</h3>
              <p class="text-gray-600 dark:text-gray-300">Modern reactive framework with TypeScript support for scalable applications.</p>
            </div>

            <div class="text-center group">
              <div class="relative mx-auto w-16 h-16 mb-6">
                <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-xl rotate-3 group-hover:rotate-6 transition-transform duration-300"></div>
                <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full flex items-center justify-center border-2 border-blue-100 dark:border-blue-800">
                  <IconPalette class="w-6 h-6 text-blue-600 dark:text-blue-400" />
                </div>
              </div>
              <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-3">Tailwind CSS</h3>
              <p class="text-gray-600 dark:text-gray-300">Utility-first CSS framework for rapid and consistent UI development.</p>
            </div>

            <div class="text-center group">
              <div class="relative mx-auto w-16 h-16 mb-6">
                <div class="absolute inset-0 bg-gradient-to-r from-indigo-500 to-purple-500 rounded-xl rotate-3 group-hover:rotate-6 transition-transform duration-300"></div>
                <div class="relative bg-white dark:bg-gray-800 rounded-xl w-full h-full flex items-center justify-center border-2 border-indigo-100 dark:border-indigo-800">
                  <IconRocket class="w-6 h-6 text-indigo-600 dark:text-indigo-400" />
                </div>
              </div>
              <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-3">Optimized Performance</h3>
              <p class="text-gray-600 dark:text-gray-300">Fast loading times and smooth interactions with modern build tools.</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Professional Footer -->
      <footer class="px-4 py-16 sm:px-6 lg:px-8 border-t border-gray-200/50 dark:border-gray-700/50">
        <div class="max-w-6xl mx-auto text-center">
          <div class="flex items-center justify-center space-x-3 mb-6">
            <div class="w-10 h-10 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-xl flex items-center justify-center">
              <span class="text-white font-bold text-lg">PS</span>
            </div>
            <span class="text-xl font-bold text-gray-900 dark:text-white">Project Showcase</span>
          </div>
          <p class="text-gray-500 dark:text-gray-400">
            Built with Vue 3, TypeScript, and Tailwind CSS
          </p>
        </div>
      </footer>
    </div>
  </div>
</template>

<script setup lang="ts">
import { 
  IconPuzzle, 
  IconCalculator, 
  IconArrowRight,
  IconCode,
  IconPalette,
  IconRocket
} from '@tabler/icons-vue'
</script>

<style scoped>
/* Professional Animations */
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-8px); }
}

@keyframes float-delay {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-12px); }
}

.animate-float {
  animation: float 4s ease-in-out infinite;
}

.animate-float-delay {
  animation: float-delay 5s ease-in-out infinite;
}

/* Smooth Transitions */
* {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}

/* Backdrop Blur Support */
@supports not (backdrop-filter: blur(12px)) {
  .backdrop-blur-xl {
    background-color: rgba(255, 255, 255, 0.9);
  }
  
  .dark .backdrop-blur-xl {
    background-color: rgba(17, 24, 39, 0.9);
  }
}
</style>