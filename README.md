<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Elijah Jeremy Siwa | Student Portfolio</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg: #EEF2F7;
      --navy: #1B2F4B;
      --deep: #14263D;
      --heading: #1B3A5C;
      --ink: #1F2933;
      --muted: #4A5868;
      --steel: #8FA7C2;
      --tint: #D9E4F1;
      --panel: #E2EAF3;
      --panel-shadow: #B5C5D9;
      --accent: #2B6CB0;
      --body: 'Poppins', 'Segoe UI', Arial, sans-serif;
    }

    * { box-sizing: border-box; }

    html { scroll-padding-top: 92px; }

    @media (prefers-reduced-motion: no-preference) {
      html { scroll-behavior: smooth; }
    }

    body {
      margin: 0;
      background: var(--bg);
      color: var(--ink);
      font-family: var(--body);
      font-size: 17px;
      line-height: 1.6;
    }

    a:focus-visible,
    input:focus-visible {
      outline: 3px solid var(--accent);
      outline-offset: 3px;
    }

    /* ---------- Navigation ---------- */
    .nav {
      position: sticky;
      top: 0;
      z-index: 20;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 8px 24px;
      padding: 14px 36px;
      background: #fff;
      border-bottom: 5px solid var(--navy);
    }

    .logo {
      font-size: 28px;
      font-weight: 800;
      letter-spacing: 0.08em;
      line-height: 1.2;
      color: var(--navy);
      text-decoration: none;
    }

    .nav-links {
      display: flex;
      flex-wrap: wrap;
      gap: 6px 34px;
    }

    .nav-links a {
      font-size: 17px;
      font-weight: 600;
      color: var(--accent);
      text-decoration: none;
    }

    .nav-links a:hover { color: var(--deep); }

    /* ---------- Buttons ---------- */
    .btn {
      display: inline-block;
      margin: 6px;
      padding: 12px 30px;
      border: 3px solid var(--navy);
      border-radius: 999px;
      background: var(--navy);
      color: #fff;
      font: 600 17px var(--body);
      text-decoration: none;
      box-shadow: 4px 4px 0 var(--panel-shadow);
      cursor: pointer;
      transition: transform 0.15s;
    }

    .btn:hover { transform: translateY(-2px); }

    .btn.alt {
      background: #fff;
      color: var(--navy);
      border-color: var(--steel);
    }

    /* ---------- Hero ---------- */
    .hero {
      padding: 72px 20px 64px;
      text-align: center;
      background-color: var(--tint);
      background-image:
        radial-gradient(circle, #fff 3.5px, transparent 4.5px),
        radial-gradient(circle, #fff 3.5px, transparent 4.5px);
      background-size: 50px 50px;
      background-position: 0 0, 25px 25px;
      border-radius: 0 0 70px 70px;
    }

    /* Circular profile with dashed ring */
    .photo {
      width: 290px;
      height: 290px;
      margin: 0 auto 30px;
      padding: 9px;
      background: #fff;
      border: 5px dashed var(--navy);
      border-radius: 50%;
      box-shadow: 0 0 0 9px var(--tint), 10px 12px 0 8px var(--panel-shadow);
    }

    .photo-inner {
      position: relative;
      width: 100%;
      height: 100%;
      overflow: hidden;
      border-radius: 50%;
      background: var(--navy);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      font-size: 64px;
      font-weight: 800;
      letter-spacing: 0.05em;
    }

    .photo-inner img {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center top;
    }

    .hello {
      margin: 0;
      font-size: 22px;
      font-weight: 600;
      color: var(--accent);
    }

    h1 {
      margin: 4px 0 14px;
      font-size: 56px;
      font-weight: 800;
      line-height: 1.2;
      color: var(--navy);
      text-shadow: 3px 3px 0 var(--panel-shadow);
    }

    .tagline {
      max-width: 620px;
      margin: 0 auto 30px;
      font-size: 19px;
      color: var(--muted);
    }

    /* ---------- Sections and cards ---------- */
    .section { padding: 84px 24px; }

    .wrap {
      max-width: 1120px;
      margin: 0 auto;
    }

    .blue {
      margin: 0 12px;
      background: var(--panel);
      border-radius: 70px;
    }

    .title {
      margin: 0 0 44px;
      font-size: 40px;
      font-weight: 800;
      line-height: 1.3;
      text-align: center;
      color: var(--navy);
    }

    .grid2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 36px;
    }

    .card {
      padding: 34px 38px;
      background: #fff;
      border: 4px solid var(--steel);
      border-radius: 28px;
      box-shadow: 10px 10px 0 var(--panel-shadow);
    }

    .card h3 {
      margin: 0 0 18px;
      font-size: 26px;
      font-weight: 700;
      line-height: 1.3;
      color: var(--heading);
    }

    /* ---------- About ---------- */
    .about-text {
      margin: 0;
      line-height: 2;
    }

    .about-text strong { color: var(--heading); }

    .facts {
      display: grid;
      grid-template-columns: max-content 1fr;
      gap: 16px;
      align-items: center;
      margin: 0;
    }

    .facts dt {
      padding: 5px 16px;
      background: var(--tint);
      border-radius: 999px;
      color: var(--navy);
      font-size: 14px;
      font-weight: 600;
      letter-spacing: 0.06em;
      text-transform: uppercase;
    }

    .facts dd {
      margin: 0;
      font-weight: 600;
    }

    /* ---------- Skills ---------- */
    .skill-list {
      display: grid;
      gap: 14px;
      margin: 0;
      padding: 0;
      list-style: none;
    }

    .skill-list li {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 6px 14px;
    }

    .chip {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 8px 20px;
      background: var(--tint);
      border-radius: 999px;
      color: var(--deep);
      font-weight: 600;
    }

    .chip i {
      font-style: normal;
      color: var(--accent);
    }

    .how {
      font-size: 16px;
      color: var(--muted);
    }

    /* ---------- Education ---------- */
    .edu-list {
      display: grid;
      gap: 28px;
    }

    .edu {
      display: flex;
      align-items: center;
      gap: 22px;
      padding: 26px 32px;
      background: #fff;
      border: 3px dashed var(--steel);
      border-radius: 26px;
    }

    .ribbon {
      font-size: 42px;
      line-height: 1;
    }

    .badge {
      display: inline-block;
      margin-bottom: 6px;
      padding: 3px 16px;
      background: var(--navy);
      border-radius: 999px;
      color: #fff;
      font-size: 14px;
      font-weight: 700;
    }

    .edu h3 {
      margin: 0 0 2px;
      font-size: 24px;
      line-height: 1.3;
      text-transform: uppercase;
      color: var(--heading);
    }

    .edu p { margin: 0; }

    /* ---------- Contact ---------- */
    .grid2.contact { align-items: start; }

    .contact-card { text-align: center; }

    .big-ico {
      font-size: 52px;
      line-height: 1.2;
    }

    .contact-card .tagline {
      margin-bottom: 20px;
      font-size: 18px;
    }

    .socials {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-top: 24px;
    }

    .social {
      padding: 6px 18px;
      background: var(--tint);
      border-radius: 999px;
      color: var(--navy);
      font-weight: 600;
      text-decoration: none;
    }

    .social:hover {
      background: var(--navy);
      color: #fff;
    }

    fieldset {
      min-width: 0;
      margin: 0;
      padding: 0;
      border: 0;
    }

    legend {
      margin: 0 0 18px;
      padding: 0;
      font-size: 26px;
      font-weight: 700;
      color: var(--heading);
    }

    label {
      display: block;
      margin-bottom: 6px;
      font-weight: 600;
      color: var(--heading);
    }

    input[type="text"],
    input[type="email"] {
      display: block;
      width: 100%;
      margin-bottom: 18px;
      padding: 12px 16px;
      background: var(--bg);
      border: 3px solid var(--steel);
      border-radius: 14px;
      color: var(--ink);
      font: 500 16px var(--body);
    }

    input::placeholder { color: #6B7A8C; }

    form .btn { margin-left: 0; }

    /* ---------- Footer ---------- */
    .footer {
      margin-top: 40px;
      padding: 40px 20px 44px;
      background: var(--deep);
      border-radius: 70px 70px 0 0;
      color: #fff;
      text-align: center;
    }

    .footer p {
      margin: 0 0 8px;
      font-size: 16px;
      font-weight: 600;
    }

    .footer a {
      color: #fff;
      font-weight: 600;
    }

    /* ---------- Phones and small screens ---------- */
    @media (max-width: 800px) {
      html { scroll-padding-top: 70px; }

      .nav {
        justify-content: center;
        padding: 10px 16px;
      }

      .nav-links { gap: 4px 20px; }
      .nav-links a { font-size: 16px; }

      .hero {
        padding: 56px 16px 48px;
        border-radius: 0 0 44px 44px;
      }

      .photo {
        width: 240px;
        height: 240px;
      }

      h1 { font-size: 36px; }

      .section { padding: 60px 16px; }

      .blue {
        margin: 0 8px;
        border-radius: 44px;
      }

      .title {
        margin-bottom: 32px;
        font-size: 32px;
      }

      .grid2 {
        grid-template-columns: 1fr;
        gap: 30px;
      }

      .card {
        padding: 26px 22px;
        border-radius: 24px;
        box-shadow: 7px 7px 0 var(--panel-shadow);
      }

      .footer { border-radius: 44px 44px 0 0; }
    }

    @media (max-width: 600px) {
      .logo { font-size: 24px; }
      .nav-links { gap: 4px 14px; }
      .nav-links a { font-size: 15px; }

      .edu {
        flex-direction: column;
        padding: 22px;
        text-align: center;
      }

      .skill-list li {
        flex-direction: column;
        align-items: flex-start;
        gap: 4px;
      }

      .facts {
        grid-template-columns: 1fr;
        gap: 6px;
      }

      .facts dt { justify-self: start; }

      .facts dd { margin-bottom: 10px; }
    }
  </style>
</head>
<body>

  <nav class="nav">
    <a class="logo" href="#home">EJS</a>
    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#education">Education</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <header id="home" class="hero">
    <div class="photo">
      <div class="photo-inner">
        EJS
        <img src="data:image/jpeg;base64,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" alt="Photo of Elijah Jeremy Siwa" onerror="this.style.display='none'">
      </div>
    </div>
    <p class="hello">Hello, I'm</p>
    <h1>Elijah Jeremy Siwa</h1>
    <p class="tagline">I'm a student who loves technology, design, and learning by building things. Welcome to my portfolio.</p>
    <a class="btn" href="#about">About me</a>
    <a class="btn alt" href="#contact">Contact me</a>
  </header>

  <main>

    <section id="about" class="section">
      <div class="wrap">
        <h2 class="title"><span aria-hidden="true">👋</span> About me</h2>

        <div class="grid2">
          <div class="card">
            <p class="about-text">I enjoy <strong>figuring out how things work</strong>, whether it's a school science project or a website I'm building for fun. I like working with a team, asking lots of questions, and turning ideas into something people can use. <em>One day I want to build apps that make life easier for others.</em></p>
          </div>

          <div class="card">
            <dl class="facts">
              <dt>School</dt>
              <dd>DFCAMCLP</dd>

              <dt>Grade level</dt>
              <dd>2nd year</dd>

              <dt>Favorite subjects</dt>
              <dd>Computer, Science</dd>

              <dt>Hobbies</dt>
              <dd>Gaming, long rides, music</dd>
            </dl>
          </div>
        </div>
      </div>
    </section>

    <section id="skills" class="section">
      <div class="wrap">
        <h2 class="title"><span aria-hidden="true">💻</span> My skills</h2>

        <div class="grid2">
          <div class="card">
            <h3>Tech</h3>
            <ul class="skill-list">
              <li><span class="chip"><i aria-hidden="true">▸</i> HTML</span> <span class="how">Building web pages</span></li>
              <li><span class="chip"><i aria-hidden="true">▸</i> CSS</span> <span class="how">Colors, layout, and design</span></li>
              <li><span class="chip"><i aria-hidden="true">▸</i> Python</span> <span class="how">School programming exercises</span></li>
              <li><span class="chip"><i aria-hidden="true">▸</i> Canva</span> <span class="how">Posters and presentations</span></li>
            </ul>
          </div>

          <div class="card">
            <h3>People</h3>
            <ul class="skill-list">
              <li><span class="chip"><i aria-hidden="true">▸</i> Teamwork</span> <span class="how">Group projects and reports</span></li>
              <li><span class="chip"><i aria-hidden="true">▸</i> Communication</span> <span class="how">Class reports and discussions</span></li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section id="education" class="section blue">
      <div class="wrap">
        <h2 class="title"><span aria-hidden="true">🎓</span> Education and achievements</h2>

        <div class="edu-list">
          <div class="edu">
            <span class="ribbon" aria-hidden="true">🏅</span>
            <div>
              <span class="badge">2024 to Now</span>
              <h3>College</h3>
              <p>DFCAMCLP. Studying subjects I enjoy all the school activities.</p>
            </div>
          </div>

          <div class="edu">
            <span class="ribbon" aria-hidden="true">🏅</span>
            <div>
              <span class="badge">2021 to 2023</span>
              <h3>Senior High School</h3>
              <p>CAA National Senior High School CAA Campus. Studying subjects I enjoy and joining school activities.</p>
            </div>
          </div>

          <div class="edu">
            <span class="ribbon" aria-hidden="true">🏅</span>
            <div>
              <span class="badge">2016 to 2020</span>
              <h3>Junior High School</h3>
              <p>CAA National High School ANNEX. This is where I first discovered my love for computers.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="contact" class="section">
      <div class="wrap">
        <h2 class="title"><span aria-hidden="true">📞</span> Let's get in touch</h2>

        <div class="grid2 contact">
          <div class="card contact-card">
            <div class="big-ico" aria-hidden="true">✉️</div>
            <p class="tagline">Have a question, a project idea, or just want to say hi? Send me a message and I'll reply as soon as I can.</p>

            <a class="btn" href="mailto:your.email@example.com">Email me</a>

            <div class="socials">
              <a class="social" href="#">Facebook</a>
              <a class="social" href="#">Instagram</a>
              <a class="social" href="#">GitHub</a>
              <a class="social" href="#">LinkedIn</a>
            </div>
          </div>

          <div class="card">
            <form method="GET" action="#">
              <fieldset>
                <legend>Send me a message</legend>

                <label for="name">Your name</label>
                <input type="text" id="name" name="name" placeholder="Name" required>

                <label for="email">Your email</label>
                <input type="email" id="email" name="email" placeholder="Email" required>

                <label for="subject">Subject</label>
                <input type="text" id="subject" name="subject" placeholder="What is this about?">

                <input class="btn" type="submit" value="Send">
              </fieldset>
            </form>
          </div>
        </div>
      </div>
    </section>

  </main>

  <footer class="footer">
    <p>&copy; 2026 Elijah Jeremy Siwa. Made with HTML and CSS.</p>
    <a href="#home">&uarr; Back to top</a>
  </footer>

</body>
</html>
