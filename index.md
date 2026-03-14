---
layout: null
title: Home
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>{{ site.title }}</title>

  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            base: '#05070d',
            panel: '#0b1220',
            text: '#e6f2ff',
            mute: '#95a7c0',
            neonCyan: '#00f5ff',
            neonBlue: '#00a8ff',
          },
        },
      },
    };
  </script>

  <style>
    html {
      scroll-behavior: smooth;
    }

    .hex-bg::before {
      content: "";
      position: fixed;
      inset: 0;
      z-index: -1;
      opacity: 0.08;
      pointer-events: none;
      background-image: url("data:image/svg+xml,%3Csvg width='60' height='52' viewBox='0 0 60 52' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M30 2l25 14v20L30 50 5 36V16L30 2z M5 36l25 14 25-14' fill='none' stroke='%2300c8ff' stroke-width='1'/%3E%3C/svg%3E");
      background-size: 200px 170px;
    }

    .glow {
      box-shadow: 0 0 36px rgba(0, 245, 255, 0.22),
                  0 0 12px rgba(0, 168, 255, 0.22);
    }

    .nav-link.active {
      color: white;
      border-bottom: 2px solid #00f5ff;
    }
    .skill-pill {
      display: flex;
      align-items: center;
      gap: 6px;
      padding: 6px 12px;
      border-radius: 9999px;
      border: 1px solid rgba(255,255,255,0.15);
      background: rgba(255,255,255,0.03);
      font-size: 12px;
      color: #cbd5e1;
      transition: all 0.25s ease;
    }
    
    .skill-pill img {
      height: 14px;
      width: auto;
      object-fit: contain;
      filter: brightness(1.2);
    }
    
    .skill-pill:hover {
      border-color: rgba(0,245,255,0.6);
      box-shadow: 0 0 12px rgba(0,245,255,0.3);
      transform: translateY(-2px);
    }

  </style>
</head>

<body class="hex-bg bg-base text-text selection:bg-cyan-300/30">

<!-- NAVBAR -->
<header class="fixed top-0 z-50 w-full border-b border-white/10 bg-base/80 backdrop-blur">
  <div class="mx-auto flex w-[min(1120px,92%)] items-center py-4">
    
    <div class="font-bold text-white">HSU SHUN LAE</div>

    <nav class="ml-auto flex gap-6 text-slate-300">
      <a href="#home" class="nav-link">Home</a>
      <a href="#about" class="nav-link">About</a>
      <a href="#projects" class="nav-link">Projects</a>
      <a href="#writeups" class="nav-link">Write-ups</a>
      <a href="#resume" class="nav-link">Resume</a>
    </nav>

    <a href="https://www.linkedin.com/messaging/compose/?recipient=hsu-shun-lae-56a90b211"
       target="_blank"
       rel="noopener noreferrer"
       class="ml-6 inline-flex items-center gap-2 rounded-lg border border-white/20 px-4 py-2 text-sm text-slate-200 hover:border-cyan-400 hover:text-white transition">
    
      <!-- LinkedIn Icon -->
      <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24">
        <path d="M20.447 20.452H16.89v-5.569c0-1.327-.024-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.94v5.666H9.345V9h3.414v1.561h.048c.476-.9 1.637-1.852 3.37-1.852 3.602 0 4.268 2.372 4.268 5.455v6.288zM5.337 7.433a1.98 1.98 0 110-3.961 1.98 1.98 0 010 3.961zM6.814 20.452H3.86V9h2.954v11.452z"/>
      </svg>
    
      Let’s Talk
    </a>


  </div>
</header>

<main class="pt-24">

