<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 relative overflow-hidden">
    <!-- Ultra Advanced Background -->
    <div class="absolute inset-0 overflow-hidden">
      <!-- Animated Mesh Gradient -->
      <div class="absolute inset-0 opacity-40">
        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-r from-purple-500/30 via-pink-500/30 to-indigo-500/30 animate-pulse"></div>
        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-b from-transparent via-blue-500/20 to-transparent animate-ping" style="animation-duration: 4s;"></div>
      </div>
      
      <!-- 3D Floating Elements -->
      <div class="absolute inset-0 perspective-1000">
        <div class="absolute top-20 left-20 w-32 h-32 bg-gradient-to-br from-purple-400 to-pink-600 rounded-3xl opacity-20 animate-float-3d transform rotate-12 hover:rotate-45 transition-all duration-1000"></div>
        <div class="absolute top-40 right-32 w-24 h-24 bg-gradient-to-br from-blue-400 to-cyan-600 rounded-full opacity-30 animate-float-3d-delay transform -rotate-12 hover:rotate-12 transition-all duration-1000"></div>
        <div class="absolute bottom-32 left-40 w-40 h-40 bg-gradient-to-br from-green-400 to-emerald-600 rounded-2xl opacity-15 animate-float-3d transform rotate-45 hover:-rotate-12 transition-all duration-1000"></div>
        <div class="absolute bottom-20 right-20 w-28 h-28 bg-gradient-to-br from-yellow-400 to-orange-600 rounded-full opacity-25 animate-float-3d-delay transform -rotate-45 hover:rotate-45 transition-all duration-1000"></div>
      </div>

      <!-- Particle System -->
      <div class="absolute inset-0">
        <div class="particle particle-1"></div>
        <div class="particle particle-2"></div>
        <div class="particle particle-3"></div>
        <div class="particle particle-4"></div>
        <div class="particle particle-5"></div>
        <div class="particle particle-6"></div>
        <div class="particle particle-7"></div>
        <div class="particle particle-8"></div>
      </div>
    </div>

    <div class="relative z-10">
      <!-- Hero Section with 3D Effects -->
      <section class="px-4 pt-32 pb-24 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
          <div class="text-center space-y-12 transform-gpu">
            
            <!-- Premium Badge -->
            <div class="inline-flex items-center px-6 py-3 rounded-full bg-gradient-to-r from-purple-600/20 to-pink-600/20 backdrop-blur-xl border border-purple-500/30 shadow-2xl transform hover:scale-105 transition-all duration-500">
              <div class="w-2 h-2 bg-gradient-to-r from-purple-400 to-pink-400 rounded-full animate-pulse mr-3"></div>
              <span class="text-sm font-bold bg-gradient-to-r from-purple-200 to-pink-200 bg-clip-text text-transparent">🚀 NEXT-GENERATION GAMING EXPERIENCE</span>
            </div>
            
            <!-- Main Title with 3D Effect -->
            <div class="space-y-8">
              <h1 class="text-6xl sm:text-8xl lg:text-9xl font-black leading-none">
                <span class="block bg-gradient-to-r from-white via-purple-200 to-blue-200 bg-clip-text text-transparent transform-gpu hover:scale-105 transition-transform duration-700 cursor-default select-none" style="text-shadow: 0 0 80px rgba(147, 51, 234, 0.5);">
                  GAMING
                </span>
                <span class="block bg-gradient-to-r from-pink-200 via-purple-200 to-indigo-200 bg-clip-text text-transparent transform-gpu hover:scale-105 transition-transform duration-700 cursor-default select-none mt-4" style="text-shadow: 0 0 80px rgba(236, 72, 153, 0.5);">
                  HUB
                </span>
              </h1>
              
              <div class="max-w-4xl mx-auto space-y-6">
                <p class="text-xl sm:text-2xl lg:text-3xl text-gray-300 leading-relaxed font-light">
                  Experience the future of 
                  <span class="font-bold text-transparent bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text">interactive entertainment</span> 
                  with cutting-edge design and 
                  <span class="font-bold text-transparent bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text">immersive gameplay</span>
                </p>
                
                <!-- CTA Buttons with 3D Effects -->
                <div class="flex flex-col sm:flex-row gap-6 justify-center items-center pt-8">
                  <router-link 
                    to="/mastermind"
                    class="group relative inline-flex items-center px-12 py-6 bg-gradient-to-r from-purple-600 via-purple-700 to-pink-600 text-white font-bold text-lg rounded-2xl shadow-2xl transform hover:scale-110 hover:-translate-y-2 transition-all duration-500 hover:shadow-purple-500/50"
                  >
                    <div class="absolute inset-0 bg-gradient-to-r from-purple-400 to-pink-400 rounded-2xl blur opacity-75 group-hover:opacity-100 transition-opacity duration-500"></div>
                    <div class="relative flex items-center space-x-3">
                      <IconPuzzle class="w-6 h-6 group-hover:rotate-180 transition-transform duration-700" />
                      <span>ENTER THE MATRIX</span>
                      <IconArrowRight class="w-6 h-6 group-hover:translate-x-2 transition-transform duration-500" />
                    </div>
                  </router-link>
                  
                  <router-link 
                    to="/parser"
                    class="group relative inline-flex items-center px-12 py-6 bg-gradient-to-r from-emerald-600 via-blue-600 to-cyan-600 text-white font-bold text-lg rounded-2xl shadow-2xl transform hover:scale-110 hover:-translate-y-2 transition-all duration-500 hover:shadow-cyan-500/50"
                  >
                    <div class="absolute inset-0 bg-gradient-to-r from-emerald-400 to-cyan-400 rounded-2xl blur opacity-75 group-hover:opacity-100 transition-opacity duration-500"></div>
                    <div class="relative flex items-center space-x-3">
                      <IconCalculator class="w-6 h-6 group-hover:rotate-180 transition-transform duration-700" />
                      <span>COMPUTE REALITY</span>
                      <IconArrowRight class="w-6 h-6 group-hover:translate-x-2 transition-transform duration-500" />
                    </div>
                  </router-link>
                </div>
              </div>
            </div>

            <!-- Advanced Stats -->
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-8 pt-16">
              <div class="group relative bg-white/5 backdrop-blur-xl rounded-3xl p-8 border border-white/10 hover:border-purple-500/50 transition-all duration-500 transform hover:scale-105 hover:-translate-y-2">
                <div class="absolute inset-0 bg-gradient-to-br from-purple-600/10 to-pink-600/10 rounded-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                <div class="relative text-center">
                  <div class="text-4xl sm:text-5xl font-black bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent mb-2">∞</div>
                  <div class="text-white font-bold text-lg mb-1">POSSIBILITIES</div>
                  <div class="text-gray-400 text-sm">Endless combinations</div>
                </div>
              </div>
              
              <div class="group relative bg-white/5 backdrop-blur-xl rounded-3xl p-8 border border-white/10 hover:border-blue-500/50 transition-all duration-500 transform hover:scale-105 hover:-translate-y-2">
                <div class="absolute inset-0 bg-gradient-to-br from-blue-600/10 to-cyan-600/10 rounded-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                <div class="relative text-center">
                  <div class="text-4xl sm:text-5xl font-black bg-gradient-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent mb-2">100%</div>
                  <div class="text-white font-bold text-lg mb-1">PRECISION</div>
                  <div class="text-gray-400 text-sm">Mathematical accuracy</div>
                </div>
              </div>
              
              <div class="group relative bg-white/5 backdrop-blur-xl rounded-3xl p-8 border border-white/10 hover:border-green-500/50 transition-all duration-500 transform hover:scale-105 hover:-translate-y-2">
                <div class="absolute inset-0 bg-gradient-to-br from-green-600/10 to-emerald-600/10 rounded-3xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                <div class="relative text-center">
                  <div class="text-4xl sm:text-5xl font-black bg-gradient-to-r from-green-400 to-emerald-400 bg-clip-text text-transparent mb-2">0ms</div>
                  <div class="text-white font-bold text-lg mb-1">LATENCY</div>
                  <div class="text-gray-400 text-sm">Instant response</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Revolutionary Application Cards -->
      <section class="px-4 py-32 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
          
          <div class="text-center mb-20">
            <h2 class="text-5xl sm:text-6xl lg:text-7xl font-black text-white mb-8 transform hover:scale-105 transition-transform duration-700">
              <span class="bg-gradient-to-r from-white via-purple-200 to-pink-200 bg-clip-text text-transparent">
                CHOOSE YOUR
              </span>
              <br />
              <span class="bg-gradient-to-r from-pink-200 via-purple-200 to-blue-200 bg-clip-text text-transparent">
                DIMENSION
              </span>
            </h2>
          </div>

          <div class="grid lg:grid-cols-2 gap-16">
            
            <!-- Mastermind: Ultra Premium Card -->
            <div class="group relative perspective-1000">
              <!-- Card Shadow/Glow -->
              <div class="absolute inset-0 bg-gradient-to-r from-purple-600 to-pink-600 rounded-3xl blur-xl opacity-50 group-hover:opacity-75 transition-all duration-700 scale-105"></div>
              
              <!-- Main Card -->
              <div class="relative bg-gradient-to-br from-gray-900/90 to-black/90 backdrop-blur-2xl rounded-3xl border border-purple-500/30 overflow-hidden transform-gpu group-hover:rotateY-5 transition-all duration-700">
                
                <!-- Header with 3D Scene -->
                <div class="relative h-80 bg-gradient-to-br from-purple-900 via-purple-800 to-pink-900 overflow-hidden">
                  <!-- 3D Background Grid -->
                  <div class="absolute inset-0 opacity-30">
                    <div class="grid-3d"></div>
                  </div>
                  
                  <!-- Floating Game Elements -->
                  <div class="absolute inset-0 flex items-center justify-center">
                    <div class="relative transform-gpu group-hover:scale-110 transition-transform duration-1000">
                      <div class="flex items-center space-x-4">
                        <div class="w-16 h-16 rounded-full bg-gradient-to-br from-red-400 to-red-600 shadow-2xl transform hover:scale-125 transition-all duration-500 animate-float-slow"></div>
                        <div class="w-16 h-16 rounded-full bg-gradient-to-br from-blue-400 to-blue-600 shadow-2xl transform hover:scale-125 transition-all duration-500 animate-float-slow" style="animation-delay: 0.5s;"></div>
                        <div class="w-16 h-16 rounded-full bg-gradient-to-br from-green-400 to-green-600 shadow-2xl transform hover:scale-125 transition-all duration-500 animate-float-slow" style="animation-delay: 1s;"></div>
                        <div class="w-16 h-16 rounded-full bg-gradient-to-br from-yellow-400 to-yellow-600 shadow-2xl transform hover:scale-125 transition-all duration-500 animate-float-slow" style="animation-delay: 1.5s;"></div>
                      </div>
                      
                      <!-- Holographic Effects -->
                      <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/20 to-transparent skew-x-12 transform translate-x-full group-hover:-translate-x-full transition-transform duration-1000"></div>
                    </div>
                  </div>

                  <!-- Status Indicator -->
                  <div class="absolute top-8 right-8">
                    <div class="flex items-center space-x-2 px-4 py-2 bg-black/50 backdrop-blur-xl rounded-full border border-purple-500/50">
                      <div class="w-3 h-3 bg-green-400 rounded-full animate-pulse"></div>
                      <span class="text-green-400 text-sm font-bold">ACTIVE</span>
                    </div>
                  </div>

                  <!-- Difficulty Badge -->
                  <div class="absolute bottom-8 left-8">
                    <div class="px-4 py-2 bg-gradient-to-r from-orange-600/80 to-red-600/80 backdrop-blur-xl rounded-full border border-orange-500/50">
                      <span class="text-white text-sm font-bold">EXPERT LEVEL</span>
                    </div>
                  </div>
                </div>

                <!-- Card Content -->
                <div class="p-10 space-y-8">
                  <div class="space-y-4">
                    <h3 class="text-4xl font-black text-white group-hover:text-purple-300 transition-colors duration-500">
                      MASTERMIND
                    </h3>
                    <p class="text-xl text-gray-300 leading-relaxed">
                      Enter the neural network of deductive reasoning. Crack impossible codes using pure logic and strategic thinking in this mind-bending puzzle experience.
                    </p>
                  </div>

                  <!-- Enhanced Stats Grid -->
                  <div class="grid grid-cols-2 gap-6">
                    <div class="bg-gradient-to-br from-purple-600/20 to-pink-600/20 rounded-2xl p-6 border border-purple-500/30">
                      <div class="text-3xl font-black text-purple-400 mb-2">10</div>
                      <div class="text-white font-bold text-sm">MAX ATTEMPTS</div>
                    </div>
                    <div class="bg-gradient-to-br from-blue-600/20 to-cyan-600/20 rounded-2xl p-6 border border-blue-500/30">
                      <div class="text-3xl font-black text-blue-400 mb-2">∞</div>
                      <div class="text-white font-bold text-sm">VARIATIONS</div>
                    </div>
                  </div>

                  <!-- Action Button -->
                  <router-link 
                    to="/mastermind"
                    class="group/btn relative w-full inline-flex items-center justify-center px-8 py-6 bg-gradient-to-r from-purple-600 to-pink-600 text-white font-black text-xl rounded-2xl overflow-hidden transform hover:scale-105 transition-all duration-500"
                  >
                    <div class="absolute inset-0 bg-gradient-to-r from-white/20 to-transparent skew-x-12 transform -translate-x-full group-hover/btn:translate-x-full transition-transform duration-700"></div>
                    <div class="relative flex items-center space-x-3">
                      <IconPuzzle class="w-6 h-6 group-hover/btn:rotate-180 transition-transform duration-700" />
                      <span>HACK THE CODE</span>
                      <IconArrowRight class="w-6 h-6 group-hover/btn:translate-x-2 transition-transform duration-500" />
                    </div>
                  </router-link>
                </div>
              </div>
            </div>

            <!-- Parser: Ultra Premium Card -->
            <div class="group relative perspective-1000">
              <!-- Card Shadow/Glow -->
              <div class="absolute inset-0 bg-gradient-to-r from-emerald-600 to-cyan-600 rounded-3xl blur-xl opacity-50 group-hover:opacity-75 transition-all duration-700 scale-105"></div>
              
              <!-- Main Card -->
              <div class="relative bg-gradient-to-br from-gray-900/90 to-black/90 backdrop-blur-2xl rounded-3xl border border-emerald-500/30 overflow-hidden transform-gpu group-hover:rotateY-5 transition-all duration-700">
                
                <!-- Header with Mathematical Scene -->
                <div class="relative h-80 bg-gradient-to-br from-emerald-900 via-blue-900 to-cyan-900 overflow-hidden">
                  <!-- Matrix Rain Effect -->
                  <div class="absolute inset-0 opacity-20">
                    <div class="matrix-rain"></div>
                  </div>
                  
                  <!-- Floating Mathematical Elements -->
                  <div class="absolute inset-0 flex items-center justify-center">
                    <div class="relative transform-gpu group-hover:scale-110 transition-transform duration-1000">
                      <div class="text-center space-y-4">
                        <div class="text-5xl font-black text-white animate-pulse">
                          E = mc²
                        </div>
                        <div class="text-2xl text-emerald-300 opacity-80">
                          ∫ f(x)dx = F(x) + C
                        </div>
                        <div class="text-lg text-cyan-300 opacity-60">
                          lim(x→∞) = ∞
                        </div>
                      </div>
                      
                      <!-- Holographic Effects -->
                      <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/20 to-transparent skew-x-12 transform translate-x-full group-hover:-translate-x-full transition-transform duration-1000"></div>
                    </div>
                  </div>

                  <!-- Performance Indicator -->
                  <div class="absolute top-8 right-8">
                    <div class="flex items-center space-x-2 px-4 py-2 bg-black/50 backdrop-blur-xl rounded-full border border-emerald-500/50">
                      <div class="w-3 h-3 bg-emerald-400 rounded-full animate-pulse"></div>
                      <span class="text-emerald-400 text-sm font-bold">QUANTUM</span>
                    </div>
                  </div>

                  <!-- Algorithm Badge -->
                  <div class="absolute bottom-8 left-8">
                    <div class="px-4 py-2 bg-gradient-to-r from-cyan-600/80 to-blue-600/80 backdrop-blur-xl rounded-full border border-cyan-500/50">
                      <span class="text-white text-sm font-bold">AI POWERED</span>
                    </div>
                  </div>
                </div>

                <!-- Card Content -->
                <div class="p-10 space-y-8">
                  <div class="space-y-4">
                    <h3 class="text-4xl font-black text-white group-hover:text-emerald-300 transition-colors duration-500">
                      MATH PARSER
                    </h3>
                    <p class="text-xl text-gray-300 leading-relaxed">
                      Unleash quantum-level computational power. Process complex mathematical expressions with AI-driven parsing algorithms and infinite precision.
                    </p>
                  </div>

                  <!-- Enhanced Stats Grid -->
                  <div class="grid grid-cols-2 gap-6">
                    <div class="bg-gradient-to-br from-emerald-600/20 to-cyan-600/20 rounded-2xl p-6 border border-emerald-500/30">
                      <div class="text-3xl font-black text-emerald-400 mb-2">∞</div>
                      <div class="text-white font-bold text-sm">OPERATIONS</div>
                    </div>
                    <div class="bg-gradient-to-br from-blue-600/20 to-cyan-600/20 rounded-2xl p-6 border border-blue-500/30">
                      <div class="text-3xl font-black text-cyan-400 mb-2">0.1ms</div>
                      <div class="text-white font-bold text-sm">RESPONSE</div>
                    </div>
                  </div>

                  <!-- Action Button -->
                  <router-link 
                    to="/parser"
                    class="group/btn relative w-full inline-flex items-center justify-center px-8 py-6 bg-gradient-to-r from-emerald-600 to-cyan-600 text-white font-black text-xl rounded-2xl overflow-hidden transform hover:scale-105 transition-all duration-500"
                  >
                    <div class="absolute inset-0 bg-gradient-to-r from-white/20 to-transparent skew-x-12 transform -translate-x-full group-hover/btn:translate-x-full transition-transform duration-700"></div>
                    <div class="relative flex items-center space-x-3">
                      <IconCalculator class="w-6 h-6 group-hover/btn:rotate-180 transition-transform duration-700" />
                      <span>COMPUTE INFINITY</span>
                      <IconArrowRight class="w-6 h-6 group-hover/btn:translate-x-2 transition-transform duration-500" />
                    </div>
                  </router-link>
                </div>
              </div>
            </div>

          </div>
        </div>
      </section>

      <!-- Premium Footer -->
      <footer class="px-4 py-16 sm:px-6 lg:px-8 border-t border-white/10">
        <div class="max-w-7xl mx-auto text-center">
          <div class="flex items-center justify-center space-x-4 mb-6">
            <div class="w-12 h-12 bg-gradient-to-r from-purple-500 to-pink-500 rounded-2xl flex items-center justify-center transform rotate-12 hover:rotate-45 transition-transform duration-500">
              <span class="text-white font-black text-xl">GH</span>
            </div>
            <span class="text-2xl font-black text-white">GAMING HUB</span>
          </div>
          <p class="text-gray-400 text-lg">
            Engineered with ❤️ using cutting-edge technology
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
  IconArrowRight
} from '@tabler/icons-vue'
</script>

