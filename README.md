<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Omar Hassaan | Full-Stack Web Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet" />
<style>
  :root {
    --bg: #F5EFE4;
    --card: #FFFBEA;
    --ink: #111111;
    --orange: #FF6B3D;
    --yellow: #FFD93D;
    --blue: #6EA8FF;
    --pink: #FF9ECD;
    --border: 4px solid var(--ink);
    --shadow: 8px 8px 0 var(--ink);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Space Grotesk', system-ui, sans-serif;
    color: var(--ink);
    background-color: var(--bg);
    background-image: radial-gradient(rgba(17, 17, 17, 0.12) 1px, transparent 1px);
    background-size: 22px 22px;
    line-height: 1.6;
  }

  a { color: inherit; }

  .wrap {
    max-width: 1100px;
    margin: 0 auto;
    padding: 32px 20px 60px;
    display: grid;
    gap: 48px;
  }

  .box {
    background: var(--card);
    border: var(--border);
    box-shadow: var(--shadow);
    padding: 28px;
    animation: rise 0.6s cubic-bezier(0.2, 0.8, 0.2, 1) backwards;
  }

  @keyframes rise {
    from { opacity: 0; transform: translateY(20px); }
  }

  /* Buttons */
  .btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 16px 26px;
    font: 700 16px/1 'Space Grotesk', sans-serif;
    text-transform: uppercase;
    letter-spacing: 0.06em;
    color: var(--ink);
    background: var(--orange);
    border: var(--border);
    box-shadow: 6px 6px 0 var(--ink);
    text-decoration: none;
    cursor: pointer;
    transition: transform 0.12s ease, box-shadow 0.12s ease;
  }
  .btn:hover { transform: translate(-3px, -3px); box-shadow: 9px 9px 0 var(--ink); }
  .btn:active { transform: translate(6px, 6px); box-shadow: 0 0 0 var(--ink); }
  .btn.alt { background: var(--yellow); }
  .btn.blue { background: var(--blue); }
  .btn.sm { padding: 12px 18px; font-size: 14px; }

  /* Header */
  .site-header {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    padding: 18px 24px;
  }
  .logo {
    display: flex;
    align-items: center;
    gap: 12px;
    font-size: 30px;
    font-weight: 700;
    letter-spacing: -0.04em;
    text-decoration: none;
  }
  .logo .tag {
    font-size: 14px;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    background: var(--yellow);
    border: 3px solid var(--ink);
    padding: 6px 12px;
    box-shadow: 3px 3px 0 var(--ink);
  }
  nav { display: flex; flex-wrap: wrap; gap: 24px; }
  nav a {
    font-weight: 700;
    text-decoration: none;
    position: relative;
  }
  nav a::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: -6px;
    width: 0;
    height: 4px;
    background: var(--orange);
    transition: width 0.2s ease;
  }
  nav a:hover::after { width: 100%; }

  /* Hero */
  .pill {
    display: inline-block;
    background: var(--yellow);
    border: var(--border);
    padding: 10px 18px;
    font-size: 15px;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    box-shadow: 4px 4px 0 var(--ink);
  }
  .hero h1 {
    margin: 28px 0 22px;
    font-size: clamp(42px, 8vw, 88px);
    font-weight: 700;
    line-height: 0.98;
    letter-spacing: -0.05em;
  }
  .hl {
    display: inline-block;
    background: var(--orange);
    border: var(--border);
    box-shadow: 6px 6px 0 var(--ink);
    padding: 0 0.12em;
    margin: 4px 0;
  }
  .hero p {
    font-size: 20px;
    max-width: 640px;
    margin-bottom: 36px;
    color: #333;
  }
  .actions { display: flex; flex-wrap: wrap; gap: 20px; }

  /* Sections */
  .section-title {
    display: flex;
    align-items: center;
    gap: 14px;
    margin-bottom: 24px;
    font-size: clamp(28px, 4vw, 40px);
    font-weight: 700;
    letter-spacing: -0.04em;
  }
  .num {
    background: var(--ink);
    color: var(--yellow);
    font-size: 16px;
    letter-spacing: 0.1em;
    padding: 6px 12px;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 28px;
  }
  .project {
    padding: 0;
    overflow: hidden;
    transition: transform 0.15s ease, box-shadow 0.15s ease;
  }
  .project:hover { transform: translate(-4px, -4px); box-shadow: 12px 12px 0 var(--ink); }
  .band {
    padding: 14px 28px;
    border-bottom: var(--border);
    font-weight: 700;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    font-size: 14px;
  }
  .project .body { padding: 28px; }
  .project h3 { font-size: 28px; letter-spacing: -0.03em; margin-bottom: 12px; }
  .project p { color: #333; margin-bottom: 24px; }
  .c-yellow { background: var(--yellow); }
  .c-blue { background: var(--blue); }
  .c-orange { background: var(--orange); }

  .stack { display: flex; flex-wrap: wrap; gap: 16px; }
  .chip {
    border: var(--border);
    box-shadow: 4px 4px 0 var(--ink);
    padding: 10px 18px;
    font-weight: 700;
    transition: transform 0.12s ease;
  }
  .chip:hover { transform: translate(-2px, -2px) rotate(-2deg); }
  .chip:nth-child(4n+1) { background: var(--yellow); }
  .chip:nth-child(4n+2) { background: var(--blue); }
  .chip:nth-child(4n+3) { background: var(--orange); }
  .chip:nth-child(4n)   { background: var(--pink); }

  /* Footer */
  .footer {
    background: var(--ink);
    color: var(--card);
    text-align: center;
    padding: 56px 28px;
    box-shadow: 8px 8px 0 var(--orange);
  }
  .footer h2 {
    font-size: clamp(30px, 5vw, 52px);
    letter-spacing: -0.04em;
    margin-bottom: 12px;
  }
  .footer p { color: #d8d2c4; margin-bottom: 30px; }
  .socials { display: flex; flex-wrap: wrap; justify-content: center; gap: 18px; }
  .footer .btn { box-shadow: 6px 6px 0 var(--card); }
  .footer .btn:hover { box-shadow: 9px 9px 0 var(--card); }

  @media (max-width: 640px) {
    .site-header .btn { width: 100%; }
    nav { width: 100%; justify-content: space-between; }
    .actions .btn { width: 100%; }
    .hero p { font-size: 18px; }
  }

  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after { animation: none !important; transition: none !important; }
  }
</style>
</head>
<body>
<div class="wrap">

  <header class="box site-header">
    <a href="#top" class="logo">Omar <span class="tag">Dev</span></a>
    <nav>
      <a href="#top">Home</a>
      <a href="#projects">Projects</a>
      <a href="#stack">Tech Stack</a>
      <a href="#contact">Contact</a>
    </nav>
    <a href="#contact" class="btn">Hire Me</a>
  </header>

  <section class="box hero" id="top">
    <span class="pill">Full-Stack Web Developer</span>
    <h1>I build digital <span class="hl">experiences</span> that people remember.</h1>
    <p>I design and develop clean, high-performance interfaces using modern web technologies, turning product ideas into engaging user experiences.</p>
    <div class="actions">
      <a href="#projects" class="btn">View Projects</a>
      <a href="#contact" class="btn alt">Let's Talk</a>
    </div>
  </section>

  <section id="projects">
    <h2 class="section-title"><span class="num">01</span> Selected Projects</h2>
    <div class="grid">
      <article class="box project">
        <div class="band c-yellow">Dashboard</div>
        <div class="body">
          <h3>Stuff Dashboard</h3>
          <p>A control panel that helps HR easily access employee information.</p>
          <a href="https://omar-dev.site" class="btn sm" target="_blank" rel="noopener">View Project</a>
        </div>
      </article>
      <article class="box project">
        <div class="band c-blue">Education</div>
        <div class="body">
          <h3>Exam Website</h3>
          <p>An online exam platform serving 32 schools in Saudi Arabia to determine students' levels.</p>
          <a href="https://omar-dev.site" class="btn sm" target="_blank" rel="noopener">View Project</a>
        </div>
      </article>
    </div>
  </section>

  <section id="stack">
    <h2 class="section-title"><span class="num">02</span> Tech Stack</h2>
    <div class="box">
      <div class="stack">
        <span class="chip">HTML</span>
        <span class="chip">CSS</span>
        <span class="chip">JavaScript</span>
        <span class="chip">TypeScript</span>
        <span class="chip">React</span>
        <span class="chip">Next.js</span>
        <span class="chip">Node.js</span>
        <span class="chip">Express</span>
        <span class="chip">MongoDB</span>
        <span class="chip">Git</span>
        <span class="chip">GitHub</span>
      </div>
    </div>
  </section>

  <footer class="box footer" id="contact">
    <h2>BUILD. CREATE. INNOVATE.</h2>
    <p>Always learning. Always building.</p>
    <div class="socials">
      <a href="https://omar-dev.site" class="btn" target="_blank" rel="noopener">Portfolio</a>
      <a href="https://www.youtube.com/@OmarDev7720" class="btn alt" target="_blank" rel="noopener">YouTube</a>
      <a href="https://www.linkedin.com/in/omar-mohammed-4a011b372" class="btn blue" target="_blank" rel="noopener">LinkedIn</a>
    </div>
  </footer>

</div>
</body>
</html>
