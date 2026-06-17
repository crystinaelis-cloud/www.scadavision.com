<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>SCADAVision — Dashboard de Diagnóstico de Comunicação</title>
<style>
  /* ── TOKENS ── */
  :root {
    --navy:    #1F1F4C;
    --teal:    #0099A8;
    --teal-lt: #E6F7F9;
    --green:   #7DC242;
    --green-lt:#EEF7E3;
    --red:     #E53935;
    --red-lt:  #FDECEA;
    --amber:   #F9A825;
    --amber-lt:#FFF8E1;
    --white:   #FFFFFF;
    --off:     #F5F8FA;
    --muted:   #6B7C93;
    --border:  #DDE4EC;
    --shadow:  0 2px 12px rgba(31,31,76,0.08);
    --shadow-lg: 0 6px 32px rgba(31,31,76,0.13);
    --radius:  12px;
    --radius-sm: 8px;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'Segoe UI', Calibri, Arial, sans-serif;
    background: var(--off);
    color: var(--navy);
    min-height: 100vh;
  }

  /* ── HEADER ── */
  .header {
    background: var(--navy);
    padding: 0 32px;
    height: 64px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 16px rgba(0,0,0,0.25);
  }
  .header-logo {
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .logo-badge {
    background: linear-gradient(135deg, var(--teal), var(--green));
    width: 36px; height: 36px;
    border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    font-size: 18px; font-weight: 900; color: white;
  }
  .header h1 {
    font-size: 20px;
    font-weight: 700;
    color: white;
    letter-spacing: -0.3px;
  }
  .header-sub {
    font-size: 11px;
    color: rgba(255,255,255,0.55);
    font-weight: 400;
    letter-spacing: 0.5px;
  }
  .header-right {
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .last-update {
    font-size: 11px;
    color: rgba(255,255,255,0.5);
  }
  #live-clock {
    font-size: 12px;
    color: var(--teal);
    font-weight: 600;
    font-variant-numeric: tabular-nums;
  }

  /* ── GRADIENT BAR (Energisa) ── */
  .energisa-bar {
    height: 5px;
    background: linear-gradient(to right, var(--teal), var(--green));
  }

  /* ── UPLOAD ZONE ── */
  .upload-zone {
    margin: 32px auto;
    max-width: 700px;
    background: white;
    border: 2px dashed var(--teal);
    border-radius: var(--radius);
    padding: 48px 32px;
    text-align: center;
    cursor: pointer;
    transition: all 0.2s;
  }
  .upload-zone:hover { background: var(--teal-lt); border-color: var(--navy); }
  .upload-zone.has-data { display: none; }
  .upload-icon { font-size: 48px; margin-bottom: 16px; }
  .upload-zone h2 { font-size: 20px; color: var(--navy); margin-bottom: 8px; }
  .upload-zone p { color: var(--muted); font-size: 14px; line-height: 1.6; }
  .upload-zone .hint {
    margin-top: 20px;
    font-size: 12px;
    color: var(--muted);
    background: var(--off);
    padding: 10px 16px;
    border-radius: 6px;
    display: inline-block;
  }
  #folder-input { display: none; }
  .btn-upload {
    margin-top: 24px;
    background: var(--teal);
    color: white;
    border: none;
    padding: 12px 28px;
    border-radius: 8px;
    font-size: 15px;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.15s;
    display: inline-flex;
    align-items: center;
    gap: 8px;
  }
  .btn-upload:hover { background: var(--navy); }

  /* ── DASHBOARD ── */
  .dashboard { display: none; padding: 24px 32px 48px; max-width: 1400px; margin: 0 auto; }
  .dashboard.visible { display: block; }

  /* ── TOOLBAR ── */
  .toolbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 12px;
    margin-bottom: 24px;
  }
  .toolbar-left { display: flex; align-items: center; gap: 12px; flex-wrap: wrap; }
  .folder-name {
    font-size: 13px;
    color: var(--muted);
    background: white;
    padding: 6px 14px;
    border-radius: 20px;
    border: 1px solid var(--border);
    display: flex; align-items: center; gap: 6px;
  }
  .btn-reload {
    background: var(--teal);
    color: white;
    border: none;
    padding: 8px 18px;
    border-radius: 8px;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    display: flex; align-items: center; gap: 6px;
    transition: background 0.15s;
  }
  .btn-reload:hover { background: var(--navy); }
  .btn-new {
    background: white;
    color: var(--navy);
    border: 1px solid var(--border);
    padding: 8px 18px;
    border-radius: 8px;
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
    display: flex; align-items: center; gap: 6px;
    transition: all 0.15s;
  }
  .btn-new:hover { border-color: var(--teal); color: var(--teal); }

  /* Search + filter */
  .search-box {
    display: flex; align-items: center; gap: 8px;
  }
  .search-box input {
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 7px 14px;
    font-size: 13px;
    width: 200px;
    outline: none;
    transition: border-color 0.15s;
  }
  .search-box input:focus { border-color: var(--teal); }
  .filter-btns { display: flex; gap: 6px; }
  .filter-btn {
    padding: 6px 14px;
    border-radius: 20px;
    border: 1.5px solid transparent;
    font-size: 12px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.15s;
    background: white;
  }
  .filter-btn.all    { border-color: var(--border); color: var(--muted); }
  .filter-btn.ok     { border-color: var(--green); color: var(--green); }
  .filter-btn.alerta { border-color: var(--amber); color: var(--amber); }
  .filter-btn.falha  { border-color: var(--red);   color: var(--red);   }
  .filter-btn.active { color: white !important; }
  .filter-btn.all.active    { background: var(--muted);  border-color: var(--muted); }
  .filter-btn.ok.active     { background: var(--green);  border-color: var(--green); }
  .filter-btn.alerta.active { background: var(--amber);  border-color: var(--amber); }
  .filter-btn.falha.active  { background: var(--red);    border-color: var(--red);   }

  /* ── KPI CARDS ── */
  .kpi-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 16px;
    margin-bottom: 24px;
  }
  .kpi-card {
    background: white;
    border-radius: var(--radius);
    padding: 22px 24px;
    box-shadow: var(--shadow);
    display: flex;
    align-items: center;
    gap: 18px;
    transition: transform 0.15s, box-shadow 0.15s;
    cursor: default;
  }
  .kpi-card:hover { transform: translateY(-2px); box-shadow: var(--shadow-lg); }
  .kpi-icon {
    width: 52px; height: 52px;
    border-radius: 14px;
    display: flex; align-items: center; justify-content: center;
    font-size: 24px;
    flex-shrink: 0;
  }
  .kpi-icon.total  { background: #EEF1FF; }
  .kpi-icon.ok     { background: var(--green-lt); }
  .kpi-icon.alerta { background: var(--amber-lt); }
  .kpi-icon.falha  { background: var(--red-lt); }
  .kpi-val {
    font-size: 32px;
    font-weight: 800;
    line-height: 1;
    letter-spacing: -1px;
  }
  .kpi-val.ok    { color: var(--green); }
  .kpi-val.alerta{ color: var(--amber); }
  .kpi-val.falha { color: var(--red);   }
  .kpi-val.total { color: var(--navy);  }
  .kpi-label { font-size: 12px; color: var(--muted); margin-top: 4px; font-weight: 500; }
  .kpi-pct   { font-size: 11px; color: var(--muted); margin-top: 2px; }

  /* ── MAIN GRID ── */
  .main-grid {
    display: grid;
    grid-template-columns: 1fr 340px;
    gap: 20px;
  }

  /* ── CHART CARD ── */
  .card {
    background: white;
    border-radius: var(--radius);
    box-shadow: var(--shadow);
    padding: 24px;
  }
  .card-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 20px;
  }
  .card-title {
    font-size: 14px;
    font-weight: 700;
    color: var(--navy);
    letter-spacing: 0.2px;
  }
  .card-sub { font-size: 11px; color: var(--muted); margin-top: 2px; }

  /* ── PROGRESS BAR ── */
  .progress-track {
    background: var(--off);
    border-radius: 4px;
    height: 10px;
    overflow: hidden;
    margin-bottom: 20px;
    display: flex;
  }
  .progress-ok     { background: var(--green); height: 100%; transition: width 0.5s; }
  .progress-alerta { background: var(--amber); height: 100%; transition: width 0.5s; }
  .progress-falha  { background: var(--red);   height: 100%; transition: width 0.5s; }
  .progress-legend {
    display: flex;
    gap: 20px;
    margin-bottom: 24px;
    flex-wrap: wrap;
  }
  .legend-item {
    display: flex; align-items: center; gap: 6px;
    font-size: 12px; color: var(--muted);
  }
  .legend-dot {
    width: 10px; height: 10px; border-radius: 50%;
  }

  /* ── TABLE ── */
  .table-wrap { overflow-x: auto; }
  table { width: 100%; border-collapse: collapse; }
  thead th {
    text-align: left;
    font-size: 11px;
    font-weight: 700;
    color: var(--muted);
    letter-spacing: 0.8px;
    text-transform: uppercase;
    padding: 0 12px 12px;
    border-bottom: 2px solid var(--border);
    white-space: nowrap;
  }
  tbody tr {
    border-bottom: 1px solid var(--off);
    transition: background 0.1s;
    cursor: default;
  }
  tbody tr:hover { background: var(--off); }
  tbody td {
    padding: 11px 12px;
    font-size: 13px;
    color: var(--navy);
    white-space: nowrap;
  }
  td.device-name { font-weight: 600; font-family: 'Courier New', monospace; font-size: 12px; }
  td.loss-cell { font-weight: 700; font-variant-numeric: tabular-nums; }

  /* Badges */
  .badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 3px 10px;
    border-radius: 20px;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.3px;
  }
  .badge.ok     { background: var(--green-lt); color: #2e7d32; }
  .badge.alerta { background: var(--amber-lt); color: #e65100; }
  .badge.falha  { background: var(--red-lt);   color: #c62828; }
  .badge-dot { width: 6px; height: 6px; border-radius: 50%; }
  .badge.ok .badge-dot     { background: var(--green); }
  .badge.alerta .badge-dot { background: var(--amber); }
  .badge.falha .badge-dot  { background: var(--red);   }

  /* Loss bar in table */
  .loss-bar-wrap {
    display: flex; align-items: center; gap: 8px;
  }
  .loss-bar-track {
    flex: 1; background: var(--off); border-radius: 3px; height: 6px; min-width: 60px;
  }
  .loss-bar-fill { height: 100%; border-radius: 3px; transition: width 0.4s; }

  /* ── SIDEBAR ── */
  .sidebar { display: flex; flex-direction: column; gap: 16px; }

  /* Donut chart */
  .donut-wrap {
    display: flex; align-items: center; justify-content: center;
    padding: 8px 0 16px;
    position: relative;
  }
  svg.donut { transform: rotate(-90deg); }
  .donut-label {
    position: absolute;
    text-align: center;
    pointer-events: none;
  }
  .donut-pct { font-size: 26px; font-weight: 800; color: var(--navy); line-height: 1; }
  .donut-txt { font-size: 11px; color: var(--muted); margin-top: 3px; }

  /* Alert list */
  .alert-list { display: flex; flex-direction: column; gap: 8px; max-height: 320px; overflow-y: auto; }
  .alert-item {
    display: flex; align-items: flex-start; gap: 10px;
    padding: 10px 12px;
    border-radius: var(--radius-sm);
    background: var(--off);
    font-size: 12px;
  }
  .alert-item.falha  { background: var(--red-lt);   border-left: 3px solid var(--red);   }
  .alert-item.alerta { background: var(--amber-lt); border-left: 3px solid var(--amber); }
  .alert-icon { font-size: 14px; flex-shrink: 0; margin-top: 1px; }
  .alert-device { font-weight: 700; color: var(--navy); font-family: monospace; }
  .alert-detail { color: var(--muted); margin-top: 1px; }

  /* ── EMPTY / ERROR ── */
  .empty-state {
    text-align: center;
    padding: 48px 24px;
    color: var(--muted);
  }
  .empty-state .icon { font-size: 40px; margin-bottom: 12px; }
  .empty-state p { font-size: 14px; }

  /* ── FOOTER ── */
  .footer {
    margin-top: 48px;
    height: 5px;
    background: linear-gradient(to right, var(--teal), var(--green));
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    .kpi-row { grid-template-columns: repeat(2, 1fr); }
    .main-grid { grid-template-columns: 1fr; }
    .dashboard { padding: 16px 16px 48px; }
  }
  @media (max-width: 500px) {
    .kpi-row { grid-template-columns: 1fr 1fr; }
    .header h1 { font-size: 16px; }
    .header-sub { display: none; }
  }

  /* Spinning loader */
  @keyframes spin { to { transform: rotate(360deg); } }
  .spinner {
    display: inline-block;
    width: 16px; height: 16px;
    border: 2px solid rgba(255,255,255,0.4);
    border-top-color: white;
    border-radius: 50%;
    animation: spin 0.7s linear infinite;
  }

  /* Pulse dot for live indicator */
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50%       { opacity: 0.4; }
  }
  .live-dot {
    width: 7px; height: 7px;
    background: var(--green);
    border-radius: 50%;
    display: inline-block;
    animation: pulse 1.8s ease-in-out infinite;
  }
</style>
</head>
<body>

<!-- ── HEADER ── -->
<header class="header">
  <div class="header-logo">
    <div class="logo-badge">S</div>
    <div>
      <h1>SCADAVision</h1>
      <div class="header-sub">DASHBOARD DE DIAGNÓSTICO DE COMUNICAÇÃO · ENERGISA PARAÍBA</div>
    </div>
  </div>
  <div class="header-right">
    <span class="live-dot"></span>
    <span id="live-clock">--:--:--</span>
    <span class="last-update" id="last-update-label">Nenhuma análise carregada</span>
  </div>
</header>
<div class="energisa-bar"></div>

<!-- ── UPLOAD ZONE ── -->
<div class="upload-zone" id="upload-zone" onclick="document.getElementById('folder-input').click()">
  <div class="upload-icon">📁</div>
  <h2>Selecione a pasta com os arquivos de ping</h2>
  <p>O dashboard lê todos os arquivos <strong>.txt</strong> da pasta,<br>
     extrai o packet loss de cada dispositivo e exibe o diagnóstico completo.</p>
  <p style="margin-top:12px; font-size:13px; color:var(--teal); font-weight:600;">
    Nenhum dado sai do seu computador — tudo roda no navegador.
  </p>
  <div class="hint">
    💡 Formato esperado: arquivos TXT com saída de <code>ping</code> contendo "Packet Loss = X%"
  </div>
  <button class="btn-upload" onclick="event.stopPropagation(); document.getElementById('folder-input').click()">
    <span>📂</span> Abrir pasta de TXTs
  </button>
</div>

<input type="file" id="folder-input" webkitdirectory multiple accept=".txt,.log,text/*"/>

<!-- ── DASHBOARD ── -->
<div class="dashboard" id="dashboard">

  <!-- TOOLBAR -->
  <div class="toolbar">
    <div class="toolbar-left">
      <div class="folder-name" id="folder-label">📁 —</div>
      <button class="btn-reload" id="btn-reload" onclick="document.getElementById('folder-input').click()">
        <span>🔄</span> Atualizar pasta
      </button>
      <button class="btn-new" onclick="resetDashboard()">
        <span>📂</span> Nova pasta
      </button>
    </div>
    <div style="display:flex; gap:10px; align-items:center; flex-wrap:wrap;">
      <div class="search-box">
        <input type="text" id="search-input" placeholder="🔍  Buscar dispositivo..." oninput="renderTable()"/>
      </div>
      <div class="filter-btns">
        <button class="filter-btn all active" onclick="setFilter('all',this)">Todos</button>
        <button class="filter-btn ok"  onclick="setFilter('ok',this)">✓ OK</button>
        <button class="filter-btn alerta" onclick="setFilter('alerta',this)">⚠ Alerta</button>
        <button class="filter-btn falha"  onclick="setFilter('falha',this)">✕ Falha</button>
      </div>
    </div>
  </div>

  <!-- KPI ROW -->
  <div class="kpi-row">
    <div class="kpi-card">
      <div class="kpi-icon total">📊</div>
      <div>
        <div class="kpi-val total" id="kpi-total">0</div>
        <div class="kpi-label">Total de dispositivos</div>
        <div class="kpi-pct" id="kpi-files">0 arquivos lidos</div>
      </div>
    </div>
    <div class="kpi-card" onclick="setFilter('ok', document.querySelector('.filter-btn.ok'))" style="cursor:pointer;">
      <div class="kpi-icon ok">✅</div>
      <div>
        <div class="kpi-val ok" id="kpi-ok">0</div>
        <div class="kpi-label">Comunicação OK</div>
        <div class="kpi-pct" id="kpi-ok-pct">0% loss</div>
      </div>
    </div>
    <div class="kpi-card" onclick="setFilter('alerta', document.querySelector('.filter-btn.alerta'))" style="cursor:pointer;">
      <div class="kpi-icon alerta">⚠️</div>
      <div>
        <div class="kpi-val alerta" id="kpi-alerta">0</div>
        <div class="kpi-label">Em alerta</div>
        <div class="kpi-pct" id="kpi-alerta-pct">50% loss</div>
      </div>
    </div>
    <div class="kpi-card" onclick="setFilter('falha', document.querySelector('.filter-btn.falha'))" style="cursor:pointer;">
      <div class="kpi-icon falha">❌</div>
      <div>
        <div class="kpi-val falha" id="kpi-falha">0</div>
        <div class="kpi-label">Falha de comunicação</div>
        <div class="kpi-pct" id="kpi-falha-pct">100% loss</div>
      </div>
    </div>
  </div>

  <!-- MAIN GRID -->
  <div class="main-grid">

    <!-- LEFT: table -->
    <div class="card">
      <div class="card-header">
        <div>
          <div class="card-title">Diagnóstico por Dispositivo</div>
          <div class="card-sub" id="table-sub">— arquivos analisados</div>
        </div>
        <button class="btn-new" onclick="exportCSV()" title="Exportar relatório CSV">
          📥 Exportar CSV
        </button>
      </div>

      <!-- Progress bar -->
      <div class="progress-track" id="progress-bar">
        <div class="progress-ok"     id="bar-ok"     style="width:0%"></div>
        <div class="progress-alerta" id="bar-alerta"  style="width:0%"></div>
        <div class="progress-falha"  id="bar-falha"   style="width:0%"></div>
      </div>
      <div class="progress-legend">
        <div class="legend-item"><div class="legend-dot" style="background:var(--green)"></div><span id="leg-ok">OK: 0</span></div>
        <div class="legend-item"><div class="legend-dot" style="background:var(--amber)"></div><span id="leg-alerta">Alerta: 0</span></div>
        <div class="legend-item"><div class="legend-dot" style="background:var(--red)"></div><span id="leg-falha">Falha: 0</span></div>
      </div>

      <div class="table-wrap">
        <table>
          <thead>
            <tr>
              <th onclick="sortBy('device')" style="cursor:pointer;">Dispositivo ↕</th>
              <th onclick="sortBy('loss')"   style="cursor:pointer;">Packet Loss ↕</th>
              <th>Status</th>
              <th>Visualização</th>
              <th onclick="sortBy('sent')"   style="cursor:pointer;">Enviados ↕</th>
              <th onclick="sortBy('recv')"   style="cursor:pointer;">Recebidos ↕</th>
              <th>IP detectado</th>
            </tr>
          </thead>
          <tbody id="table-body">
            <tr><td colspan="7"><div class="empty-state"><div class="icon">📂</div><p>Selecione uma pasta para iniciar a análise.</p></div></td></tr>
          </tbody>
        </table>
      </div>
    </div>

    <!-- RIGHT: sidebar -->
    <div class="sidebar">

      <!-- Donut -->
      <div class="card">
        <div class="card-header">
          <div class="card-title">Visão Geral</div>
        </div>
        <div class="donut-wrap">
          <svg class="donut" width="160" height="160" viewBox="0 0 160 160">
            <circle id="ring-bg"     cx="80" cy="80" r="60" fill="none" stroke="#EEF0F5" stroke-width="22"/>
            <circle id="ring-ok"     cx="80" cy="80" r="60" fill="none" stroke="var(--green)" stroke-width="22" stroke-dasharray="0 377" stroke-linecap="round"/>
            <circle id="ring-alerta" cx="80" cy="80" r="60" fill="none" stroke="var(--amber)" stroke-width="22" stroke-dasharray="0 377" stroke-linecap="round"/>
            <circle id="ring-falha"  cx="80" cy="80" r="60" fill="none" stroke="var(--red)"   stroke-width="22" stroke-dasharray="0 377" stroke-linecap="round"/>
          </svg>
          <div class="donut-label">
            <div class="donut-pct" id="donut-pct">—</div>
            <div class="donut-txt">disponível</div>
          </div>
        </div>
        <div style="display:flex; flex-direction:column; gap:8px;">
          <div class="legend-item" style="justify-content:space-between; padding:6px 0; border-bottom:1px solid var(--off);">
            <div style="display:flex;align-items:center;gap:8px;"><div class="legend-dot" style="background:var(--green)"></div><span style="font-size:13px;font-weight:600;color:var(--navy)">OK</span></div>
            <span id="side-ok" style="font-size:13px;font-weight:700;color:var(--green)">0</span>
          </div>
          <div class="legend-item" style="justify-content:space-between; padding:6px 0; border-bottom:1px solid var(--off);">
            <div style="display:flex;align-items:center;gap:8px;"><div class="legend-dot" style="background:var(--amber)"></div><span style="font-size:13px;font-weight:600;color:var(--navy)">Alerta</span></div>
            <span id="side-alerta" style="font-size:13px;font-weight:700;color:var(--amber)">0</span>
          </div>
          <div class="legend-item" style="justify-content:space-between; padding:6px 0;">
            <div style="display:flex;align-items:center;gap:8px;"><div class="legend-dot" style="background:var(--red)"></div><span style="font-size:13px;font-weight:600;color:var(--navy)">Falha</span></div>
            <span id="side-falha" style="font-size:13px;font-weight:700;color:var(--red)">0</span>
          </div>
        </div>
      </div>

      <!-- Alert list -->
      <div class="card" id="alert-card">
        <div class="card-header">
          <div>
            <div class="card-title">Alertas Ativos</div>
            <div class="card-sub" id="alert-count">Nenhum alerta</div>
          </div>
        </div>
        <div class="alert-list" id="alert-list">
          <div class="empty-state" style="padding:24px 0;">
            <div class="icon">✅</div>
            <p>Nenhum alerta detectado.</p>
          </div>
        </div>
      </div>

    </div><!-- /sidebar -->
  </div><!-- /main-grid -->
</div><!-- /dashboard -->

<div class="footer"></div>

<script>
// ── STATE ──────────────────────────────────────────────────────────────────
let allDevices = [];      // [{device, loss, status, sent, recv, ip, filename}]
let sortCol    = 'loss';
let sortDir    = -1;      // -1 = desc
let activeFilter = 'all';
let folderName = '';

// ── CLOCK ─────────────────────────────────────────────────────────────────
function updateClock() {
  const now = new Date();
  document.getElementById('live-clock').textContent =
    now.toLocaleTimeString('pt-BR');
}
setInterval(updateClock, 1000);
updateClock();

// ── FILE INPUT ────────────────────────────────────────────────────────────
document.getElementById('folder-input').addEventListener('change', async function(e) {
  const files = Array.from(e.target.files).filter(f =>
    f.name.toLowerCase().endsWith('.txt') || f.name.toLowerCase().endsWith('.log')
  );
  if (!files.length) {
    alert('Nenhum arquivo .txt encontrado na pasta selecionada.');
    return;
  }

  // Get folder name from first file path
  const fp = files[0].webkitRelativePath || files[0].name;
  folderName = fp.includes('/') ? fp.split('/')[0] : 'pasta selecionada';

  await parseFiles(files);
  this.value = ''; // allow re-selecting same folder
});

// ── PARSE TXT FILES ───────────────────────────────────────────────────────
async function parseFiles(files) {
  const results = [];

  for (const file of files) {
    const text = await readFile(file);
    const parsed = parsePingOutput(text, file.name);
    if (parsed) results.push(parsed);
  }

  if (!results.length) {
    alert('Nenhum dado de ping foi encontrado nos arquivos. Verifique o formato dos TXTs.');
    return;
  }

  allDevices = results;
  updateDashboard();
  showDashboard();
}

function readFile(file) {
  return new Promise((resolve) => {
    const reader = new FileReader();
    reader.onload = e => resolve(e.target.result || '');
    reader.onerror = () => resolve('');
    reader.readAsText(file, 'UTF-8');
  });
}

// ── PING PARSER ───────────────────────────────────────────────────────────
// Handles multiple ping output formats (Windows PT/EN, Linux)
function parsePingOutput(text, filename) {
  const device = filename.replace(/\.(txt|log)$/i, '');

  // Detect loss — try multiple patterns
  let loss = null;
  let sent = null, recv = null;

  // Pattern 1: "Perdidos = 0 (0% de perda)" — Windows PT
  let m = text.match(/perdidos\s*=\s*\d+\s*\((\d+)%/i);
  if (m) loss = parseInt(m[1]);

  // Pattern 2: "Packet Loss = 0%" — generic
  if (loss === null) {
    m = text.match(/packet\s*loss\s*[=:]\s*(\d+)%/i);
    if (m) loss = parseInt(m[1]);
  }

  // Pattern 3: "(0% loss)" — short Windows EN format
  if (loss === null) {
    m = text.match(/\((\d+)%\s*loss\)/i);
    if (m) loss = parseInt(m[1]);
  }

  // Pattern 4: "0% packet loss" — Linux
  if (loss === null) {
    m = text.match(/(\d+)%\s*packet\s*loss/i);
    if (m) loss = parseInt(m[1]);
  }

  // Pattern 5: check if all replies timed out
  if (loss === null) {
    const timedOut = (text.match(/Request timeout|timed out|esgotado/gi) || []).length;
    if (timedOut >= 2) loss = 100;
  }

  // Sent / received
  // Windows EN: "Packets: Sent = 4, Received = 4, Lost = 0"
  m = text.match(/sent\s*=\s*(\d+),?\s*received\s*=\s*(\d+)/i);
  if (m) { sent = parseInt(m[1]); recv = parseInt(m[2]); }
  // Windows PT: "Enviados = 4, Recebidos = 4, Perdidos = 0"
  if (!sent) {
    m = text.match(/enviados\s*=\s*(\d+),?\s*recebidos\s*=\s*(\d+)/i);
    if (m) { sent = parseInt(m[1]); recv = parseInt(m[2]); }
  }
  // Linux: "4 packets transmitted, 4 received"
  if (!sent) {
    m = text.match(/(\d+)\s*packets?\s*transmitted,?\s*(\d+)\s*received/i);
    if (m) { sent = parseInt(m[1]); recv = parseInt(m[2]); }
  }

  // IP address
  let ip = null;
  m = text.match(/\b(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\b/);
  if (m) ip = m[1];

  // If we couldn't parse loss but have sent/recv, compute it
  if (loss === null && sent !== null && recv !== null) {
    loss = Math.round((1 - recv / sent) * 100);
  }

  if (loss === null) return null; // couldn't parse this file

  // Clamp to 0-100
  loss = Math.max(0, Math.min(100, loss));

  let status;
  if (loss === 0)        status = 'ok';
  else if (loss < 100)   status = 'alerta';
  else                   status = 'falha';

  return { device, loss, status, sent: sent ?? '—', recv: recv ?? '—', ip: ip ?? '—', filename };
}

// ── UPDATE DASHBOARD ──────────────────────────────────────────────────────
function updateDashboard() {
  const total  = allDevices.length;
  const nOk    = allDevices.filter(d => d.status === 'ok').length;
  const nAlerta= allDevices.filter(d => d.status === 'alerta').length;
  const nFalha = allDevices.filter(d => d.status === 'falha').length;
  const pOk    = total ? Math.round(nOk    / total * 100) : 0;
  const pAlerta= total ? Math.round(nAlerta/ total * 100) : 0;
  const pFalha = total ? Math.round(nFalha / total * 100) : 0;

  // KPIs
  document.getElementById('kpi-total').textContent  = total;
  document.getElementById('kpi-files').textContent  = `${total} arquivo${total!==1?'s':''} lido${total!==1?'s':''}`;
  document.getElementById('kpi-ok').textContent     = nOk;
  document.getElementById('kpi-ok-pct').textContent = `${pOk}% dos dispositivos`;
  document.getElementById('kpi-alerta').textContent = nAlerta;
  document.getElementById('kpi-alerta-pct').textContent = `${pAlerta}% dos dispositivos`;
  document.getElementById('kpi-falha').textContent  = nFalha;
  document.getElementById('kpi-falha-pct').textContent = `${pFalha}% dos dispositivos`;

  // Progress bar
  document.getElementById('bar-ok').style.width     = pOk + '%';
  document.getElementById('bar-alerta').style.width = pAlerta + '%';
  document.getElementById('bar-falha').style.width  = pFalha + '%';

  // Legend
  document.getElementById('leg-ok').textContent     = `OK: ${nOk}`;
  document.getElementById('leg-alerta').textContent = `Alerta: ${nAlerta}`;
  document.getElementById('leg-falha').textContent  = `Falha: ${nFalha}`;

  // Sidebar counts
  document.getElementById('side-ok').textContent    = nOk;
  document.getElementById('side-alerta').textContent= nAlerta;
  document.getElementById('side-falha').textContent = nFalha;

  // Donut chart
  const circ = 2 * Math.PI * 60; // 377
  const angOk     = (nOk    / total) * circ;
  const angAlerta = (nAlerta/ total) * circ;
  const angFalha  = (nFalha / total) * circ;
  const offsetAlerta = circ - angOk;
  const offsetFalha  = circ - angOk - angAlerta;

  document.getElementById('ring-ok').setAttribute('stroke-dasharray',     `${angOk} ${circ}`);
  document.getElementById('ring-alerta').setAttribute('stroke-dasharray', `${angAlerta} ${circ}`);
  document.getElementById('ring-alerta').setAttribute('stroke-dashoffset', -angOk);
  document.getElementById('ring-falha').setAttribute('stroke-dasharray',  `${angFalha} ${circ}`);
  document.getElementById('ring-falha').setAttribute('stroke-dashoffset',  -(angOk + angAlerta));
  document.getElementById('donut-pct').textContent = pOk + '%';

  // Alert list
  const alerts = allDevices
    .filter(d => d.status !== 'ok')
    .sort((a,b) => b.loss - a.loss);
  const alertList = document.getElementById('alert-list');
  const alertCount = document.getElementById('alert-count');

  if (!alerts.length) {
    alertCount.textContent = 'Nenhum alerta';
    alertList.innerHTML = `<div class="empty-state" style="padding:24px 0;"><div class="icon">✅</div><p>Todos os dispositivos estão OK.</p></div>`;
  } else {
    alertCount.textContent = `${alerts.length} dispositivo${alerts.length>1?'s':''} com problema`;
    alertList.innerHTML = alerts.map(d => `
      <div class="alert-item ${d.status}">
        <div class="alert-icon">${d.status==='falha'?'❌':'⚠️'}</div>
        <div>
          <div class="alert-device">${d.device}</div>
          <div class="alert-detail">${d.loss}% de packet loss · IP: ${d.ip}</div>
        </div>
      </div>
    `).join('');
  }

  // Folder label
  document.getElementById('folder-label').textContent = `📁 ${folderName} (${total} arquivos)`;
  document.getElementById('table-sub').textContent = `${total} arquivo${total!==1?'s':''} analisado${total!==1?'s':''}`;

  // Last update
  const now = new Date().toLocaleTimeString('pt-BR');
  document.getElementById('last-update-label').textContent = `Última análise: ${now}`;

  renderTable();
}

// ── TABLE ─────────────────────────────────────────────────────────────────
function renderTable() {
  const search = document.getElementById('search-input').value.toLowerCase();
  let data = allDevices.filter(d => {
    if (activeFilter !== 'all' && d.status !== activeFilter) return false;
    if (search && !d.device.toLowerCase().includes(search) && !d.ip.includes(search)) return false;
    return true;
  });

  // Sort
  data.sort((a, b) => {
    let va = a[sortCol], vb = b[sortCol];
    if (sortCol === 'device') { va = va.toLowerCase(); vb = vb.toLowerCase(); }
    if (va < vb) return sortDir;
    if (va > vb) return -sortDir;
    return 0;
  });

  const tbody = document.getElementById('table-body');

  if (!data.length) {
    tbody.innerHTML = `<tr><td colspan="7"><div class="empty-state"><div class="icon">🔍</div><p>Nenhum dispositivo encontrado com esse filtro.</p></div></td></tr>`;
    return;
  }

  tbody.innerHTML = data.map(d => {
    const lossColor = d.status === 'ok' ? 'var(--green)' : d.status === 'alerta' ? 'var(--amber)' : 'var(--red)';
    const badgeClass = d.status;
    const badgeText  = d.status === 'ok' ? 'OK' : d.status === 'alerta' ? 'Alerta' : 'Falha';
    return `
      <tr>
        <td class="device-name">${escapeHtml(d.device)}</td>
        <td class="loss-cell" style="color:${lossColor}">${d.loss}%</td>
        <td><span class="badge ${badgeClass}"><span class="badge-dot"></span>${badgeText}</span></td>
        <td>
          <div class="loss-bar-wrap">
            <div class="loss-bar-track">
              <div class="loss-bar-fill" style="width:${d.loss}%; background:${lossColor}"></div>
            </div>
          </div>
        </td>
        <td style="color:var(--muted)">${d.sent}</td>
        <td style="color:var(--muted)">${d.recv}</td>
        <td style="font-family:monospace; font-size:12px; color:var(--muted)">${escapeHtml(String(d.ip))}</td>
      </tr>`;
  }).join('');
}

function escapeHtml(s) {
  return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');
}

// ── SORT ──────────────────────────────────────────────────────────────────
function sortBy(col) {
  if (sortCol === col) sortDir = -sortDir;
  else { sortCol = col; sortDir = col === 'device' ? 1 : -1; }
  renderTable();
}

// ── FILTER ────────────────────────────────────────────────────────────────
function setFilter(f, btn) {
  activeFilter = f;
  document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
  if (btn) btn.classList.add('active');
  renderTable();
}

// ── SHOW / HIDE ───────────────────────────────────────────────────────────
function showDashboard() {
  document.getElementById('upload-zone').style.display = 'none';
  document.getElementById('dashboard').classList.add('visible');
}

function resetDashboard() {
  allDevices = [];
  document.getElementById('upload-zone').style.display = '';
  document.getElementById('dashboard').classList.remove('visible');
  document.getElementById('search-input').value = '';
  setFilter('all', document.querySelector('.filter-btn.all'));
}

// ── EXPORT CSV ────────────────────────────────────────────────────────────
function exportCSV() {
  if (!allDevices.length) return;
  const header = ['Dispositivo','Packet Loss (%)','Status','Pacotes Enviados','Pacotes Recebidos','IP'];
  const rows = allDevices.map(d => [
    d.device, d.loss,
    d.status === 'ok' ? 'OK' : d.status === 'alerta' ? 'Alerta' : 'Falha',
    d.sent, d.recv, d.ip
  ]);
  const csv = [header, ...rows].map(r => r.join(';')).join('\n');
  const blob = new Blob(['\uFEFF' + csv], { type: 'text/csv;charset=utf-8;' });
  const url  = URL.createObjectURL(blob);
  const a    = document.createElement('a');
  a.href = url;
  const now  = new Date().toISOString().slice(0,16).replace('T','_').replace(':','-');
  a.download = `SCADAVision_${now}.csv`;
  a.click();
  URL.revokeObjectURL(url);
}

// ── DRAG & DROP ───────────────────────────────────────────────────────────
const zone = document.getElementById('upload-zone');
zone.addEventListener('dragover',  e => { e.preventDefault(); zone.style.background = 'var(--teal-lt)'; });
zone.addEventListener('dragleave', () => { zone.style.background = ''; });
zone.addEventListener('drop', async e => {
  e.preventDefault();
  zone.style.background = '';
  const items = Array.from(e.dataTransfer.items || []);
  const files = [];
  for (const item of items) {
    if (item.kind === 'file') {
      const entry = item.webkitGetAsEntry?.();
      if (entry?.isDirectory) {
        folderName = entry.name;
        await readDirEntry(entry, files);
      } else {
        const f = item.getAsFile();
        if (f && /\.(txt|log)$/i.test(f.name)) { files.push(f); folderName = 'arquivos soltos'; }
      }
    }
  }
  if (files.length) await parseFiles(files);
});

function readDirEntry(dirEntry, files) {
  return new Promise(resolve => {
    const reader = dirEntry.createReader();
    const readAll = () => reader.readEntries(async entries => {
      if (!entries.length) return resolve();
      for (const e of entries) {
        if (e.isFile && /\.(txt|log)$/i.test(e.name)) {
          await new Promise(r => e.file(f => { files.push(f); r(); }));
        } else if (e.isDirectory) {
          await readDirEntry(e, files);
        }
      }
      readAll();
    });
    readAll();
  });
}
</script>
</body>
</html>
