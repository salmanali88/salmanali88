<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>salmanali83 · GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Sora:wght@300;400;600;700&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --border: #30363d;
    --text: #e6edf3;
    --muted: #8b949e;
    --accent: #58a6ff;
    --green: #3fb950;
    --orange: #f78166;
    --yellow: #d29922;
    --purple: #bc8cff;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Sora', sans-serif;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    padding: 24px 16px 60px;
  }

  .page {
    width: 100%;
    max-width: 860px;
  }

  /* ── NAV ── */
  .nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 12px 16px;
    border-bottom: 1px solid var(--border);
    margin-bottom: 24px;
    background: var(--surface);
    border-radius: 10px;
  }
  .nav-tabs { display: flex; gap: 4px; }
  .nav-tab {
    padding: 6px 14px;
    border-radius: 6px;
    font-size: 13px;
    color: var(--muted);
    cursor: pointer;
    border: 1px solid transparent;
    font-family: 'JetBrains Mono', monospace;
  }
  .nav-tab.active {
    color: var(--text);
    border-color: var(--border);
    background: var(--bg);
  }
  .nav-tab span {
    background: var(--border);
    border-radius: 20px;
    padding: 1px 7px;
    font-size: 11px;
    margin-left: 4px;
  }

  /* ── LAYOUT ── */
  .layout { display: flex; gap: 24px; align-items: flex-start; }

  /* ── SIDEBAR ── */
  .sidebar { width: 220px; flex-shrink: 0; }
  .avatar-wrap { position: relative; margin-bottom: 16px; }
  .avatar {
    width: 220px;
    height: 220px;
    border-radius: 50%;
    object-fit: cover;
    border: 3px solid var(--border);
    background: linear-gradient(135deg, #1a2a4a, #0d2137);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 72px;
  }
  .avatar-emoji {
    width: 220px;
    height: 220px;
    border-radius: 50%;
    border: 3px solid var(--border);
    background: linear-gradient(135deg, #1c3a5e 0%, #0d2137 50%, #12294a 100%);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 80px;
  }
  .username-block { margin-bottom: 12px; }
  .display-name { font-size: 20px; font-weight: 700; }
  .handle { color: var(--muted); font-size: 14px; font-family: 'JetBrains Mono', monospace; }
  .follow-btn {
    width: 100%;
    padding: 7px;
    border: 1px solid var(--border);
    border-radius: 6px;
    background: var(--surface);
    color: var(--text);
    font-size: 13px;
    cursor: pointer;
    margin-bottom: 16px;
    font-family: 'Sora', sans-serif;
  }
  .follow-btn:hover { background: var(--border); }
  .bio {
    font-size: 13px;
    color: var(--muted);
    margin-bottom: 14px;
    line-height: 1.5;
  }
  .bio strong { color: var(--text); }
  .stats { display: flex; gap: 12px; font-size: 13px; color: var(--muted); margin-bottom: 20px; }
  .stats strong { color: var(--text); }

  .section-label {
    font-size: 13px;
    font-weight: 600;
    margin-bottom: 10px;
    color: var(--text);
  }

  .achievements { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 20px; }
  .badge-circle {
    width: 36px; height: 36px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 18px; border: 2px solid var(--border);
  }
  .b1 { background: linear-gradient(135deg,#1a3a6e,#2a5298); }
  .b2 { background: linear-gradient(135deg,#3a1a2e,#7a2a4e); }
  .b3 { background: linear-gradient(135deg,#1a3a1e,#2a6a3e); }
  .b4 { background: linear-gradient(135deg,#3a2a1a,#7a5a2a); }
  .b5 { background: linear-gradient(135deg,#2a1a3a,#5a2a7a); }

  .highlight-item {
    display: flex; align-items: center; gap: 8px;
    font-size: 13px; color: var(--muted); margin-bottom: 6px;
  }
  .pro-badge {
    background: var(--surface);
    border: 1px solid var(--yellow);
    color: var(--yellow);
    border-radius: 4px;
    padding: 1px 7px;
    font-size: 11px;
    font-family: 'JetBrains Mono', monospace;
    font-weight: 700;
  }

  /* ── MAIN ── */
  .main { flex: 1; min-width: 0; }

  /* ── BANNER ── */
  .banner {
    background: #010409;
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 28px 24px;
    margin-bottom: 24px;
    position: relative;
    overflow: hidden;
    text-align: center;
  }
  .stars {
    position: absolute; inset: 0;
    background-image:
      radial-gradient(1px 1px at 10% 20%, rgba(255,255,255,0.6) 0%, transparent 100%),
      radial-gradient(1px 1px at 30% 70%, rgba(255,255,255,0.5) 0%, transparent 100%),
      radial-gradient(1px 1px at 50% 15%, rgba(255,255,255,0.7) 0%, transparent 100%),
      radial-gradient(1px 1px at 70% 80%, rgba(255,255,255,0.4) 0%, transparent 100%),
      radial-gradient(1px 1px at 85% 40%, rgba(255,255,255,0.6) 0%, transparent 100%),
      radial-gradient(1px 1px at 20% 55%, rgba(255,255,255,0.3) 0%, transparent 100%),
      radial-gradient(1px 1px at 60% 90%, rgba(255,255,255,0.5) 0%, transparent 100%),
      radial-gradient(1px 1px at 90% 10%, rgba(255,255,255,0.6) 0%, transparent 100%),
      radial-gradient(1px 1px at 45% 45%, rgba(255,255,255,0.4) 0%, transparent 100%),
      radial-gradient(2px 2px at 75% 25%, rgba(255,255,255,0.3) 0%, transparent 100%),
      radial-gradient(1px 1px at 15% 85%, rgba(255,255,255,0.5) 0%, transparent 100%),
      radial-gradient(1px 1px at 35% 35%, rgba(255,255,255,0.4) 0%, transparent 100%);
  }
  .banner-name {
    font-size: 26px;
    font-weight: 700;
    position: relative;
    z-index: 1;
    letter-spacing: 0.5px;
  }
  .banner-subtitle {
    font-size: 13px;
    color: var(--muted);
    position: relative;
    z-index: 1;
    margin-top: 6px;
    font-family: 'JetBrains Mono', monospace;
  }
  .banner-subtitle span { color: var(--accent); }

  /* ── README SECTIONS ── */
  .readme-section { margin-bottom: 24px; }

  .section-heading {
    font-size: 17px;
    font-weight: 700;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .info-box {
    background: var(--surface);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    border-radius: 6px;
    padding: 14px 16px;
    font-size: 13.5px;
    line-height: 1.7;
    color: #c9d1d9;
  }
  .info-box strong { color: var(--accent); }

  /* ── BADGES ── */
  .badge-grid { display: flex; flex-wrap: wrap; gap: 8px; }
  .badge {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 5px 12px;
    border-radius: 5px;
    font-size: 12px;
    font-weight: 600;
    font-family: 'JetBrains Mono', monospace;
    letter-spacing: 0.3px;
    border: 1px solid transparent;
    transition: transform 0.15s, box-shadow 0.15s;
    cursor: default;
  }
  .badge:hover { transform: translateY(-2px); box-shadow: 0 4px 12px rgba(0,0,0,0.4); }
  .badge .dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }

  /* language colors */
  .b-python  { background: #1a2e4a; border-color: #3776AB; color: #79b8ff; }
  .b-python .dot { background: #3776AB; }
  .b-hf      { background: #2a2500; border-color: #FFD21E; color: #FFD21E; }
  .b-hf .dot { background: #FFD21E; }
  .b-pytorch { background: #2a1a1a; border-color: #EE4C2C; color: #f97583; }
  .b-pytorch .dot { background: #EE4C2C; }
  .b-tf      { background: #2a1f00; border-color: #FF6F00; color: #ffab40; }
  .b-tf .dot { background: #FF6F00; }
  .b-jupyter { background: #2a1e00; border-color: #F37626; color: #ffa94d; }
  .b-jupyter .dot { background: #F37626; }
  .b-numpy   { background: #00161a; border-color: #4DABCF; color: #56d3e0; }
  .b-numpy .dot { background: #4DABCF; }
  .b-pandas  { background: #10003a; border-color: #6e40c9; color: #c5a3ff; }
  .b-pandas .dot { background: #6e40c9; }
  .b-sklearn { background: #2a1800; border-color: #F7931E; color: #ffc56e; }
  .b-sklearn .dot { background: #F7931E; }
  .b-git     { background: #2a0f00; border-color: #F05032; color: #ff7b6b; }
  .b-git .dot { background: #F05032; }
  .b-gha     { background: #001a2a; border-color: #2088FF; color: #79c0ff; }
  .b-gha .dot { background: #2088FF; }
  .b-cv      { background: #1a1040; border-color: #7c6bd6; color: #c5b3ff; }
  .b-cv .dot { background: #7c6bd6; }
  .b-mpl     { background: #001020; border-color: #11557C; color: #56a6d8; }
  .b-mpl .dot { background: #11557C; }
  .b-sea     { background: #1a1040; border-color: #5C3EE8; color: #a78bfa; }
  .b-sea .dot { background: #5C3EE8; }
  .b-plotly  { background: #0d1420; border-color: #3F4F75; color: #7890bb; }
  .b-plotly .dot { background: #3F4F75; }
  .b-stream  { background: #2a0000; border-color: #FF4B4B; color: #ff8080; }
  .b-stream .dot { background: #FF4B4B; }
  .b-spacy   { background: #001f2a; border-color: #09A3D5; color: #56cfe1; }
  .b-spacy .dot { background: #09A3D5; }
  .b-nltk    { background: #001a2a; border-color: #3776AB; color: #79b8ff; }
  .b-nltk .dot { background: #3776AB; }
  .b-trans   { background: #2a2500; border-color: #FFD21E; color: #FFD21E; }
  .b-trans .dot { background: #FFD21E; }
  .b-ds      { background: #2a2500; border-color: #ffb700; color: #ffd166; }
  .b-ds .dot { background: #ffb700; }
  .b-black   { background: #0a0a0a; border-color: #555; color: #aaa; }
  .b-black .dot { background: #555; }
  .b-pre     { background: #2a1f00; border-color: #FAB040; color: #ffd180; }
  .b-pre .dot { background: #FAB040; }

  /* ── PINNED CARDS ── */
  .pinned-label {
    font-size: 13px; color: var(--muted); margin-bottom: 12px;
    font-family: 'JetBrains Mono', monospace;
    letter-spacing: 1px; text-transform: uppercase;
  }
  .pinned-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
  .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 16px;
    transition: border-color 0.2s, transform 0.2s;
    cursor: pointer;
  }
  .card:hover { border-color: var(--accent); transform: translateY(-2px); }
  .card-header { display: flex; align-items: center; gap: 8px; margin-bottom: 8px; }
  .repo-icon { color: var(--muted); font-size: 14px; }
  .card-name { font-size: 14px; font-weight: 600; color: var(--accent); }
  .card-pub { font-size: 11px; color: var(--muted); border: 1px solid var(--border); border-radius: 20px; padding: 1px 8px; }
  .card-desc { font-size: 12px; color: var(--muted); line-height: 1.5; margin-bottom: 12px; }
  .card-meta { display: flex; align-items: center; gap: 12px; font-size: 12px; color: var(--muted); }
  .lang-dot { width: 10px; height: 10px; border-radius: 50%; display: inline-block; margin-right: 4px; }
  .py { background: #3776AB; }
  .js { background: #f1e05a; }
  .ts { background: #3178c6; }
  .nb { background: #DA5B0B; }
  .stars-count { display: flex; align-items: center; gap: 4px; }

  /* ── VIEWS BADGE ── */
  .views-badge {
    display: inline-flex; align-items: center; gap: 6px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 4px 10px;
    font-size: 12px;
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
    margin-bottom: 20px;
  }
  .views-badge .count { color: var(--accent); font-weight: 700; }

  /* ── CONNECT ── */
  .connect-links { display: flex; flex-wrap: wrap; gap: 8px; }
  .connect-btn {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 7px 14px; border-radius: 6px;
    font-size: 12px; font-weight: 600;
    font-family: 'JetBrains Mono', monospace;
    text-decoration: none; border: 1px solid;
    transition: transform 0.15s, opacity 0.15s;
    letter-spacing: 0.5px;
  }
  .connect-btn:hover { transform: translateY(-1px); opacity: 0.85; }
  .btn-email  { background: #1a1f2e; border-color: #3b82f6; color: #93c5fd; }
  .btn-kaggle { background: #001525; border-color: #20BEFF; color: #20BEFF; }
  .btn-hf     { background: #1a1500; border-color: #FFD21E; color: #FFD21E; }
  .btn-li     { background: #001222; border-color: #0A66C2; color: #5ba4f5; }
  .btn-gh     { background: #0d1117; border-color: #555; color: #ccc; }

  /* ── DIVIDER ── */
  hr { border: none; border-top: 1px solid var(--border); margin: 20px 0; }

  /* ── ALWAYS LEARNING ── */
  .tagline {
    text-align: center;
    font-size: 14px;
    color: var(--muted);
    padding: 12px;
    font-style: italic;
  }
  .tagline span { color: var(--green); }

  @media (max-width: 680px) {
    .layout { flex-direction: column; }
    .sidebar { width: 100%; }
    .avatar-emoji { width: 100px; height: 100px; font-size: 44px; margin: 0 auto 16px; }
    .pinned-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>
<div class="page">

  <!-- nav bar -->
  <div class="nav">
    <div class="nav-tabs">
      <div class="nav-tab active">📖 Overview</div>
      <div class="nav-tab">🗂 Repositories <span>12</span></div>
      <div class="nav-tab">📦 Projects</div>
      <div class="nav-tab">📎 Packages</div>
    </div>
    <div style="font-size:12px;color:var(--muted);font-family:'JetBrains Mono',monospace;">salmanali83</div>
  </div>

  <div class="layout">

    <!-- SIDEBAR -->
    <aside class="sidebar">
      <div class="avatar-wrap">
        <div class="avatar-emoji">🧑‍💻</div>
      </div>
      <div class="username-block">
        <div class="display-name">Salman Ali</div>
        <div class="handle">salmanali83</div>
      </div>
      <button class="follow-btn">Follow</button>
      <div class="bio">
        Ph.D. student · <strong>Time Series</strong> · Knowledge Distillation · Domain Adaptation
      </div>
      <div class="stats">
        <div><strong>71</strong> followers</div>
        <div><strong>103</strong> following</div>
      </div>

      <div class="section-label">Achievements</div>
      <div class="achievements">
        <div class="badge-circle b1">🧊</div>
        <div class="badge-circle b2">🦄</div>
        <div class="badge-circle b3">🐱</div>
        <div class="badge-circle b4">🏅</div>
        <div class="badge-circle b5">🤖</div>
      </div>

      <div class="section-label">Highlights</div>
      <div class="highlight-item">⚙️ Developer Program Member</div>
      <div class="highlight-item">⭐ <span class="pro-badge">PRO</span></div>
    </aside>

    <!-- MAIN -->
    <main class="main">

      <!-- Banner -->
      <div class="banner">
        <div class="stars"></div>
        <div class="banner-name">Salman Ali</div>
        <div class="banner-subtitle">
          🎓 Ph.D. · <span>Time Series Prediction</span> · Knowledge Distillation · Domain Adaptation
        </div>
      </div>

      <!-- Greeting -->
      <div class="readme-section">
        <div class="section-heading">👋 Hi there, I'm Salman Ali</div>
        <div class="info-box">
          I'm a <strong>Ph.D. student at Nanjing University of Aeronautics and Astronautics</strong>, currently focusing on developing a framework for <strong>Time Series Prediction</strong> through <strong>Knowledge Distillation</strong> with <strong>Domain Adaptation</strong> across all domains.
        </div>
      </div>

      <!-- Views -->
      <div class="views-badge">
        👁 Profile views &nbsp;<span class="count">salmanali83</span>
      </div>

      <!-- Connect -->
      <div class="readme-section">
        <div class="section-heading">🌐 Connect with Me 🤝</div>
        <div class="connect-links">
          <a class="connect-btn btn-email" href="#">✉ EMAIL</a>
          <a class="connect-btn btn-kaggle" href="#">🏆 KAGGLE</a>
          <a class="connect-btn btn-hf" href="#">🤗 HUGGING FACE</a>
          <a class="connect-btn btn-li" href="#">in LINKEDIN</a>
          <a class="connect-btn btn-gh" href="#">🐙 GITHUB</a>
        </div>
      </div>

      <hr/>

      <!-- Stack -->
      <div class="readme-section">
        <div class="section-heading">👨‍💻 My Coding Stack 🚀</div>
        <div class="badge-grid">
          <span class="badge b-python"><span class="dot"></span>Python</span>
          <span class="badge b-hf"><span class="dot"></span>Hugging Face</span>
          <span class="badge b-pytorch"><span class="dot"></span>PyTorch</span>
          <span class="badge b-tf"><span class="dot"></span>TensorFlow</span>
          <span class="badge b-jupyter"><span class="dot"></span>Jupyter</span>
          <span class="badge b-numpy"><span class="dot"></span>NumPy</span>
          <span class="badge b-pandas"><span class="dot"></span>Pandas</span>
          <span class="badge b-sklearn"><span class="dot"></span>Scikit-learn</span>
          <span class="badge b-git"><span class="dot"></span>Git</span>
          <span class="badge b-gha"><span class="dot"></span>GitHub Actions</span>
          <span class="badge b-cv"><span class="dot"></span>OpenCV</span>
          <span class="badge b-mpl"><span class="dot"></span>Matplotlib</span>
          <span class="badge b-sea"><span class="dot"></span>Seaborn</span>
          <span class="badge b-plotly"><span class="dot"></span>Plotly</span>
          <span class="badge b-stream"><span class="dot"></span>Streamlit</span>
          <span class="badge b-spacy"><span class="dot"></span>SpaCy</span>
          <span class="badge b-nltk"><span class="dot"></span>NLTK</span>
          <span class="badge b-trans"><span class="dot"></span>Transformers</span>
          <span class="badge b-ds"><span class="dot"></span>Datasets</span>
          <span class="badge b-black"><span class="dot"></span>Black</span>
          <span class="badge b-pre"><span class="dot"></span>Pre-commit</span>
        </div>
      </div>

      <hr/>

      <!-- Pinned -->
      <div class="readme-section">
        <div class="pinned-label">📌 Pinned</div>
        <div class="pinned-grid">

          <div class="card">
            <div class="card-header">
              <span class="repo-icon">🗂</span>
              <span class="card-name">DTMN</span>
              <span class="card-pub">Public</span>
            </div>
            <div class="card-desc">Deep Temporal Mixing Network — novel time-series forecasting combining TSMixer's dual mixing with N-BEATS backcast residual stacking. Teacher-student KD variants.</div>
            <div class="card-meta">
              <span><span class="lang-dot py"></span>Python</span>
              <span class="stars-count">⭐ 6</span>
              <span>🍴 2</span>
            </div>
          </div>

          <div class="card">
            <div class="card-header">
              <span class="repo-icon">🗂</span>
              <span class="card-name">ts-kd-domain</span>
              <span class="card-pub">Public</span>
            </div>
            <div class="card-desc">Framework for time-series prediction via knowledge distillation with cross-domain adaptation. Covers industrial, climate, and financial datasets.</div>
            <div class="card-meta">
              <span><span class="lang-dot py"></span>Python</span>
              <span class="stars-count">⭐ 9</span>
              <span>🍴 3</span>
            </div>
          </div>

          <div class="card">
            <div class="card-header">
              <span class="repo-icon">🗂</span>
              <span class="card-name">pattern-recognition-lab</span>
              <span class="card-pub">Public</span>
            </div>
            <div class="card-desc">Collection of pattern recognition experiments: anomaly detection, feature extraction, and signal classification using PyTorch and scikit-learn pipelines.</div>
            <div class="card-meta">
              <span><span class="lang-dot nb"></span>Jupyter Notebook</span>
              <span class="stars-count">⭐ 14</span>
              <span>🍴 4</span>
            </div>
          </div>

          <div class="card">
            <div class="card-header">
              <span class="repo-icon">🗂</span>
              <span class="card-name">ml-forecasting-toolkit</span>
              <span class="card-pub">Public</span>
            </div>
            <div class="card-desc">Production-grade ML utilities for multivariate time series: preprocessing, sliding-window batching, evaluation metrics, and Streamlit dashboards.</div>
            <div class="card-meta">
              <span><span class="lang-dot py"></span>Python</span>
              <span class="stars-count">⭐ 11</span>
              <span>🍴 5</span>
            </div>
          </div>

        </div>
      </div>

      <hr/>

      <div class="tagline">
        <span>🌱</span> Always Learning, Always Growing
      </div>

    </main>
  </div>
</div>
</body>
</html>
