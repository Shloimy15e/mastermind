<template>
  <div class="home-page">
    <header class="hero-section">
      <div class="hero-content">
        <div class="hero-badge">
          <div class="badge-dot"></div>
          <span>Interactive Portfolio</span>
        </div>
        <h1>My Project Showcase</h1>
        <p>Welcome to my collection of interactive web applications</p>
      </div>
    </header>

    <main class="applications-showcase">
      <h2>Featured Applications</h2>
      
      <div class="app-grid">
        <!-- Mastermind Game Card -->
        <div class="app-card mastermind-card">
          <div class="app-preview">
            <div class="card-header">
              <div class="app-icon mastermind-icon">
                <IconPuzzle :size="24" />
              </div>
              <h3>Mastermind Logic Game</h3>
            </div>
            <div class="preview-content">
              <div class="color-dots">
                <div class="dot red"></div>
                <div class="dot blue"></div>
                <div class="dot green"></div>
                <div class="dot yellow"></div>
              </div>
              <p>Classic code-breaking puzzle game. Guess the secret color combination!</p>
            </div>
          </div>
          
          <div class="app-info">
            <ul class="features">
              <li><IconCheck :size="16" /> 10 attempts to crack the code</li>
              <li><IconCheck :size="16" /> 6 different colors to choose from</li>
              <li><IconCheck :size="16" /> Intelligent feedback system</li>
              <li><IconCheck :size="16" /> Built with Vue 3 & TypeScript</li>
            </ul>
            
            <div class="app-actions">
              <router-link to="/mastermind" class="play-button primary-btn">
                <IconPlayerPlay :size="18" />
                <span>Play Mastermind</span>
              </router-link>
            </div>
          </div>
        </div>

        <!-- Parser Calculator Card -->
        <div class="app-card calculator-card">
          <div class="app-preview">
            <div class="card-header">
              <div class="app-icon calculator-icon">
                <IconCalculator :size="24" />
              </div>
              <h3>Math Expression Parser</h3>
            </div>
            <div class="preview-content">
              <div class="math-example">
                <div class="expression">(2 + 3) × 4 = 20</div>
                <div class="expression">√16 + 3² = 13</div>
              </div>
              <p>Advanced calculator that parses complex mathematical expressions</p>
            </div>
          </div>
          
          <div class="app-info">
            <ul class="features">
              <li><IconCheck :size="16" /> Supports complex expressions</li>
              <li><IconCheck :size="16" /> Operator precedence handling</li>
              <li><IconCheck :size="16" /> Parentheses and functions</li>
              <li><IconCheck :size="16" /> Real-time calculation</li>
            </ul>
            
            <div class="app-actions">
              <router-link to="/parser" class="play-button secondary-btn">
                <IconMath :size="18" />
                <span>Try Calculator</span>
              </router-link>
            </div>
          </div>
        </div>
      </div>
    </main>

    <footer class="page-footer">
      <div class="footer-content">
        <div class="tech-stack">
          <IconBrandVue class="tech-icon" :size="20" />
          <IconBrandTypescript class="tech-icon" :size="20" />
          <IconCode class="tech-icon" :size="20" />
        </div>
        <p>Built with Vue 3, TypeScript, and Tailwind CSS</p>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { 
  IconPuzzle, 
  IconCalculator, 
  IconCheck, 
  IconPlayerPlay, 
  IconMath,
  IconBrandVue,
  IconBrandTypescript,
  IconCode
} from '@tabler/icons-vue'
</script>

<style scoped>
/* Exciting Professional Theme */
.home-page {
  min-height: 100vh;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  position: relative;
  overflow-x: hidden;
}

.home-page::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: 
    radial-gradient(circle at 20% 80%, rgba(120, 119, 198, 0.3) 0%, transparent 50%),
    radial-gradient(circle at 80% 20%, rgba(255, 119, 198, 0.15) 0%, transparent 50%),
    radial-gradient(circle at 40% 40%, rgba(120, 219, 255, 0.1) 0%, transparent 50%);
  pointer-events: none;
}

/* Hero Section */
.hero-section {
  text-align: center;
  padding: 4rem 2rem 2rem;
  position: relative;
  z-index: 1;
}

.hero-content {
  max-width: 800px;
  margin: 0 auto;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.5rem 1rem;
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 50px;
  color: white;
  font-size: 0.875rem;
  font-weight: 500;
  margin-bottom: 2rem;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

.badge-dot {
  width: 8px;
  height: 8px;
  background: #10b981;
  border-radius: 50%;
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.5; }
}

