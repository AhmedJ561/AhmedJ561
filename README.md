<style>
  :root {
    --primary-color: #0061ff;
    --secondary-color: #1e1e1e;
    --accent-color: #00d4ff;
    --text-light: #ffffff;
    --text-dark: #333333;
    --bg-dark: #0f0f0f;
    --bg-card: #1a1a1a;
  }

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, var(--bg-dark) 0%, var(--secondary-color) 100%);
    color: var(--text-light);
    line-height: 1.6;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 40px 20px;
  }

  .header {
    text-align: center;
    margin-bottom: 60px;
    animation: fadeInDown 0.8s ease-out;
  }

  .header h1 {
    font-size: 3.5rem;
    margin-bottom: 15px;
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--accent-color) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    font-weight: 700;
  }

  .header p {
    font-size: 1.3rem;
    color: #b0b0b0;
    margin-bottom: 30px;
  }

  .social-links {
    display: flex;
    justify-content: center;
    gap: 25px;
    flex-wrap: wrap;
    margin-bottom: 40px;
  }

  .social-links a {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border: 2px solid var(--primary-color);
    border-radius: 50px;
    color: var(--primary-color);
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    font-size: 0.95rem;
  }

  .social-links a:hover {
    background: var(--primary-color);
    color: var(--text-light);
    transform: translateY(-3px);
    box-shadow: 0 10px 25px rgba(0, 97, 255, 0.3);
  }

  .about-section {
    background: var(--bg-card);
    border: 1px solid #333;
    padding: 40px;
    border-radius: 15px;
    margin-bottom: 50px;
    animation: fadeInUp 0.8s ease-out;
  }

  .section-title {
    font-size: 2rem;
    margin-bottom: 25px;
    color: var(--primary-color);
    position: relative;
    padding-bottom: 15px;
  }

  .section-title::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 60px;
    height: 3px;
    background: linear-gradient(90deg, var(--primary-color) 0%, var(--accent-color) 100%);
    border-radius: 2px;
  }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    margin-top: 30px;
  }

  .skill-card {
    background: linear-gradient(135deg, #1e1e2e 0%, #2a2a3e 100%);
    padding: 25px;
    border-radius: 12px;
    border: 1px solid #333;
    transition: all 0.3s ease;
    cursor: pointer;
  }

  .skill-card:hover {
    border-color: var(--primary-color);
    transform: translateY(-5px);
    box-shadow: 0 15px 35px rgba(0, 97, 255, 0.2);
  }

  .skill-card h3 {
    color: var(--primary-color);
    margin-bottom: 12px;
    font-size: 1.1rem;
  }

  .skill-card p {
    color: #b0b0b0;
    font-size: 0.95rem;
    line-height: 1.5;
  }

  .projects-section {
    margin-bottom: 50px;
    animation: fadeInUp 1s ease-out;
  }

  .project-card {
    background: var(--bg-card);
    border: 1px solid #333;
    border-radius: 12px;
    padding: 30px;
    margin-bottom: 25px;
    transition: all 0.3s ease;
  }

  .project-card:hover {
    border-color: var(--primary-color);
    transform: translateX(10px);
    box-shadow: 0 15px 35px rgba(0, 97, 255, 0.15);
  }

  .project-card h3 {
    color: var(--primary-color);
    margin-bottom: 12px;
    font-size: 1.4rem;
  }

  .project-card p {
    color: #b0b0b0;
    margin-bottom: 15px;
    line-height: 1.6;
  }

  .tech-stack {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    margin-top: 15px;
  }

  .tech-tag {
    display: inline-block;
    background: rgba(0, 97, 255, 0.15);
    color: var(--primary-color);
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 0.85rem;
    border: 1px solid rgba(0, 97, 255, 0.3);
  }

  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    margin-bottom: 50px;
  }

  .stat-card {
    background: var(--bg-card);
    border: 1px solid #333;
    padding: 30px;
    border-radius: 12px;
    text-align: center;
    transition: all 0.3s ease;
  }

  .stat-card:hover {
    border-color: var(--accent-color);
    transform: scale(1.05);
  }

  .stat-number {
    font-size: 2.5rem;
    color: var(--primary-color);
    font-weight: 700;
    margin-bottom: 10px;
  }

  .stat-label {
    color: #b0b0b0;
    font-size: 1rem;
  }

  .cta-button {
    display: inline-block;
    padding: 15px 40px;
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--accent-color) 100%);
    color: var(--text-light);
    text-decoration: none;
    border-radius: 50px;
    font-weight: 600;
    transition: all 0.3s ease;
    border: none;
    cursor: pointer;
    font-size: 1rem;
  }

  .cta-button:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 35px rgba(0, 97, 255, 0.4);
  }

  .contact-section {
    background: var(--bg-card);
    border: 1px solid #333;
    padding: 40px;
    border-radius: 15px;
    text-align: center;
    animation: fadeInUp 1.2s ease-out;
  }

  .contact-section h2 {
    margin-bottom: 25px;
  }

  .contact-section p {
    color: #b0b0b0;
    margin-bottom: 30px;
    font-size: 1.05rem;
  }

  @keyframes fadeInDown {
    from {
      opacity: 0;
      transform: translateY(-30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .divider {
    height: 2px;
    background: linear-gradient(90deg, transparent 0%, var(--primary-color) 50%, transparent 100%);
    margin: 60px 0;
  }

  @media (max-width: 768px) {
    .header h1 {
      font-size: 2.2rem;
    }

    .header p {
      font-size: 1rem;
    }

    .skills-grid {
      grid-template-columns: 1fr;
    }

    .stats-grid {
      grid-template-columns: 1fr;
    }

    .section-title {
      font-size: 1.5rem;
    }
  }
</style>

<div class="container">
  <div class="header">
    <h1>👋 Ahmed J</h1>
    <p>Full Stack Developer | React & TypeScript Specialist</p>
    <p style="font-size: 1rem; color: #888;">Building modern, performant web applications with cutting-edge technologies</p>
    
    <div class="social-links">
      <a href="https://github.com/AhmedJ561" target="_blank">🔗 GitHub</a>
      <a href="https://linkedin.com" target="_blank">💼 LinkedIn</a>
      <a href="mailto:your.email@example.com">📧 Email</a>
      <a href="https://twitter.com" target="_blank">𝕏 Twitter</a>
    </div>
  </div>

  <div class="stats-grid">
    <div class="stat-card">
      <div class="stat-number">4+</div>
      <div class="stat-label">Years of Experience</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">20+</div>
      <div class="stat-label">Projects Completed</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">100%</div>
      <div class="stat-label">Client Satisfaction</div>
    </div>
  </div>

  <div class="about-section">
    <h2 class="section-title">About Me</h2>
    <p>I'm a passionate full-stack developer with expertise in React, TypeScript, and modern web technologies. I specialize in creating responsive, user-friendly applications with clean, maintainable code. My focus is on building solutions that not only work well but also provide excellent user experiences.</p>
  </div>

  <div class="divider"></div>

  <div class="about-section">
    <h2 class="section-title">🛠️ Technical Skills</h2>
    <div class="skills-grid">
      <div class="skill-card">
        <h3>Frontend Development</h3>
        <p>React, TypeScript, Vite, Tailwind CSS, Framer Motion</p>
      </div>
      <div class="skill-card">
        <h3>UI/UX Design</h3>
        <p>Responsive Design, Accessibility, Component Libraries</p>
      </div>
      <div class="skill-card">
        <h3>Tools & Technologies</h3>
        <p>GitHub, VS Code, npm, ESLint, TypeScript</p>
      </div>
      <div class="skill-card">
        <h3>Web Performance</h3>
        <p>Optimization, Fast Refresh, Build Optimization</p>
      </div>
      <div class="skill-card">
        <h3>APIs & Integration</h3>
        <p>Axios, REST APIs, Asynchronous Programming</p>
      </div>
      <div class="skill-card">
        <h3>State Management</h3>
        <p>React Hooks, Context API, Component State</p>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="projects-section">
    <h2 class="section-title">📁 Featured Projects</h2>
    
    <div class="project-card">
      <h3>Portfolio v1</h3>
      <p>A modern portfolio website built with React, TypeScript, and Tailwind CSS. Features responsive design, smooth animations with Framer Motion, and optimal performance using Vite.</p>
      <div class="tech-stack">
        <span class="tech-tag">React</span>
        <span class="tech-tag">TypeScript</span>
        <span class="tech-tag">Vite</span>
        <span class="tech-tag">Tailwind CSS</span>
        <span class="tech-tag">Framer Motion</span>
      </div>
    </div>

    <div class="project-card">
      <h3>Web Applications</h3>
      <p>Building scalable and maintainable web applications with modern JavaScript frameworks, focusing on code quality and performance optimization.</p>
      <div class="tech-stack">
        <span class="tech-tag">React</span>
        <span class="tech-tag">TypeScript</span>
        <span class="tech-tag">React Router</span>
        <span class="tech-tag">Axios</span>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="about-section">
    <h2 class="section-title">📚 Currently Learning</h2>
    <div class="skills-grid">
      <div class="skill-card">
        <h3>Next.js</h3>
        <p>Server-side rendering and static generation for React applications</p>
      </div>
      <div class="skill-card">
        <h3>Backend Development</h3>
        <p>Node.js, Express, and database management</p>
      </div>
      <div class="skill-card">
        <h3>Web Performance</h3>
        <p>Advanced optimization techniques and monitoring</p>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="contact-section">
    <h2 class="section-title" style="text-align: center;">Let's Connect!</h2>
    <p>I'm always interested in new opportunities and collaborations. Feel free to reach out!</p>
    <a href="mailto:your.email@example.com" class="cta-button">Get in Touch</a>
    
    <div class="social-links" style="margin-top: 30px; justify-content: center;">
      <a href="https://github.com/AhmedJ561" target="_blank">GitHub</a>
      <a href="https://linkedin.com" target="_blank">LinkedIn</a>
      <a href="https://twitter.com" target="_blank">Twitter</a>
    </div>
  </div>
</div>