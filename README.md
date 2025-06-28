<div align="center">

<!-- Animated Header with Marvel Theme -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=Welcome%20to%20My%20Digital%20Realm&fontSize=35&fontColor=fff&animation=twinkling&fontAlignY=35" />

</div>

<!-- Advanced CSS Styles with Animations -->
<style>
/* Main Theme Variables */
:root {
  --marvel-red: #e62429;
  --marvel-blue: #518cca;
  --tolkien-green: #228b22;
  --tolkien-gold: #ffd700;
  --gaming-purple: #6441a4;
  --gaming-cyan: #00ffff;
  --text-glow: 0 0 10px rgba(255, 255, 255, 0.8);
  --neon-blue: #00f3ff;
  --neon-pink: #ff006e;
  --neon-green: #39ff14;
}

/* Advanced Particle Background Animation */
.particle-container {
  position: relative;
  overflow: hidden;
}

.particle-container::before,
.particle-container::after {
  content: '';
  position: absolute;
  width: 4px;
  height: 4px;
  background: var(--neon-blue);
  border-radius: 50%;
  animation: float 6s ease-in-out infinite;
  box-shadow: 0 0 10px var(--neon-blue);
}

.particle-container::before {
  top: 20%;
  left: 20%;
  animation-delay: -2s;
}

.particle-container::after {
  top: 60%;
  right: 20%;
  animation-delay: -4s;
  background: var(--neon-pink);
  box-shadow: 0 0 10px var(--neon-pink);
}

@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(0deg); opacity: 1; }
  25% { transform: translateY(-20px) rotate(90deg); opacity: 0.8; }
  50% { transform: translateY(-40px) rotate(180deg); opacity: 0.6; }
  75% { transform: translateY(-20px) rotate(270deg); opacity: 0.8; }
}

/* Morphing Hero Container */
.hero-container {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border-radius: 20px;
  padding: 30px;
  margin: 20px 0;
  position: relative;
  overflow: hidden;
  animation: morphing 8s ease-in-out infinite;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}

@keyframes morphing {
  0%, 100% { 
    border-radius: 20px;
    transform: scale(1);
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  }
  25% { 
    border-radius: 40px 20px;
    transform: scale(1.02);
    background: linear-gradient(135deg, #764ba2 0%, #667eea 100%);
  }
  50% { 
    border-radius: 20px 40px;
    transform: scale(0.98);
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  }
  75% { 
    border-radius: 40px;
    transform: scale(1.01);
    background: linear-gradient(135deg, #764ba2 0%, #667eea 100%);
  }
}

/* Advanced Marvel Section with Energy Effects */
.marvel-section {
  background: linear-gradient(45deg, var(--marvel-red), var(--marvel-blue));
  border-radius: 15px;
  padding: 25px;
  margin: 20px 0;
  color: white;
  position: relative;
  overflow: hidden;
  animation: energyPulse 4s ease-in-out infinite;
}

.marvel-section::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: conic-gradient(from 0deg, transparent, rgba(255,255,255,0.3), transparent);
  animation: rotate 4s linear infinite;
}

.marvel-section::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(45deg, transparent, rgba(255,255,255,0.1), transparent);
  animation: energyWave 3s ease-in-out infinite;
}

@keyframes rotate {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

@keyframes energyPulse {
  0%, 100% { box-shadow: 0 0 20px rgba(230, 36, 41, 0.5); }
  50% { box-shadow: 0 0 40px rgba(81, 140, 202, 0.8), 0 0 60px rgba(230, 36, 41, 0.3); }
}

@keyframes energyWave {
  0% { transform: translateX(-100%) skewX(-15deg); opacity: 0; }
  50% { opacity: 1; }
  100% { transform: translateX(100%) skewX(-15deg); opacity: 0; }
}

/* Interactive 3D Flip Cards */
.flip-card {
  background-color: transparent;
  perspective: 1000px;
  height: 200px;
  margin: 20px 0;
}

.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  border-radius: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  box-sizing: border-box;
}

.flip-card-front {
  background: linear-gradient(135deg, var(--tolkien-green), var(--tolkien-gold));
  color: #2c3e50;
}

.flip-card-back {
  background: linear-gradient(135deg, var(--gaming-purple), var(--gaming-cyan));
  color: white;
  transform: rotateY(180deg);
}

