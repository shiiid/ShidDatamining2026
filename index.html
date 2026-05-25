<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>SmartJob Insight — Analitik Ketenagakerjaan Indonesia</title>
  <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>📊</text></svg>">

  <!-- Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

  <!-- Chart.js & Plotly -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>

  <style>
    /* ── VARIABLES ─────────────────────────────────────────── */
    :root {
      --bg:        #060a12;
      --bg2:       #0d1424;
      --bg3:       #111827;
      --border:    #1e293b;
      --border2:   #263246;
      --text:      #e2e8f0;
      --text2:     #94a3b8;
      --text3:     #64748b;
      --accent:    #38bdf8;
      --accent2:   #0ea5e9;
      --green:     #22c55e;
      --yellow:    #f59e0b;
      --red:       #ef4444;
      --purple:    #a855f7;
      --glow:      0 0 40px rgba(56,189,248,0.12);
      --radius:    14px;
      --radius-sm: 8px;
      --font:      'Sora', sans-serif;
      --mono:      'JetBrains Mono', monospace;
      --nav-h:     64px;
    }

    /* ── RESET ──────────────────────────────────────────────── */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      font-family: var(--font);
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
      min-height: 100vh;
      overflow-x: hidden;
    }
    ::selection { background: rgba(56,189,248,0.25); }

    /* ── SCROLLBAR ──────────────────────────────────────────── */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: var(--bg2); }
    ::-webkit-scrollbar-thumb { background: var(--border2); border-radius: 3px; }

    /* ── NOISE TEXTURE ──────────────────────────────────────── */
    body::before {
      content: '';
      position: fixed; inset: 0; pointer-events: none; z-index: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.03'/%3E%3C/svg%3E");
      opacity: 0.4;
    }

    /* ── NAV ────────────────────────────────────────────────── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      height: var(--nav-h);
      display: flex; align-items: center; justify-content: space-between;
      padding: 0 32px;
      background: rgba(6,10,18,0.85);
      backdrop-filter: blur(20px);
      border-bottom: 1px solid var(--border);
    }
    .nav-logo {
      display: flex; align-items: center; gap: 10px;
      font-size: 1.1rem; font-weight: 700; color: var(--text);
      text-decoration: none;
    }
    .nav-logo span { color: var(--accent); }
    .nav-logo .dot {
      width: 8px; height: 8px; border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 8px var(--accent);
      animation: pulse 2s infinite;
    }
    @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:.6;transform:scale(.85)} }

    .nav-links { display: flex; gap: 4px; }
    .nav-links a {
      padding: 6px 14px; border-radius: 8px;
      color: var(--text2); font-size: .875rem; font-weight: 500;
      text-decoration: none; transition: all .2s;
      cursor: pointer;
    }
    .nav-links a:hover, .nav-links a.active {
      background: rgba(56,189,248,0.1);
      color: var(--accent);
    }
    .nav-badge {
      padding: 4px 10px; border-radius: 6px;
      background: rgba(56,189,248,0.1); border: 1px solid rgba(56,189,248,0.2);
      color: var(--accent); font-size: .75rem; font-weight: 600;
      font-family: var(--mono);
    }

    /* ── MAIN LAYOUT ────────────────────────────────────────── */
    main {
      padding-top: var(--nav-h);
      min-height: 100vh;
      position: relative; z-index: 1;
    }

    .page { display: none; padding: 40px 32px; max-width: 1200px; margin: 0 auto; }
    .page.active { display: block; }

    /* ── HERO ───────────────────────────────────────────────── */
    .hero {
      padding: 80px 32px 60px;
      text-align: center;
      position: relative; overflow: hidden;
    }
    .hero-glow {
      position: absolute; top: 50%; left: 50%;
      transform: translate(-50%,-50%);
      width: 600px; height: 400px;
      background: radial-gradient(ellipse, rgba(56,189,248,0.08) 0%, transparent 70%);
      pointer-events: none;
    }
    .hero-badge {
      display: inline-flex; align-items: center; gap: 8px;
      padding: 6px 16px; border-radius: 20px;
      background: rgba(56,189,248,0.08);
      border: 1px solid rgba(56,189,248,0.2);
      color: var(--accent); font-size: .8rem; font-weight: 600;
      margin-bottom: 24px;
      animation: fadeUp .6s ease both;
    }
    .hero h1 {
      font-size: clamp(2.2rem, 5vw, 3.8rem);
      font-weight: 800; line-height: 1.15;
      letter-spacing: -0.02em;
      background: linear-gradient(135deg, #fff 30%, var(--accent) 100%);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
      animation: fadeUp .7s .1s ease both;
    }
    .hero p {
      margin-top: 20px; font-size: 1.1rem;
      color: var(--text2); max-width: 600px; margin-left: auto; margin-right: auto;
      animation: fadeUp .7s .2s ease both;
    }
    .hero-cta {
      margin-top: 36px; display: flex; gap: 12px;
      justify-content: center; flex-wrap: wrap;
      animation: fadeUp .7s .3s ease both;
    }
    @keyframes fadeUp {
      from { opacity:0; transform:translateY(20px); }
      to { opacity:1; transform:translateY(0); }
    }

    /* ── BUTTONS ────────────────────────────────────────────── */
    .btn {
      padding: 10px 22px; border-radius: 10px;
      font-family: var(--font); font-size: .9rem; font-weight: 600;
      border: none; cursor: pointer; transition: all .2s;
      display: inline-flex; align-items: center; gap: 8px;
      text-decoration: none;
    }
    .btn-primary {
      background: var(--accent); color: #000;
      box-shadow: 0 0 20px rgba(56,189,248,0.3);
    }
    .btn-primary:hover { background: #7dd3fc; transform: translateY(-1px); }
    .btn-ghost {
      background: var(--bg3); color: var(--text);
      border: 1px solid var(--border2);
    }
    .btn-ghost:hover { border-color: var(--accent); color: var(--accent); }
    .btn-danger { background: var(--red); color: #fff; }
    .btn-sm { padding: 6px 14px; font-size: .8rem; border-radius: 8px; }

    /* ── CARDS ──────────────────────────────────────────────── */
    .card {
      background: var(--bg2);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 24px;
      transition: border-color .2s;
    }
    .card:hover { border-color: var(--border2); }
    .card-glow:hover { border-color: rgba(56,189,248,0.3); box-shadow: var(--glow); }

    .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
    .grid-3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
    .grid-4 { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; }

    @media (max-width: 768px) {
      .grid-2, .grid-3, .grid-4 { grid-template-columns: 1fr; }
      nav { padding: 0 16px; }
      .page { padding: 24px 16px; }
      .hero { padding: 60px 16px 40px; }
      .nav-links { gap: 2px; }
      .nav-links a { padding: 6px 10px; font-size: .8rem; }
    }

    /* ── STAT CARDS ─────────────────────────────────────────── */
    .stat-card {
      background: var(--bg2); border: 1px solid var(--border);
      border-radius: var(--radius); padding: 20px;
      position: relative; overflow: hidden;
    }
    .stat-card::before {
      content: '';
      position: absolute; top: 0; left: 0; right: 0; height: 2px;
    }
    .stat-card.blue::before { background: linear-gradient(90deg, var(--accent), transparent); }
    .stat-card.green::before { background: linear-gradient(90deg, var(--green), transparent); }
    .stat-card.yellow::before { background: linear-gradient(90deg, var(--yellow), transparent); }
    .stat-card.purple::before { background: linear-gradient(90deg, var(--purple), transparent); }

    .stat-label { font-size: .75rem; font-weight: 600; color: var(--text3); text-transform: uppercase; letter-spacing: .08em; }
    .stat-value { font-size: 2rem; font-weight: 800; margin: 8px 0 4px; font-family: var(--mono); }
    .stat-value.blue { color: var(--accent); }
    .stat-value.green { color: var(--green); }
    .stat-value.yellow { color: var(--yellow); }
    .stat-value.purple { color: var(--purple); }
    .stat-sub { font-size: .8rem; color: var(--text3); }

    /* ── SECTION HEADERS ────────────────────────────────────── */
    .section-header { margin-bottom: 24px; }
    .section-header h2 { font-size: 1.4rem; font-weight: 700; }
    .section-header p { color: var(--text2); font-size: .9rem; margin-top: 4px; }

    /* ── CHART CONTAINERS ───────────────────────────────────── */
    .chart-wrap {
      position: relative; width: 100%;
      background: var(--bg2); border: 1px solid var(--border);
      border-radius: var(--radius); padding: 20px;
    }
    .chart-title { font-size: .9rem; font-weight: 600; color: var(--text2); margin-bottom: 16px; }
    canvas { max-height: 300px; }

    /* ── TABLE ──────────────────────────────────────────────── */
    .table-wrap { overflow-x: auto; }
    table { width: 100%; border-collapse: collapse; font-size: .875rem; }
    th {
      background: var(--bg3); color: var(--text3);
      font-weight: 600; font-size: .75rem; text-transform: uppercase; letter-spacing: .05em;
      padding: 10px 14px; text-align: left; border-bottom: 1px solid var(--border);
    }
    td { padding: 10px 14px; border-bottom: 1px solid var(--border); color: var(--text2); }
    tr:hover td { background: rgba(255,255,255,.02); }
    tr:last-child td { border-bottom: none; }

    /* ── BADGE ──────────────────────────────────────────────── */
    .badge {
      display: inline-flex; align-items: center; gap: 4px;
      padding: 3px 9px; border-radius: 6px;
      font-size: .72rem; font-weight: 700;
    }
    .badge-rendah { background: rgba(34,197,94,.12); color: #22c55e; }
    .badge-sedang { background: rgba(245,158,11,.12); color: #f59e0b; }
    .badge-tinggi { background: rgba(239,68,68,.12); color: #ef4444; }
    .badge-sangat { background: rgba(168,85,247,.12); color: #a855f7; }
    .badge-blue { background: rgba(56,189,248,.12); color: #38bdf8; }

    /* ── FORM ───────────────────────────────────────────────── */
    .form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
    @media (max-width: 600px) { .form-grid { grid-template-columns: 1fr; } }

    .form-group { display: flex; flex-direction: column; gap: 6px; }
    label { font-size: .8rem; font-weight: 600; color: var(--text2); }
    input[type="number"], input[type="text"], select {
      background: var(--bg3); border: 1px solid var(--border2);
      border-radius: var(--radius-sm); color: var(--text);
      font-family: var(--mono); font-size: .9rem;
      padding: 10px 14px; outline: none; transition: border-color .2s;
      width: 100%;
    }
    input:focus, select:focus { border-color: var(--accent); }
    .input-hint { font-size: .72rem; color: var(--text3); }

    /* ── FILE DROP ──────────────────────────────────────────── */
    .drop-zone {
      border: 2px dashed var(--border2); border-radius: var(--radius);
      padding: 40px 20px; text-align: center;
      cursor: pointer; transition: all .2s;
      background: var(--bg2);
    }
    .drop-zone:hover, .drop-zone.over {
      border-color: var(--accent);
      background: rgba(56,189,248,.04);
    }
    .drop-icon { font-size: 2.5rem; margin-bottom: 12px; }
    .drop-title { font-size: 1rem; font-weight: 600; margin-bottom: 4px; }
    .drop-sub { font-size: .85rem; color: var(--text3); }
    #file-input { display: none; }

    /* ── PREDICTION RESULT ──────────────────────────────────── */
    .pred-result {
      background: var(--bg2); border: 1px solid var(--border);
      border-radius: var(--radius); padding: 24px;
      animation: fadeUp .4s ease;
    }
    .pred-tpt {
      font-size: 3rem; font-weight: 800;
      font-family: var(--mono);
    }
    .pred-label { font-size: .85rem; color: var(--text3); margin-top: 4px; }

    /* ── CLUSTER CARD ───────────────────────────────────────── */
    .cluster-card {
      background: var(--bg2); border: 1px solid var(--border);
      border-radius: var(--radius); padding: 20px;
    }
    .cluster-id {
      width: 36px; height: 36px; border-radius: 8px;
      display: flex; align-items: center; justify-content: center;
      font-weight: 800; font-size: .9rem; margin-bottom: 12px;
    }

    /* ── LOADER ─────────────────────────────────────────────── */
    .spinner {
      display: inline-block; width: 20px; height: 20px;
      border: 2px solid rgba(56,189,248,.3);
      border-top-color: var(--accent);
      border-radius: 50%;
      animation: spin .6s linear infinite;
    }
    @keyframes spin { to { transform: rotate(360deg); } }

    .loading-state {
      display: flex; flex-direction: column;
      align-items: center; gap: 16px;
      padding: 60px 20px; color: var(--text3);
      font-size: .9rem;
    }

    /* ── HEATMAP ────────────────────────────────────────────── */
    .heatmap-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 8px;
    }
    .heatmap-cell {
      padding: 12px 14px; border-radius: 10px;
      border: 1px solid var(--border);
      cursor: pointer; transition: all .2s;
    }
    .heatmap-cell:hover { transform: scale(1.02); box-shadow: 0 4px 20px rgba(0,0,0,.3); }
    .heatmap-prov { font-size: .78rem; font-weight: 600; margin-bottom: 4px; }
    .heatmap-val { font-size: 1.2rem; font-weight: 800; font-family: var(--mono); }

    /* ── PROGRESS BAR ───────────────────────────────────────── */
    .progress-bar {
      height: 6px; border-radius: 3px;
      background: var(--border2); overflow: hidden;
    }
    .progress-fill {
      height: 100%; border-radius: 3px;
      transition: width .6s ease;
    }

    /* ── TOAST ──────────────────────────────────────────────── */
    #toast-container {
      position: fixed; bottom: 24px; right: 24px; z-index: 999;
      display: flex; flex-direction: column; gap: 8px;
    }
    .toast {
      background: var(--bg3); border: 1px solid var(--border2);
      border-radius: 10px; padding: 12px 16px;
      font-size: .85rem; color: var(--text);
      box-shadow: 0 8px 32px rgba(0,0,0,.4);
      animation: slideIn .3s ease;
      max-width: 320px;
    }
    @keyframes slideIn { from{transform:translateX(100%);opacity:0} to{transform:none;opacity:1} }

    /* ── API STATUS INDICATOR ───────────────────────────────── */
    .api-status {
      display: flex; align-items: center; gap: 8px;
      font-size: .78rem; color: var(--text3);
      padding: 6px 12px; border-radius: 6px;
      background: var(--bg3); border: 1px solid var(--border);
    }
    .api-dot { width: 7px; height: 7px; border-radius: 50%; }
    .api-dot.online { background: var(--green); box-shadow: 0 0 6px var(--green); }
    .api-dot.offline { background: var(--red); }
    .api-dot.checking { background: var(--yellow); animation: pulse 1s infinite; }

    /* ── SECTOR LIST ────────────────────────────────────────── */
    .sector-list { list-style: none; display: flex; flex-direction: column; gap: 8px; }
    .sector-item {
      display: flex; align-items: center; gap: 10px;
      padding: 10px 14px; border-radius: 8px;
      background: rgba(56,189,248,.04); border: 1px solid rgba(56,189,248,.1);
      font-size: .875rem;
    }
    .sector-num {
      width: 22px; height: 22px; border-radius: 5px;
      background: var(--accent); color: #000;
      font-size: .7rem; font-weight: 800;
      display: flex; align-items: center; justify-content: center;
      flex-shrink: 0;
    }
  </style>
</head>
<body>

<!-- ─── NAV ──────────────────────────────────────────────────── -->
<nav>
  <a class="nav-logo" href="#" onclick="showPage('home')">
    <div class="dot"></div>
    Smart<span>Job</span> Insight
  </a>
  <div class="nav-links">
    <a onclick="showPage('home')" class="active" id="nav-home">🏠 Beranda</a>
    <a onclick="showPage('dashboard')" id="nav-dashboard">📊 Dashboard</a>
    <a onclick="showPage('predict')" id="nav-predict">🔮 Prediksi</a>
    <a onclick="showPage('cluster')" id="nav-cluster">🔵 Klaster</a>
    <a onclick="showPage('heatmap')" id="nav-heatmap">🗺️ Peta</a>
    <a onclick="showPage('upload')" id="nav-upload">📤 Upload</a>
  </div>
  <div id="api-status-badge" class="api-status">
    <div class="api-dot checking" id="api-dot"></div>
    <span id="api-status-text">Menghubungkan...</span>
  </div>
</nav>

<!-- ─── MAIN ──────────────────────────────────────────────────── -->
<main>

  <!-- ════════════════════ HOME PAGE ════════════════════════ -->
  <div id="page-home" class="page active" style="padding:0; max-width:100%;">
    <div class="hero">
      <div class="hero-glow"></div>
      <div class="hero-badge">📊 Mata Kuliah Data Mining · FMIPA UNNES 2025/2026</div>
      <h1>Analitik Ketenagakerjaan<br>Indonesia Berbasis AI</h1>
      <p>Platform data mining untuk prediksi Tingkat Pengangguran Terbuka (TPT) dan pengelompokan wilayah menggunakan Random Forest & K-Means Clustering — data resmi BPS 2014–2024.</p>
      <div class="hero-cta">
        <button class="btn btn-primary" onclick="showPage('dashboard')">📊 Lihat Dashboard</button>
        <button class="btn btn-ghost" onclick="showPage('predict')">🔮 Coba Prediksi</button>
        <a href="https://github.com/USERNAME/smartjob-insight" target="_blank" class="btn btn-ghost">⭐ GitHub</a>
      </div>
    </div>

    <!-- Feature cards -->
    <div style="max-width:1200px;margin:0 auto;padding:0 32px 60px;">
      <div class="grid-3" style="margin-top:8px;">
        <div class="card card-glow" style="animation:fadeUp .6s .1s ease both;opacity:0;">
          <div style="font-size:2rem;margin-bottom:12px;">🌲</div>
          <h3 style="font-size:1rem;font-weight:700;margin-bottom:6px;">Random Forest</h3>
          <p style="font-size:.85rem;color:var(--text2);">Prediksi TPT dengan akurasi target >85% menggunakan indikator IPM, UMP, kemiskinan, dan pertumbuhan ekonomi.</p>
          <div style="margin-top:16px;display:flex;gap:8px;flex-wrap:wrap;">
            <span class="badge badge-blue">RMSE &lt; 1.0</span>
            <span class="badge badge-blue">R² &gt; 0.80</span>
          </div>
        </div>
        <div class="card card-glow" style="animation:fadeUp .6s .2s ease both;opacity:0;">
          <div style="font-size:2rem;margin-bottom:12px;">🔵</div>
          <h3 style="font-size:1rem;font-weight:700;margin-bottom:6px;">K-Means Clustering</h3>
          <p style="font-size:.85rem;color:var(--text2);">Pengelompokan 34 provinsi berdasarkan profil ketenagakerjaan untuk rekomendasi sektor potensial.</p>
          <div style="margin-top:16px;display:flex;gap:8px;flex-wrap:wrap;">
            <span class="badge badge-blue">Silhouette &gt; 0.5</span>
            <span class="badge badge-blue">4–5 Klaster</span>
          </div>
        </div>
        <div class="card card-glow" style="animation:fadeUp .6s .3s ease both;opacity:0;">
          <div style="font-size:2rem;margin-bottom:12px;">📤</div>
          <h3 style="font-size:1rem;font-weight:700;margin-bottom:6px;">Upload Dataset BPS</h3>
          <p style="font-size:.85rem;color:var(--text2);">Upload data CSV/Excel Anda sendiri dari BPS untuk mendapatkan analisis dan prediksi yang dipersonalisasi.</p>
          <div style="margin-top:16px;display:flex;gap:8px;flex-wrap:wrap;">
            <span class="badge badge-blue">CSV</span>
            <span class="badge badge-blue">Excel .xlsx</span>
          </div>
        </div>
      </div>

      <!-- Tech stack -->
      <div style="margin-top:48px;text-align:center;">
        <p style="font-size:.8rem;color:var(--text3);text-transform:uppercase;letter-spacing:.1em;margin-bottom:16px;">Teknologi</p>
        <div style="display:flex;flex-wrap:wrap;gap:10px;justify-content:center;">
          <span class="badge badge-blue" style="padding:6px 14px;font-size:.8rem;">Python 3.11</span>
          <span class="badge badge-blue" style="padding:6px 14px;font-size:.8rem;">Scikit-Learn</span>
          <span class="badge badge-blue" style="padding:6px 14px;font-size:.8rem;">FastAPI</span>
          <span class="badge badge-blue" style="padding:6px 14px;font-size:.8rem;">Chart.js</span>
          <span class="badge badge-blue" style="padding:6px 14px;font-size:.8rem;">BPS Data</span>
          <span class="badge badge-blue" style="padding:6px 14px;font-size:.8rem;">Docker</span>
        </div>
      </div>
    </div>
  </div>

  <!-- ════════════════════ DASHBOARD ═════════════════════════ -->
  <div id="page-dashboard" class="page" style="max-width:1200px;">
    <div class="section-header">
      <h2>Dashboard Nasional</h2>
      <p>Ringkasan kondisi ketenagakerjaan Indonesia berdasarkan data BPS</p>
    </div>

    <!-- Stat Cards -->
    <div class="grid-4" id="stat-cards">
      <div class="stat-card blue">
        <div class="stat-label">TPT Nasional</div>
        <div class="stat-value blue" id="stat-tpt">—</div>
        <div class="stat-sub">Tingkat Pengangguran Terbuka</div>
      </div>
      <div class="stat-card green">
        <div class="stat-label">IPM Nasional</div>
        <div class="stat-value green" id="stat-ipm">—</div>
        <div class="stat-sub">Indeks Pembangunan Manusia</div>
      </div>
      <div class="stat-card yellow">
        <div class="stat-label">UMP Rata-rata</div>
        <div class="stat-value yellow" id="stat-ump">—</div>
        <div class="stat-sub">Upah Minimum (juta Rp)</div>
      </div>
      <div class="stat-card purple">
        <div class="stat-label">Kemiskinan</div>
        <div class="stat-value purple" id="stat-kemiskinan">—</div>
        <div class="stat-sub">Tingkat kemiskinan (%)</div>
      </div>
    </div>

    <!-- Charts -->
    <div class="grid-2" style="margin-top:20px;">
      <div class="chart-wrap">
        <div class="chart-title">📈 Tren TPT Nasional 2014–2024</div>
        <canvas id="chart-trend"></canvas>
      </div>
      <div class="chart-wrap">
        <div class="chart-title">🏆 10 Provinsi TPT Tertinggi (Terbaru)</div>
        <canvas id="chart-top10"></canvas>
      </div>
    </div>

    <!-- Province Table -->
    <div class="card" style="margin-top:20px;">
      <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:16px;">
        <div style="font-weight:600;">📋 Data Semua Provinsi</div>
        <input type="text" id="search-prov" placeholder="Cari provinsi..." style="width:200px;padding:6px 12px;font-size:.8rem;">
      </div>
      <div class="table-wrap">
        <table id="province-table">
          <thead>
            <tr>
              <th>Provinsi</th>
              <th>TPT (%)</th>
              <th>IPM</th>
              <th>UMP (Juta)</th>
              <th>Kemiskinan (%)</th>
              <th>Status Risiko</th>
              <th>Klaster</th>
            </tr>
          </thead>
          <tbody id="province-tbody">
            <tr><td colspan="7" style="text-align:center;padding:24px;color:var(--text3);">
              <div class="spinner"></div> Memuat data...
            </td></tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>

  <!-- ════════════════════ PREDIKSI ══════════════════════════ -->
  <div id="page-predict" class="page" style="max-width:900px;">
    <div class="section-header">
      <h2>🔮 Prediksi Peluang Kerja</h2>
      <p>Masukkan indikator sosio-ekonomi wilayah untuk mendapatkan prediksi TPT dan rekomendasi sektor</p>
    </div>

    <div class="grid-2" style="align-items:start;gap:24px;">
      <!-- Form -->
      <div class="card">
        <div style="font-weight:700;margin-bottom:20px;">Input Indikator</div>

        <div style="margin-bottom:14px;">
          <label>Provinsi (opsional)</label>
          <select id="pred-provinsi" style="margin-top:6px;">
            <option value="">— Pilih Provinsi —</option>
          </select>
        </div>

        <div class="form-grid">
          <div class="form-group">
            <label>IPM (Indeks Pembangunan Manusia)</label>
            <input type="number" id="pred-ipm" value="70" min="50" max="100" step="0.1">
            <span class="input-hint">Skala 0–100. Nasional 2023: ±73.55</span>
          </div>
          <div class="form-group">
            <label>UMP (Juta Rp)</label>
            <input type="number" id="pred-ump" value="2.5" min="0.5" max="10" step="0.1">
            <span class="input-hint">Upah Minimum Provinsi</span>
          </div>
          <div class="form-group">
            <label>Kemiskinan (%)</label>
            <input type="number" id="pred-kemiskinan" value="10" min="0" max="40" step="0.1">
            <span class="input-hint">Tingkat kemiskinan penduduk</span>
          </div>
          <div class="form-group">
            <label>Pertumbuhan PDRB (%)</label>
            <input type="number" id="pred-pdrb" value="5" min="-10" max="15" step="0.1">
            <span class="input-hint">Pertumbuhan ekonomi daerah</span>
          </div>
          <div class="form-group">
            <label>Rata-rata Lama Sekolah (tahun)</label>
            <input type="number" id="pred-rls" value="8" min="4" max="15" step="0.1">
            <span class="input-hint">Rata-rata pendidikan penduduk</span>
          </div>
          <div class="form-group">
            <label>Tahun Prediksi</label>
            <input type="number" id="pred-tahun" value="2025" min="2014" max="2030">
            <span class="input-hint">Tahun target prediksi</span>
          </div>
        </div>

        <button class="btn btn-primary" style="width:100%;margin-top:20px;justify-content:center;" onclick="runPrediction()">
          🔮 Prediksi Sekarang
        </button>
      </div>

      <!-- Result -->
      <div id="pred-result-area">
        <div class="pred-result" style="background:var(--bg2);border:1px solid var(--border);border-radius:var(--radius);padding:24px;min-height:200px;display:flex;align-items:center;justify-content:center;">
          <div style="text-align:center;color:var(--text3);">
            <div style="font-size:2rem;margin-bottom:12px;">🔮</div>
            <p>Isi form dan klik <strong>Prediksi Sekarang</strong><br>untuk melihat hasil analisis</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Feature Importance -->
    <div class="chart-wrap" style="margin-top:20px;">
      <div class="chart-title">🌟 Feature Importance — Faktor Paling Berpengaruh</div>
      <canvas id="chart-fi" style="max-height:200px;"></canvas>
    </div>
  </div>

  <!-- ════════════════════ KLASTER ═══════════════════════════ -->
  <div id="page-cluster" class="page" style="max-width:1200px;">
    <div class="section-header">
      <h2>🔵 Klasterisasi Wilayah</h2>
      <p>Pengelompokan 34 provinsi berdasarkan profil ketenagakerjaan menggunakan K-Means Clustering</p>
    </div>

    <div id="cluster-content">
      <div class="loading-state">
        <div class="spinner"></div>
        Memuat data klaster...
      </div>
    </div>
  </div>

  <!-- ════════════════════ HEATMAP ═══════════════════════════ -->
  <div id="page-heatmap" class="page" style="max-width:1200px;">
    <div class="section-header" style="display:flex;align-items:start;justify-content:space-between;flex-wrap:wrap;gap:12px;">
      <div>
        <h2>🗺️ Peta Sebaran Ketenagakerjaan</h2>
        <p>Distribusi indikator per provinsi di Indonesia</p>
      </div>
      <div style="display:flex;gap:10px;align-items:center;">
        <label style="font-size:.8rem;">Variabel:</label>
        <select id="heatmap-var" onchange="loadHeatmap()" style="padding:6px 12px;font-size:.85rem;">
          <option value="tpt_pct">TPT (%)</option>
          <option value="ipm">IPM</option>
          <option value="kemiskinan_pct">Kemiskinan (%)</option>
          <option value="ump_juta">UMP (Juta Rp)</option>
          <option value="pdrb_growth">Pertumbuhan PDRB (%)</option>
        </select>
      </div>
    </div>

    <!-- Color legend -->
    <div style="display:flex;align-items:center;gap:12px;margin-bottom:20px;">
      <span style="font-size:.8rem;color:var(--text3);">Rendah</span>
      <div style="flex:1;height:12px;border-radius:6px;background:linear-gradient(90deg,#22c55e,#f59e0b,#ef4444);"></div>
      <span style="font-size:.8rem;color:var(--text3);">Tinggi</span>
    </div>

    <div id="heatmap-grid" class="heatmap-grid">
      <div class="loading-state"><div class="spinner"></div></div>
    </div>

    <!-- Comparison Chart -->
    <div class="chart-wrap" style="margin-top:24px;">
      <div class="chart-title">📊 Perbandingan Antar Provinsi</div>
      <canvas id="chart-compare" style="max-height:350px;"></canvas>
    </div>
  </div>

  <!-- ════════════════════ UPLOAD ════════════════════════════ -->
  <div id="page-upload" class="page" style="max-width:900px;">
    <div class="section-header">
      <h2>📤 Upload Dataset BPS</h2>
      <p>Upload data CSV atau Excel dari BPS untuk mendapatkan analisis langsung</p>
    </div>

    <!-- Format info -->
    <div class="card" style="margin-bottom:20px;border-color:rgba(56,189,248,.2);">
      <div style="font-weight:600;color:var(--accent);margin-bottom:12px;">📋 Format yang Didukung</div>
      <div class="grid-2">
        <div>
          <p style="font-size:.8rem;font-weight:600;color:var(--text3);margin-bottom:8px;">KOLOM WAJIB</p>
          <div style="display:flex;flex-direction:column;gap:4px;">
            <code style="background:var(--bg3);padding:4px 8px;border-radius:4px;font-size:.8rem;"><span style="color:var(--green)">provinsi</span> — Nama provinsi</code>
            <code style="background:var(--bg3);padding:4px 8px;border-radius:4px;font-size:.8rem;"><span style="color:var(--green)">tahun</span> — Tahun data</code>
            <code style="background:var(--bg3);padding:4px 8px;border-radius:4px;font-size:.8rem;"><span style="color:var(--green)">tpt_pct</span> — TPT dalam %</code>
          </div>
        </div>
        <div>
          <p style="font-size:.8rem;font-weight:600;color:var(--text3);margin-bottom:8px;">KOLOM OPSIONAL</p>
          <div style="display:flex;flex-direction:column;gap:4px;">
            <code style="background:var(--bg3);padding:4px 8px;border-radius:4px;font-size:.8rem;color:var(--text2);">ipm, ump_juta, kemiskinan_pct</code>
            <code style="background:var(--bg3);padding:4px 8px;border-radius:4px;font-size:.8rem;color:var(--text2);">pdrb_growth, rls_tahun, semester</code>
          </div>
          <div style="margin-top:12px;">
            <a href="data/sample/tpt_provinsi.csv" download class="btn btn-ghost btn-sm">⬇ Unduh Template</a>
          </div>
        </div>
      </div>
    </div>

    <!-- Drop Zone -->
    <div class="drop-zone" id="drop-zone" onclick="document.getElementById('file-input').click()">
      <div class="drop-icon">📂</div>
      <div class="drop-title">Seret & Lepas file di sini</div>
      <div class="drop-sub">atau klik untuk memilih file CSV / Excel</div>
      <input type="file" id="file-input" accept=".csv,.xlsx,.xls" onchange="handleFileSelect(this.files[0])">
    </div>

    <!-- Upload result -->
    <div id="upload-result" style="margin-top:20px;display:none;"></div>
  </div>

</main>

<!-- Toast container -->
<div id="toast-container"></div>

<script>
// ═══════════════════════════════════════════════════════════════
//  CONFIG
// ═══════════════════════════════════════════════════════════════

const API_URL = window.location.hostname === 'localhost' || window.location.hostname === '127.0.0.1'
  ? 'http://localhost:8000'
  : ''; // same origin when deployed together

// Demo mode — fallback data jika API tidak tersedia
let API_ONLINE = false;
let DEMO_DATA = null;

// ═══════════════════════════════════════════════════════════════
//  DEMO / FALLBACK DATA (dari sample CSV)
// ═══════════════════════════════════════════════════════════════

const PROVINCES_DATA = [
  {provinsi:"Aceh",kode_bps:11,tpt_pct:5.12,ipm:74.10,ump_juta:3.90,kemiskinan_pct:13.85,pdrb_growth:5.01,risiko_label:"Sedang",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Sumatera Utara",kode_bps:12,tpt_pct:4.95,ipm:74.22,ump_juta:3.20,kemiskinan_pct:7.75,pdrb_growth:5.08,risiko_label:"Sedang",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Sumatera Barat",kode_bps:13,tpt_pct:5.05,ipm:73.5,ump_juta:2.80,kemiskinan_pct:5.8,pdrb_growth:4.9,risiko_label:"Sedang",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Riau",kode_bps:14,tpt_pct:4.12,ipm:73.3,ump_juta:3.20,kemiskinan_pct:6.5,pdrb_growth:4.2,risiko_label:"Sedang",klaster_label:"Wilayah Potensi Tinggi"},
  {provinsi:"Jambi",kode_bps:15,tpt_pct:4.31,ipm:72.0,ump_juta:2.80,kemiskinan_pct:7.5,pdrb_growth:4.7,risiko_label:"Sedang",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Sumatera Selatan",kode_bps:16,tpt_pct:4.15,ipm:71.7,ump_juta:3.50,kemiskinan_pct:11.5,pdrb_growth:5.1,risiko_label:"Sedang",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Bengkulu",kode_bps:17,tpt_pct:3.18,ipm:71.5,ump_juta:2.50,kemiskinan_pct:14.2,pdrb_growth:4.5,risiko_label:"Rendah",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Lampung",kode_bps:18,tpt_pct:4.38,ipm:70.4,ump_juta:2.80,kemiskinan_pct:11.1,pdrb_growth:5.0,risiko_label:"Sedang",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Kepulauan Bangka Belitung",kode_bps:19,tpt_pct:4.11,ipm:72.6,ump_juta:3.50,kemiskinan_pct:4.4,pdrb_growth:4.2,risiko_label:"Sedang",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Kepulauan Riau",kode_bps:21,tpt_pct:6.85,ipm:76.5,ump_juta:3.40,kemiskinan_pct:5.9,pdrb_growth:5.3,risiko_label:"Tinggi",klaster_label:"Wilayah Maju"},
  {provinsi:"DKI Jakarta",kode_bps:31,tpt_pct:6.12,ipm:82.78,ump_juta:5.37,kemiskinan_pct:4.25,pdrb_growth:5.12,risiko_label:"Tinggi",klaster_label:"Wilayah Maju"},
  {provinsi:"Jawa Barat",kode_bps:32,tpt_pct:7.21,ipm:74.28,ump_juta:2.36,kemiskinan_pct:7.32,pdrb_growth:5.08,risiko_label:"Tinggi",klaster_label:"Wilayah Maju"},
  {provinsi:"Jawa Tengah",kode_bps:33,tpt_pct:5.01,ipm:73.90,ump_juta:2.23,kemiskinan_pct:10.01,pdrb_growth:5.10,risiko_label:"Sedang",klaster_label:"Wilayah Berkembang"},
  {provinsi:"DI Yogyakarta",kode_bps:34,tpt_pct:3.48,ipm:80.2,ump_juta:2.10,kemiskinan_pct:12.0,pdrb_growth:5.5,risiko_label:"Rendah",klaster_label:"Wilayah Maju"},
  {provinsi:"Jawa Timur",kode_bps:35,tpt_pct:4.62,ipm:73.82,ump_juta:2.31,kemiskinan_pct:9.78,pdrb_growth:5.07,risiko_label:"Sedang",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Banten",kode_bps:36,tpt_pct:7.28,ipm:73.3,ump_juta:3.00,kemiskinan_pct:5.9,pdrb_growth:5.0,risiko_label:"Tinggi",klaster_label:"Wilayah Maju"},
  {provinsi:"Bali",kode_bps:51,tpt_pct:2.53,ipm:78.32,ump_juta:3.10,kemiskinan_pct:3.68,pdrb_growth:5.91,risiko_label:"Rendah",klaster_label:"Wilayah Maju"},
  {provinsi:"Nusa Tenggara Barat",kode_bps:52,tpt_pct:3.70,ipm:69.5,ump_juta:2.40,kemiskinan_pct:13.2,pdrb_growth:4.8,risiko_label:"Rendah",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Nusa Tenggara Timur",kode_bps:53,tpt_pct:3.38,ipm:67.75,ump_juta:2.42,kemiskinan_pct:19.54,pdrb_growth:5.74,risiko_label:"Rendah",klaster_label:"Wilayah Perlu Prioritas"},
  {provinsi:"Kalimantan Barat",kode_bps:61,tpt_pct:4.81,ipm:70.5,ump_juta:2.70,kemiskinan_pct:7.0,pdrb_growth:5.1,risiko_label:"Sedang",klaster_label:"Wilayah Potensi Tinggi"},
  {provinsi:"Kalimantan Tengah",kode_bps:62,tpt_pct:3.95,ipm:72.2,ump_juta:3.20,kemiskinan_pct:5.2,pdrb_growth:5.8,risiko_label:"Rendah",klaster_label:"Wilayah Potensi Tinggi"},
  {provinsi:"Kalimantan Selatan",kode_bps:63,tpt_pct:3.94,ipm:72.9,ump_juta:3.20,kemiskinan_pct:4.5,pdrb_growth:5.2,risiko_label:"Rendah",klaster_label:"Wilayah Potensi Tinggi"},
  {provinsi:"Kalimantan Timur",kode_bps:64,tpt_pct:5.21,ipm:78.62,ump_juta:3.55,kemiskinan_pct:5.88,pdrb_growth:6.41,risiko_label:"Sedang",klaster_label:"Wilayah Maju"},
  {provinsi:"Kalimantan Utara",kode_bps:65,tpt_pct:4.02,ipm:72.1,ump_juta:3.30,kemiskinan_pct:6.1,pdrb_growth:4.8,risiko_label:"Sedang",klaster_label:"Wilayah Potensi Tinggi"},
  {provinsi:"Sulawesi Utara",kode_bps:71,tpt_pct:6.02,ipm:74.5,ump_juta:3.50,kemiskinan_pct:7.3,pdrb_growth:5.5,risiko_label:"Tinggi",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Sulawesi Tengah",kode_bps:72,tpt_pct:2.80,ipm:70.8,ump_juta:2.80,kemiskinan_pct:12.3,pdrb_growth:8.2,risiko_label:"Rendah",klaster_label:"Wilayah Potensi Tinggi"},
  {provinsi:"Sulawesi Selatan",kode_bps:73,tpt_pct:4.95,ipm:74.0,ump_juta:3.40,kemiskinan_pct:8.6,pdrb_growth:5.8,risiko_label:"Sedang",klaster_label:"Wilayah Berkembang"},
  {provinsi:"Sulawesi Tenggara",kode_bps:74,tpt_pct:3.07,ipm:72.0,ump_juta:2.80,kemiskinan_pct:11.1,pdrb_growth:5.9,risiko_label:"Rendah",klaster_label:"Wilayah Potensi Tinggi"},
  {provinsi:"Gorontalo",kode_bps:75,tpt_pct:3.19,ipm:69.3,ump_juta:2.90,kemiskinan_pct:15.1,pdrb_growth:5.2,risiko_label:"Rendah",klaster_label:"Wilayah Perlu Prioritas"},
  {provinsi:"Sulawesi Barat",kode_bps:76,tpt_pct:2.76,ipm:66.8,ump_juta:2.90,kemiskinan_pct:11.5,pdrb_growth:5.5,risiko_label:"Rendah",klaster_label:"Wilayah Perlu Prioritas"},
  {provinsi:"Maluku",kode_bps:81,tpt_pct:6.38,ipm:70.5,ump_juta:2.90,kemiskinan_pct:16.2,pdrb_growth:5.0,risiko_label:"Tinggi",klaster_label:"Wilayah Perlu Prioritas"},
  {provinsi:"Maluku Utara",kode_bps:82,tpt_pct:3.96,ipm:70.1,ump_juta:2.90,kemiskinan_pct:6.9,pdrb_growth:22.5,risiko_label:"Rendah",klaster_label:"Wilayah Potensi Tinggi"},
  {provinsi:"Papua Barat",kode_bps:91,tpt_pct:5.68,ipm:65.7,ump_juta:3.80,kemiskinan_pct:20.5,pdrb_growth:4.5,risiko_label:"Sedang",klaster_label:"Wilayah Perlu Prioritas"},
  {provinsi:"Papua",kode_bps:94,tpt_pct:2.58,ipm:63.98,ump_juta:3.80,kemiskinan_pct:24.85,pdrb_growth:5.61,risiko_label:"Rendah",klaster_label:"Wilayah Perlu Prioritas"},
];

const TREND_DATA = [
  {tahun:2014,tpt_nasional:5.94,ipm_nasional:68.9,ump_nasional:1.65,kemiskinan_nasional:10.96},
  {tahun:2015,tpt_nasional:6.18,ipm_nasional:69.55,ump_nasional:1.85,kemiskinan_nasional:11.22},
  {tahun:2016,tpt_nasional:5.61,ipm_nasional:70.18,ump_nasional:2.09,kemiskinan_nasional:10.70},
  {tahun:2017,tpt_nasional:5.50,ipm_nasional:70.81,ump_nasional:2.25,kemiskinan_nasional:10.12},
  {tahun:2018,tpt_nasional:5.34,ipm_nasional:71.39,ump_nasional:2.44,kemiskinan_nasional:9.82},
  {tahun:2019,tpt_nasional:5.28,ipm_nasional:71.92,ump_nasional:2.63,kemiskinan_nasional:9.22},
  {tahun:2020,tpt_nasional:7.07,ipm_nasional:71.94,ump_nasional:2.70,kemiskinan_nasional:10.19},
  {tahun:2021,tpt_nasional:6.49,ipm_nasional:72.29,ump_nasional:2.76,kemiskinan_nasional:9.71},
  {tahun:2022,tpt_nasional:5.86,ipm_nasional:72.91,ump_nasional:3.00,kemiskinan_nasional:9.54},
  {tahun:2023,tpt_nasional:5.32,ipm_nasional:73.55,ump_nasional:3.18,kemiskinan_nasional:9.03},
  {tahun:2024,tpt_nasional:4.91,ipm_nasional:74.10,ump_nasional:3.38,kemiskinan_nasional:8.75},
];

const CLUSTER_PROFILES = [
  {klaster_id:0,label:"Wilayah Maju",jumlah_provinsi:7,rata_tpt:5.66,rata_ipm:78.56,rata_ump_juta:3.58,rata_kemiskinan:5.12,provinsi:["DKI Jakarta","Bali","DI Yogyakarta","Kepulauan Riau","Kalimantan Timur","Banten","Jawa Barat"],warna:"#38bdf8"},
  {klaster_id:1,label:"Wilayah Berkembang",jumlah_provinsi:13,rata_tpt:4.65,rata_ipm:73.20,rata_ump_juta:2.85,rata_kemiskinan:8.95,provinsi:["Sumatera Utara","Aceh","Sumatera Barat","Jambi","Sumatera Selatan","Lampung","Kepulauan Bangka Belitung","Jawa Tengah","Jawa Timur","Nusa Tenggara Barat","Sulawesi Utara","Sulawesi Selatan","Bengkulu"],warna:"#22c55e"},
  {klaster_id:2,label:"Wilayah Potensi Tinggi",jumlah_provinsi:8,rata_tpt:3.90,rata_ipm:71.97,rata_ump_juta:3.05,rata_kemiskinan:6.35,provinsi:["Riau","Kalimantan Barat","Kalimantan Tengah","Kalimantan Selatan","Kalimantan Utara","Sulawesi Tengah","Sulawesi Tenggara","Maluku Utara"],warna:"#f59e0b"},
  {klaster_id:3,label:"Wilayah Perlu Prioritas",jumlah_provinsi:6,rata_tpt:3.94,rata_ipm:68.01,rata_ump_juta:3.09,rata_kemiskinan:17.55,provinsi:["Nusa Tenggara Timur","Gorontalo","Sulawesi Barat","Maluku","Papua Barat","Papua"],warna:"#ef4444"},
];

const SECTOR_RECS = {
  "Wilayah Maju":["Teknologi & Startup Digital","Jasa Keuangan & Perbankan","Manufaktur Teknologi Tinggi","Pariwisata Premium","Logistik & E-Commerce"],
  "Wilayah Berkembang":["Agribisnis & Pengolahan Pangan","Industri Manufaktur Menengah","Pariwisata Daerah","Konstruksi & Infrastruktur","Pendidikan & Pelatihan Vokasional"],
  "Wilayah Potensi Tinggi":["Pertambangan & Energi","Perkebunan & Kehutanan","Perikanan & Kelautan","Agrowisata","Konstruksi & Properti"],
  "Wilayah Perlu Prioritas":["Pertanian Subsisten → Agrobisnis","UMKM & Ekonomi Kreatif Lokal","Program Vokasional Pemerintah","Infrastruktur Dasar","Kesehatan & Layanan Sosial"],
};

// ═══════════════════════════════════════════════════════════════
//  NAVIGATION
// ═══════════════════════════════════════════════════════════════

let currentPage = 'home';
let chartInstances = {};

function showPage(page) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));

  document.getElementById('page-' + page).classList.add('active');
  const navEl = document.getElementById('nav-' + page);
  if (navEl) navEl.classList.add('active');
  currentPage = page;

  // Lazy load content
  if (page === 'dashboard' && !document.getElementById('chart-trend').dataset.loaded) {
    loadDashboard();
  }
  if (page === 'cluster' && !document.getElementById('cluster-content').dataset.loaded) {
    loadClusters();
  }
  if (page === 'heatmap' && !document.getElementById('heatmap-grid').dataset.loaded) {
    loadHeatmap();
    loadCompareChart();
  }
  if (page === 'predict') {
    populateProvinceSelect();
    loadFeatureImportance();
  }
}

// ═══════════════════════════════════════════════════════════════
//  API HELPERS
// ═══════════════════════════════════════════════════════════════

async function apiGet(path) {
  try {
    const r = await fetch(API_URL + path, { signal: AbortSignal.timeout(4000) });
    if (!r.ok) throw new Error(r.status);
    return await r.json();
  } catch { return null; }
}

async function apiPost(path, body) {
  try {
    const r = await fetch(API_URL + path, {
      method: 'POST', headers: {'Content-Type': 'application/json'},
      body: JSON.stringify(body), signal: AbortSignal.timeout(8000)
    });
    if (!r.ok) throw new Error(r.status);
    return await r.json();
  } catch { return null; }
}

// Check API status
async function checkAPI() {
  const dot = document.getElementById('api-dot');
  const txt = document.getElementById('api-status-text');
  dot.className = 'api-dot checking';
  txt.textContent = 'Menghubungkan...';

  const data = await apiGet('/api/v1/status');
  if (data) {
    API_ONLINE = true;
    dot.className = 'api-dot online';
    txt.textContent = 'API Online';
  } else {
    API_ONLINE = false;
    dot.className = 'api-dot offline';
    txt.textContent = 'Mode Demo';
  }
}

// ═══════════════════════════════════════════════════════════════
//  CHART HELPERS
// ═══════════════════════════════════════════════════════════════

const CHART_DEFAULTS = {
  color: '#94a3b8',
  borderColor: '#1e293b',
};

function destroyChart(id) {
  if (chartInstances[id]) { chartInstances[id].destroy(); delete chartInstances[id]; }
}

function makeLineChart(id, labels, datasets) {
  destroyChart(id);
  const ctx = document.getElementById(id);
  if (!ctx) return;
  chartInstances[id] = new Chart(ctx, {
    type: 'line',
    data: { labels, datasets: datasets.map(d => ({
      ...d, tension: 0.4, pointRadius: 4, pointHoverRadius: 6,
      borderWidth: 2, fill: d.fill ?? true,
    })) },
    options: {
      responsive: true, maintainAspectRatio: true,
      plugins: { legend: { labels: { color: '#94a3b8', font: { family: 'Sora', size: 11 } } } },
      scales: {
        x: { ticks: { color: '#64748b', font: { size: 11 } }, grid: { color: '#1e293b' } },
        y: { ticks: { color: '#64748b', font: { size: 11 } }, grid: { color: '#1e293b' } },
      }
    }
  });
}

function makeBarChart(id, labels, data, colors) {
  destroyChart(id);
  const ctx = document.getElementById(id);
  if (!ctx) return;
  chartInstances[id] = new Chart(ctx, {
    type: 'bar',
    data: { labels, datasets: [{ data, backgroundColor: colors || '#38bdf880', borderColor: colors || '#38bdf8', borderWidth: 1 }] },
    options: {
      responsive: true, maintainAspectRatio: true, indexAxis: 'y',
      plugins: { legend: { display: false } },
      scales: {
        x: { ticks: { color: '#64748b', font: { size: 10 } }, grid: { color: '#1e293b' } },
        y: { ticks: { color: '#94a3b8', font: { size: 10 } }, grid: { display: false } },
      }
    }
  });
}

// ═══════════════════════════════════════════════════════════════
//  DASHBOARD
// ═══════════════════════════════════════════════════════════════

async function loadDashboard() {
  // Stats
  let dashboard, trends, provinces;
  if (API_ONLINE) {
    [dashboard, trends, provinces] = await Promise.all([
      apiGet('/api/v1/dashboard'), apiGet('/api/v1/trends'), apiGet('/api/v1/provinces')
    ]);
  }

  const trendData = trends?.data || TREND_DATA;
  const provData = provinces?.data || PROVINCES_DATA;
  const lastYear = trendData[trendData.length - 1];

  document.getElementById('stat-tpt').textContent = (dashboard?.tpt_nasional ?? lastYear.tpt_nasional ?? lastYear.tpt_pct ?? '—') + '%';
  document.getElementById('stat-ipm').textContent = (dashboard?.ipm_nasional ?? lastYear.ipm_nasional ?? lastYear.ipm ?? '—');
  document.getElementById('stat-ump').textContent = 'Rp ' + (dashboard?.ump_nasional ?? lastYear.ump_nasional ?? lastYear.ump_juta ?? '—') + 'M';
  document.getElementById('stat-kemiskinan').textContent = (dashboard?.kemiskinan_nasional ?? lastYear.kemiskinan_nasional ?? lastYear.kemiskinan_pct ?? '—') + '%';

  // Trend chart
  makeLineChart('chart-trend',
    trendData.map(d => d.tahun),
    [{
      label: 'TPT (%)',
      data: trendData.map(d => d.tpt_nasional ?? d.tpt_pct),
      borderColor: '#38bdf8',
      backgroundColor: 'rgba(56,189,248,0.08)',
    },{
      label: 'Kemiskinan (%)',
      data: trendData.map(d => d.kemiskinan_nasional ?? d.kemiskinan_pct),
      borderColor: '#f59e0b',
      backgroundColor: 'rgba(245,158,11,0.05)',
    }]
  );
  document.getElementById('chart-trend').dataset.loaded = '1';

  // Top 10 provinces
  const sorted = [...provData].sort((a,b) => b.tpt_pct - a.tpt_pct).slice(0, 10);
  const tptColors = sorted.map(p => {
    if (p.tpt_pct >= 9) return '#a855f7cc';
    if (p.tpt_pct >= 6) return '#ef4444cc';
    if (p.tpt_pct >= 4) return '#f59e0bcc';
    return '#22c55ecc';
  });
  makeBarChart('chart-top10', sorted.map(p => p.provinsi), sorted.map(p => p.tpt_pct), tptColors);

  // Province table
  renderProvinceTable(provData);
}

function renderProvinceTable(data) {
  const tbody = document.getElementById('province-tbody');
  const riskBadge = (label) => {
    const map = { Rendah:'rendah', Sedang:'sedang', Tinggi:'tinggi', 'Sangat Tinggi':'sangat' };
    return `<span class="badge badge-${map[label]||'sedang'}">${label}</span>`;
  };
  tbody.innerHTML = data.map(p => `
    <tr>
      <td style="font-weight:600;color:var(--text);">${p.provinsi}</td>
      <td style="font-family:var(--mono);font-weight:700;color:${tptColor(p.tpt_pct)};">${(p.tpt_pct||0).toFixed(2)}%</td>
      <td style="font-family:var(--mono);">${(p.ipm||0).toFixed(1)}</td>
      <td style="font-family:var(--mono);">Rp ${(p.ump_juta||0).toFixed(2)}M</td>
      <td style="font-family:var(--mono);">${(p.kemiskinan_pct||0).toFixed(2)}%</td>
      <td>${riskBadge(p.risiko_label || riskLabel(p.tpt_pct))}</td>
      <td style="font-size:.8rem;color:var(--text2);">${p.klaster_label||'—'}</td>
    </tr>
  `).join('');

  // Search
  document.getElementById('search-prov').oninput = function() {
    const q = this.value.toLowerCase();
    const filtered = data.filter(p => p.provinsi.toLowerCase().includes(q));
    renderProvinceTable(filtered);
  };
}

function tptColor(v) {
  if (v >= 9) return '#a855f7';
  if (v >= 6) return '#ef4444';
  if (v >= 4) return '#f59e0b';
  return '#22c55e';
}
function riskLabel(v) {
  if (v >= 9) return 'Sangat Tinggi';
  if (v >= 6) return 'Tinggi';
  if (v >= 4) return 'Sedang';
  return 'Rendah';
}

// ═══════════════════════════════════════════════════════════════
//  PREDICTION
// ═══════════════════════════════════════════════════════════════

function populateProvinceSelect() {
  const sel = document.getElementById('pred-provinsi');
  if (sel.children.length > 1) return;
  PROVINCES_DATA.forEach(p => {
    const opt = document.createElement('option');
    opt.value = p.provinsi; opt.textContent = p.provinsi;
    sel.appendChild(opt);
  });
  sel.onchange = () => {
    const prov = PROVINCES_DATA.find(p => p.provinsi === sel.value);
    if (prov) {
      document.getElementById('pred-ipm').value = prov.ipm;
      document.getElementById('pred-ump').value = prov.ump_juta;
      document.getElementById('pred-kemiskinan').value = prov.kemiskinan_pct;
      document.getElementById('pred-pdrb').value = prov.pdrb_growth;
    }
  };
}

async function runPrediction() {
  const payload = {
    provinsi: document.getElementById('pred-provinsi').value || null,
    ipm: +document.getElementById('pred-ipm').value,
    ump_juta: +document.getElementById('pred-ump').value,
    kemiskinan_pct: +document.getElementById('pred-kemiskinan').value,
    pdrb_growth: +document.getElementById('pred-pdrb').value,
    rls_tahun: +document.getElementById('pred-rls').value,
    tahun: +document.getElementById('pred-tahun').value,
    delta_tpt: 0, tpt_ma3: 5, provinsi_enc: 0,
  };

  const area = document.getElementById('pred-result-area');
  area.innerHTML = `<div class="loading-state"><div class="spinner"></div> Menghitung prediksi...</div>`;

  let result = null;
  if (API_ONLINE) result = await apiPost('/api/v1/predict', payload);

  // Demo mode: simple formula
  if (!result) result = demoPrediction(payload);

  renderPrediction(result);
}

function demoPrediction(p) {
  // Simple heuristic formula
  let tpt = 12 - (p.ipm - 60) * 0.15 - p.pdrb_growth * 0.3 - (p.ump_juta - 1) * 0.5 + p.kemiskinan_pct * 0.15;
  tpt = Math.max(1, Math.min(15, tpt + (Math.random() - 0.5) * 0.5));
  const risiko_id = tpt < 4 ? 0 : tpt < 6 ? 1 : tpt < 9 ? 2 : 3;
  const risiko_labels = ['Rendah','Sedang','Tinggi','Sangat Tinggi'];
  const risiko_colors = ['#22c55e','#f59e0b','#ef4444','#a855f7'];
  const prov_data = PROVINCES_DATA.find(x => x.provinsi === p.provinsi);
  const klaster_label = prov_data?.klaster_label || 'Wilayah Berkembang';
  return {
    provinsi: p.provinsi || 'Input Manual',
    tahun_prediksi: p.tahun,
    tpt_prediksi_pct: Math.round(tpt * 100) / 100,
    risiko_id, risiko_label: risiko_labels[risiko_id],
    risiko_warna: risiko_colors[risiko_id],
    klaster_label,
    sektor_rekomendasi: SECTOR_RECS[klaster_label] || SECTOR_RECS['Wilayah Berkembang'],
    feature_importance_top5: [
      {fitur:'ipm',nilai:0.31},{fitur:'kemiskinan_pct',nilai:0.22},
      {fitur:'pdrb_growth',nilai:0.18},{fitur:'ump_juta',nilai:0.15},{fitur:'rls_tahun',nilai:0.09}
    ],
    interpretasi: `Berdasarkan indikator yang dimasukkan, wilayah ini diprediksi memiliki TPT sebesar ${tpt.toFixed(1)}% dengan tingkat risiko ${risiko_labels[risiko_id]}. Faktor terpenting: IPM.`
  };
}

function renderPrediction(r) {
  const area = document.getElementById('pred-result-area');
  const bgGradient = {
    0:'rgba(34,197,94,.06)',1:'rgba(245,158,11,.06)',2:'rgba(239,68,68,.06)',3:'rgba(168,85,247,.06)'
  }[r.risiko_id];

  area.innerHTML = `
    <div class="pred-result" style="border-color:${r.risiko_warna}40;background:${bgGradient};">
      <div style="display:flex;align-items:start;justify-content:space-between;flex-wrap:wrap;gap:12px;margin-bottom:20px;">
        <div>
          <div style="font-size:.75rem;font-weight:600;color:var(--text3);text-transform:uppercase;margin-bottom:4px;">
            ${r.provinsi} · ${r.tahun_prediksi}
          </div>
          <div class="pred-tpt" style="color:${r.risiko_warna};">${r.tpt_prediksi_pct}%</div>
          <div class="pred-label">Prediksi Tingkat Pengangguran Terbuka</div>
        </div>
        <div style="text-align:right;">
          <span class="badge" style="background:${r.risiko_warna}20;color:${r.risiko_warna};font-size:.85rem;padding:6px 14px;">
            ⚠ Risiko ${r.risiko_label}
          </span>
          ${r.klaster_label ? `<div style="font-size:.78rem;color:var(--text3);margin-top:8px;">📌 ${r.klaster_label}</div>` : ''}
        </div>
      </div>

      <div style="background:var(--bg3);border-radius:8px;padding:12px;font-size:.82rem;color:var(--text2);margin-bottom:20px;line-height:1.5;">
        ${r.interpretasi}
      </div>

      <div style="font-size:.8rem;font-weight:700;color:var(--text3);text-transform:uppercase;letter-spacing:.05em;margin-bottom:10px;">
        🏭 Rekomendasi Sektor Potensial
      </div>
      <ul class="sector-list">
        ${(r.sektor_rekomendasi||[]).map((s,i) => `
          <li class="sector-item">
            <div class="sector-num">${i+1}</div> ${s}
          </li>`).join('')}
      </ul>
    </div>
  `;
}

function loadFeatureImportance() {
  const data = [
    {label:'IPM',val:31},{label:'Kemiskinan',val:22},{label:'Pertumbuhan PDRB',val:18},
    {label:'Upah Minimum',val:15},{label:'Lama Sekolah',val:9},{label:'Delta TPT',val:5}
  ];
  destroyChart('chart-fi');
  const ctx = document.getElementById('chart-fi');
  if (!ctx) return;
  chartInstances['chart-fi'] = new Chart(ctx, {
    type: 'bar', indexAxis: 'y',
    data: {
      labels: data.map(d => d.label),
      datasets: [{
        data: data.map(d => d.val),
        backgroundColor: ['#38bdf8cc','#38bdf8aa','#38bdf888','#38bdf866','#38bdf844','#38bdf822'],
        borderColor: '#38bdf8', borderWidth: 1,
      }]
    },
    options: {
      responsive:true, maintainAspectRatio:true,
      plugins:{legend:{display:false}},
      scales:{
        x:{ticks:{color:'#64748b',font:{size:10},callback:v=>v+'%'},grid:{color:'#1e293b'}},
        y:{ticks:{color:'#94a3b8',font:{size:10}},grid:{display:false}},
      }
    }
  });
}

// ═══════════════════════════════════════════════════════════════
//  CLUSTERS
// ═══════════════════════════════════════════════════════════════

async function loadClusters() {
  const container = document.getElementById('cluster-content');
  container.dataset.loaded = '1';

  let profiles = null;
  if (API_ONLINE) {
    const data = await apiGet('/api/v1/clusters');
    profiles = data?.klaster;
  }
  if (!profiles) profiles = CLUSTER_PROFILES;

  container.innerHTML = `
    <div class="grid-2" style="margin-bottom:20px;">
      ${profiles.map(c => `
        <div class="cluster-card" style="border-color:${c.warna||'#38bdf8'}40;">
          <div style="display:flex;align-items:center;gap:12px;margin-bottom:16px;">
            <div class="cluster-id" style="background:${c.warna||'#38bdf8'}20;color:${c.warna||'#38bdf8'};">
              K${c.klaster_id}
            </div>
            <div>
              <div style="font-weight:700;">${c.label}</div>
              <div style="font-size:.78rem;color:var(--text3);">${c.jumlah_provinsi} provinsi</div>
            </div>
            <span class="badge" style="margin-left:auto;background:${c.warna||'#38bdf8'}15;color:${c.warna||'#38bdf8'};">
              TPT ${c.rata_tpt}%
            </span>
          </div>

          <div style="display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:14px;">
            <div style="background:var(--bg3);padding:10px;border-radius:8px;">
              <div style="font-size:.7rem;color:var(--text3);">IPM Rata-rata</div>
              <div style="font-weight:700;font-family:var(--mono);color:${c.warna||'#38bdf8'};">${c.rata_ipm}</div>
            </div>
            <div style="background:var(--bg3);padding:10px;border-radius:8px;">
              <div style="font-size:.7rem;color:var(--text3);">Kemiskinan</div>
              <div style="font-weight:700;font-family:var(--mono);color:${c.warna||'#38bdf8'};">${c.rata_kemiskinan}%</div>
            </div>
          </div>

          <div style="font-size:.78rem;color:var(--text3);margin-bottom:6px;font-weight:600;">Provinsi:</div>
          <div style="display:flex;flex-wrap:wrap;gap:4px;">
            ${(c.provinsi||[]).map(p => `<span style="background:${c.warna||'#38bdf8'}10;border:1px solid ${c.warna||'#38bdf8'}20;padding:2px 8px;border-radius:4px;font-size:.72rem;color:var(--text2);">${p}</span>`).join('')}
          </div>

          <div style="margin-top:14px;border-top:1px solid var(--border);padding-top:12px;">
            <div style="font-size:.75rem;color:var(--text3);font-weight:600;margin-bottom:6px;">Sektor Potensial:</div>
            ${(SECTOR_RECS[c.label]||[]).slice(0,3).map(s=>`<div style="font-size:.78rem;color:var(--text2);padding:2px 0;">→ ${s}</div>`).join('')}
          </div>
        </div>
      `).join('')}
    </div>

    <!-- Cluster comparison chart -->
    <div class="chart-wrap">
      <div class="chart-title">📊 Perbandingan Profil Klaster</div>
      <canvas id="chart-cluster-bar" style="max-height:220px;"></canvas>
    </div>
  `;

  // Render cluster comparison chart
  setTimeout(() => {
    destroyChart('chart-cluster-bar');
    const ctx = document.getElementById('chart-cluster-bar');
    if (!ctx) return;
    chartInstances['chart-cluster-bar'] = new Chart(ctx, {
      type: 'bar',
      data: {
        labels: profiles.map(c => c.label),
        datasets: [
          { label:'TPT (%)', data: profiles.map(c => c.rata_tpt), backgroundColor:'rgba(56,189,248,.6)', borderColor:'#38bdf8', borderWidth:1 },
          { label:'Kemiskinan (%)', data: profiles.map(c => c.rata_kemiskinan), backgroundColor:'rgba(239,68,68,.6)', borderColor:'#ef4444', borderWidth:1 },
          { label:'IPM (÷10)', data: profiles.map(c => +(c.rata_ipm/10).toFixed(1)), backgroundColor:'rgba(34,197,94,.6)', borderColor:'#22c55e', borderWidth:1 },
        ]
      },
      options: {
        responsive:true, maintainAspectRatio:true,
        plugins:{ legend:{ labels:{ color:'#94a3b8', font:{ family:'Sora', size:11 } } } },
        scales: {
          x:{ ticks:{ color:'#64748b', font:{size:10} }, grid:{ color:'#1e293b' } },
          y:{ ticks:{ color:'#64748b', font:{size:10} }, grid:{ color:'#1e293b' } },
        }
      }
    });
  }, 100);
}

// ═══════════════════════════════════════════════════════════════
//  HEATMAP
// ═══════════════════════════════════════════════════════════════

function loadHeatmap() {
  const varKey = document.getElementById('heatmap-var').value;
  const varLabels = {tpt_pct:'TPT (%)',ipm:'IPM',kemiskinan_pct:'Kemiskinan (%)',ump_juta:'UMP (Juta Rp)',pdrb_growth:'Pertumbuhan PDRB (%)'};
  const grid = document.getElementById('heatmap-grid');
  grid.dataset.loaded = '1';

  const data = PROVINCES_DATA.map(p => ({
    provinsi: p.provinsi, nilai: p[varKey] || 0,
  }));
  const values = data.map(d => d.nilai);
  const min = Math.min(...values), max = Math.max(...values);

  function getColor(v) {
    const t = (v - min) / (max - min);
    if (varKey === 'ipm' || varKey === 'ump_juta' || varKey === 'pdrb_growth') {
      // Green = high is good
      const r = Math.round(239 + (34-239)*t);
      const g = Math.round(68 + (197-68)*t);
      const b = Math.round(68 + (94-68)*t);
      return `rgb(${r},${g},${b})`;
    } else {
      // Red = high is bad
      const r = Math.round(34 + (239-34)*t);
      const g = Math.round(197 + (68-197)*t);
      const b = Math.round(94 + (68-94)*t);
      return `rgb(${r},${g},${b})`;
    }
  }

  const sorted = [...data].sort((a,b) => b.nilai - a.nilai);
  grid.innerHTML = sorted.map(d => {
    const color = getColor(d.nilai);
    const textColor = d.nilai > (min+max)/2 ? '#fff' : '#000';
    return `
      <div class="heatmap-cell" style="background:${color}18;border-color:${color}40;"
           onclick="toast('${d.provinsi}: ${d.nilai.toFixed(2)} ${varLabels[varKey]}', 'ℹ️')">
        <div class="heatmap-prov" style="color:${color};">${d.provinsi}</div>
        <div class="heatmap-val" style="color:${color};">${d.nilai.toFixed(2)}</div>
        <div style="font-size:.7rem;color:${color}88;">${varLabels[varKey]}</div>
      </div>
    `;
  }).join('');
}

function loadCompareChart() {
  const sorted = [...PROVINCES_DATA].sort((a,b) => b.tpt_pct - a.tpt_pct);
  destroyChart('chart-compare');
  const ctx = document.getElementById('chart-compare');
  if (!ctx) return;
  chartInstances['chart-compare'] = new Chart(ctx, {
    type:'bar', indexAxis:'y',
    data: {
      labels: sorted.map(p=>p.provinsi),
      datasets: [{
        label:'TPT (%)',
        data: sorted.map(p=>p.tpt_pct),
        backgroundColor: sorted.map(p => tptColor(p.tpt_pct) + 'aa'),
        borderColor: sorted.map(p => tptColor(p.tpt_pct)),
        borderWidth: 1,
      }]
    },
    options:{
      responsive:true, maintainAspectRatio:false,
      plugins:{legend:{display:false}},
      scales:{
        x:{ticks:{color:'#64748b',font:{size:9}},grid:{color:'#1e293b'}},
        y:{ticks:{color:'#94a3b8',font:{size:9}},grid:{display:false}},
      }
    }
  });
  ctx.style.maxHeight='700px';
}

// ═══════════════════════════════════════════════════════════════
//  UPLOAD
// ═══════════════════════════════════════════════════════════════

const dropZone = document.getElementById('drop-zone');
dropZone.addEventListener('dragover', e => { e.preventDefault(); dropZone.classList.add('over'); });
dropZone.addEventListener('dragleave', () => dropZone.classList.remove('over'));
dropZone.addEventListener('drop', e => {
  e.preventDefault(); dropZone.classList.remove('over');
  const file = e.dataTransfer.files[0];
  if (file) handleFileSelect(file);
});

async function handleFileSelect(file) {
  if (!file) return;
  const allowed = ['text/csv','application/vnd.openxmlformats-officedocument.spreadsheetml.sheet','application/vnd.ms-excel'];
  if (!allowed.some(t => file.type.includes(t)) && !file.name.match(/\.(csv|xlsx|xls)$/i)) {
    toast('Format tidak didukung. Gunakan CSV atau Excel.', '❌');
    return;
  }

  const resultArea = document.getElementById('upload-result');
  resultArea.style.display = 'block';
  resultArea.innerHTML = `<div class="loading-state"><div class="spinner"></div> Menganalisis ${file.name}...</div>`;

  // Try API first
  let result = null;
  if (API_ONLINE) {
    const form = new FormData();
    form.append('file', file);
    try {
      const r = await fetch(API_URL + '/api/v1/upload', { method:'POST', body:form });
      if (r.ok) result = await r.json();
    } catch {}
  }

  // Demo: parse CSV client-side
  if (!result && file.name.endsWith('.csv')) {
    result = await parseCsvDemo(file);
  }

  if (result) renderUploadResult(result, file.name);
  else {
    resultArea.innerHTML = `<div class="card" style="border-color:var(--red)20;color:var(--red);">
      ❌ Gagal memproses file. Pastikan format sesuai template.
    </div>`;
  }
}

async function parseCsvDemo(file) {
  return new Promise(resolve => {
    const reader = new FileReader();
    reader.onload = e => {
      const lines = e.target.result.split('\n').filter(l => l.trim());
      const headers = lines[0].split(',').map(h => h.trim().toLowerCase());
      const rows = lines.slice(1).map(l => {
        const vals = l.split(',');
        const obj = {};
        headers.forEach((h, i) => obj[h] = vals[i]?.trim());
        return obj;
      });

      const tpts = rows.map(r => +r.tpt_pct).filter(v => !isNaN(v));
      const provs = [...new Set(rows.map(r => r.provinsi).filter(Boolean))];
      const years = [...new Set(rows.map(r => +r.tahun).filter(v => !isNaN(v)))].sort();

      resolve({
        status:'success', filename: file.name,
        jumlah_baris: rows.length, jumlah_provinsi: provs.length,
        provinsi_ditemukan: provs.slice(0,20),
        tahun_range: [years[0], years[years.length-1]],
        statistik_tpt: {
          mean: (tpts.reduce((a,b)=>a+b,0)/tpts.length).toFixed(2),
          min: Math.min(...tpts).toFixed(2),
          max: Math.max(...tpts).toFixed(2),
          count: tpts.length
        },
        preview: rows.slice(0, 8),
        prediksi_sample: []
      });
    };
    reader.readAsText(file);
  });
}

function renderUploadResult(r, filename) {
  const area = document.getElementById('upload-result');
  area.innerHTML = `
    <div class="card" style="border-color:rgba(34,197,94,.3);">
      <div style="display:flex;align-items:center;gap:10px;margin-bottom:20px;">
        <span style="font-size:1.5rem;">✅</span>
        <div>
          <div style="font-weight:700;">${filename}</div>
          <div style="font-size:.8rem;color:var(--text3);">${r.jumlah_baris} baris · ${r.jumlah_provinsi} provinsi · ${r.tahun_range?.[0]}–${r.tahun_range?.[1]}</div>
        </div>
      </div>

      <div class="grid-4" style="margin-bottom:20px;">
        <div style="background:var(--bg3);padding:12px;border-radius:8px;text-align:center;">
          <div style="font-size:.7rem;color:var(--text3);">Total Baris</div>
          <div style="font-size:1.5rem;font-weight:800;color:var(--accent);font-family:var(--mono);">${r.jumlah_baris}</div>
        </div>
        <div style="background:var(--bg3);padding:12px;border-radius:8px;text-align:center;">
          <div style="font-size:.7rem;color:var(--text3);">Provinsi</div>
          <div style="font-size:1.5rem;font-weight:800;color:var(--green);font-family:var(--mono);">${r.jumlah_provinsi}</div>
        </div>
        <div style="background:var(--bg3);padding:12px;border-radius:8px;text-align:center;">
          <div style="font-size:.7rem;color:var(--text3);">TPT Rata-rata</div>
          <div style="font-size:1.5rem;font-weight:800;color:var(--yellow);font-family:var(--mono);">${r.statistik_tpt?.mean}%</div>
        </div>
        <div style="background:var(--bg3);padding:12px;border-radius:8px;text-align:center;">
          <div style="font-size:.7rem;color:var(--text3);">Rentang TPT</div>
          <div style="font-size:1rem;font-weight:800;color:var(--purple);font-family:var(--mono);">${r.statistik_tpt?.min}–${r.statistik_tpt?.max}%</div>
        </div>
      </div>

      <div style="font-size:.8rem;font-weight:600;color:var(--text3);margin-bottom:8px;">Provinsi Ditemukan:</div>
      <div style="display:flex;flex-wrap:wrap;gap:6px;margin-bottom:20px;">
        ${(r.provinsi_ditemukan||[]).map(p=>`<span class="badge badge-blue">${p}</span>`).join('')}
      </div>

      <div style="font-size:.8rem;font-weight:600;color:var(--text3);margin-bottom:8px;">Preview Data (8 baris pertama):</div>
      <div class="table-wrap">
        <table>
          <thead><tr>${Object.keys(r.preview?.[0]||{}).map(k=>`<th>${k}</th>`).join('')}</tr></thead>
          <tbody>${(r.preview||[]).map(row=>`<tr>${Object.values(row).map(v=>`<td style="font-family:var(--mono);font-size:.8rem;">${v||'—'}</td>`).join('')}</tr>`).join('')}</tbody>
        </table>
      </div>

      ${r.prediksi_sample?.length ? `
        <div style="margin-top:20px;font-size:.8rem;font-weight:600;color:var(--text3);margin-bottom:8px;">Prediksi Sample (via Model RF):</div>
        <div class="table-wrap">
          <table>
            <thead><tr><th>Provinsi</th><th>Tahun</th><th>TPT Aktual</th><th>TPT Prediksi</th></tr></thead>
            <tbody>${r.prediksi_sample.map(p=>`<tr>
              <td>${p.provinsi}</td>
              <td>${p.tahun}</td>
              <td style="font-family:var(--mono);color:var(--text2);">${p.tpt_aktual}%</td>
              <td style="font-family:var(--mono);color:var(--accent);font-weight:700;">${p.tpt_prediksi}%</td>
            </tr>`).join('')}</tbody>
          </table>
        </div>
      ` : ''}
    </div>
  `;
}

// ═══════════════════════════════════════════════════════════════
//  TOAST
// ═══════════════════════════════════════════════════════════════

function toast(msg, icon = 'ℹ️') {
  const c = document.getElementById('toast-container');
  const t = document.createElement('div');
  t.className = 'toast';
  t.textContent = `${icon} ${msg}`;
  c.appendChild(t);
  setTimeout(() => { t.style.opacity='0'; t.style.transform='translateX(100%)'; t.style.transition='all .3s'; setTimeout(()=>t.remove(),300); }, 3000);
}

// ═══════════════════════════════════════════════════════════════
//  INIT
// ═══════════════════════════════════════════════════════════════

window.addEventListener('DOMContentLoaded', async () => {
  // Animate home cards
  document.querySelectorAll('.card').forEach((c, i) => {
    c.style.animationDelay = `${i * 0.1}s`;
  });

  await checkAPI();

  // Auto-load dashboard on first visit
  setTimeout(() => {
    if (currentPage === 'home') {
      // preload province select
      populateProvinceSelect();
    }
  }, 500);
});
</script>
</body>
</html>
