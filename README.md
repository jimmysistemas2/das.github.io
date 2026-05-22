<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>RIS Ate | Sistema de Información y Estadística en Salud</title>
  <link rel="stylesheet" href="styles.css" />
  <script defer src="data-ris-ate.js"></script>
  <script defer src="script.js"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">
</head>
<body>
  <header class="topbar">
    <button class="menu-btn" id="menuBtn" aria-label="Abrir menú">☰</button>
    <div class="brand">
      <img src="assets/logo-diris-lima-este.png" alt="MINSA DIRIS Lima Este" class="logo-diris">
      <div class="logo-ris">
        <div class="ris-icon">✦</div>
        <div><strong>RED INTEGRADA</strong><span>DE SALUD</span><b>ATE</b></div>
      </div>
    </div>
    <div class="title-block">
      <h1>RIS ATE</h1>
      <p>Sistema de Información y Estadística en Salud</p>
    </div>
    <div class="date-card">
      <span>📅</span>
      <div><strong id="fechaActual">Actualizando...</strong><small id="horaActual"></small></div>
    </div>
  </header>

  <div class="layout">
    <aside class="sidebar" id="sidebar">
      <nav>
        <p class="section-title">INICIO</p>
        <a class="nav-link active" data-module="inicio">🏠 Página de inicio</a>

        <p class="section-title">INDICADORES</p>
        <a class="nav-link" data-module="indicadores">📊 Indicadores de Gestión</a>
        <a class="nav-link" data-module="fed">📈 Indicadores FED</a>
        <a class="nav-link" data-module="convenio">🤝 Convenio de Gestión</a>

        <p class="section-title">ESTRATEGIAS SANITARIAS</p>
        <a class="nav-link" data-module="curso-vida">🧍 Curso de Vida</a>
        <a class="nav-link" data-module="inmunizaciones">💉 Inmunizaciones</a>
        <a class="nav-link" data-module="materno">🤰 Salud Materno</a>
        <a class="nav-link" data-module="bucal">🦷 Salud Bucal</a>
        <a class="nav-link" data-module="mental">🧠 Salud Mental</a>
        <a class="nav-link" data-module="zoonosis">🦟 Metaxénicas y Zoonosis</a>
        <a class="nav-link" data-module="emergencias">🚑 Urgencias y Emergencias</a>

        <p class="section-title">ATENCIONES EN SALUD</p>
        <a class="nav-link" data-module="atenciones">👥 Atendidos y Atenciones</a>
        <a class="nav-link" data-module="ranking-ipress">🏆 Ranking IPRESS</a>
        <a class="nav-link" data-module="ranking-ups">🎖️ Ranking UPS</a>
      </nav>
    </aside>

    <main class="content">
      <section class="hero panel">
        <div class="hero-text">
          <h2>Bienvenido a RIS ATE</h2>
          <h3>Red Integrada de Salud Ate - DIRIS Lima Este</h3>
          <p>Plataforma para el monitoreo, análisis y evaluación de indicadores de salud, producción de servicios y estrategias sanitarias en la jurisdicción de la Red Integrada de Salud Ate.</p>
          <p>Información confiable y oportuna para fortalecer la toma de decisiones y la mejora continua de los servicios de salud.</p>
          <div class="line"></div>
          <div class="stats">
            <div class="stat blue"><span>🏥</span><strong id="totalIpress">12</strong><small>IPRESS RIS Ate</small></div>
            <div class="stat green"><span>🧩</span><strong id="totalUps">24</strong><small>UPS catalogadas</small></div>
            <div class="stat yellow"><span>🧑‍🤝‍🧑</span><strong id="totalPoblacion">Validar</strong><small>Población oficial</small></div>
            <div class="stat purple"><span>✅</span><strong>RIS</strong><small>Ate</small></div>
          </div>
        </div>
        <div class="map-zone" aria-label="Mapa referencial RIS Ate">
          <div class="map-shape shape1">RIS<br>ATE</div>
          <div class="map-shape shape2"></div>
          <div class="map-shape shape3"></div>
          <div class="quote">“Datos que transforman información en decisiones que salvan vidas.”</div>
        </div>
      </section>


      <section class="panel data-section" id="datosRisAte">
        <div class="section-head">
          <div>
            <h2>Datos base de la RIS Ate</h2>
            <p>Relación inicial de IPRESS, catálogo UPS y campo de población listo para actualizar con fuente oficial vigente.</p>
          </div>
          <span class="data-badge">IPRESS · UPS · Población</span>
        </div>
        <div class="data-grid">
          <div class="table-card">
            <h3>IPRESS de la RIS Ate</h3>
            <div class="table-wrap"><table><thead><tr><th>N°</th><th>IPRESS</th><th>Tipo</th><th>Población</th></tr></thead><tbody id="ipressBody"></tbody></table></div>
          </div>
          <div class="table-card">
            <h3>UPS catalogadas</h3>
            <div class="table-wrap"><table><thead><tr><th>Código</th><th>UPS</th></tr></thead><tbody id="upsBody"></tbody></table></div>
          </div>
        </div>
      </section>

      <section class="module-grid">
        <article class="module-card" data-module="indicadores"><div class="circle">📊</div><h3>Indicadores</h3><p>Seguimiento de metas, indicadores de gestión y FED.</p><button>Ver más →</button></article>
        <article class="module-card" data-module="atenciones"><div class="circle green">🏥</div><h3>Atenciones</h3><p>Análisis de atendidos, atenciones y producción de servicios.</p><button>Ver más →</button></article>
        <article class="module-card" data-module="ranking-ipress"><div class="circle yellow">🏆</div><h3>Ranking IPRESS</h3><p>Comparativo de desempeño entre establecimientos de salud.</p><button>Ver más →</button></article>
        <article class="module-card" data-module="ranking-ups"><div class="circle purple">🎖️</div><h3>Ranking UPS</h3><p>Evaluación y ranking de Unidades Productoras de Servicios.</p><button>Ver más →</button></article>
        <article class="module-card" data-module="reportes"><div class="circle cyan">📋</div><h3>Reportes</h3><p>Informes, tableros y reportes ejecutivos para la gestión.</p><button>Ver más →</button></article>
      </section>

      <section class="panel module-view" id="moduleView">
        <h2 id="moduleTitle">Página de inicio</h2>
        <p id="moduleDescription">Seleccione un módulo del menú lateral o de las tarjetas principales.</p>
        <div class="placeholder">
          <strong>Espacio listo para conectar dashboards, tablas, gráficos o enlaces externos.</strong>
          <span>Puede reemplazar este bloque por gráficos, Google Sheets, Looker Studio, Power BI o nuevos archivos HTML.</span>
        </div>
      </section>

      <footer class="footer panel">
        <div>ⓘ <strong>RIS ATE - DIRIS Lima Este</strong><br><small>Sistema desarrollado para fortalecer la gestión de la información en salud.</small></div>
        <div>© 2026 DIRIS Lima Este<br><small>Versión 1.0.0</small></div>
      </footer>
    </main>
  </div>
</body>
</html>
