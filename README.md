
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#090d18">
  <meta name="description" content="Vince Callado - Aspiring Web Developer and IT Student.">
  <title>Vince Callado | Digital Portfolio</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;600;700;800&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg: #090d18;
      --panel: #101827;
      --cyan: #00f5e9;
      --pink: #ed36dc;
      --white: #f4f7ff;
      --muted: #9ba9bd;
      --border: rgba(0,245,233,.22);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      background: var(--bg);
      color: var(--white);
      font-family: 'Inter', sans-serif;
      line-height: 1.7;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: -1;
      background:
        linear-gradient(rgba(0,245,233,.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(0,245,233,.025) 1px, transparent 1px);
      background-size: 35px 35px;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1100px, 90%);
      margin: auto;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 10;
      background: rgba(9,13,24,.94);
      border-bottom: 1px solid var(--border);
      backdrop-filter: blur(12px);
    }

    nav {
      min-height: 72px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 15px;
    }

    .logo {
      font-family: 'Orbitron', sans-serif;
      font-size: 1.15rem;
      font-weight: 800;
      color: var(--cyan);
      letter-spacing: 2px;
    }

    .nav-links {
      display: flex;
      gap: 24px;
      list-style: none;
    }

    .nav-links a {
      color: var(--muted);
      font-size: .85rem;
      transition: color .2s;
    }

    .nav-links a:hover {
      color: var(--cyan);
    }

    .menu-btn {
      display: none;
      background: transparent;
      border: 1px solid var(--cyan);
      color: var(--cyan);
      padding: 7px 12px;
      border-radius: 5px;
      font-size: 1.1rem;
      cursor: pointer;
    }

    section {
      padding: 90px 0;
      scroll-margin-top: 70px;
    }

    .hero {
      min-height: 88vh;
      display: flex;
      align-items: center;
      position: relative;
    }

    .hero-content {
      max-width: 760px;
    }

    .eyebrow {
      color: var(--cyan);
      font-family: 'Orbitron', sans-serif;
      font-size: .75rem;
      letter-spacing: 3px;
      margin-bottom: 20px;
    }

    h1 {
      font-family: 'Orbitron', sans-serif;
      font-size: clamp(2.6rem, 9vw, 5.5rem);
      line-height: 1.12;
      letter-spacing: -2px;
      margin-bottom: 18px;
    }

    .neon {
      color: var(--cyan);
      text-shadow: 0 0 18px rgba(0,245,233,.35);
    }

    .hero h2 {
      color: var(--pink);
      font-family: 'Orbitron', sans-serif;
      font-size: clamp(.9rem, 3vw, 1.3rem);
      letter-spacing: 2px;
      margin-bottom: 20px;
    }

    .description {
      color: var(--muted);
      max-width: 570px;
      margin-bottom: 30px;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 13px;
    }

    .btn {
      display: inline-block;
      padding: 12px 23px;
      border: 1px solid var(--cyan);
      border-radius: 5px;
      color: var(--cyan);
      font-weight: 600;
      font-size: .9rem;
      transition: .2s;
    }

    .btn.primary {
      background: var(--cyan);
      color: #071116;
    }

    .btn:hover {
      box-shadow: 0 0 18px rgba(0,245,233,.3);
      transform: translateY(-2px);
    }

    .section-title {
      font-family: 'Orbitron', sans-serif;
      font-size: clamp(1.5rem, 5vw, 2.3rem);
      margin-bottom: 12px;
    }

    .section-title span {
      color: var(--cyan);
    }

    .section-subtitle {
      color: var(--muted);
      margin-bottom: 35px;
      font-size: .95rem;
    }

    .panel {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 27px;
      transition: border-color .2s;
    }

    .panel:hover {
      border-color: var(--cyan);
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1.3fr 1fr;
      gap: 22px;
    }

    .about-text {
      color: var(--muted);
    }

    .status {
      color: var(--cyan);
      font-family: 'Orbitron', sans-serif;
      font-size: .75rem;
      margin-bottom: 15px;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 15px;
    }

    .skill {
      text-align: center;
      padding: 22px 10px;
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 8px;
    }

    .skill strong {
      display: block;
      color: var(--cyan);
      font-family: 'Orbitron', sans-serif;
      font-size: .9rem;
      margin-bottom: 5px;
    }

    .skill small {
      color: var(--muted);
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
    }

    .project-number {
      color: var(--pink);
      font-family: 'Orbitron', sans-serif;
      font-size: .8rem;
    }

    .project h3 {
      margin: 12px 0;
      font-family: 'Orbitron', sans-serif;
      font-size: 1rem;
    }

    .project p {
      color: var(--muted);
      font-size: .9rem;
      margin-bottom: 18px;
    }

    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .tag {
      color: var(--cyan);
      border: 1px solid var(--border);
      border-radius: 4px;
      padding: 4px 9px;
      font-size: .7rem;
    }

    .contact-box {
      text-align: center;
      max-width: 700px;
      margin: auto;
    }

    .contact-box p {
      color: var(--muted);
      margin: 15px 0 25px;
    }

    footer {
      padding: 25px 0;
      border-top: 1px solid var(--border);
      text-align: center;
      color: var(--muted);
      font-size: .8rem;
    }

    footer span {
      color: var(--cyan);
    }

    @media (max-width: 650px) {
      nav {
        min-height: 65px;
      }

      .menu-btn {
        display: block;
      }

      .nav-links {
        display: none;
        position: absolute;
        top: 65px;
        left: 0;
        width: 100%;
        padding: 20px 5%;
        background: #0c1422;
        border-bottom: 1px solid var(--border);
        flex-direction: column;
        gap: 17px;
      }

      .nav-links.active {
        display: flex;
      }

      section {
        padding: 65px 0;
      }

      .hero {
        min-height: 78vh;
      }

      .about-grid,
      .projects-grid {
        grid-template-columns: 1fr;
      }

      .skills-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .panel {
        padding: 21px;
      }

      h1 {
        letter-spacing: -1px;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        scroll-behavior: auto !important;
        transition: none !important;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="container">
      <nav>
        <a href="#home" class="logo">VC.DEV</a>

        <button class="menu-btn" id="menuBtn"
          aria-label="Toggle navigation"
          aria-expanded="false">☰</button>

        <ul class="nav-links" id="navLinks">
          <li><a href="#home">Home</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#skills">Skills</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" id="home">
      <div class="container hero-content">
        <p class="eyebrow">WELCOME TO MY DIGITAL SPACE</p>

        <h1>
          VINCE<br>
          <span class="neon">CALLADO.</span>
        </h1>

        <h2>ASPIRING WEB DEVELOPER</h2>

        <p class="description">
          Hello! I'm Vince Callado, an IT student passionate
          about technology, programming, and creating
          digital experiences. I'm constantly learning,
          exploring, and building something new.
        </p>

        <div class="buttons">
          <a href="#projects" class="btn primary">Explore Projects</a>
          <a href="#contact" class="btn">Contact Me</a>
        </div>
      </div>
    </section>

    <section id="about">
      <div class="container">
        <h2 class="section-title">ABOUT <span>ME</span></h2>
        <p class="section-subtitle">Get to know the person behind the code.</p>

        <div class="about-grid">
          <div class="panel">
            <p class="status">// PROFILE_INFORMATION</p>
            <p class="about-text">
              I'm Vince Callado, a Bachelor of Science in
              Information Technology student. I enjoy learning
              about computers, software development, and
              the creative side of technology.

              <br><br>

              My goal is to improve my programming skills
              and develop useful, creative, and user-friendly
              digital projects.
            </p>
          </div>

          <div class="panel">
            <p class="status">// CURRENT_STATUS</p>
            <h3>IT STUDENT</h3>
            <p class="about-text">BSIT 2-C</p>
            <br>
            <h3 class="neon">LEARNING MODE: ON</h3>
            <p class="about-text">Always improving. Always creating.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="skills">
      <div class="container">
        <h2 class="section-title">MY <span>SKILLS</span></h2>
        <p class="section-subtitle">Technologies and tools I'm exploring.</p>

        <div class="skills-grid">
          <div class="skill">
            <strong>HTML</strong>
            <small>Web Structure</small>
          </div>

          <div class="skill">
            <strong>CSS</strong>
            <small>Web Design</small>
          </div>

          <div class="skill">
            <strong>C++</strong>
            <small>Programming</small>
          </div>

          <div class="skill">
            <strong>GITHUB</strong>
            <small>Version Control</small>
          </div>

          <div class="skill">
            <strong>NETWORKING</strong>
            <small>IT Fundamentals</small>
          </div>

          <div class="skill">
            <strong>PROBLEM SOLVING</strong>
            <small>Logical Thinking</small>
          </div>
        </div>
      </div>
    </section>

    <section id="projects">
      <div class="container">
        <h2 class="section-title">MY <span>PROJECTS</span></h2>
        <p class="section-subtitle">Some of my work and learning experiences.</p>

        <div class="projects-grid">

          <div class="panel project">
            <span class="project-number">PROJECT_001</span>
            <h3>PERSONAL PORTFOLIO</h3>
            <p>
              My personal website showcasing my background,
              skills, and journey as an IT student.
            </p>
            <div class="tags">
              <span class="tag">HTML</span>
              <span class="tag">CSS</span>
              <span class="tag">GITHUB PAGES</span>
            </div>
          </div>

          <div class="panel project">
            <span class="project-number">PROJECT_002</span>
            <h3>CODING PRACTICE</h3>
            <p>
              Programming exercises and activities
              developed while learning C++ and
              fundamental programming concepts.
            </p>
            <div class="tags">
              <span class="tag">C++</span>
              <span class="tag">LOGIC</span>
            </div>
          </div>

        </div>
      </div>
    </section>

    <section id="contact">
      <div class="container contact-box">
        <p class="eyebrow">LET'S CONNECT</p>
        <h2 class="section-title">CONTACT <span>ME</span></h2>
        <p>
          Have a project, idea, or opportunity?
          Feel free to reach out. Let's create something great!
        </p>

        <div class="buttons" style="justify-content:center">
          <!-- Replace with your real email -->
          <a href="mailto:YOUR_EMAIL@example.com" class="btn primary">
            Send Me an Email
          </a>

          <a href="https://github.com/vcallado"
             target="_blank" rel="noopener noreferrer" class="btn">
            My GitHub
          </a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <p>© 2026 <span>VINCE CALLADO</span> | Built with creativity and code.</p>
      <p>DESIGN · DEVELOP · INNOVATE</p>
    </div>
  </footer>

  <script>
    const menuBtn = document.getElementById("menuBtn");
    const navLinks = document.getElementById("navLinks");

    menuBtn.addEventListener("click", () => {
      const isOpen = navLinks.classList.toggle("active");
      menuBtn.setAttribute("aria-expanded", isOpen);
      menuBtn.textContent = isOpen ? "✕" : "☰";
    });

    document.querySelectorAll(".nav-links a").forEach(link => {
      link.addEventListener("click", () => {
        navLinks.classList.remove("active");
        menuBtn.setAttribute("aria-expanded", "false");
        menuBtn.textContent = "☰";
      });
    });
  </script>

</body>
</html>
