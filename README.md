<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Balaji V — AI/ML Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Manrope:wght@400;500;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0d1117;
    --bg-alt:#161b22;
    --border:#30363d;
    --border-soft:#21262d;
    --text:#e6edf3;
    --text-dim:#8b949e;
    --accent:#3fb950;
    --accent-dim:#3fb95022;
    --accent-cyan:#58a6ff;
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--bg);
    color:var(--text);
    font-family:'Manrope',sans-serif;
    line-height:1.6;
  }
  .mono{font-family:'JetBrains Mono',monospace;}
  a{color:inherit;text-decoration:none;}
  ::selection{background:var(--accent-dim);color:var(--accent);}

  /* subtle dot grid backdrop */
  .grid-bg{
    background-image: radial-gradient(circle, #ffffff12 1px, transparent 1px);
    background-size: 24px 24px;
  }

  .container{max-width:1080px;margin:0 auto;padding:0 24px;}

  /* nav */
  nav{
    position:sticky;top:0;z-index:50;
    background:#0d1117cc;backdrop-filter:blur(8px);
    border-bottom:1px solid var(--border-soft);
  }
  nav .inner{display:flex;align-items:center;justify-content:space-between;height:64px;}
  .logo{font-family:'JetBrains Mono',monospace;font-weight:700;font-size:16px;display:flex;align-items:center;gap:8px;}
  .logo .dot{width:8px;height:8px;border-radius:50%;background:var(--accent);box-shadow:0 0 8px var(--accent);}
  .nav-links{display:flex;gap:28px;font-size:14px;color:var(--text-dim);}
  .nav-links a:hover{color:var(--text);}
  .btn{
    display:inline-flex;align-items:center;gap:8px;
    padding:8px 16px;border-radius:6px;font-size:14px;font-weight:600;
    border:1px solid var(--border);transition:all .15s ease;
  }
  .btn-primary{background:var(--accent);color:#0d1117;border-color:var(--accent);}
  .btn-primary:hover{background:#4ac95c;}
  .btn-ghost{color:var(--text);}
  .btn-ghost:hover{background:var(--bg-alt);border-color:#484f58;}

  @media (max-width:720px){ .nav-links{display:none;} }

  /* hero */
  .hero{padding:96px 0 72px;}
  .eyebrow{
    font-family:'JetBrains Mono',monospace;font-size:13px;color:var(--accent);
    display:flex;align-items:center;gap:8px;margin-bottom:20px;
  }
  .hero h1{
    font-size:clamp(2.4rem,5vw,3.6rem);font-weight:800;letter-spacing:-0.03em;line-height:1.08;
    margin-bottom:20px;
  }
  .hero h1 span{color:var(--text-dim);font-weight:500;}
  .hero p.lead{font-size:18px;color:var(--text-dim);max-width:560px;margin-bottom:32px;}
  .hero-ctas{display:flex;gap:12px;margin-bottom:56px;flex-wrap:wrap;}

  /* terminal */
  .terminal{
    background:var(--bg-alt);border:1px solid var(--border);border-radius:10px;
    overflow:hidden;box-shadow:0 20px 60px -20px #000000aa;
  }
  .terminal-bar{
    display:flex;align-items:center;gap:8px;padding:10px 14px;
    border-bottom:1px solid var(--border-soft);background:#0d1117;
  }
  .terminal-bar span{width:11px;height:11px;border-radius:50%;}
  .terminal-bar .r{background:#ff5f56;} .terminal-bar .y{background:#ffbd2e;} .terminal-bar .g{background:#27c93f;}
  .terminal-bar .fname{margin-left:8px;font-family:'JetBrains Mono',monospace;font-size:12px;color:var(--text-dim);}
  .terminal pre{
    padding:20px 22px;font-family:'JetBrains Mono',monospace;font-size:13.5px;line-height:1.7;
    color:#c9d1d9;overflow-x:auto;
  }
  .terminal .c1{color:var(--accent-cyan);} .terminal .c2{color:var(--accent);} .terminal .c3{color:#f0883e;} .terminal .c4{color:var(--text-dim);}
  .cursor{display:inline-block;width:7px;height:14px;background:var(--accent);vertical-align:middle;animation:blink 1s step-end infinite;}
  @keyframes blink{50%{opacity:0;}}

  /* stats */
  .stats{
    display:grid;grid-template-columns:repeat(4,1fr);gap:1px;
    background:var(--border-soft);border:1px solid var(--border-soft);border-radius:10px;overflow:hidden;
    margin-top:56px;
  }
  .stat{background:var(--bg);padding:22px 16px;text-align:center;}
  .stat .num{font-family:'JetBrains Mono',monospace;font-weight:700;font-size:26px;color:var(--accent);}
  .stat .lbl{font-size:12.5px;color:var(--text-dim);margin-top:4px;}
  @media (max-width:640px){ .stats{grid-template-columns:repeat(2,1fr);} }

  section{padding:72px 0;border-top:1px solid var(--border-soft);}
  .section-head{margin-bottom:36px;}
  .section-head .tag{font-family:'JetBrains Mono',monospace;font-size:12.5px;color:var(--accent-cyan);margin-bottom:8px;display:block;}
  .section-head h2{font-size:28px;font-weight:800;letter-spacing:-0.02em;}
  .section-head p{color:var(--text-dim);margin-top:8px;max-width:560px;}

  /* about */
  .about-grid{display:grid;grid-template-columns:1.3fr 1fr;gap:48px;align-items:start;}
  .about-grid p{color:var(--text-dim);margin-bottom:14px;}
  .about-grid strong{color:var(--text);font-weight:600;}
  .fact-list{list-style:none;display:flex;flex-direction:column;gap:10px;}
  .fact-list li{
    font-size:14px;color:var(--text-dim);padding-left:20px;position:relative;
  }
  .fact-list li::before{content:"›";position:absolute;left:0;color:var(--accent);font-weight:700;}
  @media (max-width:800px){ .about-grid{grid-template-columns:1fr;} }

  /* skills - contribution-graph style */
  .skill-group{margin-bottom:26px;}
  .skill-group .gname{font-family:'JetBrains Mono',monospace;font-size:13px;color:var(--text-dim);margin-bottom:10px;}
  .skill-row{display:flex;flex-wrap:wrap;gap:8px;}
  .chip{
    display:flex;align-items:center;gap:8px;
    padding:6px 12px;border:1px solid var(--border);border-radius:6px;
    font-size:13px;background:var(--bg-alt);
  }
  .chip .heat{width:8px;height:8px;border-radius:2px;}
  /* heat levels mimic contribution graph intensity */
  .h1{background:#0e4429;} .h2{background:#006d32;} .h3{background:#26a641;} .h4{background:#39d353;}

  /* projects - repo card style */
  .repo-list{display:flex;flex-direction:column;gap:14px;}
  .repo-card{
    border:1px solid var(--border);border-radius:10px;padding:20px 22px;
    background:var(--bg-alt);transition:border-color .15s ease, transform .15s ease;
  }
  .repo-card:hover{border-color:#484f58;transform:translateY(-2px);}
  .repo-top{display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap;}
  .repo-name{font-family:'JetBrains Mono',monospace;font-weight:700;color:var(--accent-cyan);font-size:15.5px;}
  .repo-meta{display:flex;align-items:center;gap:16px;font-size:12.5px;color:var(--text-dim);}
  .repo-meta .lang{display:flex;align-items:center;gap:6px;}
  .lang-dot{width:9px;height:9px;border-radius:50%;}
  .repo-desc{color:var(--text-dim);font-size:14px;margin:10px 0 14px;max-width:640px;}
  .topics{display:flex;flex-wrap:wrap;gap:8px;}
  .topic{
    font-family:'JetBrains Mono',monospace;font-size:11.5px;color:var(--accent-cyan);
    background:#1f6feb1a;border:1px solid #1f6feb33;padding:3px 9px;border-radius:14px;
  }

  /* contact */
  .contact-card{
    border:1px solid var(--border);border-radius:12px;padding:40px;text-align:center;
    background:radial-gradient(ellipse at top, #3fb95012, transparent 60%), var(--bg-alt);
  }
  .contact-card h2{font-size:26px;font-weight:800;margin-bottom:10px;}
  .contact-card p{color:var(--text-dim);margin-bottom:26px;}
  .contact-links{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;}

  footer{
    border-top:1px solid var(--border-soft);padding:28px 0;
    display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:12px;
    font-size:13px;color:var(--text-dim);
  }
  footer .mono{color:#484f58;}

  .reveal{opacity:0;transform:translateY(14px);transition:opacity .5s ease, transform .5s ease;}
  .reveal.visible{opacity:1;transform:translateY(0);}
</style>
</head>
<body class="grid-bg">

<nav>
  <div class="container inner">
    <div class="logo"><span class="dot"></span>balaji<span class="mono" style="color:var(--text-dim)">.dev</span></div>
    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </div>
    <a href="#contact" class="btn btn-primary">Get in touch</a>
  </div>
</nav>

<header class="hero">
  <div class="container">
    <div class="eyebrow">● available for AI/ML roles</div>
    <h1>Balaji V<br><span>AI/ML Engineer building models that ship, not just notebooks that run.</span></h1>
    <p class="lead">M.Sc. Data Science grad specializing in applied ML — computer vision, GenAI agents, and anomaly detection — deployed as real APIs and apps, not just Jupyter demos.</p>
    <div class="hero-ctas">
      <a href="#projects" class="btn btn-primary">View projects</a>
      <a href="#" class="btn btn-ghost">↓ Download resume</a>
      <a href="https://github.com/Balaji-2001" class="btn btn-ghost">GitHub ↗</a>
    </div>

    <div class="terminal reveal">
      <div class="terminal-bar">
        <span class="r"></span><span class="y"></span><span class="g"></span>
        <span class="fname">deploy.py</span>
      </div>
      <pre><span class="c4"># loading production ensemble</span>
<span class="c1">model</span> = load_ensemble(<span class="c3">"isolation_forest"</span>, <span class="c3">"ocsvm"</span>, <span class="c3">"lstm_autoencoder"</span>)
<span class="c1">app</span> = FastAPI()

<span class="c4">@app.post(</span><span class="c3">"/predict"</span><span class="c4">)</span>
<span class="c2">def</span> detect_anomaly(sensor_data: SensorInput):
    <span class="c2">return</span> model.score(sensor_data)

<span class="c4">$</span> uvicorn deploy:app --host 0.0.0.0<span class="cursor"></span></pre>
    </div>

    <div class="stats reveal">
      <div class="stat"><div class="num">90%</div><div class="lbl">detection precision (YOLOv8)</div></div>
      <div class="stat"><div class="num">3</div><div class="lbl">model ensemble in production</div></div>
      <div class="stat"><div class="num">4+</div><div class="lbl">deployed end-to-end projects</div></div>
      <div class="stat"><div class="num">6</div><div class="lbl">ML/cloud certifications</div></div>
    </div>
  </div>
</header>

<section id="about">
  <div class="container about-grid">
    <div class="reveal">
      <span class="section-head tag" style="display:block;margin-bottom:8px;">01 · about</span>
      <h2 style="margin-bottom:16px;">From research notebooks to running APIs</h2>
      <p>I'm an <strong>AI/ML Engineer</strong> based in Chennai, with an M.Sc. in Data Science and hands-on experience across the full ML lifecycle — from model training to containerized deployment.</p>
      <p>I spent a remote internship as a Data Scientist at <strong>Wright Logic (Malaysia)</strong>, and a year as a <strong>Guest Lecturer</strong> teaching data science concepts — which keeps my explanations as clean as my code.</p>
      <p>My focus areas are computer vision pipelines, LLM/RAG-based agent systems, and anomaly detection for industrial sensor data — always with an eye toward what it takes to actually run in production.</p>
    </div>
    <ul class="fact-list reveal">
      <li>M.Sc. Data Science — Periyar University</li>
      <li>B.Sc. Computer Science — Thiruvalluvar University</li>
      <li>Ex-Data Scientist Intern, Wright Logic (Malaysia)</li>
      <li>Ex-Guest Lecturer, Theivanai Ammal College for Women</li>
      <li>IBM · Microsoft · Kaggle certified</li>
    </ul>
  </div>
</section>

<section id="skills">
  <div class="container">
    <div class="section-head reveal">
      <span class="tag">02 · stack</span>
      <h2>Tools I reach for</h2>
      <p>Grouped by domain — brightness roughly maps to how often each one shows up in my projects.</p>
    </div>

    <div class="skill-group reveal">
      <div class="gname">// generative ai & agents</div>
      <div class="skill-row">
        <span class="chip"><span class="heat h4"></span>LangChain</span>
        <span class="chip"><span class="heat h4"></span>LangGraph</span>
        <span class="chip"><span class="heat h3"></span>RAG</span>
        <span class="chip"><span class="heat h3"></span>Vector DBs (FAISS)</span>
        <span class="chip"><span class="heat h2"></span>Multi-Agent Orchestration</span>
      </div>
    </div>

    <div class="skill-group reveal">
      <div class="gname">// ml frameworks</div>
      <div class="skill-row">
        <span class="chip"><span class="heat h4"></span>PyTorch</span>
        <span class="chip"><span class="heat h3"></span>TensorFlow / Keras</span>
        <span class="chip"><span class="heat h4"></span>Scikit-learn</span>
        <span class="chip"><span class="heat h3"></span>XGBoost</span>
        <span class="chip"><span class="heat h3"></span>OpenCV</span>
      </div>
    </div>

    <div class="skill-group reveal">
      <div class="gname">// data & deployment</div>
      <div class="skill-row">
        <span class="chip"><span class="heat h4"></span>Pandas / NumPy</span>
        <span class="chip"><span class="heat h2"></span>SQL / MySQL</span>
        <span class="chip"><span class="heat h3"></span>FastAPI</span>
        <span class="chip"><span class="heat h2"></span>Django</span>
        <span class="chip"><span class="heat h3"></span>Docker</span>
        <span class="chip"><span class="heat h2"></span>AWS</span>
        <span class="chip"><span class="heat h2"></span>Streamlit</span>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="container">
    <div class="section-head reveal">
      <span class="tag">03 · projects</span>
      <h2>Featured repositories</h2>
      <p>Four projects that span the stack — from computer vision to GenAI agents to industrial anomaly detection.</p>
    </div>

    <div class="repo-list">
      <div class="repo-card reveal">
        <div class="repo-top">
          <span class="repo-name">📦 talentpulse</span>
          <div class="repo-meta">
            <span class="lang"><span class="lang-dot" style="background:#3572A5"></span>Python</span>
          </div>
        </div>
        <p class="repo-desc">Hybrid ATS resume screener combining semantic + keyword matching. Uses a Groq-hosted LLM for candidate reasoning, FAISS for retrieval, served through an interactive Streamlit UI.</p>
        <div class="topics"><span class="topic">langchain</span><span class="topic">faiss</span><span class="topic">llm</span><span class="topic">streamlit</span></div>
      </div>

      <div class="repo-card reveal">
        <div class="repo-top">
          <span class="repo-name">📦 pothole-detection-yolov8</span>
          <div class="repo-meta">
            <span class="lang"><span class="lang-dot" style="background:#3572A5"></span>Python</span>
          </div>
        </div>
        <p class="repo-desc">Real-time road hazard detection pipeline built on YOLOv8-Ultralytics, hitting 90% precision. Full OpenCV video pipeline with FFmpeg post-processing for smooth output.</p>
        <div class="topics"><span class="topic">yolov8</span><span class="topic">opencv</span><span class="topic">computer-vision</span><span class="topic">ffmpeg</span></div>
      </div>

      <div class="repo-card reveal">
        <div class="repo-top">
          <span class="repo-name">📦 wind-turbine-intelligence-platform</span>
          <div class="repo-meta">
            <span class="lang"><span class="lang-dot" style="background:#3572A5"></span>Python</span>
          </div>
        </div>
        <p class="repo-desc">Industrial anomaly detection microservice for turbine sensor data. Ensembles Isolation Forest, One-Class SVM, and an LSTM Autoencoder, served via FastAPI.</p>
        <div class="topics"><span class="topic">fastapi</span><span class="topic">anomaly-detection</span><span class="topic">lstm</span><span class="topic">time-series</span></div>
      </div>

      <div class="repo-card reveal">
        <div class="repo-top">
          <span class="repo-name">📦 paintpulse-quant-engine</span>
          <div class="repo-meta">
            <span class="lang"><span class="lang-dot" style="background:#3572A5"></span>Python</span>
          </div>
        </div>
        <p class="repo-desc">XGBoost-powered stock forecasting engine with a live interactive front end, deployed on Hugging Face Spaces.</p>
        <div class="topics"><span class="topic">xgboost</span><span class="topic">forecasting</span><span class="topic">huggingface</span></div>
      </div>
    </div>
  </div>
</section>

<section id="contact">
  <div class="container">
    <div class="contact-card reveal">
      <h2>Let's build something that ships</h2>
      <p>Open to AI/ML Engineer and Data Scientist roles — happy to walk through any project above in detail.</p>
      <div class="contact-links">
        <a href="mailto:your.email@example.com" class="btn btn-primary">✉ Email me</a>
        <a href="https://github.com/Balaji-2001" class="btn btn-ghost">GitHub ↗</a>
        <a href="https://linkedin.com/in/balaji-v-aiml" class="btn btn-ghost">LinkedIn ↗</a>
      </div>
    </div>
  </div>
</section>

<footer class="container">
  <span>© 2026 Balaji V. Built with intent.</span>
  <span class="mono">git commit -m "always be shipping"</span>
</footer>

<script>
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('visible'); io.unobserve(e.target); } });
  },{threshold:0.15});
  document.querySelectorAll('.reveal').forEach(el=>io.observe(el));
</script>

</body>
</html>
