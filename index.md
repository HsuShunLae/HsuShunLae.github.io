---
layout: home
title: "Home"
---

## Hi, I’m **Hsu Shun Lae** — Security Analyst / Engineer

I hunt, harden, and help teams respond to cyber threats. My focus: **blue team analytics**, **practical exploit labs**, and **cloud security**.  
👇 Highlights:

<div class="grid">
  {% include project-card.html
     title="Threat Hunting with Zeek + Wazuh"
     stack="Zeek • Wazuh • Filebeat • MITRE ATT&CK"
     summary="Built a small lab to detect C2 and exfiltration; wrote Sigma rules and dashboards."
     repo="https://github.com/YOUR-USERNAME/zeek-wazuh-lab"
     post="/writeups/2025/01/10/soc-hunting-zeek-wazuh.html"
     tags="['Blue Team','Sigma','Dashboards']" %}
  {% include project-card.html
     title="CVE-2024-XXXX Buffer Overflow Lab"
     stack="C • GDB • pwntools"
     summary="End-to-end exploit development with safe, reproducible steps and mitigations."
     repo="https://github.com/YOUR-USERNAME/cve-bof-lab"
     post="/writeups/2025/02/18/cve-lab-bof-walkthrough.html"
     tags="['Exploit Dev','Reverse Engineering']" %}
  {% include project-card.html
     title="Azure Hardening Playbook"
     stack="Azure • Defender for Cloud • Terraform"
     summary="Baseline guardrails: identity, network segmentation, logging, alerts."
     repo="https://github.com/YOUR-USERNAME/azure-sec-playbook"
     tags="['Cloud','IaC']" %}
</div>

### Core skills
<div class="badges">
  {% for s in site.data.skills.blue_team %}{% include badge.html text=s %}{% endfor %}
  {% for s in site.data.skills.red_team %}{% include badge.html text=s %}{% endfor %}
  {% for s in site.data.skills.cloud %}{% include badge.html text=s %}{% endfor %}
</div>
