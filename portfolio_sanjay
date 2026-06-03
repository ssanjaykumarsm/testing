<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>IMRAN | UE5 Game Developer</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;500;700;900&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --gold: #d4af37;
      --gold-light: #f5d97a;
      --dark-gold: #8a6b12;
      --black: #050505;
      --soft-black: #101010;
      --card: rgba(20, 20, 20, 0.85);
      --white: #f5f5f5;
      --gray: #999;
      --border: rgba(212, 175, 55, 0.2);
    }

    body {
      background: var(--black);
      color: var(--white);
      font-family: 'Poppins', sans-serif;
      overflow-x: hidden;
      scroll-behavior: smooth;
      background-image:
        radial-gradient(circle at top left, rgba(212, 175, 55, 0.08), transparent 25%),
        radial-gradient(circle at bottom right, rgba(255, 100, 0, 0.08), transparent 20%);
    }

    ::selection {
      background: var(--gold);
      color: black;
    }

    /* Scroll Bar */
    ::-webkit-scrollbar {
      width: 8px;
    }

    ::-webkit-scrollbar-track {
      background: #0d0d0d;
    }

    ::-webkit-scrollbar-thumb {
      background: linear-gradient(var(--gold), #ff7300);
      border-radius: 10px;
    }

    /* NAVBAR */
    nav {
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 8%;
      backdrop-filter: blur(12px);
      background: rgba(0, 0, 0, 0.35);
      border-bottom: 1px solid rgba(255,255,255,0.05);
    }

    .logo {
      font-family: 'Cinzel', serif;
      font-size: 1.3rem;
      color: var(--gold);
      letter-spacing: 3px;
      font-weight: 700;
    }

    nav ul {
      display: flex;
      list-style: none;
      gap: 30px;
    }

    nav ul li a {
      color: white;
      text-decoration: none;
      font-size: 0.9rem;
      transition: 0.3s;
      position: relative;
    }

    nav ul li a::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      background: var(--gold);
      left: 0;
      bottom: -6px;
      transition: 0.4s ease;
    }

    nav ul li a:hover::after {
      width: 100%;
    }

    nav ul li a:hover {
      color: var(--gold-light);
    }

    /* HERO SECTION */
    .hero {
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 0 8%;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      inset: 0;
      background:
        linear-gradient(to bottom, rgba(0,0,0,0.4), rgba(0,0,0,0.9)),
        url('https://images.unsplash.com/photo-1511512578047-dfb367046420?q=80&w=1400&auto=format&fit=crop');
      background-size: cover;
      background-position: center;
      opacity: 0.35;
      animation: zoomBg 12s ease-in-out infinite alternate;
    }

    @keyframes zoomBg {
      from {
        transform: scale(1);
      }
      to {
        transform: scale(1.08);
      }
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 900px;
      text-align: center;
    }

    .tag {
      display: inline-block;
      padding: 8px 18px;
      border: 1px solid var(--gold);
      border-radius: 40px;
      color: var(--gold);
      letter-spacing: 2px;
      font-size: 0.75rem;
      margin-bottom: 25px;
      backdrop-filter: blur(10px);
      background: rgba(255,255,255,0.03);
      box-shadow: 0 0 25px rgba(212, 175, 55, 0.12);
    }

    .hero h1 {
      font-family: 'Cinzel', serif;
      font-size: clamp(4rem, 10vw, 8rem);
      line-height: 1;
      letter-spacing: 10px;
      color: var(--gold);
      text-transform: uppercase;
      animation: fadeUp 1.5s ease;
      text-shadow: 0 0 30px rgba(212,175,55,0.2);
    }

    .hero h2 {
      margin-top: 20px;
      font-size: 1.3rem;
      font-weight: 300;
      color: #d8d8d8;
      letter-spacing: 4px;
      animation: fadeUp 2s ease;
    }

    .hero p {
      margin: 30px auto;
      max-width: 700px;
      color: #bdbdbd;
      line-height: 1.9;
      font-size: 1rem;
      animation: fadeUp 2.4s ease;
    }

    .hero-buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 40px;
      flex-wrap: wrap;
    }

    .btn {
      padding: 14px 32px;
      border-radius: 40px;
      text-decoration: none;
      font-size: 0.95rem;
      transition: 0.4s ease;
      font-weight: 500;
      letter-spacing: 1px;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--gold), #ff8400);
      color: black;
      box-shadow: 0 0 30px rgba(212, 175, 55, 0.3);
    }

    .btn-primary:hover {
      transform: translateY(-4px) scale(1.02);
      box-shadow: 0 0 40px rgba(212, 175, 55, 0.45);
    }

    .btn-outline {
      border: 1px solid rgba(255,255,255,0.2);
      color: white;
      backdrop-filter: blur(8px);
      background: rgba(255,255,255,0.03);
    }

    .btn-outline:hover {
      border-color: var(--gold);
      color: var(--gold);
      transform: translateY(-4px);
    }

    .scroll-text {
      position: absolute;
      bottom: 40px;
      left: 50%;
      transform: translateX(-50%);
      color: var(--gold);
      font-size: 0.8rem;
      letter-spacing: 4px;
      animation: float 2s infinite;
      z-index: 2;
    }

    @keyframes float {
      0%, 100% {
        transform: translateX(-50%) translateY(0);
      }
      50% {
        transform: translateX(-50%) translateY(10px);
      }
    }

    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(40px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* SECTION TITLE */
    .section-title {
      text-align: center;
      margin-bottom: 70px;
    }

    .section-title h2 {
      font-family: 'Cinzel', serif;
      color: var(--gold);
      font-size: 3rem;
      margin-bottom: 15px;
      letter-spacing: 4px;
    }

    .section-title p {
      color: #a1a1a1;
      max-width: 700px;
      margin: auto;
      line-height: 1.8;
    }

    /* ABOUT */
    .about {
      padding: 120px 8%;
    }

    .about-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 50px;
      align-items: center;
    }

    .about-box {
      background: var(--card);
      border: 1px solid var(--border);
      padding: 40px;
      border-radius: 24px;
      backdrop-filter: blur(12px);
      transition: 0.4s ease;
      position: relative;
      overflow: hidden;
    }

    .about-box::before {
      content: '';
      position: absolute;
      width: 180px;
      height: 180px;
      background: radial-gradient(circle, rgba(212,175,55,0.2), transparent 70%);
      top: -80px;
      right: -80px;
    }

    .about-box:hover {
      transform: translateY(-8px);
      border-color: rgba(212,175,55,0.4);
      box-shadow: 0 20px 40px rgba(0,0,0,0.5);
    }

    .about-box h3 {
      color: var(--gold);
      margin-bottom: 18px;
      font-size: 1.4rem;
    }

    .about-box p {
      color: #c5c5c5;
      line-height: 1.9;
    }

    /* PROJECTS */
    .projects {
      padding: 120px 8%;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 35px;
    }

    .project-card {
      background: var(--card);
      border-radius: 26px;
      overflow: hidden;
      border: 1px solid var(--border);
      transition: 0.5s ease;
      position: relative;
      opacity: 0;
      transform: translateY(40px);
    }

    .project-card.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .project-card:hover {
      transform: translateY(-12px) scale(1.01);
      box-shadow: 0 20px 45px rgba(0,0,0,0.6);
      border-color: rgba(212,175,55,0.5);
    }

    .project-image {
      height: 260px;
      overflow: hidden;
      position: relative;
    }

    .project-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: 0.6s ease;
    }

    .project-card:hover img {
      transform: scale(1.08);
    }

    .project-content {
      padding: 30px;
    }

    .project-content h3 {
      color: var(--gold);
      font-size: 1.6rem;
      margin-bottom: 12px;
      font-family: 'Cinzel', serif;
    }

    .project-content p {
      color: #bdbdbd;
      line-height: 1.8;
      margin-bottom: 20px;
    }

    .tech-stack {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .tech-stack span {
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.08);
      padding: 8px 14px;
      border-radius: 30px;
      font-size: 0.75rem;
      color: var(--gold-light);
    }

    /* SKILLS */
    .skills {
      padding: 120px 8%;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 25px;
    }

    .skill-box {
      background: linear-gradient(145deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 35px 25px;
      text-align: center;
      transition: 0.4s ease;
    }

    .skill-box:hover {
      transform: translateY(-8px);
      border-color: rgba(212,175,55,0.5);
    }

    .skill-box h3 {
      color: var(--gold);
      margin-bottom: 12px;
    }

    .skill-box p {
      color: #b5b5b5;
      font-size: 0.9rem;
      line-height: 1.7;
    }

    /* CONTACT */
    .contact {
      padding: 120px 8%;
    }

    .contact-card {
      max-width: 850px;
      margin: auto;
      background: linear-gradient(145deg, rgba(255,255,255,0.04), rgba(255,255,255,0.02));
      border: 1px solid var(--border);
      border-radius: 28px;
      padding: 60px;
      text-align: center;
      position: relative;
      overflow: hidden;
    }

    .contact-card::before {
      content: '';
      position: absolute;
      width: 300px;
      height: 300px;
      background: radial-gradient(circle, rgba(212,175,55,0.18), transparent 70%);
      top: -150px;
      left: -100px;
    }

    .contact-card h2 {
      font-family: 'Cinzel', serif;
      color: var(--gold);
      font-size: 3rem;
      margin-bottom: 20px;
    }

    .contact-card p {
      color: #c8c8c8;
      line-height: 1.9;
      margin-bottom: 35px;
    }

    .contact-links {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 18px;
    }

    .contact-links a {
      text-decoration: none;
      padding: 14px 24px;
      border-radius: 40px;
      color: white;
      border: 1px solid rgba(255,255,255,0.1);
      transition: 0.3s ease;
      background: rgba(255,255,255,0.03);
    }

    .contact-links a:hover {
      color: black;
      background: var(--gold);
      border-color: var(--gold);
    }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 40px 20px;
      border-top: 1px solid rgba(255,255,255,0.08);
      color: #8a8a8a;
      letter-spacing: 2px;
      font-size: 0.85rem;
    }

    /* RESPONSIVE */
    @media(max-width: 768px) {
      nav {
        padding: 18px 5%;
      }

      nav ul {
        gap: 18px;
      }

      .hero {
        padding: 0 5%;
      }

      .hero h2 {
        font-size: 1rem;
        letter-spacing: 2px;
      }

      .about,
      .projects,
      .skills,
      .contact {
        padding: 90px 5%;
      }

      .section-title h2 {
        font-size: 2.2rem;
      }

      .contact-card {
        padding: 40px 25px;
      }

      .contact-card h2 {
        font-size: 2.2rem;
      }
    }
  </style>