/* Advanced Skill Bars with Liquid Animation */
.skill-container {
  position: relative;
  margin: 15px 0;
  height: 40px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 25px;
  overflow: hidden;
  box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.2);
}

.skill-liquid {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  border-radius: 25px;
  display: flex;
  align-items: center;
  padding: 0 15px;
  font-weight: bold;
  color: white;
  overflow: hidden;
  animation: liquidFill 3s ease-out forwards;
}

.skill-liquid::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
  animation: liquidWave 2s ease-in-out infinite;
}

.skill-liquid::after {
  content: '';
  position: absolute;
  top: -50%;
  left: 0;
  width: 200%;
  height: 200%;
  background: radial-gradient(ellipse at center, rgba(255,255,255,0.2) 0%, transparent 70%);
  animation: bubble 4s ease-in-out infinite;
}

@keyframes liquidFill {
  from { width: 0; }
}

@keyframes liquidWave {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(200%); }
}

@keyframes bubble {
  0%, 100% { transform: scale(1) rotate(0deg); opacity: 0.3; }
  50% { transform: scale(1.2) rotate(180deg); opacity: 0.6; }
}

/* Floating Action Buttons */
.floating-icons {
  position: fixed;
  right: 20px;
  top: 50%;
  transform: translateY(-50%);
  z-index: 1000;
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.floating-icon {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  text-decoration: none;
  font-size: 20px;
  transition: all 0.3s ease;
  animation: floatUpDown 3s ease-in-out infinite;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
}

.floating-icon:nth-child(1) {
  background: linear-gradient(135deg, #0077b5, #00a0dc);
  animation-delay: 0s;
}

.floating-icon:nth-child(2) {
  background: linear-gradient(135deg, #20beff, #1ca0f7);
  animation-delay: -1s;
}

.floating-icon:nth-child(3) {
  background: linear-gradient(135deg, #ea4335, #fbbc04);
  animation-delay: -2s;
}

.floating-icon:hover {
  transform: scale(1.2) rotate(360deg);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
}

@keyframes floatUpDown {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

/* Interactive Timeline */
.timeline {
  position: relative;
  padding: 20px 0;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 4px;
  background: linear-gradient(to bottom, var(--neon-blue), var(--neon-pink), var(--neon-green));
  animation: timelineGlow 3s ease-in-out infinite alternate;
}

@keyframes timelineGlow {
  from { box-shadow: 0 0 5px var(--neon-blue); }
  to { box-shadow: 0 0 20px var(--neon-pink), 0 0 30px var(--neon-blue); }
}

.timeline-item {
  position: relative;
  margin: 30px 0;
  animation: slideInFromLeft 1s ease-out forwards;
  opacity: 0;
}

.timeline-item:nth-child(even) {
  animation: slideInFromRight 1s ease-out forwards;
}

.timeline-item:nth-child(1) { animation-delay: 0.2s; }
.timeline-item:nth-child(2) { animation-delay: 0.4s; }
.timeline-item:nth-child(3) { animation-delay: 0.6s; }

@keyframes slideInFromLeft {
  from { transform: translateX(-100px); opacity: 0; }
  to { transform: translateX(0); opacity: 1; }
}

@keyframes slideInFromRight {
  from { transform: translateX(100px); opacity: 0; }
  to { transform: translateX(0); opacity: 1; }
}

/* Holographic Text Effect */
.holographic {
  background: linear-gradient(45deg, #ff006e, #8338ec, #3a86ff, #06ffa5, #ffbe0b);
  background-size: 400% 400%;
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: holographicShift 4s ease-in-out infinite;
  font-weight: bold;
}

@keyframes holographicShift {
  0%, 100% { background-position: 0% 50%; }
  25% { background-position: 100% 50%; }
  50% { background-position: 100% 100%; }
  75% { background-position: 0% 100%; }
}

/* Matrix Rain Effect */
.matrix-bg {
  position: relative;
  overflow: hidden;
}

.matrix-bg::before {
  content: '01001001 01001100 01001111 01010110 01000101 01000001 01001001';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  font-family: 'Courier New', monospace;
  font-size: 12px;
  color: rgba(0, 255, 0, 0.1);
  white-space: pre-wrap;
  animation: matrixRain 10s linear infinite;
  pointer-events: none;
}

@keyframes matrixRain {
  0% { transform: translateY(-100%); }
  100% { transform: translateY(100%); }
}

/* Interactive Hover Cards with Magnetic Effect */
.magnetic-card {
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  cursor: pointer;
  position: relative;
}

.magnetic-card:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 
    0 20px 40px rgba(0, 0, 0, 0.2),
    0 0 20px rgba(255, 255, 255, 0.1);
}

.magnetic-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.magnetic-card:hover::before {
  opacity: 1;
  animation: magneticSweep 0.6s ease-out;
}

@keyframes magneticSweep {
  0% { transform: translateX(-100%) rotate(45deg); }
  100% { transform: translateX(100%) rotate(45deg); }
}

/* Pulsating Orbs */
.orb {
  position: absolute;
  border-radius: 50%;
  animation: orbPulse 4s ease-in-out infinite;
}

.orb-1 {
  width: 20px;
  height: 20px;
  background: radial-gradient(circle, var(--neon-blue), transparent);
  top: 10%;
  left: 10%;
  animation-delay: 0s;
}

.orb-2 {
  width: 15px;
  height: 15px;
  background: radial-gradient(circle, var(--neon-pink), transparent);
  top: 70%;
  right: 15%;
  animation-delay: -2s;
}

.orb-3 {
  width: 25px;
  height: 25px;
  background: radial-gradient(circle, var(--neon-green), transparent);
  bottom: 20%;
  left: 60%;
  animation-delay: -1s;
}

@keyframes orbPulse {
  0%, 100% { 
    transform: scale(1);
    opacity: 0.6;
    box-shadow: 0 0 10px currentColor;
  }
  50% { 
    transform: scale(1.5);
    opacity: 1;
    box-shadow: 0 0 30px currentColor;
  }
}

/* Responsive Design */
@media (max-width: 768px) {
  .floating-icons {
    position: relative;
    right: auto;
    top: auto;
    transform: none;
    flex-direction: row;
    justify-content: center;
    margin: 20px 0;
  }
  
  .timeline::before {
    left: 20px;
  }
  
  .hero-container, .marvel-section, .tolkien-section, .gaming-section {
    margin: 10px 5px;
    padding: 15px;
  }
}

/* Accessibility */
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
</style>

<!-- Floating Action Buttons -->
<div class="floating-icons">
  <a href="https://linkedin.com/in/yourprofile" class="floating-icon" target="_blank" aria-label="LinkedIn Profile">
    💼
  </a>
  <a href="https://kaggle.com/yourprofile" class="floating-icon" target="_blank" aria-label="Kaggle Profile">
    🏆
  </a>
  <a href="mailto:your.email@example.com" class="floating-icon" aria-label="Send Email">
    📧
  </a>
</div>

<!-- Hero Section with Advanced Animations -->
<div class="hero-container particle-container">
  <div class="orb orb-1"></div>
  <div class="orb orb-2"></div>
  <div class="orb orb-3"></div>
  
  <h1 align="center" class="holographic">
    🩺 Dr. [Your Name] 🤖
  </h1>
  <h3 align="center">
    <em>"With great power comes great responsibility"</em> - Applying AI to heal the world 🌍
  </h3>
  
  <p align="center">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=FFD700&center=true&vCenter=true&multiline=true&width=600&height=100&lines=Doctor+%7C+AI+Researcher+%7C+Healthcare+Innovator;From+Stethoscope+to+Algorithms;One+does+not+simply+debug+medical+AI..." alt="Typing SVG" />
  </p>
</div>

<!-- Interactive 3D Flip Card About Section -->
<div class="flip-card magnetic-card">
  <div class="flip-card-inner">
    <div class="flip-card-front">
      <div>
        <h2>🦸‍♀️ Origin Story</h2>
        <p><strong>Hover to reveal the secret!</strong></p>
      </div>
    </div>
    <div class="flip-card-back">
      <div>
        <h3>🚀 The Real Story</h3>
        <p>Like Tony Stark combining arc reactor technology with his genius intellect, I'm fusing my medical expertise with AI superpowers! A 27-year-old physician from Algeria 🇩🇿, revolutionizing healthcare through AI!</p>
      </div>
    </div>
  </div>
</div>

<!-- Animated Timeline Education Section -->
<div class="tolkien-section magnetic-card matrix-bg">
  <h2 class="holographic">📚 The Fellowship of Learning</h2>
  <blockquote>
    <em>"All we have to decide is what to do with the time that is given us."</em> - Gandalf
  </blockquote>
  
  <div class="timeline">
    <div class="timeline-item">
      <h3>🏰 The Halls of Healing</h3>
      <ul>
        <li><strong>🎓 Doctor of Medicine (MD)</strong> - University of Algiers (2022)</li>
        <li><em>Where my journey as a healer began...</em></li>
      </ul>
    </div>
    
    <div class="timeline-item">
      <h3>🧙‍♀️ The Path of the Code Wizard</h3>
      <ul>
        <li><strong>⚡ CS50's Introduction to Programming with Python</strong> - Harvard University</li>
        <li><strong>🗄️ CS50's Introduction to Databases with SQL</strong> - Harvard University</li>
        <li><strong>🤖 Machine Learning Specialization</strong> - Andrew Ng, Coursera</li>
      </ul>
    </div>
  </div>
</div>

<!-- Advanced Marvel Skills Section -->
<div class="marvel-section magnetic-card">
  <h2 class="holographic">💪 Superpowers & Abilities</h2>
  
  <h3>🐍 Primary Weapon: Python</h3>
  <div class="skill-container">
    <div class="skill-liquid" style="width: 85%; background: linear-gradient(90deg, #ff6b6b, #ee5a24);">
      Python - Advanced
    </div>
  </div>
  
  <h3>🗄️ Database Mastery: SQL</h3>
  <div class="skill-container">
    <div class="skill-liquid" style="width: 75%; background: linear-gradient(90deg, #4834d4, #686de0);">
      SQL - Proficient
    </div>
  </div>
  
  <h3>🧠 AI Arsenal</h3>
  <div class="skill-container">
    <div class="skill-liquid" style="width: 80%; background: linear-gradient(90deg, #00d2d3, #54a0ff);">
      Machine Learning - Advanced
    </div>
  </div>
  
  <div class="skill-container">
    <div class="skill-liquid" style="width: 70%; background: linear-gradient(90deg, #5f27cd, #a55eea);">
      MONAI Framework - Intermediate
    </div>
  </div>
  
  <div class="skill-container">
    <div class="skill-liquid" style="width: 65%; background: linear-gradient(90deg, #ff9ff3, #f368e0);">
      MedSAM - Learning
    </div>
  </div>
  
  <h3>🏆 Battle Platforms</h3>
  <p>
    🏅 <strong>Kaggle:</strong> Competing in data science battles<br>
    🐙 <strong>GitHub:</strong> Building and sharing my arsenal<br>
    🔬 <strong>Medical Imaging:</strong> Annotation warrior and CNN architect
  </p>
</div>

<!-- Gaming Section with Particle Effects -->
<div class="gaming-section magnetic-card particle-container">
  <h2 class="holographic">🎮 Current Quests & Side Missions</h2>
  
  <h3>🎯 Main Questline</h3>
  <ul>
    <li><strong>🏥 Medical Imaging AI</strong> - Developing diagnostic superpowers</li>
    <li><strong>🔪 Surgical AI</strong> - Precision-guided healing magic</li>
    <li><strong>👁️ Computer Vision in Radiology</strong> - X-ray vision for doctors</li>
  </ul>
  
  <h3>⚔️ Current Boss Battles</h3>
  <ul>
    <li>🧠 Building CNN architectures for medical classification</li>
    <li>🎯 Mastering MONAI workflows for medical imaging</li>
    <li>🔬 Implementing MedSAM for medical segmentation</li>
    <li>📊 Contributing to open-source medical AI projects</li>
  </ul>
  
  <div align="center">
    <img src="https://github-readme-stats.vercel.app/api?username=yourusername&show_icons=true&theme=radical&title_color=ff6b6b&icon_color=00d2d3&text_color=ffffff&bg_color=0d1117" alt="GitHub Stats" />
  </div>
</div>

<!-- Interactive Connect Section -->
<div align="center" class="magnetic-card" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); border-radius: 15px; padding: 20px; margin: 20px 0; position: relative; overflow: hidden;">
  <div class="orb orb-1"></div>
  <div class="orb orb-2"></div>
  
  <h2 style="color: white;" class="holographic">🌐 Assemble Your Team!</h2>
  <p style="color: white;"><em>Looking for fellow heroes to join the quest of revolutionizing healthcare through AI!</em></p>
  
  <div>
    <a href="https://linkedin.com/in/yourprofile" target="_blank">
      <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" class="magnetic-card" />
    </a>
    <a href="https://kaggle.com/yourprofile" target="_blank">
      <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle" class="magnetic-card" />
    </a>
    <a href="mailto:your.email@example.com">
      <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" class="magnetic-card" />
    </a>
  </div>
</div>

<!-- Fun Facts with Advanced Animations -->
<div align="center" class="magnetic-card particle-container" style="background: linear-gradient(45deg, #ff6b6b, #ee5a24); border-radius: 15px; padding: 20px; margin: 20px 0; color: white; position: relative; overflow: hidden;">
  <div class="orb orb-3"></div>
  
  <h2 class="holographic">🎲 Easter Eggs & Fun Facts</h2>
  <ul style="list-style: none; padding: 0;">
    <li>🇩🇿 <strong>Proudly Algerian</strong> - Representing North Africa in the global AI community!</li>
    <li>⚡ <strong>From Stethoscope to Algorithms</strong> - Because debugging code is like diagnosing patients!</li>
    <li>🎬 <strong>Marvel Fan</strong> - Believes AI can be as revolutionary as the arc reactor</li>
    <li>📚 <strong>Tolkien Enthusiast</strong> - Every coding journey is an epic adventure</li>
    <li>🎮 <strong>Gamer at Heart</strong> - Treating real-world problems like boss battles to conquer</li>
  </ul>
</div>

<!-- Inspirational Quote with Holographic Effect -->
<div align="center" class="magnetic-card" style="background: rgba(0,0,0,0.8); border-radius: 15px; padding: 20px; margin: 20px 0; color: #ffd700; border: 2px solid #ffd700; position: relative; overflow: hidden;">
  <div class="orb orb-1"></div>
  <div class="orb orb-2"></div>
  
  <h3 class="holographic">💫 Words to Live By</h3>
  <blockquote style="font-size: 18px; font-style: italic;">
    "I am Iron Man... but with a medical degree and a passion for saving lives through AI!"
  </blockquote>
  <p><em>- Dr. [Your Name], Healthcare AI Avenger</em></p>
</div>

<!-- Activity Graph -->
<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=yourusername&theme=react-dark&hide_border=true&area=true" alt="GitHub Activity Graph" class="magnetic-card" />
</div>

<!-- Footer -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer" />
  
  <p>
    <img src="https://komarev.com/ghpvc/?username=yourusername&label=Profile%20views&color=0e75b6&style=flat" alt="Profile Views" class="magnetic-card" />
  </p>
  
  <p class="holographic"><em>⚡ "With great code comes great responsibility!" ⚡</em></p>
</div>

<!-- Hidden Message for Fellow Geeks -->
<!--
🎊 CONGRATULATIONS! 🎊 
You found the secret message! 
You're clearly a fellow code archaeologist!
May the Force be with you, and may your deployments be ever successful!
- Dr. [Your Name] 🤓

P.S. - If you made it this far, you deserve a cookie 🍪
-->

<!-- JavaScript for Enhanced Interactivity -->
<script>
// Add mouse tracking for magnetic effect (if supported)
document.addEventListener('mousemove', (e) => {
  const cards = document.querySelectorAll('.magnetic-card');
  cards.forEach(card => {
    const rect = card.getBoundingClientRect();
    const x = e.clientX - rect.left - rect.width / 2;
    const y = e.clientY - rect.top - rect.height / 2;
    
    if (Math.abs(x) < 100 && Math.abs(y) < 100) {
      card.style.transform = `translate(\${x * 0.1}px, \${y * 0.1}px) scale(1.02)`;
    } else {
      card.style.transform = 'translate(0px, 0px) scale(1)';
    }
  });
});

// Intersection Observer for timeline animations
const observerOptions = {
  threshold: 0.1,
  rootMargin: '0px 0px -50px 0px'
};

const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.style.animationPlayState = 'running';
    }
  });
}, observerOptions);

document.querySelectorAll('.timeline-item').forEach(item => {
  observer.observe(item);
});
</script>
```
```


