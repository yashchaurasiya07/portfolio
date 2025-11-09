<!doctype html>
<html lang="en">

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Yash Dinesh Chaurasiya — Portfolio</title>
  <meta name="description"
    content="Portfolio of Yash Dinesh Chaurasiya — Frontend Developer, Digital Designer, Prompt Engineer.">

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">

  <!-- AOS (Animate on Scroll) -->
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">

  <!-- Font Awesome Icons -->
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" rel="stylesheet">

  <style>
    :root {
      --bg: #0f1724;
      --card: #0b1220;
      --accent: #7c3aed;
      --muted: #94a3b8;
      --glass: rgba(255, 255, 255, 0.04);
      --radius: 14px;
      --fw-sans: 'Inter', system-ui, Arial;
    }

    * {
      box-sizing: border-box
    }

    html,
    body {
      height: 100%
    }

    body {
      margin: 0;
      font-family: var(--fw-sans);
      background: linear-gradient(180deg, #020617 0%, #071028 60%);
      color: #e6eef8;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    /* Container */
    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 36px
    }

    /* NAV */
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 12px 0
    }

    .brand {
      display: flex;
      gap: 14px;
      align-items: center
    }

    .logo {
      width: 48px;
      height: 48px;
      border-radius: 10px;
      background: linear-gradient(135deg, var(--accent), #06b6d4);
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 700;
      color: white
    }

    nav a {
      color: var(--muted);
      text-decoration: none;
      margin-left: 18px;
      font-weight: 600
    }

    nav a:hover {
      color: white
    }

    /* HERO */
    .hero {
      display: grid;
      grid-template-columns: 1fr 420px;
      gap: 32px;
      padding: 48px 0;
      align-items: center
    }

    .intro h1 {
      font-size: 36px;
      margin: 0 0 8px
    }

    .intro h1 .name {
      background: linear-gradient(90deg, #fff 0%, #c7b6ff 100%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent
    }

    .typed {
      color: var(--accent);
      font-weight: 700
    }

    .cta {
      margin-top: 18px
    }

    .btn {
      background: linear-gradient(90deg, var(--accent), #06b6d4);
      border: none;
      padding: 12px 18px;
      border-radius: 12px;
      color: white;
      font-weight: 700;
      cursor: pointer;
      box-shadow: 0 6px 18px rgba(124, 58, 237, 0.18);
      transition: all .3s ease
    }

    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 25px rgba(124, 58, 237, 0.3)
    }

    .hero-card {
      background: linear-gradient(180deg, rgba(255, 255, 255, 0.02), rgba(255, 255, 255, 0.01));
      padding: 18px;
      border-radius: 18px;
      box-shadow: 0 8px 30px rgba(2, 6, 23, 0.7)
    }

    .profile {
      display: flex;
      gap: 14px;
      align-items: center
    }

    .avatar {
      width: 84px;
      height: 84px;
      border-radius: 12px;
      background: linear-gradient(135deg, #334155, #0ea5a4);
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 800
    }

    .meta p {
      margin: 0;
      color: var(--muted)
    }

    /* Skills */
    .skills {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      margin-top: 22px
    }

    .skill {
      background: var(--glass);
      padding: 10px 14px;
      border-radius: 12px;
      font-weight: 700;
      color: var(--muted)
    }

    /* Projects */
    .projects {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
      margin-top: 26px
    }

    .project {
      background: linear-gradient(180deg, rgba(255, 255, 255, 0.02), rgba(255, 255, 255, 0.01));
      padding: 14px;
      border-radius: 12px;
      overflow: hidden;
      border: 1px solid rgba(255, 255, 255, 0.03);
      cursor: pointer;
      transition: transform .35s, box-shadow .35s
    }

    .project:hover {
      transform: translateY(-8px);
      box-shadow: 0 18px 40px rgba(2, 6, 23, 0.6)
    }

    .project img {
      width: 100%;
      height: 160px;
      object-fit: cover;
      border-radius: 8px
    }

    .project h3 {
      margin: 10px 0 6px
    }

    .project p {
      margin: 0;
      color: var(--muted);
      font-size: 14px
    }

    /* Timeline / Education */
    .timeline {
      margin-top: 30px;
      border-left: 3px solid rgba(255, 255, 255, 0.04);
      padding-left: 40px
    }

    .timeline-item {
      margin: 14px 0;
      position: relative
    }

    .timeline-item::before {
      content: '';
      position: absolute;
      left: -35px;
      top: 6px;
      width: 18px;
      height: 18px;
      background: var(--accent);
      border-radius: 50%
    }

    /* Achievements */
    .achievements {
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
      margin-top: 18px
    }

    .badge {
      padding: 10px 12px;
      border-radius: 10px;
      background: linear-gradient(90deg, rgba(124, 58, 237, 0.12), rgba(6, 182, 212, 0.06));
      font-weight: 700;
      color: #fff
    }

    /* Contact */
    .contact {
      display: grid;
      grid-template-columns: 1fr 320px;
      gap: 18px;
      margin-top: 26px
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 10px
    }

    input,
    textarea {
      background: transparent;
      border: 1px solid rgba(255, 255, 255, 0.06);
      padding: 12px;
      border-radius: 8px;
      color: #e6eef8
    }

    textarea {
      min-height: 120px
    }

    /* Footer */
    footer {
      margin-top: 36px;
      padding: 22px 0;
      color: var(--muted);
      text-align: center;
      border-top: 1px solid rgba(255, 255, 255, 0.05);
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 22px;
      margin-top: 10px;
    }

    .social-links a {
      color: var(--muted);
      font-size: 22px;
      transition: all .3s ease;
    }

    .social-links a:hover {
      color: var(--accent);
      transform: translateY(-3px);
    }

    /* Responsive */
    @media (max-width:980px) {
      .hero {
        grid-template-columns: 1fr;
      }

      .projects {
        grid-template-columns: 1fr
      }

      .contact {
        grid-template-columns: 1fr
      }

      nav a {
        display: none
      }
    }
  </style>
</head>

<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">YD</div>
        <div>
          <div style="font-weight:800">Yash Chaurasiya</div>
          <div style="font-size:12px;color:var(--muted)">Frontend Developer • Digital Designer</div>
        </div>
      </div>
      <nav>
        <a href="#about">About</a>
        <a href="#projects">Projects</a>
        <a href="#education">Education</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <!-- HERO -->
    <section class="hero">
      <div class="intro" data-aos="fade-up">
        <h1>Hi, I'm <span class="name">Yash Dinesh Chaurasiya</span></h1>
        <h2><span id="typed-text" class="typed"></span></h2>
        <p style="color:var(--muted);max-width:60%;">BCA student (Final year) with a 9.39 CGPA. Frontend Developer who
          crafts visually-focused responsive websites and digital content. Skilled in HTML, CSS, JavaScript, Canva and
          prompt engineering.</p>
        <div class="cta">
          <button class="btn" id="view-projects">View Projects</button>
        </div>

        <div class="skills" aria-hidden="false">
          <div class="skill">HTML5</div>
          <div class="skill">CSS3</div>
          <div class="skill">JavaScript</div>
          <div class="skill">Canva</div>
          <div class="skill">Prompt Eng.</div>
          <div class="skill">Google Cloud</div>
        </div>
      </div>

      <aside class="hero-card" data-aos="fade-left">
        <div class="profile">
          <div class="avatar">Y</div>
          <div class="meta">
            <div style="font-weight:800">Yash Dinesh Chaurasiya</div>
            <p>SYBCA • KCE Society's IMR Jalgaon</p>
            <p style="color:var(--muted);font-size:13px;margin-top:6px">CGPA: <strong>9.39 / 10</strong></p>
          </div>
        </div>

        <div style="margin-top:12px">
          <div style="display:flex;justify-content:space-between;color:var(--muted);font-size:13px">
            <div>
              <div style="font-weight:700">Phone</div>
              <div>7507184322</div>
            </div>
            <div style="text-align:right">
              <div style="font-weight:700">Email</div>
              <div>chaurasiyayash25@gmail.com</div>
            </div>
          </div>

          <div style="margin-top:12px;display:flex;gap:8px;flex-wrap:wrap">
            <a href="#projects" class="btn" style="padding:14px 12px;font-size:14px; text-decoration: none;">My Work</a>
            <a href="#contact" class="btn"
              style="background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted);box-shadow:none;text-decoration: none;">Contact
              Me</a>

            <!-- ✅ Resume Download -->
            <a href="https://drive.google.com/file/d/10goSoylGg2tt8xsVnnVSIxHt0eNLfFJh/view?usp=drive_link" download class="btn"
              style="padding:10px 12px;font-size:14px; text-decoration: none;">
              📄 Resume
            </a>
          </div>
        </div>
      </aside>
    </section>

    <!-- PROJECTS -->
    <section id="projects" data-aos="fade-up">
      <h2>Selected Projects</h2>
      <div class="projects">
        <div class="project" onclick="openModal('kick')" role="button" tabindex="0">
          <img src="https://images.unsplash.com/photo-1524758631624-e2822e304c36?q=80&w=1200&auto=format&fit=crop"
            alt="KickStore Screenshot">
          <h3>Kick{Store} — Static E-Commerce</h3>
          <p>Frontend design & prototype built with HTML/CSS. Responsive layouts, product grid, and visual hierarchy
            focused on conversions.</p>
        </div>

        <div class="project" onclick="openModal('portfolio')" role="button" tabindex="0">
          <img src="https://images.unsplash.com/photo-1506765515384-028b60a970df?q=80&w=1200&auto=format&fit=crop"
            alt="Content Portfolio">
          <h3>Digital Content Portfolio</h3>
          <p>30+ thumbnails & short-form video edits. Visual consistency using Canva and editing tools.</p>
        </div>
      </div>
    </section>

    <!-- Education -->
    <section id="education" data-aos="fade-up">
      <h2>Education</h2>
      <div class="timeline">
        <div class="timeline-item"><strong>2023 – 2026</strong>
          <div>BCA — KCE Society's IMR Jalgaon</div>
        </div>
        <div class="timeline-item"><strong>2021 – 2022</strong>
          <div>HSC — P.O. Nahata College, Bhusawal</div>
        </div>
        <div class="timeline-item"><strong>2008 – 2021</strong>
          <div>School — Dr. Ulhas Patil English Medium, Bhusawal</div>
        </div>
      </div>
    </section>

    <!-- Achievements -->
    <section data-aos="fade-up">
      <h2>Achievements & Training</h2>
      <div class="achievements">
        <div class="badge">Prompt Engineering — Course</div>
        <div class="badge">Google Cloud Workshop</div>
        <div class="badge">High CGPA — 9.39</div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact" data-aos="fade-up">
      <h2>Contact</h2>
      <div class="contact">
        <form id="contact-form" onsubmit="submitForm(event)">
          <input type="text" id="name" placeholder="Your name" required>
          <input type="email" id="email" placeholder="Email" required>
          <textarea id="message" placeholder="Your message" required></textarea>
          <button class="btn" type="submit">Send Message</button>
        </form>

        <aside class="hero-card" style="padding:14px">
          <h3>Get in touch</h3>
          <p style="color:var(--muted)">Phone: 7507184322</p>
          <p style="color:var(--muted)">Email: chaurasiyayash25@gmail.com</p>
          <p><a href="www.linkedin.com/in/yash-chaurasiya-5a1689308" style="color:var(--muted);text-decoration:underline"
              target="_blank">LinkedIn Profile</a></p>

          <!-- ✅ Lottie animation -->
          <lottie-player src="https://assets4.lottiefiles.com/packages/lf20_jcikwtux.json" background="transparent"
            speed="1" style="width:100%; height:200px;" loop autoplay>
          </lottie-player>
        </aside>
      </div>
    </section>

    <!-- ✅ FOOTER WITH SOCIAL LINKS -->
    <footer>
      <small>© 2025 Yash Dinesh Chaurasiya</small>
      <div class="social-links">
        <a href="https://youtube.com/@yash_prankster369?si=u77Wc6JZDbh7-QFf" target="_blank" title="YouTube"><i
            class="fab fa-youtube"></i></a>
        <a href="https://www.instagram.com/chaurasiya_yash07?igsh=MTBzY3F3MHkxOTYxZQ==" target="_blank" title="Instagram"><i
            class="fab fa-instagram"></i></a>
        <a href="www.linkedin.com/in/yash-chaurasiya-5a1689308" target="_blank" title="LinkedIn"><i
            class="fab fa-linkedin"></i></a>
        <a href="https://github.com/yourgithub" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>
      </div>
    </footer>
  </div>

  <!-- Modal -->
  <div id="modal"
    style="position:fixed;inset:0;background:rgba(2,6,23,0.7);display:none;align-items:center;justify-content:center;padding:20px;z-index:9999">
    <div
      style="background:#061126;padding:18px;border-radius:12px;max-width:900px;width:100%;color:#e6eef8;position:relative">
      <button onclick="closeModal()"
        style="position:absolute;right:12px;top:12px;border:none;background:transparent;color:var(--muted);font-size:20px;cursor:pointer">✕</button>
      <div id="modal-content"></div>
    </div>
  </div>

  <!-- Scripts -->
  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/typed.js/2.0.12/typed.min.js"></script>
  <script src="https://unpkg.com/@lottiefiles/lottie-player@latest/dist/lottie-player.js"></script>

  <script>
    // Init AOS
    AOS.init({ duration: 700, once: true, easing: 'ease-out-cubic' });

    // Typed.js intro
    new Typed('#typed-text', {
      strings: ["Frontend Developer", "Digital Designer", "Prompt Engineer", "Google Cloud Enthusiast"],
      typeSpeed: 70, backSpeed: 40, backDelay: 1400, loop: true
    });

    // Smooth scroll to Projects
    document.getElementById('view-projects').addEventListener('click', () => document.getElementById('projects').scrollIntoView({ behavior: 'smooth' }));

    // Modal
    function openModal(id) {
      const modal = document.getElementById('modal');
      const content = document.getElementById('modal-content');
      if (id === 'kick') {
        content.innerHTML = `
          <h2>Kick{Store} — Static E-Commerce</h2>
          <p style="color:var(--muted)">Role: Frontend Designer & Developer<br>Technologies: HTML, CSS</p>
          <img src="https://images.unsplash.com/photo-1524758631624-e2822e304c36?q=80&w=1600&auto=format&fit=crop" style="width:100%;border-radius:8px;margin-top:12px">
        `;
      } else {
        content.innerHTML = `
          <h2>Digital Content Portfolio</h2>
          <p style="color:var(--muted)">Role: Graphic & Video Editor<br>Tools: Canva, CapCut, Photoshop</p>
          <img src="https://images.unsplash.com/photo-1506765515384-028b60a970df?q=80&w=1600&auto=format&fit=crop" style="width:100%;border-radius:8px;margin-top:12px">
        `;
      }
      modal.style.display = 'flex';
    }
    function closeModal() { document.getElementById('modal').style.display = 'none' }

    // Form submission mock
    function submitForm(e) {
      e.preventDefault();
      alert('Thank you, your message has been sent!');
      e.target.reset();
    }
  </script>
</body>

</html>
