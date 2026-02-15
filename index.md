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
      <a href="#labs" class="nav-link">Labs</a>
      <a href="#writeups" class="nav-link">Write-ups</a>
      <a href="#resume" class="nav-link">Resume</a>
    </nav>

    <a href="#contact"
       class="ml-6 rounded-lg border border-white/20 px-4 py-2 text-sm text-slate-200 hover:border-white/40">
      Let’s Talk
    </a>
  </div>
</header>

<main class="pt-24">

<!-- HERO SECTION -->
<section id="home" class="min-h-screen flex items-center">
  <div class="mx-auto grid w-[min(1120px,92%)] items-center gap-10 md:grid-cols-2">

    <div>
      <p class="mb-2 text-xs tracking-[0.18em] uppercase text-slate-300">
        I’m <strong>Hsu Shun Lae</strong>
      </p>

      <h1 class="mb-4 text-4xl font-extrabold leading-tight sm:text-5xl">
        Uncover vulnerabilities through
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-600">
          cyber solutions
        </span>
        <br />
        for your
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-300 to-blue-700">
          security
        </span>
      </h1>

      <p class="max-w-prose text-mute">
        My goal is to think like an attacker, expose weaknesses, and demonstrate real-world risks.
        I provide clear incident notes, detection guidance, and defensive recommendations
        to strengthen security posture.
      </p>

      <div class="mt-6 flex gap-4">
        <a href="#projects"
           class="rounded-xl bg-gradient-to-br from-neonCyan to-neonBlue px-6 py-3 font-semibold text-slate-900 glow transition hover:-translate-y-1">
          Get Started
        </a>
        <a href="#about"
           class="rounded-xl border border-white/25 px-6 py-3 font-semibold text-slate-200 hover:border-white/40">
          Learn More
        </a>
      </div>
    </div>

    <div class="relative flex justify-center">
      <div class="absolute -inset-6 rounded-full blur-2xl"
           style="background: radial-gradient(60% 60% at 50% 40%, rgba(0,245,255,.18), rgba(0,168,255,.08) 60%, transparent 61%);">
      </div>

      <div class="relative aspect-square w-[80%] max-w-[420px] overflow-hidden rounded-full ring-2 ring-cyan-400">
        <img src="{{ '/assets/img/HsuShun.png' | relative_url }}" alt="Portrait">
      </div>
    </div>

  </div>
</section>

<!-- ABOUT -->
<section id="about" class="min-h-screen flex items-center">
  <div class="mx-auto w-[min(1120px,92%)]">
    <h2 class="text-3xl font-bold mb-6">About Me</h2>
    <p class="text-mute max-w-3xl">
      Add your detailed background, certifications, and technical focus here.
    </p>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects" class="min-h-screen flex items-center">
  <div class="mx-auto w-[min(1120px,92%)]">
    <h2 class="text-3xl font-bold mb-6">Projects</h2>
  </div>
</section>

<!-- LABS -->
<section id="labs" class="min-h-screen flex items-center">
  <div class="mx-auto w-[min(1120px,92%)]">
    <h2 class="text-3xl font-bold mb-6">Labs</h2>
  </div>
</section>

<!-- WRITEUPS -->
<section id="writeups" class="min-h-screen flex items-center">
  <div class="mx-auto w-[min(1120px,92%)]">
    <h2 class="text-3xl font-bold mb-6">Write-ups</h2>
  </div>
</section>

<!-- RESUME -->
<section id="resume" class="min-h-screen flex items-center">
  <div class="mx-auto w-[min(1120px,92%)]">
    <h2 class="text-3xl font-bold mb-6">Resume</h2>
    <a href="{{ '/assets/img/HsuShunLae_Resume.pdf' | relative_url }}"
       class="text-cyan-400 underline">
      Download Resume
    </a>
  </div>
</section>

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

  window.addEventListener("scroll", () => {
    let current = "";

    sections.forEach(section => {
      const sectionTop = section.offsetTop - 150;
      if (window.pageYOffset >= sectionTop) {
        current = section.getAttribute("id");
      }
    });

    navLinks.forEach(link => {
      link.classList.remove("active");
      if (link.getAttribute("href") === "#" + current) {
        link.classList.add("active");
      }
    });
  });
</script>

</body>
</html>
