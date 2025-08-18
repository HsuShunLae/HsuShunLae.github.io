---
layout: page
title: Home
---


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
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-600">
            cyber solutions
          </span><br/>
          for your <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-300 to-blue-700">security</span>
        </h1>

        <p class="max-w-prose text-mute">
          My goal is to think like an attacker, expose weaknesses, and demonstrate real-world risks. I provide values by delivering clear incident notes, detection guidance, and defensive recommendations to strengthen security posture.
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
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Nmap</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">BurpSuite</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Bash</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Python</span>
          <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">OWASP</span>
        </div>
      </div>

      <!-- Portrait / art -->
      <div class="relative min-h-[360px]">
        <!-- soft glow -->
        <div class="pointer-events-none absolute -inset-6 -z-10 rounded-full blur-2xl"
             style="background: radial-gradient(60% 60% at 50% 40%, rgba(0,245,255,.18), rgba(0,168,255,.08) 60%, transparent 61%);"></div>
        <!-- photo with circular frame -->
        <div class="mx-auto relative aspect-square w-[86%] max-w-[520px]">
          <!-- background circle (frame) -->
          <div class="absolute inset-0 rounded-full bg-cyan-500/20"></div>
          
          <!-- smaller photo -->
          <div class="relative mx-auto aspect-square w-[80%] overflow-hidden rounded-full ring-2 ring-cyan-400">
            <img src="{{ '/assets/img/HsuShun.png' | relative_url }}"
                 alt="Portrait"/>
          </div>
        </div>
        <!-- Decorative icons -->
        <div class="absolute left-4 top-4 grid h-10 w-10 place-content-center rounded-full border border-cyan-400/40 bg-cyan-400/10 backdrop-blur">
          <svg viewBox="0 0 24 24" class="h-5 w-5 fill-cyan-300"><path d="M6 10V8a6 6 0 1 1 12 0v2h1a1 1 0 0 1 1 1v10a1 1 0 0 1-1 1H5a1 1 0 0 1-1-1V11a1 1 0 0 1 1-1h1zm2 0h8V8a4 4 0 1 0-8 0v2z"/></svg>
        </div>
        <div class="absolute bottom-6 right-6 grid h-10 w-10 place-content-center rounded-full border border-cyan-400/40 bg-cyan-400/10 backdrop-blur">
          <svg viewBox="0 0 24 24" class="h-5 w-5 fill-cyan-300"><path d="M6 10V8a6 6 0 1 1 12 0v2h1a1 1 0 0 1 1 1v10a1 1 0 0 1-1 1H5a1 1 0 0 1-1-1V11a1 1 0 0 1 1-1h1zm2 0h8V8a4 4 0 1 0-8 0v2z"/></svg>
        </div>
      </div>
    </section>
  </main>

