---
layout: page
title: Projects
permalink: /projects
---

A curated list of my security projects with code and write-ups.

{% include project-card.html
   title="SOC Detections Pack"
   stack="Sigma • Wazuh • Zeek"
   summary="Custom Sigma rules for credential access and lateral movement with ATT&CK mappings."
   repo="https://github.com/YOUR-USERNAME/sigma-detections"
   post="/writeups/2025/01/10/soc-hunting-zeek-wazuh.html"
   tags="['ATT&CK','Detections']" %}

{% include project-card.html
   title="Web App Pentest Playbook"
   stack="OWASP ZAP • Burp • Python"
   summary="Checklists, payloads, and safe test targets with reproducible scripts."
   repo="https://github.com/YOUR-USERNAME/web-pentest-playbook"
   tags="['OWASP','Automation']" %}