<!-- HERO SECTION -->
<section id="home" class="relative min-h-screen flex items-center overflow-hidden">

  <!-- Background glow layers -->
  <div class="absolute inset-0 -z-10">
    <div class="absolute w-[900px] h-[600px] bg-cyan-500/10 blur-[120px] top-[-200px] right-[-200px] rounded-full"></div>
    <div class="absolute w-[700px] h-[500px] bg-blue-500/10 blur-[100px] bottom-[-150px] left-[-150px] rounded-full"></div>
  </div>

  <div class="mx-auto w-full max-w-[1300px] px-8 grid md:grid-cols-2 gap-12 items-center">

    <!-- LEFT SIDE -->
    <div class="space-y-6">

      <p class="text-xs tracking-[0.18em] uppercase text-slate-300">
        I’m <strong>Hsu Shun Lae</strong>
      </p>

      <h1 class="text-5xl font-extrabold leading-tight tracking-tight">
        Uncover vulnerabilities through
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-600">
          cyber solutions
        </span>
        for your
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-300 to-blue-700">
          security
        </span>
      </h1>

      <p class="text-mute max-w-xl text-lg">
        My goal is to think like an attacker, expose weaknesses,
        and demonstrate real-world risks through practical
        defensive strategies.
      </p>

      <div class="flex gap-4 pt-4">
        <a href="#projects"
           class="rounded-xl bg-gradient-to-br from-neonCyan to-neonBlue px-6 py-3 font-semibold text-slate-900 shadow-[0_0_40px_rgba(0,245,255,0.4)] transition hover:-translate-y-1">
          Get Started
        </a>
        <a href="#about"
           class="rounded-xl border border-white/25 px-6 py-3 font-semibold text-slate-200 hover:border-white/40">
          Learn More
        </a>
      </div>
      <div class="mt-3 flex flex-wrap gap-3">

        <div class="skill-pill">
          <img src="https://wazuh.com/wp-content/themes/wazuh-v3/assets/images/favicon.ico?v=1767701209057" alt="">
          <span>Wazuh</span>
        </div>
      
        <div class="skill-pill">
          <img src="https://suricata.io/wp-content/uploads/2023/09/Logo-Suricata-vert-whitetype-R.png" alt="">
          <span>Suricata</span>
        </div>
      
        <div class="skill-pill">
          <img src="https://nmap.org/images/sitelogo.png" alt="">
          <span>Nmap</span>
        </div>
      
        <div class="skill-pill">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/BurpSuite_Comunity_Edition.svg/330px-BurpSuite_Comunity_Edition.svg.png" alt="">
          <span>BurpSuite</span>
        </div>
      
        <div class="skill-pill">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" alt="">
          <span>Bash</span>
        </div>
      
        <div class="skill-pill">
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="">
          <span>Python</span>
        </div>
      
        <div class="skill-pill">
          <img src="https://owasp.org/assets/images/logo.png" alt="">
          <span>OWASP</span>
        </div>
      
      </div>

    </div>

    <!-- RIGHT SIDE -->
    <div class="relative flex justify-center">

      <div class="absolute -inset-12 rounded-full blur-3xl opacity-60"
           style="background: radial-gradient(circle at center, rgba(0,245,255,0.3), rgba(0,168,255,0.25), transparent 70%);">
      </div>

      <div class="relative p-[4px] rounded-full bg-gradient-to-br from-cyan-400 via-blue-500 to-cyan-300 shadow-[0_0_60px_rgba(0,245,255,0.4)]">
        <div class="p-[6px] rounded-full bg-base">
          <div class="aspect-square w-[380px] overflow-hidden rounded-full">
            <img src="{{ '/assets/img/HsuShun.png' | relative_url }}"
                 alt="Portrait"
                 class="w-full h-full object-cover">
          </div>
        </div>
      </div>

    </div>

  </div>
  

</section>



<!-- ABOUT -->
{% include about-section.html %} 

<!-- PROJECTS -->
{% include project-section.html %} 

<!-- WRITEUPS -->
{% include writeup-section.html %} 

</main>

<footer class="border-t border-white/10 py-6">
  <div class="mx-auto w-[min(1120px,92%)] text-sm text-slate-400">
    © {{ 'now' | date: '%Y' }} Hsu Shun Lae - Cybersecurity
  </div>
</footer>

<!-- ACTIVE NAV SCRIPT -->
<script>
  const sections = document.querySelectorAll("section");
  const navLinks = document.querySelectorAll(".nav-link");

  function setActiveLink() {
    let current = "";

    sections.forEach(section => {
      const sectionTop = section.offsetTop - 120;
      const sectionHeight = section.offsetHeight;

      if (
        window.scrollY >= sectionTop &&
        window.scrollY < sectionTop + sectionHeight
      ) {
        current = section.getAttribute("id");
      }
    });

    navLinks.forEach(link => {
      link.classList.remove("active");
      if (link.getAttribute("href") === "#" + current) {
        link.classList.add("active");
      }
    });
  }

  window.addEventListener("scroll", setActiveLink);
  window.addEventListener("load", setActiveLink);
</script>


</body>
</html>