<style scoped>
/* Advanced 3D Animations */
@keyframes float-3d {
  0%, 100% { 
    transform: translateY(0px) rotateX(0deg) rotateY(0deg); 
  }
  50% { 
    transform: translateY(-20px) rotateX(10deg) rotateY(5deg); 
  }
}

@keyframes float-3d-delay {
  0%, 100% { 
    transform: translateY(0px) rotateX(0deg) rotateY(0deg); 
  }
  50% { 
    transform: translateY(-30px) rotateX(-10deg) rotateY(-5deg); 
  }
}

@keyframes float-slow {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

.animate-float-3d {
  animation: float-3d 6s ease-in-out infinite;
}

.animate-float-3d-delay {
  animation: float-3d-delay 8s ease-in-out infinite;
}

.animate-float-slow {
  animation: float-slow 4s ease-in-out infinite;
}

/* 3D Perspective */
.perspective-1000 {
  perspective: 1000px;
}

.transform-gpu {
  transform: translateZ(0);
  backface-visibility: hidden;
}

.rotateY-5:hover {
  transform: rotateY(5deg);
}

/* Particle System */
.particle {
  position: absolute;
  width: 4px;
  height: 4px;
  background: radial-gradient(circle, #8b5cf6, transparent);
  border-radius: 50%;
  opacity: 0.6;
}

.particle-1 { top: 20%; left: 10%; animation: float-3d 8s ease-in-out infinite; }
.particle-2 { top: 40%; right: 15%; animation: float-3d-delay 10s ease-in-out infinite; }
.particle-3 { bottom: 30%; left: 20%; animation: float-3d 12s ease-in-out infinite; }
.particle-4 { top: 60%; left: 70%; animation: float-3d-delay 7s ease-in-out infinite; }
.particle-5 { bottom: 20%; right: 25%; animation: float-3d 9s ease-in-out infinite; }
.particle-6 { top: 80%; left: 60%; animation: float-3d-delay 11s ease-in-out infinite; }
.particle-7 { top: 10%; right: 40%; animation: float-3d 13s ease-in-out infinite; }
.particle-8 { bottom: 50%; left: 80%; animation: float-3d-delay 6s ease-in-out infinite; }

/* 3D Grid Effect */
.grid-3d {
  background-image: 
    linear-gradient(rgba(147, 51, 234, 0.3) 1px, transparent 1px),
    linear-gradient(90deg, rgba(147, 51, 234, 0.3) 1px, transparent 1px);
  background-size: 50px 50px;
  transform: perspective(500px) rotateX(60deg);
  animation: grid-move 20s linear infinite;
}

@keyframes grid-move {
  from { transform: perspective(500px) rotateX(60deg) translateY(0); }
  to { transform: perspective(500px) rotateX(60deg) translateY(50px); }
}

/* Matrix Rain Effect */
.matrix-rain {
  background: linear-gradient(0deg, transparent 0%, rgba(16, 185, 129, 0.1) 50%, transparent 100%);
  background-size: 100% 100px;
  animation: matrix-fall 3s linear infinite;
}

@keyframes matrix-fall {
  from { background-position: 0 -100px; }
  to { background-position: 0 100vh; }
}

/* Enhanced Transitions */
* {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}

/* Backdrop Blur Support */
@supports not (backdrop-filter: blur(20px)) {
  .backdrop-blur-2xl {
    background-color: rgba(17, 24, 39, 0.9);
  }
}
</style>