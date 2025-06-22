<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800 relative overflow-hidden">
    <!-- Subtle Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute inset-0 opacity-20">
        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-r from-blue-500/8 via-indigo-500/8 to-purple-500/8"></div>
      </div>
      
      <!-- Minimal Floating Elements with Golden Ratio Positioning -->
      <div class="absolute inset-0">
        <div class="absolute top-[12%] left-[8%] w-20 h-20 bg-gradient-to-br from-blue-400/15 to-indigo-600/15 rounded-2xl opacity-40 animate-float transform rotate-12"></div>
        <div class="absolute top-[25%] right-[15%] w-16 h-16 bg-gradient-to-br from-indigo-400/15 to-purple-600/15 rounded-full opacity-30 animate-float-delay"></div>
        <div class="absolute bottom-[20%] left-[18%] w-24 h-24 bg-gradient-to-br from-purple-400/15 to-pink-600/15 rounded-xl opacity-25 animate-float"></div>
      </div>
    </div>

    <div class="relative z-10">
      <!-- Hero Section with Golden Ratio Proportions -->
      <section class="px-6 pt-20 pb-32 sm:px-8 lg:px-12">
        <div class="max-w-4xl mx-auto">
          <div class="text-center">
            
            <!-- Professional Badge with Optical Centering -->
            <div class="mb-16">
              <div class="inline-flex items-center px-5 py-2.5 rounded-full bg-white/90 dark:bg-gray-800/90 backdrop-blur-xl border border-gray-200/60 dark:border-gray-700/60 shadow-lg">
                <div class="w-1.5 h-1.5 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-full animate-pulse mr-2.5"></div>
                <span class="text-xs font-medium text-gray-700 dark:text-gray-300 tracking-wide">PORTFOLIO OF INTERACTIVE PROJECTS</span>
              </div>
            </div>
            
            <!-- Main Title with Perfect Typography Hierarchy -->
            <div class="mb-20">
              <h1 class="mb-8">
                <span class="block text-6xl sm:text-7xl lg:text-8xl xl:text-9xl font-black leading-[0.85] tracking-tighter mb-3 bg-gradient-to-r from-gray-900 via-blue-800 to-indigo-900 dark:from-white dark:via-blue-200 dark:to-indigo-200 bg-clip-text text-transparent">
                  Project
                </span>
                <span class="block text-6xl sm:text-7xl lg:text-8xl xl:text-9xl font-black leading-[0.85] tracking-tighter bg-gradient-to-r from-indigo-800 via-purple-800 to-blue-900 dark:from-indigo-200 dark:via-purple-200 dark:to-blue-200 bg-clip-text text-transparent">
                  Showcase
                </span>
              </h1>
              
              <!-- Perfect Typography with Golden Ratio Spacing -->
              <div class="max-w-2xl mx-auto mb-12">
                <p class="text-xl sm:text-2xl leading-[1.6] font-light text-gray-600 dark:text-gray-300">
                  A curated collection of 
                  <span class="font-semibold text-blue-600 dark:text-blue-400">interactive tools</span> and 
                  <span class="font-semibold text-indigo-600 dark:text-indigo-400">problem-solving applications</span> 
                  built with modern web technologies.
                </p>
              </div>
                
              <!-- CTA Buttons with Perfect Visual Weight -->
              <div class="flex flex-col sm:flex-row gap-5 justify-center items-center mb-16">
                <router-link 
                  to="/mastermind"
                  class="group inline-flex items-center px-7 py-3.5 bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-semibold rounded-lg shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-[1.02]"
                >
                  <IconPuzzle class="w-4 h-4 mr-2.5 group-hover:rotate-12 transition-transform duration-300" />
                  <span class="text-sm">Explore Logic Puzzle</span>
                  <IconArrowRight class="w-4 h-4 ml-2.5 group-hover:translate-x-0.5 transition-transform duration-300" />
                </router-link>
                
                <router-link 
                  to="/parser"
                  class="group inline-flex items-center px-7 py-3.5 bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-700 hover:to-purple-700 text-white font-semibold rounded-lg shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-[1.02]"
                >
                  <IconCalculator class="w-4 h-4 mr-2.5 group-hover:rotate-12 transition-transform duration-300" />
                  <span class="text-sm">Try Math Parser</span>
                  <IconArrowRight class="w-4 h-4 ml-2.5 group-hover:translate-x-0.5 transition-transform duration-300" />
                </router-link>
              </div>
            </div>

            <!-- Stats with Golden Ratio Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-6 max-w-3xl mx-auto">
              <div class="text-center p-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-0.5">
                <div class="text-3xl font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent mb-2">2</div>
                <div class="text-gray-700 dark:text-gray-300 font-medium text-xs mb-1">Active Projects</div>
                <div class="text-gray-500 dark:text-gray-400 text-xs">Interactive applications</div>
              </div>
              
              <div class="text-center p-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-0.5">
                <div class="text-3xl font-bold bg-gradient-to-r from-indigo-600 to-purple-600 bg-clip-text text-transparent mb-2">100%</div>
                <div class="text-gray-700 dark:text-gray-300 font-medium text-xs mb-1">Open Source</div>
                <div class="text-gray-500 dark:text-gray-400 text-xs">MIT Licensed</div>
              </div>
              
              <div class="text-center p-6 bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl border border-gray-200/40 dark:border-gray-700/40 shadow-md hover:shadow-lg transition-all duration-300 transform hover:-translate-y-0.5">
                <div class="text-3xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent mb-2">Vue 3</div>
                <div class="text-gray-700 dark:text-gray-300 font-medium text-xs mb-1">Technology</div>
                <div class="text-gray-500 dark:text-gray-400 text-xs">Modern framework</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Projects Section with Perfect Visual Hierarchy -->
      <section class="px-6 py-24 sm:px-8 lg:px-12">
        <div class="max-w-5xl mx-auto">
          
          <!-- Section Header with Proper Proportions -->
          <div class="text-center mb-16">
            <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-gray-900 dark:text-white mb-4 tracking-tight">
              Featured Projects
            </h2>
            <p class="text-lg text-gray-600 dark:text-gray-300 max-w-xl mx-auto leading-relaxed">
              Each project demonstrates different aspects of modern web development and user interaction design
            </p>
          </div>

          <!-- Perfect Grid with Golden Ratio Spacing -->
          <div class="grid lg:grid-cols-2 gap-10 items-start">
            
            <!-- Mastermind Project -->
            <div class="group">
              <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 overflow-hidden shadow-lg hover:shadow-xl transition-all duration-500 transform hover:-translate-y-1">
                
                <!-- Project Header -->
                <div class="relative h-48 bg-gradient-to-br from-blue-500 via-indigo-600 to-purple-600 overflow-hidden">
                  <div class="absolute inset-0 opacity-20">
                    <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 20px 20px;"></div>
                  </div>
                  
                  <!-- Perfect Visual Centering -->
                  <div class="absolute inset-0 flex items-center justify-center">
                    <div class="flex items-center space-x-3">
                      <div class="w-10 h-10 rounded-full bg-red-400 shadow-md animate-float"></div>
                      <div class="w-10 h-10 rounded-full bg-blue-400 shadow-md animate-float" style="animation-delay: 0.3s;"></div>
                      <div class="w-10 h-10 rounded-full bg-green-400 shadow-md animate-float" style="animation-delay: 0.6s;"></div>
                      <div class="w-10 h-10 rounded-full bg-yellow-400 shadow-md animate-float" style="animation-delay: 0.9s;"></div>
                    </div>
                  </div>

                  <!-- Badges with Perfect Positioning -->
                  <div class="absolute top-4 right-4">
                    <div class="px-3 py-1.5 bg-white/25 backdrop-blur-md rounded-full border border-white/30">
                      <span class="text-white text-xs font-medium">Logic Game</span>
                    </div>
                  </div>

                  <div class="absolute bottom-4 left-4">
                    <div class="flex items-center space-x-1.5 px-3 py-1.5 bg-white/25 backdrop-blur-md rounded-full border border-white/30">
                      <div class="w-1.5 h-1.5 bg-yellow-400 rounded-full"></div>
                      <span class="text-white text-xs font-medium">Intermediate</span>
                    </div>
                  </div>
                </div>

                <!-- Project Content with Perfect Spacing -->
                <div class="p-6 space-y-5">
                  <div class="space-y-3">
                    <h3 class="text-xl font-bold text-gray-900 dark:text-white leading-tight">
                      Mastermind Logic Game
                    </h3>
                    <p class="text-gray-600 dark:text-gray-300 leading-relaxed text-sm">
                      A digital implementation of the classic Mastermind puzzle. Test your deductive reasoning skills by solving color-based logic problems with intelligent feedback systems.
                    </p>
                  </div>

                  <!-- Tech Stack -->
                  <div class="flex flex-wrap gap-2">
                    <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900/30 text-blue-700 dark:text-blue-300 rounded-full text-xs font-medium">Vue 3</span>
                    <span class="px-3 py-1 bg-indigo-100 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 rounded-full text-xs font-medium">TypeScript</span>
                    <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 rounded-full text-xs font-medium">Logic Design</span>
                  </div>

                  <!-- Project Stats -->
                  <div class="grid grid-cols-2 gap-4 pt-4 border-t border-gray-200 dark:border-gray-700">
                    <div class="text-center">
                      <div class="text-2xl font-bold text-gray-900 dark:text-white mb-1">10</div>
                      <span class="text-xs text-gray-500 dark:text-gray-400 font-medium">Max Attempts</span>
                    </div>
                    <div class="text-center">
                      <div class="text-2xl font-bold text-gray-900 dark:text-white mb-1">6</div>
                      <span class="text-xs text-gray-500 dark:text-gray-400 font-medium">Color Options</span>
                    </div>
                  </div>

                  <!-- Action Button -->
                  <router-link 
                    to="/mastermind"
                    class="w-full inline-flex items-center justify-center px-6 py-3 bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-medium rounded-lg transition-all duration-300 transform hover:scale-[1.02] shadow-md hover:shadow-lg text-sm"
                  >
                    <span class="mr-2">View Project</span>
                    <IconArrowRight class="w-4 h-4 group-hover:translate-x-0.5 transition-transform" />
                  </router-link>
                </div>
              </div>
            </div>

            <!-- Math Parser Project -->
            <div class="group">
              <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 overflow-hidden shadow-lg hover:shadow-xl transition-all duration-500 transform hover:-translate-y-1">
                
                <!-- Project Header -->
                <div class="relative h-48 bg-gradient-to-br from-indigo-500 via-purple-600 to-pink-600 overflow-hidden">
                  <div class="absolute inset-0 opacity-20">
                    <div class="absolute inset-0" style="background-image: linear-gradient(45deg, transparent 35%, white 35%, white 65%, transparent 65%), linear-gradient(-45deg, transparent 35%, white 35%, white 65%, transparent 65%); background-size: 16px 16px;"></div>
                  </div>
                  
                  <!-- Mathematical Visualization -->
                  <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center space-y-2">
                      <div class="text-xl font-bold text-white animate-pulse">
                        (2 + 3) × 4 = 20
                      </div>
                      <div class="text-base text-white/80">
                        √(16) + 3² = 13
                      </div>
                      <div class="text-xs text-white/60">
                        Complex expressions supported
                      </div>
                    </div>
                  </div>

                  <!-- Badges -->
                  <div class="absolute top-4 right-4">
                    <div class="px-3 py-1.5 bg-white/25 backdrop-blur-md rounded-full border border-white/30">
                      <span class="text-white text-xs font-medium">Calculator</span>
                    </div>
                  </div>

                  <div class="absolute bottom-4 left-4">
                    <div class="flex items-center space-x-1.5 px-3 py-1.5 bg-white/25 backdrop-blur-md rounded-full border border-white/30">
                      <div class="w-1.5 h-1.5 bg-green-400 rounded-full animate-pulse"></div>
                      <span class="text-white text-xs font-medium">Real-time</span>
                    </div>
                  </div>
                </div>

                <!-- Project Content -->
                <div class="p-6 space-y-5">
                  <div class="space-y-3">
                    <h3 class="text-xl font-bold text-gray-900 dark:text-white leading-tight">
                      Mathematical Expression Parser
                    </h3>
                    <p class="text-gray-600 dark:text-gray-300 leading-relaxed text-sm">
                      An advanced calculator that parses and evaluates complex mathematical expressions. Features operator precedence, parentheses support, and comprehensive error handling.
                    </p>
                  </div>

                  <!-- Tech Stack -->
                  <div class="flex flex-wrap gap-2">
                    <span class="px-3 py-1 bg-indigo-100 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 rounded-full text-xs font-medium">Parsing Algorithms</span>
                    <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 rounded-full text-xs font-medium">Real-time</span>
                    <span class="px-3 py-1 bg-pink-100 dark:bg-pink-900/30 text-pink-700 dark:text-pink-300 rounded-full text-xs font-medium">Error Handling</span>
                  </div>

                  <!-- Project Stats -->
                  <div class="grid grid-cols-2 gap-4 pt-4 border-t border-gray-200 dark:border-gray-700">
                    <div class="text-center">
                      <div class="text-2xl font-bold text-gray-900 dark:text-white mb-1">∞</div>
                      <span class="text-xs text-gray-500 dark:text-gray-400 font-medium">Operations</span>
                    </div>
                    <div class="text-center">
                      <div class="text-2xl font-bold text-gray-900 dark:text-white mb-1">100%</div>
                      <span class="text-xs text-gray-500 dark:text-gray-400 font-medium">Accuracy</span>
                    </div>
                  </div>

                  <!-- Action Button -->
                  <router-link 
                    to="/parser"
                    class="w-full inline-flex items-center justify-center px-6 py-3 bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-700 hover:to-purple-700 text-white font-medium rounded-lg transition-all duration-300 transform hover:scale-[1.02] shadow-md hover:shadow-lg text-sm"
                  >
                    <span class="mr-2">View Project</span>
                    <IconArrowRight class="w-4 h-4 group-hover:translate-x-0.5 transition-transform" />
                  </router-link>
                </div>
              </div>
            </div>

          </div>
        </div>
      </section>

      <!-- Technologies Section -->
      <section class="px-6 py-20 sm:px-8 lg:px-12 bg-white/40 dark:bg-gray-900/40 backdrop-blur-xl">
        <div class="max-w-4xl mx-auto">
          <div class="text-center mb-12">
            <h2 class="text-2xl sm:text-3xl font-bold text-gray-900 dark:text-white mb-3">
              Built With Modern Technologies
            </h2>
            <p class="text-base text-gray-600 dark:text-gray-300 max-w-lg mx-auto leading-relaxed">
              These projects showcase best practices in modern web development
            </p>
          </div>

          <!-- Perfect Three-Column Grid -->
          <div class="grid md:grid-cols-3 gap-8">
            <div class="text-center group">
              <div class="relative mx-auto w-16 h-16 mb-5">
                <div class="absolute inset-0 bg-gradient-to-r from-emerald-500 to-blue-500 rounded-lg rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                <div class="relative bg-white dark:bg-gray-800 rounded-lg w-full h-full flex items-center justify-center border border-emerald-100 dark:border-emerald-800">
                  <IconCode class="w-6 h-6 text-emerald-600 dark:text-emerald-400" />
                </div>
              </div>
              <h3 class="text-lg font-bold text-gray-900 dark:text-white mb-2">Vue 3 Composition API</h3>
              <p class="text-sm text-gray-600 dark:text-gray-300 leading-relaxed">Modern reactive framework with TypeScript support for scalable applications.</p>
            </div>

            <div class="text-center group">
              <div class="relative mx-auto w-16 h-16 mb-5">
                <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-lg rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                <div class="relative bg-white dark:bg-gray-800 rounded-lg w-full h-full flex items-center justify-center border border-blue-100 dark:border-blue-800">
                  <IconPalette class="w-6 h-6 text-blue-600 dark:text-blue-400" />
                </div>
              </div>
              <h3 class="text-lg font-bold text-gray-900 dark:text-white mb-2">Tailwind CSS</h3>
              <p class="text-sm text-gray-600 dark:text-gray-300 leading-relaxed">Utility-first CSS framework for rapid and consistent UI development.</p>
            </div>

            <div class="text-center group">
              <div class="relative mx-auto w-16 h-16 mb-5">
                <div class="absolute inset-0 bg-gradient-to-r from-indigo-500 to-purple-500 rounded-lg rotate-2 group-hover:rotate-6 transition-transform duration-300"></div>
                <div class="relative bg-white dark:bg-gray-800 rounded-lg w-full h-full flex items-center justify-center border border-indigo-100 dark:border-indigo-800">
                  <IconRocket class="w-6 h-6 text-indigo-600 dark:text-indigo-400" />
                </div>
              </div>
              <h3 class="text-lg font-bold text-gray-900 dark:text-white mb-2">Optimized Performance</h3>
              <p class="text-sm text-gray-600 dark:text-gray-300 leading-relaxed">Fast loading times and smooth interactions with modern build tools.</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Footer -->
      <footer class="px-6 py-16 sm:px-8 lg:px-12 border-t border-gray-200/50 dark:border-gray-700/50">
        <div class="max-w-4xl mx-auto text-center">
          <div class="flex items-center justify-center space-x-3 mb-4">
            <div class="w-10 h-10 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-lg flex items-center justify-center">
              <span class="text-white font-bold text-base">PS</span>
            </div>
            <span class="text-xl font-bold text-gray-900 dark:text-white">Project Showcase</span>
          </div>
          <p class="text-gray-500 dark:text-gray-400 text-base">
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
/* Professional Animations with Perfect Timing */
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

/* Perfect Smooth Transitions with Optimal Timing Function */
* {
  transition-timing-function: cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

/* Backdrop Blur Fallback */
@supports not (backdrop-filter: blur(12px)) {
  .backdrop-blur-xl {
    background-color: rgba(255, 255, 255, 0.85);
  }
  
  .dark .backdrop-blur-xl {
    background-color: rgba(17, 24, 39, 0.85);
  }

  .backdrop-blur-md {
    background-color: rgba(255, 255, 255, 0.75);
  }
  
  .dark .backdrop-blur-md {
    background-color: rgba(17, 24, 39, 0.75);
  }
}

/* Perfect Typography System */
h1, h2, h3, h4, h5, h6 {
  letter-spacing: -0.02em;
  font-feature-settings: 'liga' 1, 'kern' 1;
}

/* Optimal Line Heights for Readability */
p {
  line-height: 1.6;
  font-feature-settings: 'liga' 1, 'kern' 1;
}

/* Subtle Text Rendering Optimization */
.text-xs, .text-sm, .text-base, .text-lg, .text-xl, .text-2xl, .text-3xl, .text-4xl, .text-5xl, .text-6xl, .text-7xl, .text-8xl, .text-9xl {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>