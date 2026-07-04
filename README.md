<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Shabeen Begum S | Cybersecurity Portfolio</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #0a0e1a;
      color: #e0e0e0;
    }

    /* NAV */
    nav {
      position: fixed;
      top: 0; width: 100%;
      background: rgba(10,14,26,0.95);
      padding: 16px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #1e3a5f;
      z-index: 1000;
    }
    .logo {
      font-size: 20px;
      font-weight: 700;
      color: #00d4ff;
    }
    .nav-links a {
      color: #a0b4c8;
      text-decoration: none;
      margin-left: 24px;
      font-size: 14px;
      transition: color 0.3s;
    }
    .nav-links a:hover { color: #00d4ff; }

    /* HERO */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 100px 20px 60px;
      background: linear-gradient(135deg, #0a0e1a 0%, #0d1b2e 50%, #0a1628 100%);
    }
    .hero-badge {
      display: inline-block;
      background: rgba(0,212,255,0.1);
      border: 1px solid #00d4ff;
      color: #00d4ff;
      padding: 6px 16px;
      border-radius: 20px;
      font-size: 13px;
      margin-bottom: 20px;
    }
    .hero h1 {
      font-size: 52px;
      font-weight: 700;
      color: #ffffff;
      margin-bottom: 12px;
    }
    .hero h1 span { color: #00d4ff; }
    .hero p {
      font-size: 18px;
      color: #a0b4c8;
      max-width: 600px;
      margin: 0 auto 32px;
      line-height: 1.7;
    }
    .hero-buttons {
      display: flex;
      gap: 16px;
      justify-content: center;
      flex-wrap: wrap;
    }
    .btn-primary {
      background: #00d4ff;
      color: #0a0e1a;
      padding: 12px 28px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: 600;
      font-size: 15px;
      transition: all 0.3s;
    }
    .btn-primary:hover {
      background: #00b8d9;
      transform: translateY(-2px);
    }
    .btn-secondary {
      border: 1px solid #00d4ff;
      color: #00d4ff;
      padding: 12px 28px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: 600;
      font-size: 15px;
      transition: all 0.3s;
    }
    .btn-secondary:hover {
      background: rgba(0,212,255,0.1);
      transform: translateY(-2px);
    }
    .status-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(0,255,136,0.1);
      border: 1px solid #00ff88;
      color: #00ff88;
      padding: 8px 20px;
      border-radius: 20px;
      font-size: 13px;
      margin-top: 32px;
    }
    .status-dot {
      width: 8px; height: 8px;
      background: #00ff88;
      border-radius: 50%;
      animation: pulse 2s infinite;
    }
    @keyframes pulse {
      0%,100% { opacity: 1; }
      50% { opacity: 0.3; }
    }

    /* SECTIONS */
    section {
      padding: 80px 40px;
      max-width: 1100px;
      margin: 0 auto;
    }
    .section-title {
      font-size: 32px;
      font-weight: 700;
      color: #ffffff;
      margin-bottom: 8px;
    }
    .section-title span { color: #00d4ff; }
    .section-subtitle {
      color: #a0b4c8;
      font-size: 15px;
      margin-bottom: 48px;
    }
    .divider {
      width: 60px; height: 3px;
      background: #00d4ff;
      margin: 12px 0 40px;
      border-radius: 2px;
    }

    /* ABOUT */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 48px;
      align-items: start;
    }
    .about-text p {
      color: #a0b4c8;
      line-height: 1.8;
      margin-bottom: 16px;
    }
    .about-info {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .info-item {
      display: flex;
      gap: 12px;
      padding: 12px 16px;
      background: rgba(255,255,255,0.03);
      border: 1px solid #1e3a5f;
      border-radius: 8px;
    }
    .info-label {
      color: #00d4ff;
      font-size: 13px;
      min-width: 100px;
      font-weight: 600;
    }
    .info-value {
      color: #e0e0e0;
      font-size: 13px;
    }

    /* SKILLS */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 24px;
    }
    .skill-card {
      background: rgba(255,255,255,0.03);
      border: 1px solid #1e3a5f;
      border-radius: 12px;
      padding: 24px;
      transition: all 0.3s;
    }
    .skill-card:hover {
      border-color: #00d4ff;
      transform: translateY(-4px);
      background: rgba(0,212,255,0.05);
    }
    .skill-icon {
      font-size: 28px;
      margin-bottom: 12px;
    }
    .skill-card h3 {
      color: #ffffff;
      font-size: 16px;
      margin-bottom: 12px;
    }
    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
    }
    .tag {
      background: rgba(0,212,255,0.1);
      border: 1px solid rgba(0,212,255,0.3);
      color: #00d4ff;
      padding: 3px 10px;
      border-radius: 12px;
      font-size: 12px;
    }

    /* PROJECTS */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 24px;
    }
    .project-card {
      background: rgba(255,255,255,0.03);
      border: 1px solid #1e3a5f;
      border-radius: 12px;
      padding: 28px;
      transition: all 0.3s;
      position: relative;
      overflow: hidden;
    }
    .project-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 3px;
      background: linear-gradient(90deg, #00d4ff, #0066ff);
    }
    .project-card:hover {
      border-color: #00d4ff;
      transform: translateY(-4px);
    }
    .project-badge {
      display: inline-block;
      background: rgba(0,255,136,0.1);
      border: 1px solid #00ff88;
      color: #00ff88;
      padding: 3px 10px;
      border-radius: 12px;
      font-size: 11px;
      margin-bottom: 16px;
    }
    .project-card h3 {
      color: #ffffff;
      font-size: 18px;
      margin-bottom: 10px;
    }
    .project-card p {
      color: #a0b4c8;
      font-size: 14px;
      line-height: 1.7;
      margin-bottom: 20px;
    }
    .project-stats {
      display: flex;
      gap: 16px;
      margin-bottom: 20px;
    }
    .stat {
      text-align: center;
    }
    .stat-number {
      font-size: 22px;
      font-weight: 700;
      color: #00d4ff;
    }
    .stat-label {
      font-size: 11px;
      color: #a0b4c8;
    }
    .project-tech {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-bottom: 20px;
    }
    .tech-tag {
      background: rgba(255,255,255,0.05);
      border: 1px solid #2a4a6b;
      color: #a0b4c8;
      padding: 3px 10px;
      border-radius: 6px;
      font-size: 12px;
    }
    .project-links {
      display: flex;
      gap: 12px;
    }
    .project-links a {
      color: #00d4ff;
      text-decoration: none;
      font-size: 13px;
      font-weight: 600;
      border: 1px solid #00d4ff;
      padding: 6px 16px;
      border-radius: 6px;
      transition: all 0.3s;
    }
    .project-links a:hover {
      background: rgba(0,212,255,0.1);
    }

    /* MITRE */
    .mitre-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 16px;
    }
    .mitre-card {
      background: rgba(255,255,255,0.03);
      border: 1px solid #1e3a5f;
      border-radius: 10px;
      padding: 20px;
      text-align: center;
      transition: all 0.3s;
    }
    .mitre-card:hover {
      border-color: #00d4ff;
      background: rgba(0,212,255,0.05);
    }
    .mitre-id {
      font-size: 18px;
      font-weight: 700;
      color: #00d4ff;
      margin-bottom: 6px;
    }
    .mitre-name {
      font-size: 13px;
      color: #ffffff;
      margin-bottom: 4px;
    }
    .mitre-tactic {
      font-size: 11px;
      color: #a0b4c8;
    }

    /* CONTACT */
    .contact-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
    }
    .contact-card {
      background: rgba(255,255,255,0.03);
      border: 1px solid #1e3a5f;
      border-radius: 12px;
      padding: 28px 20px;
      text-align: center;
      text-decoration: none;
      transition: all 0.3s;
    }
    .contact-card:hover {
      border-color: #00d4ff;
      transform: translateY(-4px);
      background: rgba(0,212,255,0.05);
    }
    .contact-icon { font-size: 32px; margin-bottom: 12px; }
    .contact-card h3 { color: #ffffff; font-size: 16px; margin-bottom: 6px; }
    .contact-card p { color: #a0b4c8; font-size: 13px; }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 40px;
      border-top: 1px solid #1e3a5f;
      color: #a0b4c8;
      font-size: 13px;
    }
    footer span { color: #00d4ff; }

    /* RESPONSIVE */
    @media (max-width: 768px) {
      .hero h1 { font-size: 36px; }
      .about-grid { grid-template-columns: 1fr; }
      nav { padding: 16px 20px; }
      section { padding: 60px 20px; }
      .nav-links a { margin-left: 12px; font-size: 13px; }
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="logo">Shabeen Shafi</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<!-- HERO -->
<div class="hero">
  <div>
    <div class="hero-badge">🛡️ Cybersecurity Fresher</div>
    <h1>Hi, I'm <span>Shabeen Begum S</span></h1>
    <p>Aspiring SOC Analyst passionate about Blue Team 
    operations, threat detection, and incident response. 
    Building real-world skills through hands-on homelabs.</p>
    <div class="hero-buttons">
      <a href="#projects" class="btn-primary">View My Projects</a>
      <a href="#contact" class="btn-secondary">Contact Me</a>
    </div>
    <div class="status-badge">
      <div class="status-dot"></div>
      Open to SOC Analyst Opportunities
    </div>
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="section-title">About <span>Me</span></div>
  <div class="divider"></div>
  <div class="about-grid">
    <div class="about-text">
      <p>I am a cybersecurity fresher with a strong passion 
      for Blue Team security operations. I built this SOC 
      homelab project from scratch to develop hands-on skills 
      in SIEM deployment, threat detection, and incident 
      investigation.</p>
      <p>Through this project I learned to deploy Wazuh SIEM, 
      configure agents on Linux and Windows, simulate real 
      attacks, investigate alerts, and map threats to the 
      MITRE ATT&CK framework — skills directly applicable 
      to SOC Analyst roles.</p>
      <p>I am actively seeking entry-level SOC Analyst or 
      Blue Team positions where I can contribute and grow 
      my cybersecurity career.</p>
    </div>
    <div class="about-info">
      <div class="info-item">
        <span class="info-label">Name</span>
        <span class="info-value">Shabeen Begum S</span>
      </div>
      <div class="info-item">
        <span class="info-label">Location</span>
        <span class="info-value">Chennai, Tamil Nadu, India</span>
      </div>
      <div class="info-item">
        <span class="info-label">Focus</span>
        <span class="info-value">Blue Team / SOC Operations</span>
      </div>
      <div class="info-item">
        <span class="info-label">SIEM</span>
        <span class="info-value">Wazuh 4.7</span>
      </div>
      <div class="info-item">
        <span class="info-label">Status</span>
        <span class="info-value">🟢 Open to Work</span>
      </div>
      <div class="info-item">
        <span class="info-label">GitHub</span>
        <span class="info-value">github.com/shabeenshafi26</span>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-title">Technical <span>Skills</span></div>
  <div class="divider"></div>
  <div class="skills-grid">
    <div class="skill-card">
      <div class="skill-icon">🛡️</div>
      <h3>SIEM & Monitoring</h3>
      <div class="skill-tags">
        <span class="tag">Wazuh 4.7</span>
        <span class="tag">OpenSearch</span>
        <span class="tag">Alert Analysis</span>
        <span class="tag">Log Management</span>
        <span class="tag">Dashboard</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">⚔️</div>
      <h3>Attack Simulation</h3>
      <div class="skill-tags">
        <span class="tag">Hydra</span>
        <span class="tag">Nmap</span>
        <span class="tag">Netcat</span>
        <span class="tag">Brute Force</span>
        <span class="tag">Port Scanning</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🐧</div>
      <h3>Linux</h3>
      <div class="skill-tags">
        <span class="tag">Ubuntu 22.04</span>
        <span class="tag">Bash</span>
        <span class="tag">systemctl</span>
        <span class="tag">File System</span>
        <span class="tag">SSH</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🪟</div>
      <h3>Windows</h3>
      <div class="skill-tags">
        <span class="tag">Windows 10</span>
        <span class="tag">PowerShell</span>
        <span class="tag">Event Logs</span>
        <span class="tag">Event ID 4625</span>
        <span class="tag">Services</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🌐</div>
      <h3>Networking</h3>
      <div class="skill-tags">
        <span class="tag">TCP/IP</span>
        <span class="tag">Ports/Protocols</span>
        <span class="tag">Host-Only Network</span>
        <span class="tag">VirtualBox</span>
        <span class="tag">Subnetting</span>
      </div>
    </div>
    <div class="skill-card">
      <div class="skill-icon">🎯</div>
      <h3>Frameworks</h3>
      <div class="skill-tags">
        <span class="tag">MITRE ATT&CK</span>
        <span class="tag">T1046</span>
        <span class="tag">T1078</span>
        <span class="tag">T1110</span>
        <span class="tag">T1565</span>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-title">Featured <span>Projects</span></div>
  <div class="divider"></div>
  <div class="projects-grid">
    <div class="project-card">
      <div class="project-badge">✅ Completed</div>
      <h3>🛡️ SOC Homelab — Wazuh SIEM</h3>
      <p>Built a complete Security Operations Center homelab 
      using Wazuh 4.7 SIEM. Deployed agents on Ubuntu Desktop 
      and Windows 10, simulated real attacks, and investigated 
      alerts using the MITRE ATT&CK framework.</p>
      <div class="project-stats">
        <div class="stat">
          <div class="stat-number">2</div>
          <div class="stat-label">Agents</div>
        </div>
        <div class="stat">
          <div class="stat-number">30+</div>
          <div class="stat-label">Alerts</div>
        </div>
        <div class="stat">
          <div class="stat-number">4</div>
          <div class="stat-label">Attacks</div>
        </div>
        <div class="stat">
          <div class="stat-number">6</div>
          <div class="stat-label">MITRE TTPs</div>
        </div>
      </div>
      <div class="project-tech">
        <span class="tech-tag">Wazuh 4.7</span>
        <span class="tech-tag">Ubuntu 22.04</span>
        <span class="tech-tag">Windows 10</span>
        <span class="tech-tag">VirtualBox</span>
        <span class="tech-tag">Nmap</span>
        <span class="tech-tag">Hydra</span>
        <span class="tech-tag">MITRE ATT&CK</span>
      </div>
      <div class="project-links">
        <a href="https://github.com/shabeenshafi26/SOC-Homelab--Wazuh-SIEM" target="_blank">GitHub Repo</a>
        <a href="https://linkedin.com/in/yourprofile" target="_blank">LinkedIn Post</a>
      </div>
    </div>

    <div class="project-card">
      <div class="project-badge" style="border-color:#ffaa00;color:#ffaa00;background:rgba(255,170,0,0.1)">🔄 Coming Soon</div>
      <h3>🔍 Network Traffic Analysis</h3>
      <p>Upcoming project — analyzing network packets using 
      Wireshark to detect suspicious traffic patterns and 
      investigate potential network intrusions.</p>
      <div class="project-tech">
        <span class="tech-tag">Wireshark</span>
        <span class="tech-tag">tcpdump</span>
        <span class="tech-tag">Network Analysis</span>
      </div>
      <div class="project-links">
        <a href="#" style="opacity:0.5;cursor:not-allowed">Coming Soon</a>
      </div>
    </div>
  </div>
</section>

<!-- MITRE -->
<section>
  <div class="section-title">MITRE ATT&CK <span>Coverage</span></div>
  <div class="divider"></div>
  <p style="color:#a0b4c8;margin-bottom:32px;font-size:14px">
  Techniques detected and investigated in the SOC Homelab project:
  </p>
  <div class="mitre-grid">
    <div class="mitre-card">
      <div class="mitre-id">T1046</div>
      <div class="mitre-name">Network Service Scanning</div>
      <div class="mitre-tactic">Reconnaissance</div>
    </div>
    <div class="mitre-card">
      <div class="mitre-id">T1110</div>
      <div class="mitre-name">Brute Force</div>
      <div class="mitre-tactic">Credential Access</div>
    </div>
    <div class="mitre-card">
      <div class="mitre-id">T1078</div>
      <div class="mitre-name">Valid Accounts</div>
      <div class="mitre-tactic">Initial Access</div>
    </div>
    <div class="mitre-card">
      <div class="mitre-id">T1565</div>
      <div class="mitre-name">Data Manipulation</div>
      <div class="mitre-tactic">Impact</div>
    </div>
    <div class="mitre-card">
      <div class="mitre-id">T1543</div>
      <div class="mitre-name">Create/Modify System Process</div>
      <div class="mitre-tactic">Persistence</div>
    </div>
    <div class="mitre-card">
      <div class="mitre-id">T1059</div>
      <div class="mitre-name">Command and Scripting</div>
      <div class="mitre-tactic">Execution</div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-title">Contact <span>Me</span></div>
  <div class="divider"></div>
  <p style="color:#a0b4c8;margin-bottom:32px;font-size:15px">
  I am actively looking for entry-level SOC Analyst opportunities. 
  Feel free to reach out!
  </p>
  <div class="contact-grid">
    <a href="https://linkedin.com/in/yourprofile" 
       target="_blank" class="contact-card">
      <div class="contact-icon">💼</div>
      <h3>LinkedIn</h3>
      <p>Connect with me</p>
    </a>
    <a href="https://github.com/shabeenshafi26" 
       target="_blank" class="contact-card">
      <div class="contact-icon">🐙</div>
      <h3>GitHub</h3>
      <p>View my projects</p>
    </a>
    <a href="mailto:youremail@gmail.com" class="contact-card">
      <div class="contact-icon">📧</div>
      <h3>Email</h3>
      <p>youremail@gmail.com</p>
    </a>
    <a href="https://github.com/shabeenshafi26/SOC-Homelab--Wazuh-SIEM" 
       target="_blank" class="contact-card">
      <div class="contact-icon">🛡️</div>
      <h3>SOC Project</h3>
      <p>View on GitHub</p>
    </a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>Built by <span>Shabeen Shafi</span> — 
  Cybersecurity Fresher | Aspiring SOC Analyst</p>
  <p style="margin-top:8px">
  🛡️ Open to SOC Analyst Opportunities — 
  Coimbatore, Tamil Nadu, India</p>
</footer>

</body>
</html>
