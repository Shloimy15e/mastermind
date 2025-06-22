<template>
  <div class="home-page">
    <header class="hero-section">
      <h1>My Project Showcase</h1>
      <p>Welcome to my collection of interactive web applications</p>
    </header>

    <main class="applications-showcase">
      <h2>Featured Applications</h2>
      
      <div class="app-grid">
        <!-- Mastermind Game Card -->
        <div class="app-card">
          <div class="app-preview">
            <h3>Mastermind Logic Game</h3>
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
              <li>10 attempts to crack the code</li>
              <li>6 different colors to choose from</li>
              <li>Intelligent feedback system</li>
              <li>Built with Vue 3 & TypeScript</li>
            </ul>
            
            <div class="app-actions">
              <router-link to="/mastermind" class="play-button">
                🎯 Play Mastermind
              </router-link>
            </div>
          </div>
        </div>

        <!-- Parser Calculator Card -->
        <div class="app-card">
          <div class="app-preview">
            <h3>Math Expression Parser</h3>
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
              <li>Supports complex expressions</li>
              <li>Operator precedence handling</li>
              <li>Parentheses and functions</li>
              <li>Real-time calculation</li>
            </ul>
            
            <div class="app-actions">
              <router-link to="/parser" class="play-button">
                🧮 Try Calculator
              </router-link>
            </div>
          </div>
        </div>
      </div>
    </main>

    <footer class="page-footer">
      <p>Built with Vue 3, TypeScript, and Tailwind CSS</p>
    </footer>
  </div>
</template>

<script setup lang="ts">
// Simple functional component - no complex logic needed yet
</script>

<style scoped>
/* Basic functional styling - clean and simple */
.home-page {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
  font-family: system-ui, -apple-system, sans-serif;
}

.hero-section {
  text-align: center;
  margin-bottom: 3rem;
}

.hero-section h1 {
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 1rem;
  color: #1f2937;
}

.hero-section p {
  font-size: 1.125rem;
  color: #6b7280;
}

.applications-showcase h2 {
  font-size: 2rem;
  font-weight: bold;
  text-align: center;
  margin-bottom: 2rem;
  color: #1f2937;
}

.app-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: 2rem;
  margin-bottom: 3rem;
}

.app-card {
  border: 1px solid #e5e7eb;
  border-radius: 0.5rem;
  padding: 1.5rem;
  background: white;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
}

.app-preview h3 {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 1rem;
  color: #1f2937;
}

.preview-content {
  margin-bottom: 1.5rem;
}

.preview-content p {
  color: #6b7280;
  margin-top: 1rem;
}

/* Mastermind preview */
.color-dots {
  display: flex;
  gap: 0.5rem;
  margin-bottom: 1rem;
}

.dot {
  width: 2rem;
  height: 2rem;
  border-radius: 50%;
  border: 2px solid #374151;
}

.dot.red { background-color: #ef4444; }
.dot.blue { background-color: #3b82f6; }
.dot.green { background-color: #10b981; }
.dot.yellow { background-color: #f59e0b; }

/* Parser preview */
.math-example {
  font-family: 'Courier New', monospace;
  background: #f3f4f6;
  padding: 1rem;
  border-radius: 0.25rem;
  margin-bottom: 1rem;
}

.expression {
  font-size: 1.125rem;
  margin-bottom: 0.5rem;
  color: #1f2937;
}

.expression:last-child {
  margin-bottom: 0;
}

/* App info */
.features {
  list-style: none;
  padding: 0;
  margin-bottom: 1.5rem;
}

.features li {
  padding: 0.5rem 0;
  border-bottom: 1px solid #f3f4f6;
  color: #4b5563;
}

.features li:before {
  content: "✓ ";
  color: #10b981;
  font-weight: bold;
}

.features li:last-child {
  border-bottom: none;
}

/* Action buttons */
.play-button {
  display: inline-block;
  background: #3b82f6;
  color: white;
  padding: 0.75rem 1.5rem;
  border-radius: 0.5rem;
  text-decoration: none;
  font-weight: 600;
  transition: background-color 0.2s;
}

.play-button:hover {
  background: #2563eb;
}

.page-footer {
  text-align: center;
  padding-top: 2rem;
  border-top: 1px solid #e5e7eb;
  color: #6b7280;
}

/* Dark mode support */
@media (prefers-color-scheme: dark) {
  .home-page {
    background: #111827;
    color: #f9fafb;
  }
  
  .hero-section h1,
  .applications-showcase h2,
  .app-preview h3 {
    color: #f9fafb;
  }
  
  .app-card {
    background: #1f2937;
    border-color: #374151;
  }
  
  .math-example {
    background: #374151;
  }
  
  .expression {
    color: #f9fafb;
  }
}
</style>