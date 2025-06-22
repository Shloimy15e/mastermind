<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-blue-50 to-indigo-100 dark:from-gray-950 dark:via-slate-900 dark:to-gray-900 relative overflow-hidden">
    <!-- Animated Background Elements -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div class="absolute -top-40 -right-40 w-80 h-80 bg-gradient-to-br from-purple-400/20 to-pink-400/20 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute -bottom-40 -left-40 w-80 h-80 bg-gradient-to-br from-blue-400/20 to-cyan-400/20 rounded-full blur-3xl animate-pulse delay-1000"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-96 h-96 bg-gradient-to-br from-green-400/10 to-emerald-400/10 rounded-full blur-3xl animate-pulse delay-500"></div>
    </div>

    <div class="relative z-10">
      <!-- Hero Section -->
      <section class="px-4 pt-20 pb-16 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
          <div class="text-center space-y-8">
            <!-- Main Heading -->
            <div class="space-y-6">
              <div class="inline-flex items-center px-4 py-2 rounded-full bg-gradient-to-r from-purple-100 to-pink-100 dark:from-purple-900/30 dark:to-pink-900/30 border border-purple-200/50 dark:border-purple-700/50">
                <span class="text-sm font-medium text-purple-700 dark:text-purple-300">🎯 Welcome to the ultimate</span>
              </div>
              
              <h1 class="text-4xl sm:text-6xl lg:text-7xl font-black bg-gradient-to-r from-gray-900 via-purple-800 to-indigo-900 dark:from-white dark:via-purple-300 dark:to-blue-300 bg-clip-text text-transparent leading-tight">
                Gaming Hub
              </h1>
              
              <p class="text-lg sm:text-xl lg:text-2xl text-gray-600 dark:text-gray-300 max-w-4xl mx-auto leading-relaxed font-light">
                Immerse yourself in our curated collection of 
                <span class="font-semibold text-purple-600 dark:text-purple-400">mind-bending puzzles</span> and 
                <span class="font-semibold text-blue-600 dark:text-blue-400">powerful tools</span> 
                crafted for the modern digital experience.
              </p>
            </div>

            <!-- Quick Stats -->
            <div class="flex justify-center items-center space-x-8 pt-8">
              <div class="text-center">
                <div class="text-2xl sm:text-3xl font-bold text-purple-600 dark:text-purple-400">2</div>
                <div class="text-sm text-gray-500 dark:text-gray-400 font-medium">Applications</div>
              </div>
              <div class="w-px h-12 bg-gray-300 dark:bg-gray-600"></div>
              <div class="text-center">
                <div class="text-2xl sm:text-3xl font-bold text-blue-600 dark:text-blue-400">∞</div>
                <div class="text-sm text-gray-500 dark:text-gray-400 font-medium">Possibilities</div>
              </div>
              <div class="w-px h-12 bg-gray-300 dark:bg-gray-600"></div>
              <div class="text-center">
                <div class="text-2xl sm:text-3xl font-bold text-green-600 dark:text-green-400">100%</div>
                <div class="text-sm text-gray-500 dark:text-gray-400 font-medium">Free</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Applications Section -->
      <section class="px-4 py-24 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
          <div class="text-center mb-16">
            <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-gray-900 dark:text-white mb-6">
              Choose Your Adventure
            </h2>
            <p class="text-lg text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">
              Each application is meticulously designed to provide a unique and engaging experience
            </p>
          </div>

          <div class="grid lg:grid-cols-2 gap-8 lg:gap-12">
            
            <!-- Mastermind Game Card -->
            <div class="group relative">
              <div class="absolute inset-0 bg-gradient-to-r from-purple-600 to-pink-600 rounded-3xl blur opacity-25 group-hover:opacity-40 transition-opacity duration-500"></div>
              <div class="relative bg-white/80 dark:bg-gray-900/80 backdrop-blur-xl rounded-3xl border border-white/20 dark:border-gray-700/50 overflow-hidden hover:shadow-2xl hover:shadow-purple-500/25 transition-all duration-500 group-hover:-translate-y-2">
                
                <!-- Card Header -->
                <div class="relative h-64 bg-gradient-to-br from-purple-500 via-purple-600 to-pink-600 overflow-hidden">
                  <!-- Background Pattern -->
                  <div class="absolute inset-0 opacity-20">
                    <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 20px 20px;"></div>
                  </div>
                  
                  <!-- Floating Elements -->
                  <div class="absolute inset-0 flex items-center justify-center">
                    <div class="relative">
                      <div class="flex items-center space-x-3">
                        <div class="w-12 h-12 rounded-full bg-red-500 shadow-2xl animate-bounce" style="animation-delay: 0s;"></div>
                        <div class="w-12 h-12 rounded-full bg-blue-500 shadow-2xl animate-bounce" style="animation-delay: 0.2s;"></div>
                        <div class="w-12 h-12 rounded-full bg-green-500 shadow-2xl animate-bounce" style="animation-delay: 0.4s;"></div>
                        <div class="w-12 h-12 rounded-full bg-yellow-500 shadow-2xl animate-bounce" style="animation-delay: 0.6s;"></div>
                      </div>
                      <div class="absolute -top-2 -right-2 w-8 h-8 bg-white/20 rounded-full backdrop-blur animate-pulse"></div>
                      <div class="absolute -bottom-2 -left-2 w-6 h-6 bg-white/20 rounded-full backdrop-blur animate-pulse delay-300"></div>
                    </div>
                  </div>

                  <!-- Icon Badge -->
                  <div class="absolute top-6 right-6">
                    <div class="w-16 h-16 bg-white/20 backdrop-blur-lg rounded-2xl flex items-center justify-center border border-white/30">
                      <IconPuzzle class="w-8 h-8 text-white" />
                    </div>
                  </div>

                  <!-- Difficulty Badge -->
                  <div class="absolute bottom-6 left-6">
                    <div class="inline-flex items-center px-3 py-1 rounded-full bg-white/20 backdrop-blur-lg border border-white/30">
                      <div class="w-2 h-2 bg-orange-400 rounded-full mr-2"></div>
                      <span class="text-white text-sm font-medium">Intermediate</span>
                    </div>
                  </div>
                </div>

                <!-- Card Content -->
                <div class="p-8 space-y-6">
                  <div class="space-y-4">
                    <div class="flex items-center justify-between">
                      <h3 class="text-2xl sm:text-3xl font-bold text-gray-900 dark:text-white">
                        Mastermind Game
                      </h3>
                      <div class="flex items-center space-x-1">
                        <div class="w-2 h-2 bg-green-500 rounded-full animate-pulse"></div>
                        <span class="text-sm text-green-600 dark:text-green-400 font-medium">Active</span>
                      </div>
                    </div>
                    
                    <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                      Master the art of deductive reasoning in this classic code-breaking puzzle. 
                      Analyze clues, eliminate possibilities, and crack the secret combination using pure logic.
                    </p>
                  </div>

                  <!-- Features -->
                  <div class="flex flex-wrap gap-2">
                    <span class="px-3 py-1 bg-purple-100 dark:bg-purple-900/30 text-purple-700 dark:text-purple-300 rounded-full text-sm font-medium">Logic Puzzle</span>
                    <span class="px-3 py-1 bg-pink-100 dark:bg-pink-900/30 text-pink-700 dark:text-pink-300 rounded-full text-sm font-medium">Pattern Recognition</span>
                    <span class="px-3 py-1 bg-indigo-100 dark:bg-indigo-900/30 text-indigo-700 dark:text-indigo-300 rounded-full text-sm font-medium">Strategic Thinking</span>
                  </div>

                  <!-- Stats -->
                  <div class="grid grid-cols-2 gap-4 pt-4 border-t border-gray-200 dark:border-gray-700">
                    <div class="text-center">
                      <div class="flex items-center justify-center mb-2">
                        <IconTarget class="w-5 h-5 text-purple-500 mr-2" />
                        <span class="text-2xl font-bold text-gray-900 dark:text-white">10</span>
                      </div>
                      <span class="text-sm text-gray-500 dark:text-gray-400">Max Attempts</span>
                    </div>
                    <div class="text-center">
                      <div class="flex items-center justify-center mb-2">
                        <IconClock class="w-5 h-5 text-blue-500 mr-2" />
                        <span class="text-2xl font-bold text-gray-900 dark:text-white">15</span>
                      </div>
                      <span class="text-sm text-gray-500 dark:text-gray-400">Minutes</span>
                    </div>
                  </div>

                  <!-- Action Button -->
                  <router-link 
                    to="/mastermind"
                    class="w-full inline-flex items-center justify-center px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 hover:from-purple-700 hover:to-pink-700 text-white font-semibold rounded-2xl transition-all duration-300 group-hover:shadow-xl group-hover:shadow-purple-500/25 transform hover:scale-105"
                  >
                    <span class="mr-3">Start Playing</span>
                    <IconArrowRight class="w-5 h-5 group-hover:translate-x-1 transition-transform" />
                  </router-link>
                </div>
              </div>
            </div>

            <!-- Parser Calculator Card -->
            <div class="group relative">
              <div class="absolute inset-0 bg-gradient-to-r from-green-600 to-blue-600 rounded-3xl blur opacity-25 group-hover:opacity-40 transition-opacity duration-500"></div>
              <div class="relative bg-white/80 dark:bg-gray-900/80 backdrop-blur-xl rounded-3xl border border-white/20 dark:border-gray-700/50 overflow-hidden hover:shadow-2xl hover:shadow-blue-500/25 transition-all duration-500 group-hover:-translate-y-2">
                
                <!-- Card Header -->
                <div class="relative h-64 bg-gradient-to-br from-green-500 via-emerald-600 to-blue-600 overflow-hidden">
                  <!-- Background Pattern -->
                  <div class="absolute inset-0 opacity-20">
                    <div class="absolute inset-0" style="background-image: linear-gradient(45deg, transparent 35%, white 35%, white 65%, transparent 65%), linear-gradient(-45deg, transparent 35%, white 35%, white 65%, transparent 65%); background-size: 20px 20px;"></div>
                  </div>
                  
                  <!-- Mathematical Expressions -->
                  <div class="absolute inset-0 flex items-center justify-center">
                    <div class="relative">
                      <div class="text-white font-mono text-center space-y-2">
                        <div class="text-3xl font-bold animate-pulse">2³ + √16 = 12</div>
                        <div class="text-lg opacity-80">(5 × 3) ÷ 2 + 7</div>
                        <div class="text-sm opacity-60">∫ x² dx = x³/3 + C</div>
                      </div>
                      <div class="absolute -top-4 -right-4 w-8 h-8 bg-white/20 rounded-full backdrop-blur animate-spin"></div>
                      <div class="absolute -bottom-4 -left-4 w-6 h-6 bg-white/20 rounded-full backdrop-blur animate-ping"></div>
                    </div>
                  </div>

                  <!-- Icon Badge -->
                  <div class="absolute top-6 right-6">
                    <div class="w-16 h-16 bg-white/20 backdrop-blur-lg rounded-2xl flex items-center justify-center border border-white/30">
                      <IconCalculator class="w-8 h-8 text-white" />
                    </div>
                  </div>

                  <!-- Performance Badge -->
                  <div class="absolute bottom-6 left-6">
                    <div class="inline-flex items-center px-3 py-1 rounded-full bg-white/20 backdrop-blur-lg border border-white/30">
                      <div class="w-2 h-2 bg-green-400 rounded-full mr-2 animate-pulse"></div>
                      <span class="text-white text-sm font-medium">Ultra Fast</span>
                    </div>
                  </div>
                </div>

                <!-- Card Content -->
                <div class="p-8 space-y-6">
                  <div class="space-y-4">
                    <div class="flex items-center justify-between">
                      <h3 class="text-2xl sm:text-3xl font-bold text-gray-900 dark:text-white">
                        Math Parser
                      </h3>
                      <div class="flex items-center space-x-1">
                        <div class="w-2 h-2 bg-blue-500 rounded-full animate-pulse"></div>
                        <span class="text-sm text-blue-600 dark:text-blue-400 font-medium">Advanced</span>
                      </div>
                    </div>
                    
                    <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                      Unleash the power of mathematical computation with our advanced expression parser. 
                      Handle complex equations, nested operations, and mathematical functions with precision.
                    </p>
                  </div>

                  <!-- Features -->
                  <div class="flex flex-wrap gap-2">
                    <span class="px-3 py-1 bg-green-100 dark:bg-green-900/30 text-green-700 dark:text-green-300 rounded-full text-sm font-medium">Expression Parser</span>
                    <span class="px-3 py-1 bg-blue-100 dark:bg-blue-900/30 text-blue-700 dark:text-blue-300 rounded-full text-sm font-medium">Real-time</span>
                    <span class="px-3 py-1 bg-teal-100 dark:bg-teal-900/30 text-teal-700 dark:text-teal-300 rounded-full text-sm font-medium">Error Handling</span>
                  </div>

                  <!-- Stats -->
                  <div class="grid grid-cols-2 gap-4 pt-4 border-t border-gray-200 dark:border-gray-700">
                    <div class="text-center">
                      <div class="flex items-center justify-center mb-2">
                        <IconBolt class="w-5 h-5 text-yellow-500 mr-2" />
                        <span class="text-2xl font-bold text-gray-900 dark:text-white">∞</span>
                      </div>
                      <span class="text-sm text-gray-500 dark:text-gray-400">Operations</span>
                    </div>
                    <div class="text-center">
                      <div class="flex items-center justify-center mb-2">
                        <IconMath class="w-5 h-5 text-green-500 mr-2" />
                        <span class="text-2xl font-bold text-gray-900 dark:text-white">100%</span>
                      </div>
                      <span class="text-sm text-gray-500 dark:text-gray-400">Accurate</span>
                    </div>
                  </div>

                  <!-- Action Button -->
                  <router-link 
                    to="/parser"
                    class="w-full inline-flex items-center justify-center px-8 py-4 bg-gradient-to-r from-green-600 to-blue-600 hover:from-green-700 hover:to-blue-700 text-white font-semibold rounded-2xl transition-all duration-300 group-hover:shadow-xl group-hover:shadow-blue-500/25 transform hover:scale-105"
                  >
                    <span class="mr-3">Try Calculator</span>
                    <IconArrowRight class="w-5 h-5 group-hover:translate-x-1 transition-transform" />
                  </router-link>
                </div>
              </div>
            </div>

          </div>
        </div>
      </section>

      <!-- Features Showcase -->
      <section class="px-4 py-24 sm:px-6 lg:px-8 bg-white/50 dark:bg-gray-900/50 backdrop-blur-xl">
        <div class="max-w-7xl mx-auto">
          <div class="text-center mb-16">
            <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 dark:text-white mb-4">
              Built for Excellence
            </h2>
            <p class="text-lg text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">
              Every feature is crafted with attention to detail and modern best practices
            </p>
          </div>

          <div class="grid md:grid-cols-3 gap-8">
            <div class="text-center group">
              <div class="relative mx-auto w-20 h-20 mb-6">
                <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-purple-500 rounded-2xl rotate-6 group-hover:rotate-12 transition-transform duration-300"></div>
                <div class="relative bg-white dark:bg-gray-800 rounded-2xl w-full h-full flex items-center justify-center border-2 border-blue-100 dark:border-blue-800">
                  <IconDeviceDesktop class="w-8 h-8 text-blue-600 dark:text-blue-400" />
                </div>
              </div>
              <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-3">Responsive Design</h3>
              <p class="text-gray-600 dark:text-gray-300">Flawlessly adapts to any screen size, from mobile to desktop, ensuring a perfect experience everywhere.</p>
            </div>

            <div class="text-center group">
              <div class="relative mx-auto w-20 h-20 mb-6">
                <div class="absolute inset-0 bg-gradient-to-r from-purple-500 to-pink-500 rounded-2xl rotate-6 group-hover:rotate-12 transition-transform duration-300"></div>
                <div class="relative bg-white dark:bg-gray-800 rounded-2xl w-full h-full flex items-center justify-center border-2 border-purple-100 dark:border-purple-800">
                  <IconPalette class="w-8 h-8 text-purple-600 dark:text-purple-400" />
                </div>
              </div>
              <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-3">Beautiful Interface</h3>
              <p class="text-gray-600 dark:text-gray-300">Stunning gradients, smooth animations, and thoughtful micro-interactions create a delightful user experience.</p>
            </div>

            <div class="text-center group">
              <div class="relative mx-auto w-20 h-20 mb-6">
                <div class="absolute inset-0 bg-gradient-to-r from-green-500 to-teal-500 rounded-2xl rotate-6 group-hover:rotate-12 transition-transform duration-300"></div>
                <div class="relative bg-white dark:bg-gray-800 rounded-2xl w-full h-full flex items-center justify-center border-2 border-green-100 dark:border-green-800">
                  <IconRocket class="w-8 h-8 text-green-600 dark:text-green-400" />
                </div>
              </div>
              <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-3">Lightning Fast</h3>
              <p class="text-gray-600 dark:text-gray-300">Built with Vue 3, TypeScript, and optimized for performance. Every interaction is instant and smooth.</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Call to Action -->
      <section class="px-4 py-24 sm:px-6 lg:px-8">
        <div class="max-w-4xl mx-auto text-center">
          <div class="space-y-8">
            <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-gray-900 dark:text-white">
              Ready to Begin?
            </h2>
            <p class="text-lg text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">
              Choose your preferred application and start exploring the possibilities
            </p>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center items-center pt-8">
              <router-link 
                to="/mastermind"
                class="inline-flex items-center px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 hover:from-purple-700 hover:to-pink-700 text-white font-semibold rounded-2xl transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-purple-500/25"
              >
                <IconPuzzle class="w-5 h-5 mr-3" />
                <span>Play Mastermind</span>
              </router-link>
              
              <router-link 
                to="/parser"
                class="inline-flex items-center px-8 py-4 bg-gradient-to-r from-green-600 to-blue-600 hover:from-green-700 hover:to-blue-700 text-white font-semibold rounded-2xl transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-blue-500/25"
              >
                <IconCalculator class="w-5 h-5 mr-3" />
                <span>Use Calculator</span>
              </router-link>
            </div>
          </div>
        </div>
      </section>

      <!-- Footer -->
      <footer class="px-4 py-12 sm:px-6 lg:px-8 border-t border-gray-200/50 dark:border-gray-700/50">
        <div class="max-w-7xl mx-auto text-center">
          <div class="flex items-center justify-center space-x-2 mb-4">
            <div class="w-8 h-8 bg-gradient-to-r from-purple-500 to-pink-500 rounded-lg flex items-center justify-center">
              <span class="text-white font-bold text-sm">GH</span>
            </div>
            <span class="text-lg font-bold text-gray-900 dark:text-white">Gaming Hub</span>
          </div>
          <p class="text-gray-500 dark:text-gray-400">
            Crafted with ❤️ using Vue 3, TypeScript, and Tailwind CSS
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
/* Custom animations */
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

.animate-float {
  animation: float 3s ease-in-out infinite;
}

.animate-float-delay {
  animation: float 3s ease-in-out infinite;
  animation-delay: 1s;
}

/* Backdrop blur fallback */
@supports not (backdrop-filter: blur(10px)) {
  .backdrop-blur-xl {
    background-color: rgba(255, 255, 255, 0.9);
  }
  
  .dark .backdrop-blur-xl {
    background-color: rgba(17, 24, 39, 0.9);
  }
}
</style>