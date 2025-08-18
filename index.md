---
layout: null
title: Home
---

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>{{ site.title }}</title>

  <!-- Tailwind (Play CDN) — no build step -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            base:  '#0b1220',
            panel: '#0f172a',
            text:  '#e6edf3',
            mute:  '#9aa4b2',
            brand: '#1fdf86',
            brand2:'#14b86e',
          },
        }
      }
    }
  </script>

  <!-- tiny helper styles for the subtle hex background -->
  <style>
    .hex-bg::before{
      content:""; position:fixed; inset:0; z-index:-1; opacity:.06; pointer-events:none;
      background-image:url("data:image/svg+xml,%3Csvg width='60' height='52' viewBox='0 0 60 52' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M30 2l25 14v20L30 50 5 36V16L30 2z M5 36l25 14 25-14' fill='none' stroke='%23ffffff' stroke-width='1'/%3E%3C/svg%3E");
      background-size:200px 170px;
    }
  </style>
</head>

<body class="hex-bg bg-base text-text selection:bg-emerald-400/30">
  <!-- Sticky nav -->
  <header class="sticky top-0 z-20 border-b border-white/10 bg-base/80 backdrop-blur">
    <div class="mx-auto flex w-[min(1120px,92%)] items-center gap-3 py-3">
      <a href="{{ '/' | relative_url }}" class="flex items-center gap-2 font-extrabold text-white">
        <span class="h-7 w-7 rounded-full bg-gradient-to-br from-emerald-300 via-brand to-brand2 shadow-[inset_0_0_20px_rgba(31,223,134,.6)]"></span>
        <span>CSume<span class="font-light opacity-80">Security</span></span>
      </a>

      <!-- Mobile toggle -->
      <button class="ml-auto inline-flex items-center justify-center rounded-md p-2 text-slate-300 ring-1 ring-white/10 hover:text-white md:hidden"
              aria-label="Toggle menu" aria-expanded="false" id="navBtn">☰</button>

      <!-- Menu -->
      <nav id="menu" class="ml-auto hidden flex-col gap-3 rounded-lg border border-white/10 bg-base/95 p-3 md:static md:flex md:flex-row md:gap-5 md:border-0 md:bg-transparent md:p-0">
        {% for item in site.nav %}
          <a href="{{ item.link | relative_url }}"
             class="text-slate-300 hover:text-white {% if page.url == item.link %}text-white{% endif %}">
            {{ item.name }}
          </a>
        {% endfor %}
      </nav>

      <a href="{{ '/contact' | relative_url }}" class="ml-3 hidden rounded-lg border border-white/20 px-4 py-2 text-sm text-slate-200 hover:border-white/40 md:inline-block">Let’s Talk</a>
    </div>
  </header>

  <!-- Hero -->
  <main>
    <section class="mx-auto grid w-[min(1120px,92%)] items-center gap-10 py-10 md:grid-cols-2 lg:py-16">
      <!-- copy -->
      <div>
        <p class="mb-2 text-xs tracking-[0.18em] text-slate-300 uppercase">I’m <strong>Your Name</strong></p>

        <h1 class="mb-4 text-4xl font-extrabold leading-tight tracking-tight sm:text-5xl">
          Provide the best
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-300 via-emerald-400 to-emerald-600">
            cyber solutions
          </span><br/>
          for your <span class="text-transparent bg-clip-text bg-gradient-to-r from-emerald-200 to-emerald-500">security</span>
        </h1>

        <p class="max-w-prose text-mute">
          I protect websites, servers, and cloud apps against modern threats.
          Blue-team detections, secure architecture, and clear incident notes.
        </p>

        <div class="mt-5 flex flex-wrap gap-3">
          <a href="{{ '/projects' | relative_url }}" class="rounded-xl bg-gradient-to-br from-brand to-brand2 px-5 py-3 font-semibold text-base text-base/90 text-base-900 text-slate-900 shadow-[0_10px_24px_rgba(31,223,134,.25)] hover:translate-y-[-2px] transition">
            Get Started
          </a>
          <a href="{{ '/about' | relative_url }}" class="rounded-xl border border-white/20 px-5 py-3 font-semibold text-slate-200 hover:border-white/40 transition">
            Learn More
          </a>
        </div>

        <div class="mt-4 flex flex-wrap gap-2">
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Wazuh</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Zeek</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Suricata</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Azure</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Python</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">OWASP</span>
        </div>
      </div>

      <!-- art / portrait -->
      <div class="relative min-h-[360px]">
        <!-- soft radial glow -->
        <div class="pointer-events-none absolute -inset-6 -z-10 rounded-full bg-[radial-gradient(50%_60%_at_50%_40%,rgba(31,223,134,.20),rgba(31,223,134,.05)_60%,transparent_61%)]"></div>

        <!-- circle photo -->
        <div class="mx-auto aspect-square w-[86%] max-w-[520px] overflow-hidden rounded-full ring-1 ring-emerald-400/20">
          <img src="{{ '/assets/img/hero.png' | relative_url }}" alt="Portrait" class="h-full w-full object-cover translate-y-1" />
        </div>

        <!-- tiny icons (decorative) -->
        <div class="absolute left-4 top-4 grid h-10 w-10 place-content-center rounded-full border border-emerald-400/30 bg-emerald-400/10">
          <svg viewBox="0 0 24 24" class="h-5 w-5 fill-emerald-400"><path d="M6 10V8a6 6 0 1 1 12 0v2h1a1 1 0 0 1 1 1v10a1 1 0 0 1-1 1H5a1 1 0 0 1-1-1V11a1 1 0 0 1 1-1h1zm2 0h8V8a4 4 0 1 0-8 0v2z"/></svg>
        </div>
        <div class="absolute bottom-6 right-6 grid h-10 w-10 place-content-center rounded-full border border-emerald-400/30 bg-emerald-400/10">
          <svg viewBox="0 0 24 24" class="h-5 w-5 fill-emerald-400"><path d="M11 2a5 5 0 0 1 5 5v2h-2V7a3 3 0 1 0-6 0v6.1l-.7-.7a2 2 0 1 0-2.8 2.8l4.5 4.5H18a2 2 0 0 0 2-2v-3a4 4 0 0 0-4-4h-1v-2h1a6 6 0 0 1 6 6v3a4 4 0 0 1-4 4H10.6l-5.2-5.2a4 4 0 0 1 5.7-5.6l.9.9V7a5 5 0 0 1 5-5z"/></svg>
        </div>
      </div>
    </section>
  </main>

  <footer class="border-t border-white/10 py-4">
    <div class="mx-auto w-[min(1120px,92%)] text-sm text-slate-400">
      © {{ 'now' | date: '%Y' }} Your Name — Cybersecurity
    </div>
  </footer>

  <script>
    const btn = document.getElementById('navBtn');
    const menu = document.getElementById('menu');
    btn.addEventListener('click', () => {
      const open = menu.classList.toggle('hidden') === false;
      btn.setAttribute('aria-expanded', String(open));
    });
  </script>
</body>
</html>
