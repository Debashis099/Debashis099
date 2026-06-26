<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Debashis Mangaraj - GitHub README</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@400;600;700&family=Share+Tech+Mono&display=swap');

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: #020b18;
    font-family: 'Rajdhani', sans-serif;
    color: #e0eaff;
    overflow-x: hidden;
  }

  /* ── GRID BACKGROUND ── */
  .grid-bg {
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,200,255,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,200,255,0.04) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .wrapper {
    position: relative;
    z-index: 1;
    max-width: 780px;
    margin: 0 auto;
    padding: 0 0 40px;
  }

  /* ── HEADER ── */
  .header {
    background: linear-gradient(160deg, #0a1628 0%, #050e1e 60%, #071220 100%);
    border-bottom: 2px solid #00c8ff44;
    padding: 36px 32px 28px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .header::before {
    content: '';
    position: absolute;
    top: -60px; left: 50%;
    transform: translateX(-50%);
    width: 500px; height: 200px;
    background: radial-gradient(ellipse, #00c8ff18 0%, transparent 70%);
    pointer-events: none;
  }

  .globe-icon {
    width: 90px; height: 90px;
    border-radius: 50%;
    background: radial-gradient(circle at 35% 35%, #1a3a5c, #040d1a);
    border: 3px solid #00c8ff;
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 16px;
    font-size: 38px;
    box-shadow: 0 0 30px #00c8ff55, inset 0 0 20px #00c8ff22;
    animation: pulse 3s ease-in-out infinite;
  }

  @keyframes pulse {
    0%, 100% { box-shadow: 0 0 30px #00c8ff55, inset 0 0 20px #00c8ff22; }
    50% { box-shadow: 0 0 50px #00c8ff88, inset 0 0 30px #00c8ff33; }
  }

  .header h1 {
    font-family: 'Orbitron', sans-serif;
    font-size: 28px;
    font-weight: 900;
    letter-spacing: 3px;
    background: linear-gradient(90deg, #00c8ff, #a78bfa, #00c8ff);
    background-size: 200%;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: shimmer 4s linear infinite;
  }

  @keyframes shimmer {
    0% { background-position: 0% }
    100% { background-position: 200% }
  }

  .header .tagline {
    font-family: 'Rajdhani', sans-serif;
    font-size: 14px;
    color: #f59e0b;
    letter-spacing: 2px;
    margin: 6px 0 4px;
    font-weight: 600;
  }

  .header .sub {
    font-size: 13px;
    color: #64748b;
    letter-spacing: 1px;
  }

  .contact-row {
    display: flex;
    justify-content: center;
    gap: 16px;
    margin-top: 18px;
    flex-wrap: wrap;
  }

  .contact-badge {
    display: flex;
    align-items: center;
    gap: 6px;
    background: rgba(0,200,255,0.08);
    border: 1px solid #00c8ff33;
    border-radius: 20px;
    padding: 5px 14px;
    font-size: 12px;
    color: #94a3b8;
    font-family: 'Share Tech Mono', monospace;
  }

  .contact-badge span { color: #00c8ff; }

  /* ── HERO BANNER ── */
  .hero {
    background: linear-gradient(90deg, #0f2a1e 0%, #0a1628 50%, #1a0a2e 100%);
    border-top: 1px solid #00ff8833;
    border-bottom: 1px solid #a78bfa33;
    padding: 20px 32px;
    text-align: center;
  }

  .hero h2 {
    font-family: 'Orbitron', sans-serif;
    font-size: 22px;
    font-weight: 700;
  }

  .hero h2 span.green { color: #00ff88; }
  .hero h2 span.purple { color: #a78bfa; }
  .hero h2 span.orange { color: #f59e0b; }

  .hero p {
    font-size: 13px;
    color: #94a3b8;
    margin-top: 6px;
    letter-spacing: 1px;
  }

  /* ── SECTION ── */
  .section {
    padding: 24px 32px 0;
  }

  .section-title {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 16px;
  }

  .section-title .icon {
    width: 32px; height: 32px;
    background: rgba(0,200,255,0.12);
    border: 1px solid #00c8ff44;
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    font-size: 15px;
  }

  .section-title h3 {
    font-family: 'Orbitron', sans-serif;
    font-size: 13px;
    letter-spacing: 2px;
    color: #00c8ff;
  }

  .section-title .line {
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, #00c8ff44, transparent);
  }

  /* ── ROADMAP ── */
  .roadmap {
    display: flex;
    gap: 12px;
    padding: 0 32px 24px;
  }

  .rm-col {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .rm-box {
    background: rgba(255,255,255,0.03);
    border-radius: 10px;
    padding: 14px 16px;
    position: relative;
    overflow: hidden;
  }

  .rm-box::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
  }

  .rm-box.cyan::before { background: linear-gradient(90deg, #00c8ff, transparent); }
  .rm-box.green::before { background: linear-gradient(90deg, #00ff88, transparent); }
  .rm-box.purple::before { background: linear-gradient(90deg, #a78bfa, transparent); }
  .rm-box.orange::before { background: linear-gradient(90deg, #f59e0b, transparent); }
  .rm-box.pink::before { background: linear-gradient(90deg, #f472b6, transparent); }

  .rm-box .rm-label {
    font-family: 'Orbitron', sans-serif;
    font-size: 10px;
    letter-spacing: 1.5px;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .rm-box.cyan .rm-label { color: #00c8ff; }
  .rm-box.green .rm-label { color: #00ff88; }
  .rm-box.purple .rm-label { color: #a78bfa; }
  .rm-box.orange .rm-label { color: #f59e0b; }
  .rm-box.pink .rm-label { color: #f472b6; }

  .skill-chip {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    margin: 3px;
    padding: 4px 10px;
    border-radius: 12px;
    font-size: 11px;
    font-weight: 600;
    font-family: 'Share Tech Mono', monospace;
  }

  .chip-cyan { background: rgba(0,200,255,0.12); border: 1px solid #00c8ff44; color: #67e8f9; }
  .chip-green { background: rgba(0,255,136,0.10); border: 1px solid #00ff8844; color: #6ee7b7; }
  .chip-purple { background: rgba(167,139,250,0.12); border: 1px solid #a78bfa44; color: #c4b5fd; }
  .chip-orange { background: rgba(245,158,11,0.12); border: 1px solid #f59e0b44; color: #fcd34d; }
  .chip-pink { background: rgba(244,114,182,0.12); border: 1px solid #f472b644; color: #f9a8d4; }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    padding: 0 32px 24px;
  }

  .project-card {
    background: rgba(255,255,255,0.025);
    border-radius: 12px;
    padding: 16px;
    border: 1px solid rgba(255,255,255,0.06);
    position: relative;
    overflow: hidden;
    transition: transform 0.2s;
  }

  .project-card::after {
    content: '';
    position: absolute;
    bottom: 0; right: 0;
    width: 60px; height: 60px;
    border-radius: 50%;
    filter: blur(20px);
    opacity: 0.3;
  }

  .project-card.p1::after { background: #00c8ff; }
  .project-card.p2::after { background: #00ff88; }
  .project-card.p3::after { background: #a78bfa; }
  .project-card.p4::after { background: #f59e0b; }

  .project-card .p-icon { font-size: 22px; margin-bottom: 8px; }

  .project-card h4 {
    font-family: 'Orbitron', sans-serif;
    font-size: 10px;
    letter-spacing: 1px;
    margin-bottom: 6px;
  }

  .project-card.p1 h4 { color: #00c8ff; }
  .project-card.p2 h4 { color: #00ff88; }
  .project-card.p3 h4 { color: #a78bfa; }
  .project-card.p4 h4 { color: #f59e0b; }

  .project-card p {
    font-size: 11px;
    color: #64748b;
    line-height: 1.5;
  }

  .project-card .p-tags {
    margin-top: 8px;
    display: flex;
    flex-wrap: wrap;
    gap: 4px;
  }

  .p-tag {
    font-size: 9px;
    font-family: 'Share Tech Mono', monospace;
    padding: 2px 7px;
    border-radius: 8px;
    background: rgba(255,255,255,0.06);
    color: #94a3b8;
  }

  /* ── STATS ROW ── */
  .stats-row {
    display: flex;
    gap: 12px;
    padding: 0 32px 24px;
  }

  .stat-card {
    flex: 1;
    background: rgba(255,255,255,0.03);
    border-radius: 10px;
    padding: 16px 12px;
    text-align: center;
    border: 1px solid rgba(255,255,255,0.06);
  }

  .stat-card .s-num {
    font-family: 'Orbitron', sans-serif;
    font-size: 24px;
    font-weight: 900;
  }

  .stat-card .s-label {
    font-size: 10px;
    color: #64748b;
    letter-spacing: 1px;
    margin-top: 4px;
  }

  .c1 .s-num { color: #00c8ff; }
  .c2 .s-num { color: #00ff88; }
  .c3 .s-num { color: #a78bfa; }
  .c4 .s-num { color: #f59e0b; }

  /* ── EDUCATION ── */
  .edu-row {
    padding: 0 32px 24px;
    display: flex;
    gap: 12px;
  }

  .edu-card {
    flex: 1;
    background: rgba(255,255,255,0.025);
    border-radius: 10px;
    padding: 14px 16px;
    border-left: 3px solid;
    position: relative;
  }

  .edu-card.e1 { border-color: #a78bfa; }
  .edu-card.e2 { border-color: #00ff88; }

  .edu-card .e-icon { font-size: 20px; margin-bottom: 6px; }

  .edu-card h4 {
    font-family: 'Orbitron', sans-serif;
    font-size: 10px;
    letter-spacing: 1px;
    margin-bottom: 4px;
  }

  .edu-card.e1 h4 { color: #a78bfa; }
  .edu-card.e2 h4 { color: #00ff88; }

  .edu-card p { font-size: 11px; color: #94a3b8; line-height: 1.5; }
  .edu-card .e-year { font-size: 10px; color: #475569; margin-top: 6px; font-family: 'Share Tech Mono', monospace; }

  /* ── FOOTER ── */
  .footer {
    background: linear-gradient(90deg, #0f2a1e 0%, #0a1628 50%, #1a0a2e 100%);
    border-top: 2px solid #00c8ff22;
    padding: 20px 32px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .footer .takeaway {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    max-width: 340px;
  }

  .footer .t-icon {
    width: 32px; height: 32px;
    background: rgba(245,158,11,0.15);
    border: 1px solid #f59e0b44;
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    font-size: 15px;
    flex-shrink: 0;
  }

  .footer .takeaway p {
    font-size: 11px;
    color: #94a3b8;
    line-height: 1.6;
  }

  .footer .takeaway strong { color: #f59e0b; }

  .footer .connect {
    text-align: right;
  }

  .footer .connect p {
    font-size: 11px;
    color: #475569;
    margin-bottom: 6px;
    font-family: 'Share Tech Mono', monospace;
  }

  .footer .connect .email {
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    color: #00c8ff;
    background: rgba(0,200,255,0.08);
    border: 1px solid #00c8ff33;
    border-radius: 6px;
    padding: 5px 12px;
    display: inline-block;
  }

  .footer-tagline {
    background: #020b18;
    padding: 14px;
    text-align: center;
    font-family: 'Orbitron', sans-serif;
    font-size: 11px;
    letter-spacing: 4px;
    color: #1e3a5f;
  }

  .footer-tagline span.c { color: #00c8ff; }
  .footer-tagline span.g { color: #00ff88; }
  .footer-tagline span.p { color: #a78bfa; }
  .footer-tagline span.o { color: #f59e0b; }

  /* ── CONNECTOR LINES ── */
  .connector {
    display: flex;
    align-items: center;
    padding: 0 32px;
    margin-bottom: -8px;
    margin-top: 4px;
  }

  .connector .dot {
    width: 8px; height: 8px;
    border-radius: 50%;
    background: #00c8ff;
    box-shadow: 0 0 8px #00c8ff;
    flex-shrink: 0;
  }

  .connector .line-h {
    height: 1px;
    flex: 1;
    background: linear-gradient(90deg, #00c8ff44, transparent);
  }
</style>
</head>
<body>

<div class="grid-bg"></div>

<div class="wrapper">

  <!-- HEADER -->
  <div class="header">
    <div class="globe-icon">🧠</div>
    <h1>DEBASHIS MANGARAJ</h1>
    <div class="tagline">DATA ANALYST · ML ENGINEER · GENERATIVE AI</div>
    <div class="sub">MCA 2026 · Hyderabad, India</div>
    <div class="contact-row">
      <div class="contact-badge">📞 <span>+91 7205147189</span></div>
      <div class="contact-badge">✉️ <span>debashismangaraj8@gmail.com</span></div>
      <div class="contact-badge">🔗 <span>linkedin.com/in/debashis-mangaraj</span></div>
    </div>
  </div>

  <!-- HERO -->
  <div class="hero">
    <h2>
      <span class="green">Data Science</span>
      <span style="color:#475569"> &amp; </span>
      <span class="purple">AI Engineering</span>
      <span style="color:#475569"> Made </span>
      <span class="orange">Impactful</span>
    </h2>
    <p>End-to-End Pipelines · Predictive Models · Real-World AI Solutions</p>
  </div>

  <!-- STATS -->
  <div class="section">
    <div class="section-title">
      <div class="icon">📊</div>
      <h3>BY THE NUMBERS</h3>
      <div class="line"></div>
    </div>
  </div>

  <div class="stats-row">
    <div class="stat-card c1">
      <div class="s-num">10K+</div>
      <div class="s-label">RECORDS ANALYZED</div>
    </div>
    <div class="stat-card c2">
      <div class="s-num">85%</div>
      <div class="s-label">MODEL ACCURACY</div>
    </div>
    <div class="stat-card c3">
      <div class="s-num">4+</div>
      <div class="s-label">AI PROJECTS</div>
    </div>
    <div class="stat-card c4">
      <div class="s-num">40%</div>
      <div class="s-label">REPORTING SAVED</div>
    </div>
  </div>

  <!-- TECH STACK ROADMAP -->
  <div class="section">
    <div class="section-title">
      <div class="icon">⚙️</div>
      <h3>TECH STACK ROADMAP</h3>
      <div class="line"></div>
    </div>
  </div>

  <div class="roadmap">
    <!-- Col 1 -->
    <div class="rm-col">
      <div class="rm-box cyan">
        <div class="rm-label">💻 CORE LANGUAGES</div>
        <span class="skill-chip chip-cyan">🐍 Python</span>
        <span class="skill-chip chip-cyan">🗄️ SQL</span>
      </div>

      <div class="rm-box green">
        <div class="rm-label">📊 DATA ANALYSIS</div>
        <span class="skill-chip chip-green">Pandas</span>
        <span class="skill-chip chip-green">NumPy</span>
        <span class="skill-chip chip-green">Excel</span>
        <span class="skill-chip chip-green">Statsmodels</span>
      </div>

      <div class="rm-box orange">
        <div class="rm-label">📈 VISUALIZATION</div>
        <span class="skill-chip chip-orange">Power BI</span>
        <span class="skill-chip chip-orange">Plotly</span>
        <span class="skill-chip chip-orange">Seaborn</span>
        <span class="skill-chip chip-orange">Matplotlib</span>
        <span class="skill-chip chip-orange">Bokeh</span>
      </div>
    </div>

    <!-- Col 2 -->
    <div class="rm-col">
      <div class="rm-box purple">
        <div class="rm-label">🤖 MACHINE LEARNING</div>
        <span class="skill-chip chip-purple">Scikit-Learn</span>
        <span class="skill-chip chip-purple">XGBoost</span>
        <span class="skill-chip chip-purple">Random Forest</span>
        <span class="skill-chip chip-purple">GridSearchCV</span>
      </div>

      <div class="rm-box pink">
        <div class="rm-label">🧬 DEEP LEARNING</div>
        <span class="skill-chip chip-pink">TensorFlow</span>
        <span class="skill-chip chip-pink">Keras</span>
        <span class="skill-chip chip-pink">PyTorch</span>
        <span class="skill-chip chip-pink">OpenCV</span>
        <span class="skill-chip chip-pink">MobileNet</span>
        <span class="skill-chip chip-pink">YOLO</span>
      </div>

      <div class="rm-box cyan">
        <div class="rm-label">🗣️ NLP</div>
        <span class="skill-chip chip-cyan">BERT</span>
        <span class="skill-chip chip-cyan">NLTK</span>
        <span class="skill-chip chip-cyan">SpaCy</span>
        <span class="skill-chip chip-cyan">Word2Vec</span>
        <span class="skill-chip chip-cyan">HuggingFace</span>
      </div>
    </div>

    <!-- Col 3 -->
    <div class="rm-col">
      <div class="rm-box orange">
        <div class="rm-label">✨ GENERATIVE AI</div>
        <span class="skill-chip chip-orange">LangChain</span>
        <span class="skill-chip chip-orange">OpenAI</span>
        <span class="skill-chip chip-orange">Gemini</span>
        <span class="skill-chip chip-orange">Claude</span>
        <span class="skill-chip chip-orange">LLaMA</span>
        <span class="skill-chip chip-orange">Bedrock</span>
      </div>

      <div class="rm-box green">
        <div class="rm-label">☁️ CLOUD & MLOPS</div>
        <span class="skill-chip chip-green">Azure ML</span>
        <span class="skill-chip chip-green">AWS SageMaker</span>
        <span class="skill-chip chip-green">Vertex AI</span>
        <span class="skill-chip chip-green">MLflow</span>
        <span class="skill-chip chip-green">Kubeflow</span>
      </div>

      <div class="rm-box purple">
        <div class="rm-label">🌐 WEB & APIs</div>
        <span class="skill-chip chip-purple">Streamlit</span>
        <span class="skill-chip chip-purple">FastAPI</span>
        <span class="skill-chip chip-purple">Flask</span>
        <span class="skill-chip chip-purple">Django</span>
        <span class="skill-chip chip-purple">Gradio</span>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section">
    <div class="section-title">
      <div class="icon">🚀</div>
      <h3>FEATURED PROJECTS</h3>
      <div class="line"></div>
    </div>
  </div>

  <div class="projects-grid">

    <div class="project-card p1">
      <div class="p-icon">📊</div>
      <h4>SALES DATA DASHBOARD</h4>
      <p>Analyzed 10,000+ sales records, uncovering seasonal trends and revenue drivers. Reduced stakeholder reporting effort by ~40%.</p>
      <div class="p-tags">
        <span class="p-tag">Python</span>
        <span class="p-tag">Pandas</span>
        <span class="p-tag">Plotly</span>
        <span class="p-tag">Power BI</span>
      </div>
    </div>

    <div class="project-card p2">
      <div class="p-icon">🔮</div>
      <h4>CUSTOMER CHURN PREDICTOR</h4>
      <p>Built ML classifiers achieving ~85% accuracy. Identified top churn predictors enabling targeted retention campaigns.</p>
      <div class="p-tags">
        <span class="p-tag">XGBoost</span>
        <span class="p-tag">Scikit-Learn</span>
        <span class="p-tag">Random Forest</span>
      </div>
    </div>

    <div class="project-card p3">
      <div class="p-icon">🧠</div>
      <h4>SENTIMENT NLP PIPELINE</h4>
      <p>Processed 5,000+ reviews using BERT embeddings for context-aware classification. Outperformed baseline bag-of-words models.</p>
      <div class="p-tags">
        <span class="p-tag">BERT</span>
        <span class="p-tag">NLTK</span>
        <span class="p-tag">SpaCy</span>
        <span class="p-tag">Plotly</span>
      </div>
    </div>

    <div class="project-card p4">
      <div class="p-icon">⚡</div>
      <h4>STREAMLIT ANALYTICS APP</h4>
      <p>No-code analytics web app — upload a CSV and instantly get visual reports, KPI summaries, heatmaps, and distribution plots.</p>
      <div class="p-tags">
        <span class="p-tag">Streamlit</span>
        <span class="p-tag">Pandas</span>
        <span class="p-tag">Seaborn</span>
        <span class="p-tag">Matplotlib</span>
      </div>
    </div>

  </div>

  <!-- EDUCATION -->
  <div class="section">
    <div class="section-title">
      <div class="icon">🎓</div>
      <h3>EDUCATION & CERTIFICATIONS</h3>
      <div class="line"></div>
    </div>
  </div>

  <div class="edu-row">
    <div class="edu-card e1">
      <div class="e-icon">🏛️</div>
      <h4>MASTER OF COMPUTER APPLICATIONS</h4>
      <p>Nalanda Institute of Technology</p>
      <div class="e-year">EXPECTED 2026</div>
    </div>
    <div class="edu-card e2">
      <div class="e-icon">🏆</div>
      <h4>DATA SCIENCE CERTIFICATION</h4>
      <p>Naresh IT, Hyderabad<br>Data Analytics · ML · Deep Learning · NLP · Generative AI · Cloud</p>
      <div class="e-year">2026</div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="takeaway">
      <div class="t-icon">🎯</div>
      <p><strong>Key Focus:</strong> Buildi
