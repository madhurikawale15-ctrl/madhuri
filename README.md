<!DOCTYPE html>
<html lang="mr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>माझी GitHub Website</title>

  <style>
    :root{
      --bg:#f6f8fb;
      --primary:#0b66ff;
      --dark:#102a43;
      --muted:#556377;
      --card:#ffffff;
      --radius:12px;
      --container:1100px;
    }

    *{box-sizing:border-box;margin:0;padding:0;font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, Arial;}

    body{
      background:var(--bg);
      color:var(--dark);
      line-height:1.6;
    }

    .container{
      width:90%;
      max-width:var(--container);
      margin:0 auto;
    }

    /* header */
    .site-header{
      background:#fff;
      border-bottom:1px solid #e6eef6;
      position:sticky;
      top:0;
      z-index:10;
    }
    .site-header .container{
      display:flex;
      align-items:center;
      justify-content:space-between;
      padding:18px 0;
    }
    .logo{ font-size:1.2rem; color:var(--primary); }
    .site-header nav a{
      margin-left:18px;
      text-decoration:none;
      color:var(--muted);
      font-weight:600;
    }
    .site-header nav a:hover{ color:var(--primary); }

    /* hero */
    .hero{
      padding:70px 0;
      background:linear-gradient(180deg, rgba(11,102,255,0.06), transparent 60%);
    }
    .hero-inner{
      text-align:left;
      padding:40px;
      border-radius:14px;
      background:rgba(255,255,255,0.7);
      box-shadow:0 6px 22px rgba(16,42,67,0.06);
    }
    .hero h2{ font-size:2rem; color:var(--dark); margin-bottom:10px;}
    .hero p{ color:var(--muted); margin-bottom:16px; max-width:720px; }
    .btn{
      display:inline-block;
      padding:10px 16px;
      background:var(--primary);
      color:#fff;
      text-decoration:none;
      border-radius:10px;
      font-weight:700;
    }

    /* sections */
    .section{ padding:48px 0; }
    .section h3{ font-size:1.2rem; margin-bottom:8px; color:var(--dark); }
    .section p{ color:var(--muted); max-width:900px; }

    /* cards */
    .cards{
      display:grid;
      grid-template-columns:repeat(auto-fit, minmax(220px, 1fr));
      gap:18px;
    }
    .card{
      background:var(--card);
      padding:18px;
      border-radius:var(--radius);
      box-shadow:0 6px 18px rgba(16,42,67,0.04);
    }

    /* footer */
    .site-footer{
      padding:20px 0;
      text-align:center;
      color:var(--muted);
      border-top:1px solid #e6eef6;
      margin-top:30px;
    }

    @media (max-width:700px){
      .site-header .container{ flex-direction:column; gap:10px; align-items:flex-start; }
      .hero-inner{ padding:20px; text-align:center; }
    }
  </style>
</head>
<body>
  <header class="site-header">
    <div class="container">
      <h1 class="logo">माझं वेबपेज</h1>
      <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main>
    <section id="home" class="hero">
      <div class="container hero-inner">
        <h2>🚀 Welcome to my GitHub Pages site</h2>
        <p>हे एक simple आणि सुंदर static site template आहे — GitHub Pages वर सहज host करता येईल.</p>
        <a class="btn" href="#about">Learn more</a>
      </div>
    </section>

    <section id="about" class="section container">
      <h3>About Me</h3>
      <p>मी एक student/developer आहे. हा template GitHub Pages वर दाखवण्यासाठी बनवलाय.</p>
    </section>

    <section id="services" class="section container cards">
      <article class="card">
        <h4>Web Design</h4>
        <p>Simple, responsive design for small projects and portfolios.</p>
      </article>
      <article class="card">
        <h4>Projects</h4>
        <p>Static websites, portfolio pages, small apps built with HTML/CSS/JS.</p>
      </article>
      <article class="card">
        <h4>Contact</h4>
        <p>Reach out via email or GitHub profile link below.</p>
      </article>
    </section>

    <section id="contact" class="section container">
      <h3>Contact</h3>
      <p>Email: <a href="mailto:yourname@example.com">yourname@example.com</a></p>
      <p>GitHub: <a href="https://github.com/username" target="_blank">github.com/username</a></p>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container">
      <p>© <span id="year"></span> तुमचं नाव • बनवलं GitHub Pages वर</p>
    </div>
  </footer>

  <script>
    // वर्ष आपोआप अपडेट होईल
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
