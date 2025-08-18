---
layout: null
title: Home
---

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>{{ site.title }}</title>

  <!-- Tailwind via CDN (no build step) -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            base:    '#05070d',   // near-black
            panel:   '#0b1220',
            text:    '#e6f2ff',
            mute:    '#95a7c0',
            neonCyan:'#00f5ff',
            neonBlue:'#00a8ff',
          }
        }
      }
    }
  </script>

  <!-- Tiny helpers for hex background + neon text/glow -->
  <style>
    .hex-bg::before{
      content:""; position:fixed; inset:0; z-index:-1; opacity:.08; pointer-events:none;
      background-image:url("data:image/svg+xml,%3Csvg width='60' height='52' viewBox='0 0 60 52' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M30 2l25 14v20L30 50 5 36V16L30 2z M5 36l25 14 25-14' fill='none' stroke='%2300c8ff' stroke-width='1'/%3E%3C/svg%3E");
      background-size:200px 170px;
    }
    .neon { text-shadow: 0 0 14px rgba(0,245,255,.55), 0 0 28px rgba(0,168,255,.35); }
    .glow  { box-shadow: 0 0 36px rgba(0,245,255,.22), 0 0 12px rgba(0,168,255,.22); }
  </style>
</head>

<body class="hex-bg bg-base text-text selection:bg-cyan-300/30">
  <!-- Sticky nav -->
  <header class="sticky top-0 z-20 border-b border-white/10 bg-base/80 backdrop-blur">
    <div class="mx-auto flex w-[min(1120px,92%)] items-center gap-3 py-3">
      <a href="{{ '/' | relative_url }}" class="flex items-center gap-2 font-extrabold text-white">
        <span class="h-7 w-7 rounded-full bg-[radial-gradient(circle_at_30%_30%,#a9f7ff,#00f5ff_60%,#00a8ff)] shadow-[inset_0_0_20px_rgba(0,245,255,.6),0_0_12px_rgba(0,168,255,.5)]"></span>
        <span>CSume<span class="font-light opacity-80">Security</span></span>
      </a>

      <!-- Mobile toggle -->
      <button id="navBtn"
        class="ml-auto inline-flex items-center justify-center rounded-md p-2 text-slate-300 ring-1 ring-white/10 hover:text-white md:hidden"
        aria-label="Toggle menu" aria-expanded="false">☰</button>

      <!-- Menu -->
      <nav id="menu" class="ml-auto hidden flex-col gap-3 rounded-lg border border-white/10 bg-base/95 p-3 md:static md:flex md:flex-row md:gap-5 md:border-0 md:bg-transparent md:p-0">
        {% for item in site.nav %}
          <a href="{{ item.link | relative_url }}"
             class="text-slate-300 hover:text-white {% if page.url == item.link %}text-white{% endif %}">
            {{ item.name }}
          </a>
        {% endfor %}
      </nav>

      <a href="{{ '/contact' | relative_url }}" class="ml-3 hidden rounded-lg border border-white/20 px-4 py-2 text-sm text-slate-200 hover:border-white/40 md:inline-block">
        Let’s Talk
      </a>
    </div>
  </header>

  <!-- My Profile -->
  <main>
    <section class="mx-auto grid w-[min(1120px,92%)] items-center gap-10 py-10 md:grid-cols-2 lg:py-16"
             style="background:
               radial-gradient(900px 500px at 75% 30%, rgba(0,245,255,.10), transparent 60%),
               radial-gradient(800px 450px at 20% 80%, rgba(0,168,255,.07), transparent 60%);">
      <!-- Copy -->
      <div>
        <p class="mb-2 text-xs tracking-[0.18em] text-slate-300 uppercase">I’m <strong>Hsu Shun Lae</strong></p>

        <h1 class="mb-4 text-4xl font-extrabold leading-tight tracking-tight sm:text-5xl">
          Uncover vulnerabilities through
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-neonCyan to-neonBlue neon">
            cyber solutions
          </span><br/>
          for your <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-200 to-neonBlue neon">security</span>
        </h1>

        <p class="max-w-prose text-mute">
          My goal is to think like an attacker, expose weaknesses, and demonstrate real-world risks. Alongside offensive testing, I provide blue-team value by delivering clear incident notes, detection guidance, and defensive recommendations to strengthen security posture.
        </p>

        <div class="mt-5 flex flex-wrap gap-3">
          <a href="{{ '/projects' | relative_url }}"
             class="rounded-xl bg-gradient-to-br from-neonCyan to-neonBlue px-5 py-3 font-semibold text-slate-900 glow transition hover:-translate-y-0.5">
            Get Started
          </a>
          <a href="{{ '/about' | relative_url }}"
             class="rounded-xl border border-white/25 px-5 py-3 font-semibold text-slate-200 transition hover:border-white/40">
            Learn More
          </a>
        </div>

        <div class="mt-4 flex flex-wrap gap-2">
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Wazuh</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Suricata</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Azure</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Python</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">OWASP</span>
        </div>
      </div>

      <!-- Portrait / art -->
      <div class="relative min-h-[360px]">
        <!-- soft glow -->
        <div class="pointer-events-none absolute -inset-6 -z-10 rounded-full blur-2xl"
             style="background: radial-gradient(60% 60% at 50% 40%, rgba(0,245,255,.18), rgba(0,168,255,.08) 60%, transparent 61%);"></div>

        <!-- photo -->
        <div class="mx-auto aspect-square w-[86%] max-w-[520px] overflow-hidden rounded-full ring-1 ring-cyan-300/25 glow">
          <img src="{{ '/assets/img/HsuShun.png' | relative_url }}" alt="Portrait" class="h-full w-full object-cover object-center" />
        </div>

        <!-- Decorative icons -->
        <div class="absolute left-4 top-4 grid h-10 w-10 place-content-center rounded-full border border-cyan-400/40 bg-cyan-400/10 backdrop-blur">
          <svg viewBox="0 0 24 24" class="h-5 w-5 fill-cyan-300"><path d="M6 10V8a6 6 0 1 1 12 0v2h1a1 1 0 0 1 1 1v10a1 1 0 0 1-1 1H5a1 1 0 0 1-1-1V11a1 1 0 0 1 1-1h1zm2 0h8V8a4 4 0 1 0-8 0v2z"/></svg>
        </div>
        <div class="absolute bottom-6 right-6 grid h-10 w-10 place-content-center rounded-full border border-cyan-400/40 bg-cyan-400/10 backdrop-blur">
          <svg viewBox="0 0 24 24" class="h-5 w-5 fill-cyan-300"><path d="M11 2a5 5 0 0 1 5 5v2h-2V7a3 3 0 1 0-6 0v6.1l-.7-.7a2 2 0 1 0-2.8 2.8l4.5 4.5H18a2 2 0 0 0 2-2v-3a4 4 0 0 0-4-4h-1v-2h1a6 6 0 0 1 6 6v3a4 4 0 0 1-4 4H10.6l-5.2-5.2a4 4 0 0 1 5.7-5.6l.9.9V7a5 5 0 0 1 5-5z"/></svg>
        </div>
      </div>
    </section>
  </main>

  <footer class="border-t border-white/10 py-4">
    <div class="mx-auto w-[min(1120px,92%)] text-sm text-slate-400">
      © {{ 'now' | date: '%Y' }} Hsu Shun Lae - Cybersecurity
    </div>
  </footer>

  <script>
    const btn = document.getElementById('navBtn');
    const menu = document.getElementById('menu');
    btn.addEventListener('click', () => {
      const wasHidden = menu.classList.toggle('hidden');
      btn.setAttribute('aria-expanded', String(!wasHidden));
    });
  </script>
</body>
</html>
