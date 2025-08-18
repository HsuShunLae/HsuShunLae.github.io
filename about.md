---
layout: page
title: About
permalink: /about
---

<!-- Top summary + contact card -->
<div class="grid gap-8 md:grid-cols-3">

  <!-- Summary -->
  <div class="md:col-span-2 space-y-4">

    <div class="rounded-xl border border-white/10 bg-panel/60 p-5">
      <h3 class="mb-2 text-cyan-300 font-semibold">What I bring</h3>
      <ul class="list-disc pl-5 space-y-2 text-slate-200">
        <li>Build-and-hunt approach: Suricata sensors, Wazuh pipelines, meaningful dashboards.</li>
        <li>Deploying Hybrid Intrusion Detection System (Signature + Anomaly {ML Integrated})</li>
        <li>Practical offensive labs (Nmap, Burp Suite, BOF) to surface real risk and validate controls.</li>
        <li>Clear deliverables: findings, reproductions, and prioritized defensive recommendations.</li>
      </ul>
    </div>

    <!-- Skills chips -->
    <div>
      <h3 class="mb-2 text-cyan-300 font-semibold">Focus areas</h3>
      <div class="flex flex-wrap gap-2">
        <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">IDS</span>
        <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Detection Engineering</span>
        <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">SIEM (Wazuh)</span>
        <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Network (Suricata)</span>
        <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Web App Testing</span>
        <span class="rounded-lg border border-white/15 px-2.5 py-1 text-xs text-slate-300">Python / Bash</span>
      </div>
    </div>
  </div>

  <!-- Contact / quick facts -->
  <aside class="rounded-xl border border-white/10 bg-panel/60 p-5 space-y-3">
    <h3 class="text-cyan-300 font-semibold">Contact</h3>
    <p class="text-slate-200 text-sm">
      Email: <a href="mailto:emails.im84@gmail.com" class="text-cyan-300 hover:underline">emails.im84@gmail.com</a><br/><br/><br/>
      LinkedIn: <a href="https://www.linkedin.com/in/hsu-shun-lae-56a90b211/" class="text-cyan-300 hover:underline">/in/hsu-shun-lae-56a90b211</a><br/><br/><br/>
      Phone: +353870029026 <br/><br/><br/>
      Location: Dublin, Ireland<br/><br/><br/>
    </p>
    <div class="flex gap-2 pt-1">
      <a href="/projects" class="rounded-xl bg-gradient-to-br from-neonCyan to-neonBlue px-4 py-2 text-sm font-semibold text-slate-900 glow">See Projects</a>
      <a href="/resume" class="rounded-xl border border-white/25 px-4 py-2 text-sm text-slate-200 hover:border-white/40">Résumé</a>
    </div>
  </aside>
</div>

<!-- Highlights / samples -->
<div class="mt-10 grid gap-6 md:grid-cols-3">
  <div class="rounded-xl border border-white/10 bg-panel/60 p-5">
    <h4 class="mb-1 font-semibold text-white">Threat Hunting Lab</h4>
    <p class="text-mute text-sm">Zeek/Suricata → Wazuh → dashboards. Detections for DNS tunneling & beaconing with ATT&CK mapping.</p>
    <a href="/projects" class="text-cyan-300 hover:underline text-sm">Details →</a>
  </div>
  <div class="rounded-xl border border-white/10 bg-panel/60 p-5">
    <h4 class="mb-1 font-semibold text-white">Exploit Walkthrough</h4>
    <p class="text-mute text-sm">Buffer overflow to ROP on a lab binary; includes mitigations and secure coding notes.</p>
    <a href="/writeups" class="text-cyan-300 hover:underline text-sm">Read the write-up →</a>
  </div>
  <div class="rounded-xl border border-white/10 bg-panel/60 p-5">
    <h4 class="mb-1 font-semibold text-white">Azure Baseline</h4>
    <p class="text-mute text-sm">Guardrails for IAM, logging, and network segmentation with practical monitoring tips.</p>
    <a href="/projects" class="text-cyan-300 hover:underline text-sm">Playbook →</a>
  </div>
</div>

<!-- Optional: certifications / interests -->
<div class="mt-10 rounded-xl border border-white/10 bg-panel/60 p-5">
  <h3 class="mb-2 text-cyan-300 font-semibold">Certifications & Interests</h3>
  <p class="text-slate-200 text-sm">
    (Add yours here) e.g., CompTIA Security+, AZ-900 • Interests: Blue team, DFIR, detection engineering, secure cloud.
  </p>
</div>
