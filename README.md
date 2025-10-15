<!doctype html>

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>EL BRAHAM — Digital Architect</title>
  <meta name="description" content="Akintonde Akolade — Digital Architect & Developer" />
  <style>
    /* UI/UX-focused dark tech + gold marble theme
       Mobile-first, clean layout, polished micro-interactions */
    :root{
      --bg:#07080a;
      --panel: rgba(255,255,255,0.035);
      --muted:#9aa0a6;
      --gold:#d4af37;
      --glass: rgba(255,255,255,0.03);
      --accent-glow: 0 10px 30px rgba(212,175,55,0.12);
      --container:18px;
      --max-w:1100px;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
    }
    html,body{height:100%;margin:0;background:var(--bg);color:#eaeef6}/* Elegant marble texture using layered gradients */
.bg-marble{position:fixed;inset:0;z-index:0;pointer-events:none;background:
  linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00)),
  radial-gradient(800px 120px at 5% 10%, rgba(212,175,55,0.03), transparent 6%),
  linear-gradient(120deg, rgba(212,175,55,0.02), rgba(255,255,255,0.01));
  mix-blend-mode:overlay;filter:blur(8px);opacity:0.95}

.marble-streak{position:fixed;left:-20%;top:35%;width:140%;height:22vh;transform:rotate(-7deg);z-index:0;background:linear-gradient(90deg, rgba(212,175,55,0.06) 0%, rgba(255,255,255,0.02) 30%, rgba(212,175,55,0.05) 100%);opacity:0.9}

.container{position:relative;z-index:1;max-width:var(--max-w);margin:26px auto;padding:var(--container)}

