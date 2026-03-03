<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Paula Distefano – README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;600;700&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --rose:   #e8927c;
  --rose2:  #d4756a;
  --rose3:  #e8a598;
  --rose4:  #c96b5a;
  --blush:  #f9c5d1;
  --cream:  #fff9f7;
  --paper:  #fffcfb;
  --ink:    #4a2c1a;
  --muted:  #9a7060;
  --soft:   #fdf0ec;
  --border: #f0ddd6;
}

body {
  background: #f3e9e4;
  min-height: 100vh;
  padding: 2rem 1rem;
  font-family: 'Sora', sans-serif;
  color: var(--ink);
}

.card {
  max-width: 700px;
  margin: 0 auto;
  background: var(--paper);
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 8px 60px rgba(180,100,80,0.13);
}

.wave-top {
  width: 100%;
  height: 90px;
  background: linear-gradient(135deg, #f9c5d1 0%, #e8927c 100%);
  position: relative;
}
.wave-top svg { position: absolute; bottom: -1px; left: 0; width: 100%; }

.body { padding: 2rem 2.5rem 2.5rem; }

/* HERO */
.hero { text-align: center; margin-bottom: 1.8rem; animation: rise 0.4s ease both; }
.hero h1 { font-size: 1.9rem; font-weight: 700; letter-spacing: -0.02em; margin-bottom: 0.2rem; }
.hero .tagline { font-family: 'DM Mono', monospace; font-size: 0.68rem; color: var(--rose); letter-spacing: 0.06em; margin-bottom: 0.9rem; }
.hero .bio { font-size: 0.8rem; color: var(--muted); line-height: 1.75; max-width: 460px; margin: 0 auto 1.1rem; }
.chips { display: flex; justify-content: center; gap: 0.5rem; flex-wrap: wrap; }
.chip { font-size: 0.6rem; font-family: 'DM Mono', monospace; background: var(--rose); color: white; padding: 0.28rem 0.75rem; border-radius: 20px; text-decoration: none; transition: background 0.2s; }
.chip:hover { background: var(--rose2); }

.div { border: none; border-top: 1px solid var(--border); margin: 1.6rem 0; }

.sec-label { font-size: 0.62rem; font-family: 'DM Mono', monospace; letter-spacing: 0.18em; text-transform: uppercase; color: var(--rose); margin-bottom: 1rem; display: flex; align-items: center; gap: 0.5rem; }
.sec-label::after { content: ''; flex: 1; height: 1px; background: var(--border); }

/* ABOUT */
.about-list { list-style: none; display: flex; flex-direction: column; gap: 0.5rem; }
.about-list li { font-size: 0.79rem; color: var(--muted); display: flex; gap: 0.6rem; line-height: 1.5; }
.about-list li b { color: var(--ink); }

/* TECH */
.tech-section { display: flex; flex-direction: column; gap: 0.9rem; }
.tech-row { display: flex; gap: 0.4rem; flex-wrap: wrap; align-items: center; }
.tech-lbl { font-size: 0.56rem; font-family: 'DM Mono', monospace; color: var(--rose3); letter-spacing: 0.1em; text-transform: uppercase; min-width: 95px; }
.pill { font-size: 0.6rem; font-family: 'DM Mono', monospace; background: var(--soft); color: var(--ink); padding: 0.22rem 0.55rem; border-radius: 4px; border: 1px solid var(--border); }

/* PROJECTS */
.proj-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 0.85rem; }
.proj-card { background: var(--cream); border: 1px solid var(--border); border-radius: 10px; padding: 1rem 1.1rem; position: relative; overflow: hidden; transition: transform 0.2s, box-shadow 0.2s; cursor: default; }
.proj-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; background: linear-gradient(90deg, var(--rose), var(--blush)); transform: scaleX(0); transform-origin: left; transition: transform 0.25s ease; }
.proj-card:hover::before { transform: scaleX(1); }
.proj-card:hover { transform: translateY(-2px); box-shadow: 0 6px 20px rgba(180,100,80,0.11); }
.proj-card .icon { font-size: 1rem; margin-bottom: 0.4rem; }
.proj-card h3 { font-size: 0.83rem; font-weight: 600; margin-bottom: 0.3rem; }
.proj-card p { font-size: 0.69rem; color: var(--muted); line-height: 1.6; margin-bottom: 0.55rem; }
.proj-tags { display: flex; gap: 0.3rem; flex-wrap: wrap; }
.proj-tag { font-size: 0.54rem; font-family: 'DM Mono', monospace; background: #fde8e2; color: var(--rose2); padding: 0.15rem 0.45rem; border-radius: 3px; }

/* STATS */
.stats-row { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; margin-bottom: 1.2rem; }
.stat-card { background: var(--soft); border: 1px solid var(--border); border-radius: 14px; padding: 1.2rem 1.6rem; text-align: center; flex: 1; min-width: 110px; transition: transform 0.2s; }
.stat-card:hover { transform: translateY(-2px); }
.stat-card .num { font-size: 1.7rem; font-weight: 700; color: var(--rose); line-height: 1; margin-bottom: 0.4rem; }
.stat-card .lbl { font-size: 0.56rem; font-family: 'DM Mono', monospace; color: var(--muted); letter-spacing: 0.12em; text-transform: uppercase; }

.visits { text-align: center; }
.visits span { font-size: 0.62rem; font-family: 'DM Mono', monospace; color: var(--muted); background: var(--soft); border: 1px solid var(--border); padding: 0.25rem 0.75rem; border-radius: 20px; }

/* FOOTER */
.footer { text-align: center; padding: 1.2rem 2rem 0; font-size: 0.75rem; color: var(--muted); }
.footer a { color: var(--rose); text-decoration: none; font-weight: 600; }

.wave-bottom { width: 100%; height: 60px; background: linear-gradient(135deg, #e8927c 0%, #f9c5d1 100%); margin-top: 1.5rem; position: relative; }
.wave-bottom svg { position: absolute; top: -1px; left: 0; width: 100%; }

.body > * { animation: rise 0.45s ease both; }
.body > *:nth-child(1) { animation-delay: 0.04s; }
.body > *:nth-child(2) { animation-delay: 0.08s; }
.body > *:nth-child(3) { animation-delay: 0.12s; }
.body > *:nth-child(4) { animation-delay: 0.16s; }
.body > *:nth-child(5) { animation-delay: 0.20s; }
.body > *:nth-child(6) { animation-delay: 0.24s; }
.body > *:nth-child(7) { animation-delay: 0.28s; }
.body > *:nth-child(8) { animation-delay: 0.32s; }
.body > *:nth-child(9) { animation-delay: 0.36s; }
.body > *:nth-child(10) { animation-delay: 0.40s; }
.body > *:nth-child(11) { animation-delay: 0.44s; }

@keyframes rise { from { opacity: 0; transform: translateY(12px); } to { opacity: 1; transform: translateY(0); } }
</style>
</head>
<body>
<div class="card">

  <div class="wave-top">
    <svg viewBox="0 0 1440 40" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M0,20 C360,40 1080,0 1440,20 L1440,40 L0,40 Z" fill="#fffcfb"/>
    </svg>
  </div>

  <div class="body">

    <div class="hero">
      <h1>Paula Distefano</h1>
      <div class="tagline">< construyendo cosas / aprendiendo siempre /></div>
      <p class="bio">Estudiante de Desarrollo de Software de Mendoza. Me gusta que las cosas funcionen bien, se vean mejor, y tengan un propósito.</p>
      <div class="chips">
        <a class="chip" href="https://linkedin.com/in/paula-distefano">in · LinkedIn</a>
        <a class="chip" href="mailto:paudistefano03@gmail.com">✉ Email</a>
      </div>
    </div>

    <hr class="div">

    <div class="sec-label">🌱 un poco sobre mí</div>
    <ul class="about-list">
      <li>📍 Mendoza, Argentina</li>
      <li>🎓 Tecnicatura en Desarrollo de Software · <b>UNCuyo</b> · en curso</li>
      <li>🛠️ Construí proyectos con <b>Flutter, React, Node.js y Python</b></li>
      <li>☁️ Conocimiento en <b>AWS, Docker y Kubernetes</b></li>
      <li>🗣️ Español nativo · Inglés en proceso (A2–B1)</li>
      <li>✨ Siempre buscando el equilibrio entre código limpio y buena UX</li>
    </ul>

    <hr class="div">

    <div class="sec-label">🛠️ tecnologías</div>
    <div class="tech-section">
      <div class="tech-row"><span class="tech-lbl">lenguajes</span><span class="pill">JavaScript</span><span class="pill">Python</span><span class="pill">Java</span><span class="pill">Dart</span></div>
      <div class="tech-row"><span class="tech-lbl">interfaz</span><span class="pill">HTML5</span><span class="pill">CSS3</span><span class="pill">Bootstrap</span><span class="pill">Tailwind</span><span class="pill">React</span><span class="pill">Vue</span></div>
      <div class="tech-row"><span class="tech-lbl">backend</span><span class="pill">Node.js</span><span class="pill">Express</span><span class="pill">Spring</span></div>
      <div class="tech-row"><span class="tech-lbl">mobile</span><span class="pill">Flutter</span></div>
      <div class="tech-row"><span class="tech-lbl">bases de datos</span><span class="pill">PostgreSQL</span><span class="pill">MySQL</span><span class="pill">MongoDB</span><span class="pill">Neo4j</span></div>
      <div class="tech-row"><span class="tech-lbl">BaaS</span><span class="pill">Supabase</span><span class="pill">Firebase</span></div>
      <div class="tech-row"><span class="tech-lbl">devops</span><span class="pill">AWS</span><span class="pill">Docker</span><span class="pill">Kubernetes</span><span class="pill">ArgoCD</span></div>
      <div class="tech-row"><span class="tech-lbl">herramientas</span><span class="pill">Git</span><span class="pill">GitHub</span><span class="pill">Jira</span><span class="pill">Postman</span><span class="pill">Netlify</span><span class="pill">Render</span></div>
    </div>

    <hr class="div">

    <div class="sec-label">📌 proyectos que me enorgullecen</div>
    <div class="proj-grid">
      <div class="proj-card"><div class="icon">🏥</div><h3>cllinichealth</h3><p>App mobile para gestión de consultorio — agenda, historial y check-in por QR.</p><div class="proj-tags"><span class="proj-tag">Flutter</span><span class="proj-tag">Dart</span></div></div>
      <div class="proj-card"><div class="icon">🎬</div><h3>moodflix</h3><p>Chatbot de Telegram que recomienda pelis según tu mood. OpenAI + TMDB + Spotify.</p><div class="proj-tags"><span class="proj-tag">Python</span><span class="proj-tag">OpenAI</span></div></div>
      <div class="proj-card"><div class="icon">📚</div><h3>book-tracker</h3><p>Seguimiento de lecturas con Google Books API y metas mensuales.</p><div class="proj-tags"><span class="proj-tag">React</span><span class="proj-tag">Node.js</span></div></div>
      <div class="proj-card"><div class="icon">🛒</div><h3>Marketplace Libros</h3><p>Compra y venta de libros usados con auth y CRUD completo.</p><div class="proj-tags"><span class="proj-tag">HTML</span><span class="proj-tag">JavaScript</span></div></div>
    </div>

    <hr class="div">

    <div class="sec-label">📊 mis stats</div>
    <div class="stats-row">
      <div class="stat-card"><div class="num">188</div><div class="lbl">contribuciones</div></div>
      <div class="stat-card"><div class="num">6</div><div class="lbl">repositorios</div></div>
      <div class="stat-card"><div class="num">2023</div><div class="lbl">en GitHub desde</div></div>
    </div>
    <div class="visits"><span>👁 visitas al perfil · contador activo en GitHub</span></div>

    <hr class="div">

    <div class="footer">
      ¿Querés charlar sobre un proyecto o una oportunidad?<br/>
      <a href="mailto:paudistefano03@gmail.com">escribime</a> · ✉️
    </div>

  </div>

  <div class="wave-bottom">
    <svg viewBox="0 0 1440 40" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M0,20 C360,0 1080,40 1440,20 L1440,0 L0,0 Z" fill="#fffcfb"/>
    </svg>
  </div>

</div>
</body>
</html>