</head>
<body>

  <!-- NAVIGATION -->
  <nav>
    <div class="logo">IMRAN</div>

    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-content">

      <div class="tag">UNREAL ENGINE GAME DEVELOPER</div>

      <h1>IMRAN</h1>

      <h2>CINEMATIC STORYTELLER • GAME DESIGNER • UE5 CREATOR</h2>

      <p>
        I create immersive gameplay experiences using Unreal Engine 5.
        From dark cinematic environments to intense action mechanics,
        I focus on building games that feel emotional, powerful, and unforgettable.
      </p>

      <div class="hero-buttons">
        <a href="#projects" class="btn btn-primary">VIEW PROJECTS</a>
        <a href="#contact" class="btn btn-outline">CONTACT ME</a>
      </div>
    </div>

    <div class="scroll-text">SCROLL TO EXPLORE</div>
  </section>

  <!-- ABOUT -->
  <section class="about" id="about">

    <div class="section-title">
      <h2>ABOUT ME</h2>
      <p>
        Passionate about creating cinematic experiences, gameplay systems,
        and emotional storytelling through Unreal Engine 5.
      </p>
    </div>

    <div class="about-container">

      <div class="about-box">
        <h3>Game Developer</h3>
        <p>
          Specialized in Unreal Engine 5 development with focus on action gameplay,
          cinematic storytelling, blueprint systems, AI mechanics, and immersive environments.
        </p>
      </div>

      <div class="about-box">
        <h3>Creative Storytelling</h3>
        <p>
          I believe every game should tell a story. My goal is to create worlds,
          emotions, and experiences players remember long after they finish the game.
        </p>
      </div>

      <div class="about-box">
        <h3>Leadership & Vision</h3>
        <p>
          Founder of Miracle Football Academy and a creator who combines leadership,
          creativity, and discipline into both sports and game development.
        </p>
      </div>

    </div>
  </section>

  <!-- PROJECTS -->
  <section class="projects" id="projects">

    <div class="section-title">
      <h2>FEATURED PROJECTS</h2>
      <p>
        A showcase of cinematic worlds, gameplay systems, and immersive experiences.
      </p>
    </div>

    <div class="projects-grid">

      <div class="project-card">
        <div class="project-image">
          <img src="ChatGPT Image May 30, 2026, 10_22_31 PM.png">
        </div>

        <div class="project-content">
          <div class="tag">ACTION / PUZZLE</div>
          <h3>MAZE RUNNER</h3>

          <p>
            A high-intensity survival puzzle game focused on dynamic environments,
            procedural pathways, and immersive tension mechanics.
          </p>

          <div class="tech-stack">
            <span>UE5</span>
            <span>Blueprints</span>
            <span>AI Logic</span>
            <span>Puzzle Design</span>
          </div>
        </div>
      </div>

      <div class="project-card">
        <div class="project-image">
          <img src="ChatGPT Image May 30, 2026, 09_44_34 PM.png">
        </div>

        <div class="project-content">
          <div class="tag">THIRD PERSON SHOOTER</div>
          <h3>RED DOCK</h3>

          <p>
            A cinematic rescue mission set inside a dangerous enemy-controlled port.
            The player fights through intense combat zones to rescue a hostage and escape.
          </p>

          <div class="tech-stack">
            <span>Combat System</span>
            <span>Animation Blend</span>
            <span>Cinematics</span>
            <span>Level Design</span>
          </div>
        </div>
      </div>

      <div class="project-card">
        <div class="project-image">
          <<img src="ChatGPT Image May 30, 2026, 10_28_56 PM.png">>
        </div>

        <div class="project-content">
          <div class="tag">DARK CINEMATIC WORLD</div>
          <h3>THE LAVA LAND</h3>

          <p>
            A narrative-driven volcanic world where environmental storytelling,
            lighting, and destruction create the feeling of a fallen civilization.
          </p>

          <div class="tech-stack">
            <span>Environment Art</span>
            <span>Lighting</span>
            <span>World Building</span>
            <span>Storytelling</span>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- SKILLS -->
  <section class="skills" id="skills">

    <div class="section-title">
      <h2>SKILLS</h2>
      <p>
        Technical and creative abilities used to build immersive gameplay experiences.
      </p>
    </div>

    <div class="skills-grid">

      <div class="skill-box">
        <h3>Unreal Engine 5</h3>
        <p>Gameplay systems, environment design, blueprints, and optimization.</p>
      </div>

      <div class="skill-box">
        <h3>Blueprint Scripting</h3>
        <p>Creating responsive mechanics, interactions, and gameplay logic.</p>
      </div>

      <div class="skill-box">
        <h3>Cinematic Design</h3>
        <p>Story-focused scenes using camera work, lighting, and atmosphere.</p>
      </div>

      <div class="skill-box">
        <h3>Level Design</h3>
        <p>Designing engaging worlds with flow, tension, and exploration.</p>
      </div>

      <div class="skill-box">
        <h3>Game Storytelling</h3>
        <p>Building emotional narratives and immersive player experiences.</p>
      </div>

      <div class="skill-box">
        <h3>Leadership</h3>
        <p>Managing teams, academy operations, and creative project execution.</p>
      </div>

    </div>
  </section>

  <!-- CONTACT -->
  <section class="contact" id="contact">

    <div class="contact-card">
      <h2>LET'S BUILD WORLDS</h2>

      <p>
        Interested in collaborating, hiring, or discussing game development projects?
        Let's create something unforgettable.
      </p>

      <div class="contact-links">
        <a href="mailto:imran.brin@gmail.com">Email</a>
        <a href="https://www.linkedin.com" target="_blank">LinkedIn</a>
        <a href="https://github.com" target="_blank">GitHub</a>
      </div>
    </div>

  </section>

  <!-- FOOTER -->
  <footer>
    DREAMING IN 60 FPS • IMRAN 2026
  </footer>

  <script>

    // Reveal Animation
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, {
      threshold: 0.2
    });

    document.querySelectorAll('.project-card').forEach((card) => {
      observer.observe(card);
    });


    // Smooth Navbar Background on Scroll
    window.addEventListener('scroll', () => {
      const nav = document.querySelector('nav');

      if (window.scrollY > 80) {
        nav.style.background = 'rgba(0,0,0,0.75)';
      } else {
        nav.style.background = 'rgba(0,0,0,0.35)';
      }
    });

  </script>

</body>
</html>