header{display:flex;align-items:center;justify-content:space-between;gap:12px;padding:12px;border-radius:14px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.02);box-shadow:var(--accent-glow)}
.brand{display:flex;align-items:center;gap:12px}
.logo{width:56px;height:56px;border-radius:12px;background:linear-gradient(135deg,#0f1113, rgba(212,175,55,0.08));display:flex;align-items:center;justify-content:center;font-weight:800;color:var(--gold);font-size:20px;border:1px solid rgba(212,175,55,0.12)}
.title{font-weight:800;font-size:15px}
.sub{font-size:12px;color:var(--muted)}

nav{display:flex;gap:10px}
.nav-link{color:var(--muted);font-weight:700;text-decoration:none;padding:8px 10px;border-radius:8px}
.nav-link:hover{color:#fff;background:rgba(255,255,255,0.02)}

/* Hero / showcase */
.hero{display:grid;grid-template-columns:1fr;gap:16px;padding:20px;margin-top:16px;border-radius:14px;background:linear-gradient(180deg, rgba(255,255,255,0.015), rgba(255,255,255,0.008));border:1px solid rgba(255,255,255,0.02)}
.hero-left{display:flex;flex-direction:column;gap:14px}
.eyebrow{color:var(--gold);font-weight:800;font-size:12px;letter-spacing:1px}
.hero-title{font-size:28px;font-weight:900;line-height:1.02}
.hero-title .gold{color:var(--gold);text-shadow:0 10px 30px rgba(212,175,55,0.08)}
.hero-desc{color:var(--muted);line-height:1.6}

.cta-row{display:flex;gap:10px;flex-wrap:wrap}
.btn{background:transparent;border:1px solid rgba(255,255,255,0.04);padding:10px 14px;border-radius:10px;color:#fff;text-decoration:none;font-weight:800}
.btn.primary{background:linear-gradient(90deg, rgba(212,175,55,0.12), rgba(212,175,55,0.06));border:1px solid rgba(212,175,55,0.18);box-shadow:var(--accent-glow)}

/* right card */
.hero-card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:16px;border-radius:12px;border:1px solid rgba(255,255,255,0.02);align-self:center}
.hero-card h4{margin:0 0 6px 0}
.meta{color:var(--muted);font-size:13px}

/* grid for sections */
.grid{display:grid;grid-template-columns:1fr;gap:14px;margin-top:18px}
.panel{padding:16px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.015), rgba(255,255,255,0.006));border:1px solid rgba(255,255,255,0.02)}

.skills{display:flex;gap:8px;flex-wrap:wrap;margin-top:8px}
.chip{padding:8px 10px;border-radius:999px;background:rgba(255,255,255,0.02);font-weight:800}

/* Projects showcase */
.projects-grid{display:grid;grid-template-columns:1fr;gap:10px;margin-top:12px}
.proj{padding:12px;border-radius:10px;background:linear-gradient(90deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.02);display:flex;flex-direction:column;gap:8px}
.proj .title{font-weight:800}
.proj .desc{color:var(--muted);font-size:13px}

/* contact */
.contact-row{display:flex;flex-direction:column;gap:12px}
.contact-card{display:flex;justify-content:space-between;align-items:center}
.contact-card .info{display:flex;flex-direction:column}
.contact-card .info .muted{color:var(--muted)}

footer{margin-top:20px;text-align:center;color:var(--muted);font-size:13px}

/* responsive for larger screens */
@media(min-width:800px){
  .hero{grid-template-columns:1fr 360px}
  .grid{grid-template-columns:1fr 380px}
  .projects-grid{grid-template-columns:repeat(2,1fr)}
  .hero-title{font-size:40px}
}

/* micro interactions */
.btn, .proj{transition:all .22s cubic-bezier(.2,.9,.2,1)}
.btn:hover{transform:translateY(-4px)}
.proj:hover{transform:translateY(-6px);box-shadow:var(--accent-glow)}

  </style>
</head>
<body>
  <div class="bg-marble"></div>
  <div class="marble-streak"></div>  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">EB</div>
        <div>
          <div class="title">Akintonde Akolade</div>
          <div class="sub">EL BRAHAM — Digital Architect</div>
        </div>
      </div>
      <nav>
        <a class="nav-link" href="#about">About</a>
        <a class="nav-link" href="#skills">Skills</a>
        <a class="nav-link" href="#projects">Projects</a>
        <a class="nav-link" href="#contact">Contact</a>
      </nav>
    </header><section class="hero">
  <div class="hero-left">
    <div class="eyebrow">DIGITAL ARCHITECT</div>
    <div class="hero-title">EL <span class="gold">BRAHAM</span> — Crafting Intelligent Web Experiences</div>
    <div class="hero-desc">I build fast, accessible, and conversion-focused websites. I merge design thinking with clean code to create products that scale.</div>
    <div class="cta-row">
      <a class="btn primary" href="mailto:akintondeakolade10@gmail.com">Hire Me</a>
      <a class="btn" href="#projects">View Projects</a>
      <a class="btn" href="https://wa.me/2347034016397" target="_blank">Message</a>
    </div>
    <div style="margin-top:8px;color:var(--muted);font-size:13px">Location: Lagos, Nigeria • Available for remote & local projects</div>
  </div>

  <aside class="hero-card">
    <h4 style="margin:0">Quick Profile</h4>
    <div class="meta" style="margin-top:6px">Akintonde Akolade — EL BRAHAM</div>
    <div style="margin-top:10px;font-weight:800">Expertise</div>
    <div style="display:flex;gap:8px;margin-top:8px;flex-wrap:wrap">
      <div class="chip">HTML</div>
      <div class="chip">CSS</div>
      <div class="chip">JavaScript</div>
      <div class="chip">UI/UX</div>
      <div class="chip">Vercel</div>
    </div>
  </aside>
</section>

<div class="grid">
  <div class="panel" id="about">
    <h3 style="margin-top:0">About</h3>
    <p style="color:var(--muted);line-height:1.6">I'm Akintonde Akolade, known professionally as <strong>EL BRAHAM</strong>. I design and develop modern web products focused on performance, user experience, and measurable results. I take concepts from idea to live product with an emphasis on speed and clarity.</p>
  </div>

  <aside class="panel" id="skills">
    <h4 style="margin-top:0">Skills</h4>
    <div class="skills">
      <div class="chip">Responsive Design</div>
      <div class="chip">Performance Optimization</div>
      <div class="chip">Accessibility (a11y)</div>
      <div class="chip">Component-Driven UI</div>
      <div class="chip">Deployment (Vercel)</div>
    </div>

    <div style="margin-top:12px">
      <h4 style="margin-bottom:8px">What I deliver</h4>
      <div style="color:var(--muted);font-size:13px;line-height:1.5">Premium landing pages, portfolio sites, and front-end builds that are fast and easy to maintain. I focus on clean code and strong visuals that convert.</div>
    </div>
  </aside>

  <div class="panel" id="projects">
    <h3 style="margin-top:0">Projects</h3>
    <div class="projects-grid">
      <div class="proj">
        <div class="title">Premium Landing Page</div>
        <div class="desc">High-converting landing page built for small businesses. Features fast load time and responsive design.</div>
        <div style="display:flex;gap:8px;margin-top:8px"><span class="chip">HTML</span><span class="chip">CSS</span></div>
      </div>

      <div class="proj">
        <div class="title">Personal Portfolio (This Site)</div>
        <div class="desc">A dark-tech UI/UX focused portfolio showcasing skills, contact, and project demos.</div>
        <div style="display:flex;gap:8px;margin-top:8px"><span class="chip">HTML</span><span class="chip">CSS</span><span class="chip">JS</span></div>
      </div>

      <div class="proj">
        <div class="title">E-commerce Template</div>
        <div class="desc">Component-driven product pages optimized for quick store setup.</div>
        <div style="display:flex;gap:8px;margin-top:8px"><span class="chip">Responsive</span><span class="chip">Performance</span></div>
      </div>

      <div class="proj">
        <div class="title">Landing Page for SaaS</div>
        <div class="desc">Modern marketing site with clear CTA and analytics-ready structure.</div>
        <div style="display:flex;gap:8px;margin-top:8px"><span class="chip">SEO</span><span class="chip">Vercel</span></div>
      </div>
    </div>
  </div>

  <div class="panel" id="contact">
    <h3 style="margin-top:0">Contact</h3>
    <div class="contact-row">
      <div class="contact-card">
        <div class="info">
          <div style="font-weight:800">Email</div>
          <div class="muted">akintondeakolade10@gmail.com</div>
        </div>
        <a class="btn primary" href="mailto:akintondeakolade10@gmail.com">Email</a>
      </div>

      <div class="contact-card">
        <div class="info">
          <div style="font-weight:800">Phone</div>
          <div class="muted">07034016397 (WhatsApp)</div>
        </div>
        <a class="btn" href="https://wa.me/2347034016397" target="_blank">Message</a>
      </div>
    </div>
  </div>
</div>

<footer>
  © <span id="year"></span> EL BRAHAM — Digital Architect • Built by Akintonde Akolade
</footer>

  </div>  <script>
    document.getElementById('year').textContent = new Date().getFullYear();

    // Smooth scroll for internal links
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click',function(e){
        e.preventDefault();
        const id = this.getAttribute('href').slice(1);
        const el = document.getElementById(id);
        if(el) el.scrollIntoView({behavior:'smooth',block:'start'});
      });
    });
  </script></body>
</html>