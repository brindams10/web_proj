
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Brinda M S | Portfolio</title>

  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: Arial, sans-serif; }
    html { scroll-behavior: smooth; }
    body { background: #0f172a; color: #e5e7eb; overflow-x: hidden; }

    /* ===== PAGE TRANSITION OVERLAY ===== */
    .page-transition {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: #020617;
      z-index: 9999;
      transform: translateX(-100%);
      transition: 0.6s ease;
    }

    .page-transition.active {
      transform: translateX(0);
    }

    header { 
      background: linear-gradient(135deg, #2563eb, #1e40af); 
      padding: 80px 20px; 
      text-align: center;
      animation: fadeDown 1.2s ease;
    }

    @keyframes fadeDown {
      from { opacity: 0; transform: translateY(-40px); }
      to { opacity: 1; transform: translateY(0); }
    }

    header h1 {
      font-size: 40px;
      margin-bottom: 10px;
      animation: zoomIn 1.2s ease;
    }

    @keyframes zoomIn {
      from { transform: scale(0.8); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    header p { font-size: 18px; opacity: 0.9; }

    nav { 
      background: #020617; 
      padding: 12px 0; 
      position: sticky; 
      top: 0; 
      z-index: 100;
    }

    nav ul { list-style: none; display: flex; justify-content: center; gap: 25px; }

    nav a { 
      text-decoration: none; 
      color: #e5e7eb; 
      font-weight: 600; 
      padding: 8px 14px;
      border-radius: 8px;
      transition: 0.3s;
    }

    nav a:hover { 
      color: #60a5fa; 
      background: rgba(255,255,255,0.1);
      box-shadow: 0 0 12px #2563eb;
      transform: translateY(-2px);
    }

    /* ===== SECTION SCROLL ANIMATION ===== */
    section { 
      max-width: 1000px; 
      margin: 60px auto; 
      padding: 0 20px; 
      opacity: 0;
      transform: translateY(50px);
      transition: all 0.9s ease;
    }

    section.show { opacity: 1; transform: translateY(0); }

    section h2 { font-size: 28px; margin-bottom: 20px; color: #60a5fa; }
    .about p { line-height: 1.7; }

    /* ===== SKILLS WITH PROJECT-STYLE ANIMATION ===== */
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 15px; }

    .skill { 
      background: #020617; 
      padding: 12px; 
      text-align: center; 
      border-radius: 10px; 
      transition: 0.4s;
    }

    .skill:hover {
      transform: translateY(-8px) scale(1.05);
      box-shadow: 0 0 18px #2563eb;
    }

    /* ===== PROJECTS ===== */
    .projects-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }

    .project-card { 
      background: #020617; 
      padding: 20px; 
      border-radius: 14px; 
      box-shadow: 0 10px 20px rgba(0,0,0,0.25); 
      transition: 0.4s;
    }

    .project-card:hover {
      transform: translateY(-10px) scale(1.02);
      box-shadow: 0 0 25px #2563eb;
    }

    .project-card h3 { margin-bottom: 10px; color: #93c5fd; }

    /* ===== CERTIFICATION HOVER TOO ===== */
    #certifications p {
      background: #020617;
      padding: 14px;
      border-radius: 10px;
      transition: 0.4s;
      display: inline-block;
    }

    #certifications p:hover {
      transform: translateY(-6px);
      box-shadow: 0 0 18px #2563eb;
    }

    .contact p { margin-bottom: 10px; }
    .contact a { color: #60a5fa; text-decoration: none; }

    footer { text-align: center; padding: 30px; background: #020617; margin-top: 60px; font-size: 14px; opacity: 0.8; }

    /* ===== PREMIUM BUTTON ===== */
    button { 
      padding: 10px 20px; 
      border: none; 
      background: #2563eb; 
      color: white; 
      border-radius: 8px; 
      cursor: pointer; 
      margin-top: 10px; 
      position: relative;
      overflow: hidden;
      transition: 0.25s;
    }

    button:hover { 
      background: #1d4ed8; 
      transform: translateY(-3px) scale(1.06);
      box-shadow: 0 10px 25px rgba(37, 99, 235, 0.6);
    }

    button:active { transform: scale(0.95); }

    button span {
      position: absolute;
      border-radius: 50%;
      transform: scale(0);
      animation: ripple 0.6s linear;
      background: rgba(255, 255, 255, 0.6);
    }

    @keyframes ripple {
      to { transform: scale(4); opacity: 0; }
    }
  </style>
</head>

<body>

<div class="page-transition" id="pageTransition"></div>

<header>
  <h1>Brinda M S</h1>
  <p>Computer Science Engineering Student</p>
</header>

<nav>
  <ul>
    <li><a href="#about" class="nav-link">About</a></li>
    <li><a href="#skills" class="nav-link">Skills</a></li>
    <li><a href="#projects" class="nav-link">Projects</a></li>
    <li><a href="#certifications" class="nav-link">Certifications</a></li>
    <li><a href="#contact" class="nav-link">Contact</a></li>
  </ul>
</nav>

<section id="about" class="about">
  <h2>About Me</h2>
  <p>Aspiring Computer Science Engineer with strong programming, analytical, and technical skills.</p>
</section>

<section id="skills">
  <h2>Technical Skills</h2>
  <div class="skills-grid">
    <div class="skill">C</div>
    <div class="skill">C++</div>
    <div class="skill">Java</div>
    <div class="skill">Python</div>
    <div class="skill">MySQL</div>
    <div class="skill">HTML</div>
    <div class="skill">CSS</div>
    <div class="skill">Power BI</div>
    <div class="skill">MS Excel</div>
  </div>
</section>

<section id="projects">
  <h2>Projects</h2>
  <div class="projects-grid">
    <div class="project-card">
      <h3>Hospital Insulin Level Report</h3>
      <p>Python visualization and preprocessing project.</p>
    </div>
    <div class="project-card">
      <h3>Netflix Power BI Dashboard</h3>
      <p>Interactive analysis using Power BI.</p>
    </div>
  </div>
</section>

<section id="certifications">
  <h2>Certifications</h2>
  <p>• NPTEL Elite – Competitive Programming</p>
</section>

<section id="contact" class="contact">
  <h2>Contact Me</h2>
  <p>Email: brindams10@gmail.com</p>
  <p>Phone: 6360228240</p>
  <a href="C:\Users\Brinda MS\Downloads\brinda ms.pdf" download><button>Download Resume</button></a>
</section>

<footer>
  <p>© 2025 Brinda M S</p>
</footer>

<script>
  /* SECTION REVEAL */
  const sections = document.querySelectorAll("section");
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) entry.target.classList.add("show");
    });
  }, { threshold: 0.2 });

  sections.forEach(sec => observer.observe(sec));

  /* BUTTON RIPPLE */
  document.querySelectorAll("button").forEach(btn => {
    btn.addEventListener("click", e => {
      const circle = document.createElement("span");
      const x = e.clientX - btn.getBoundingClientRect().left;
      const y = e.clientY - btn.getBoundingClientRect().top;
      circle.style.left = x + "px";
      circle.style.top = y + "px";
      btn.appendChild(circle);
      setTimeout(() => circle.remove(), 600);
    });
  });

  /* NAV CLICK PAGE SHIFT EFFECT */
  const transition = document.getElementById("pageTransition");
  document.querySelectorAll(".nav-link").forEach(link => {
    link.addEventListener("click", e => {
      e.preventDefault();
      const target = link.getAttribute("href");
      transition.classList.add("active");

      setTimeout(() => {
        document.querySelector(target).scrollIntoView({ behavior: "smooth" });
        transition.classList.remove("active");
      }, 600);
    });
  });
</script>

</body>
</html>