.hero-section h1 {
  font-size: clamp(2.5rem, 5vw, 4rem);
  font-weight: 800;
  background: linear-gradient(135deg, #ffffff 0%, #f0f9ff 50%, #e0e7ff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 1rem;
  line-height: 1.1;
}

.hero-section p {
  font-size: 1.25rem;
  color: rgba(255, 255, 255, 0.9);
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

/* Applications Showcase */
.applications-showcase {
  padding: 3rem 2rem;
  position: relative;
  z-index: 1;
}

.applications-showcase h2 {
  font-size: 2.5rem;
  font-weight: 700;
  text-align: center;
  margin-bottom: 3rem;
  color: white;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.app-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}

/* Enhanced App Cards */
.app-card {
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 20px;
  padding: 2rem;
  box-shadow: 
    0 20px 25px -5px rgba(0, 0, 0, 0.1),
    0 10px 10px -5px rgba(0, 0, 0, 0.04);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.app-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  transition: all 0.3s ease;
}

.mastermind-card::before {
  background: linear-gradient(90deg, #667eea 0%, #764ba2 100%);
}

.calculator-card::before {
  background: linear-gradient(90deg, #f093fb 0%, #f5576c 100%);
}

.app-card:hover {
  transform: translateY(-8px);
  box-shadow: 
    0 25px 50px -12px rgba(0, 0, 0, 0.15),
    0 20px 25px -5px rgba(0, 0, 0, 0.1);
}

/* Card Headers */
.card-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.app-icon {
  width: 48px;
  height: 48px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.mastermind-icon {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.calculator-icon {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}

.app-preview h3 {
  font-size: 1.5rem;
  font-weight: 700;
  color: #1f2937;
  margin: 0;
}

.preview-content {
  margin-bottom: 2rem;
}

.preview-content p {
  color: #6b7280;
  margin-top: 1rem;
  line-height: 1.6;
}

/* Enhanced Color Dots */
.color-dots {
  display: flex;
  gap: 0.75rem;
  margin-bottom: 1rem;
}

.dot {
  width: 2.5rem;
  height: 2.5rem;
  border-radius: 50%;
  border: 3px solid #ffffff;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  transition: transform 0.2s ease;
}

.dot:hover {
  transform: scale(1.1);
}

.dot.red { background: linear-gradient(135deg, #ef4444 0%, #dc2626 100%); }
.dot.blue { background: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%); }
.dot.green { background: linear-gradient(135deg, #10b981 0%, #059669 100%); }
.dot.yellow { background: linear-gradient(135deg, #f59e0b 0%, #d97706 100%); }

/* Enhanced Math Example */
.math-example {
  font-family: 'JetBrains Mono', 'Fira Code', monospace;
  background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
  padding: 1.5rem;
  border-radius: 12px;
  margin-bottom: 1rem;
  border: 1px solid #e2e8f0;
  box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.04);
}

.expression {
  font-size: 1.125rem;
  margin-bottom: 0.75rem;
  color: #1f2937;
  font-weight: 500;
}

.expression:last-child {
  margin-bottom: 0;
}

/* Enhanced Features List */
.features {
  list-style: none;
  padding: 0;
  margin-bottom: 2rem;
  space-y: 0.75rem;
}

.features li {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.75rem 0;
  color: #374151;
  font-weight: 500;
  border-bottom: 1px solid #f3f4f6;
}

.features li:last-child {
  border-bottom: none;
}

.features li svg {
  color: #10b981;
  flex-shrink: 0;
}

/* Enhanced Action Buttons */
.play-button {
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  padding: 1rem 2rem;
  border-radius: 12px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  position: relative;
  overflow: hidden;
}

.primary-btn {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
}

.secondary-btn {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
  color: white;
}

.play-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
}

.play-button:active {
  transform: translateY(0);
}

/* Enhanced Footer */
.page-footer {
  text-align: center;
  padding: 3rem 2rem 2rem;
  position: relative;
  z-index: 1;
}

.footer-content {
  max-width: 600px;
  margin: 0 auto;
}

.tech-stack {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-bottom: 1rem;
}

.tech-icon {
  color: rgba(255, 255, 255, 0.8);
  transition: all 0.3s ease;
}

.tech-icon:hover {
  color: white;
  transform: scale(1.2);
}

.page-footer p {
  color: rgba(255, 255, 255, 0.8);
  font-size: 1rem;
  margin: 0;
}

/* Responsive Design */
@media (max-width: 768px) {
  .app-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
  
  .app-card {
    padding: 1.5rem;
  }
  
  .hero-section {
    padding: 3rem 1rem 1rem;
  }
  
  .applications-showcase {
    padding: 2rem 1rem;
  }
}

@media (max-width: 480px) {
  .color-dots {
    gap: 0.5rem;
  }
  
  .dot {
    width: 2rem;
    height: 2rem;
  }
  
  .card-header {
    flex-direction: column;
    align-items: flex-start;
    gap: 0.75rem;
  }
  
  .play-button {
    width: 100%;
    justify-content: center;
    padding: 1rem;
  }
}
</style>