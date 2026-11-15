<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abir Al Mahdi Akhand - GitHub Intro</title>
<style>
  :root {
    --bg: #0d1117;
    --card-bg: #161b22;
    --border: #30363d;
    --text: #c9d1d9;
    --text-muted: #8b949e;
    --accent: #58a6ff;
    --accent-2: #f78166;
    --success: #3fb950;
    --radius: 12px;
    --shadow: 0 4px 16px rgba(0,0,0,0.3);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.6;
    padding: 24px;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    min-height: 100vh;
  }

  .profile-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 32px;
    max-width: 760px;
    width: 100%;
    box-shadow: var(--shadow);
  }

  /* Header */
  .header {
    display: flex;
    align-items: center;
    gap: 20px;
    margin-bottom: 28px;
    padding-bottom: 24px;
    border-bottom: 1px solid var(--border);
  }

  .avatar {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent), var(--accent-2));
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 36px;
    font-weight: 700;
    color: #fff;
    flex-shrink: 0;
    box-shadow: 0 0 0 4px rgba(88, 166, 255, 0.15);
  }

  .header-text h1 {
    font-size: 28px;
    color: #fff;
    margin-bottom: 4px;
  }

  .header-text .tagline {
    color: var(--accent);
    font-size: 15px;
    font-weight: 600;
    margin-bottom: 6px;
  }

  .header-text .status {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    color: var(--success);
    font-size: 13px;
    font-weight: 500;
  }

  .status::before {
    content: '';
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: var(--success);
    box-shadow: 0 0 8px var(--success);
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  /* Contact links */
  .contact-links {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 10px;
  }

  .contact-link {
    color: var(--text-muted);
    text-decoration: none;
    font-size: 12px;
    display: inline-flex;
    align-items: center;
    gap: 4px;
    padding: 3px 8px;
    border-radius: 6px;
    transition: background 0.2s, color 0.2s;
  }

  .contact-link:hover {
    background: rgba(88, 166, 255, 0.1);
    color: var(--accent);
  }

  /* Sections */
  section { margin-bottom: 24px; }

  section h2 {
    font-size: 16px;
    color: #fff;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  section h2 .icon { font-size: 18px; }

  .about p {
    color: var(--text-muted);
    font-size: 14px;
    line-height: 1.7;
  }

  /* Stats */
  .stats {
    display: flex;
    gap: 12px;
    margin-top: 8px;
    flex-wrap: wrap;
  }

  .stat {
    background: rgba(88, 166, 255, 0.08);
    border: 1px solid rgba(88, 166, 255, 0.2);
    border-radius: 8px;
    padding: 10px 16px;
    text-align: center;
    min-width: 90px;
  }

  .stat-value {
    font-size: 20px;
    font-weight: 700;
    color: var(--accent);
  }

  .stat-label {
    font-size: 11px;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }

  /* Skills */
  .skill-category { margin-bottom: 14px; }

  .skill-category-title {
    font-size: 13px;
    color: var(--text);
    font-weight: 600;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .skill-tag {
    background: rgba(88, 166, 255, 0.1);
    border: 1px solid rgba(88, 166, 255, 0.3);
    color: var(--accent);
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 13px;
    font-weight: 500;
    transition: transform 0.15s, background 0.2s;
  }

  .skill-tag:hover {
    transform: translateY(-2px);
    background: rgba(88, 166, 255, 0.2);
  }

  /* Lists */
  ul {
    list-style: none;
    padding: 0;
  }

  li {
    padding: 7px 0 7px 22px;
    position: relative;
    font-size: 14px;
    color: var(--text-muted);
  }

  li::before {
    content: '▸';
    position: absolute;
    left: 6px;
    color: var(--accent);
    font-size: 12px;
  }

  /* Experience items */
  .exp-item { margin-bottom: 14px; }

  .exp-item:last-child { margin-bottom: 0; }

  .exp-title {
    font-size: 14px;
    color: #fff;
    font-weight: 600;
  }

  .exp-company {
    color: var(--accent-2);
    font-size: 13px;
    font-weight: 500;
  }

  .exp-date {
    color: var(--text-muted);
    font-size: 12px;
  }

  .exp-desc {
    color: var(--text-muted);
    font-size: 13px;
    margin-top: 4px;
    line-height: 1.5;
  }

  /* Project highlight */
  .project-highlight {
    background: rgba(247, 129, 102, 0.06);
    border-left: 3px solid var(--accent-2);
    padding: 10px 14px;
    border-radius: 0 8px 8px 0;
    margin-top: 8px;
    font-size: 13px;
    color: var(--text-muted);
  }

  /* Footer */
  .footer {
    margin-top: 28px;
    padding-top: 20px;
    border-top: 1px solid var(--border);
    display: flex;
    gap: 14px;
    flex-wrap: wrap;
  }

  .footer a {
    color: var(--accent);
    text-decoration: none;
    font-size: 13px;
    display: inline-flex;
    align-items: center;
    gap: 6px;
    transition: color 0.2s;
  }

  .footer a:hover { color: #fff; }

  @media (max-width: 540px) {
    .profile-card { padding: 20px; }
    .header { flex-direction: column; text-align: center; }
    .header-text { text-align: center; }
    .stats { justify-content: center; }
    .contact-links { justify-content: center; }
  }
</style>
</head>
<body>
  <div class="profile-card">
    <!-- Header -->
    <div class="header">
      <div class="avatar">AA</div>
      <div class="header-text" style="flex:1;">
        <h1>Abir Al Mahdi Akhand</h1>
        <div class="tagline">Full-Stack Developer | Machine Learning Engineer</div>
        <div class="status">Open to opportunities</div>
        <div class="contact-links">
          <a href="mailto:abiralmahdi@gmail.com">✉️ abiralmahdi@gmail.com</a>
          <a href="tel:+8801769025257">📞 +8801769025257</a>
          <a href="https://github.com/abiralmahdi" target="_blank">🔗 github.com/abiralmahdi</a>
          <a href="https://linkedin.com/in/abir-al-mahdi-akhand" target="_blank">💼 LinkedIn</a>
          <a href="https://abiralmahdi.vercel.app" target="_blank">🌐 Portfolio</a>
        </div>
      </div>
    </div>


    <section class="about">
      <h2><span class="icon">📄</span> Professional Summary</h2>
      <p>Computer Science graduate (CGPA: 3.57/4.00) with real-world experience shipping production software across full-stack web development, machine learning, and IoT integration. Has built and deployed systems including a stock market back-testing engine, a live IoT-connected energy management platform, and an AI-powered video anomaly detection tool. Comfortable working across the full stack, with a particular interest in backend APIs and machine learning. Thrives in collaborative team environments and brings genuine enthusiasm for tackling technically challenging, meaningful problems.</p>
    </section>

    <!-- Stats -->
    <section>
      <div class="stats">
        <div class="stat">
          <div class="stat-value">3.57/4.0</div>
          <div class="stat-label">CGPA</div>
        </div>
        <div class="stat">
          <div class="stat-value">3+</div>
          <div class="stat-label">Production Systems</div>
        </div>
        <div class="stat">
          <div class="stat-value">2025</div>
          <div class="stat-label">Graduated</div>
        </div>
        <div class="stat">
          <div class="stat-value">7</div>
          <div class="stat-label">Key Projects</div>
        </div>
      </div>
    </section>

    <!-- Experience -->
    <section>
      <h2><span class="icon">💼</span> Professional Experience</h2>
      <div class="exp-item">
        <div class="exp-title">Data Engineer</div>
        <div class="exp-company">Evoliq Tech Ltd, Baridhara DOHS, Dhaka</div>
        <div class="exp-date">April 2026 – Present</div>
        <div class="exp-desc">Developing the backend of an Ed-tech Platform with student registration, content uploading, MCQ generation, and SSL-Commerz payment gateway integration. Designed and deployed a Stock Market Back-testing Engine using FastAPI and Python for automated strategy evaluation across foreign stock exchanges.</div>
      </div>
      <div class="exp-item">
        <div class="exp-title">Junior Software Developer</div>
        <div class="exp-company">Marks Automation Ltd, Mirpur DOHS, Dhaka</div>
        <div class="exp-date">January 2026 – March 2026</div>
        <div class="exp-desc">Developed a full-stack Energy Management System using Django and Chart.js with real-time monitoring and visualization. Integrated industrial IoT devices and smart electricity meters via MODBUS and OPC-UA communication protocols using PyModbus.</div>
      </div>
      <div class="exp-item">
        <div class="exp-title">Software Developer Intern</div>
        <div class="exp-company">Marks Automation Ltd, Mirpur DOHS, Dhaka</div>
        <div class="exp-date">May 2025 – December 2025</div>
        <div class="exp-desc">Built a full-featured HR Management System and mini-ERP application using Django. Designed and deployed the company's official website as the primary client-facing digital touchpoint.</div>
      </div>
    </section>

    <!-- Key Projects -->
    <section>
      <h2><span class="icon">🚀</span> Key Projects</h2>
      <ul>
        <li>
          <b>Stock Market Analysis, Back-testing & Prediction Engine</b>
          <div class="project-highlight">FastAPI, Scikit-Learn, Next.js, PostgreSQL, Claude Code — end-to-end pipeline for ingesting, analyzing, and back-testing trading strategies with automated reporting.</div>
        </li>
        <li>
          <b>VisionGuard: AI-Powered Video Anomaly Detection</b>
          <div class="project-highlight">Django, PyTorch, Computer Vision, NLP — intelligent surveillance system detecting anomalous events in real-time video streams. <a href="https://github.com/abiralmahdi/MomentDetection" style="color:var(--accent);text-decoration:none;">github.com/abiralmahdi/MomentDetection</a></div>
        </li>
        <li>
          <b>Energy Management System (IoT)</b>
          <div class="project-highlight">Django, PyModbus, ChartJS, HTML5, CSS3, JS — dashboard displaying real-time energy and power consumption from PLCs and SCADA systems.</div>
        </li>
        <li>
          <b>Facial Detection Model Pruning via Local Sensitivity Awareness</b>
          <div class="project-highlight">PyTorch, Deep Learning, NumPy, Matplotlib — custom neural network pruning algorithm reducing model size while preserving facial detection accuracy.</div>
        </li>
        <li>
          <b>Full-Stack E-Commerce Web Application</b>
          <div class="project-highlight">React.js, Django REST Framework, RESTful API, SQLite — feature-complete e-commerce platform with product listings, cart, and order management.</div>
        </li>
        <li>
          <b>StatistiKids: Kid-Friendly Statistics Programming Language</b>
          <div class="project-highlight">Compiler Design, Lexical Analysis, Parser — domain-specific programming language to teach statistics concepts to children, including a full compiler pipeline.</div>
        </li>
        <li>
          <b>Android-Powered Smart Home Automation System</b>
          <div class="project-highlight">Flutter, MicroPython, Raspberry Pi Pico, Prompt Engineering — IoT-enabled home automation system controlled via Android app with microcontroller firmware and mobile UI.</div>
        </li>
      </ul>
    </section>

    <!-- Skills -->
    <section>
      <h2><span class="icon">💻</span> Technical Skills</h2>
      <div class="skill-category">
        <div class="skill-category-title">Languages</div>
        <div class="skill-tags">
          <span class="skill-tag">Python</span>
          <span class="skill-tag">JavaScript</span>
          <span class="skill-tag">Java</span>
          <span class="skill-tag">C/C++</span>
          <span class="skill-tag">HTML/CSS</span>
          <span class="skill-tag">MySQL</span>
          <span class="skill-tag">SQLite</span>
          <span class="skill-tag">MicroPython</span>
          <span class="skill-tag">ARM Assembly</span>
        </div>
      </div>
      <div class="skill-category">
        <div class="skill-category-title">Frameworks & Libraries</div>
        <div class="skill-tags">
          <span class="skill-tag">React.js</span>
          <span class="skill-tag">Django</span>
          <span class="skill-tag">Django REST</span>
          <span class="skill-tag">FastAPI</span>
          <span class="skill-tag">Flask</span>
          <span class="skill-tag">PyTorch</span>
          <span class="skill-tag">OpenCV</span>
          <span class="skill-tag">Scikit-Learn</span>
          <span class="skill-tag">Pandas</span>
          <span class="skill-tag">NumPy</span>
          <span class="skill-tag">Matplotlib</span>
          <span class="skill-tag">TailwindCSS</span>
          <span class="skill-tag">Bootstrap</span>
          <span class="skill-tag">Selenium</span>
          <span class="skill-tag">BeautifulSoup</span>
          <span class="skill-tag">Kivy</span>
          <span class="skill-tag">Tkinter</span>
          <span class="skill-tag">JavaFX</span>
        </div>
      </div>
      <div class="skill-category">
        <div class="skill-category-title">Domains & Tools</div>
        <div class="skill-tags">
          <span class="skill-tag">Full-Stack Web</span>
          <span class="skill-tag">RESTful APIs</span>
          <span class="skill-tag">Machine Learning</span>
          <span class="skill-tag">Deep Learning</span>
          <span class="skill-tag">Computer Vision</span>
          <span class="skill-tag">NLP</span>
          <span class="skill-tag">IoT Integration</span>
          <span class="skill-tag">Web Scraping</span>
          <span class="skill-tag">Docker</span>
          <span class="skill-tag">Git/GitHub</span>
          <span class="skill-tag">WebRTC</span>
          <span class="skill-tag">TradingView</span>
        </div>
      </div>
    </section>

    <!-- Education -->
    <section>
      <h2><span class="icon">🎓</span> Education</h2>
      <ul>
        <li><b>B.Sc. in Computer Science & Engineering</b> — North South University, Dhaka (2022–2025) — CGPA: 3.57/4.00</li>
        <li><b>HSC (Science)</b> — Adamjee Cantonment College, Dhaka (2019–2021) — GPA: 5.00/5.00</li>
        <li><b>SSC (Science)</b> — Adamjee Cantonment Public School, Dhaka (2017–2019) — GPA: 5.00/5.00</li>
      </ul>
    </section>

    <!-- Soft Skills -->
    <section>
      <h2><span class="icon">🗣</span> Soft Skills & Languages</h2>
      <div class="skill-tags">
        <span class="skill-tag">Leadership</span>
        <span class="skill-tag">Teamwork</span>
        <span class="skill-tag">Research</span>
        <span class="skill-tag">Presentation</span>
        <span class="skill-tag">Interpersonal Communication</span>
        <span class="skill-tag">Punctuality</span>
        <span class="skill-tag">Anchoring</span>
        <span class="skill-tag">English (Proficient)</span>
        <span class="skill-tag">Bengali (Native)</span>
      </div>
    </section>

    <!-- Footer -->
    <div class="footer">
      <a href="mailto:abiralmahdi@gmail.com">✉️ abiralmahdi@gmail.com</a>
      <a href="https://github.com/abiralmahdi" target="_blank">💻 GitHub</a>
      <a href="https://linkedin.com/in/abir-al-mahdi-akhand" target="_blank">💼 LinkedIn</a>
      <a href="https://abiralmahdi.vercel.app" target="_blank">🌐 Portfolio</a>
      <a href="https://github.com/abiralmahdi/MomentDetection" target="_blank">👁️ VisionGuard</a>
    </div>
  </div>
</body>
</html>
