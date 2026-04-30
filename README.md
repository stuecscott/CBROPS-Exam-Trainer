# CBROPS-Exam-Trainer

CBROPS 200-201 Exam Trainer
A self-contained, browser-based exam trainer for the Cisco Certified CyberOps Associate certification - Understanding Cisco Cybersecurity Operations Fundamentals (200-201 CBROPS) v1.2.
Built as a single HTML file with 175 questions mapped to the official Cisco blueprint, three study modes, persistent progress tracking, and a dark SOC-themed interface.
---
Features
175 questions across all 5 official exam domains, weighted to match the real exam
Three modes:
Study - answer-by-answer with explanations revealed immediately
Practice - pick a domain and question count, scored at the end
Exam Sim - 95 questions, 120-minute timer, quick-jump grid, flag-for-review
Persistent progress tracking, scores, per-domain accuracy, and session history saved to `localStorage`
Weak-area mode - prioritizes questions you've previously missed or haven't seen yet
Detailed explanations for every question
Dark theme — designed for long study sessions
No installation, no dependencies, opens in any modern browser
---
Question Distribution
Domain	Weight	Questions
Security Concepts	20%	40
Security Monitoring	25%	40
Host-Based Analysis	20%	35
Network Intrusion Analysis	20%	35
Security Policies & Procedures	15%	25
Total	100%	175
Topics Covered
Security Concepts - CIA triad, defense in depth, access control models, Cyber Kill Chain, Diamond Model, CVSS, social engineering, malware classification, PKI/certificates, evasion techniques
Security Monitoring - SIEM/SOAR, NetFlow & 5-tuple, deep packet inspection, TLS/SNI, signature vs. anomaly detection, taps & SPAN, Wireshark, baselines, Windows Event IDs
Host-Based Analysis - Windows/Linux logs, registry & persistence, Sysmon, Sysinternals, ASLR/DEP, file systems, hashing, EDR, fileless attacks, forensic imaging
Network Intrusion Analysis - TCP/IP fundamentals, port scanning, ARP/DNS attacks, JA3 fingerprinting, DGAs, domain fronting, IOCs, fragmentation evasion
Security Policies & Procedures - NIST SP 800-61, BCP/DRP, RTO/RPO, MITRE ATT&CK, chain of custody, compliance frameworks (PCI-DSS, HIPAA, NIST CSF)
---
Usage
Quick Start
Download `cbrops-exam-trainer.html`
Double-click to open in your browser
Start training
That's it. No build step, no server, no dependencies.
Recommended Study Path
Week 1–2: Run Study Mode through each domain to learn with explanations
Week 3: Switch to Practice Mode with 25–50 questions per session, focusing on weaker domains
Final week: Take 1–2 full Exam Sim runs (95 questions, 120 min) to build pacing
Use weak-areas toggle in your final review sessions to drill missed questions
The dashboard flags `EXAM_READY` once your overall accuracy hits 82% (the approximate CBROPS pass mark).
---
Technical Notes
Single HTML file - all CSS, JavaScript, and questions embedded
Storage - uses `localStorage` for persistence; data stays on your device
Privacy - no analytics, no network calls, no telemetry
Browser support - any modern browser (Chrome, Firefox, Edge, Safari)
Mobile - responsive layout works on phones and tablets
Resetting Progress
Click ANALYTICS → RESET ALL PROGRESS to clear all saved scores and session history.
---
Disclaimer
This trainer is an independent study aid and is not affiliated with, endorsed by, or sponsored by Cisco Systems, Inc. Cisco®, CCNA®, and CyberOps® are trademarks of Cisco Systems, Inc.
Questions are written to align with the publicly published v1.2 blueprint topics and are intended to reinforce understanding of the exam objectives. They are not real exam questions and passing this trainer does not guarantee passing the certification exam.
---
License
MIT
---
Contributing
Spot a question that needs correction or want to add more? Open an issue or pull request. Each question entry follows a simple structure:
```js
{
  id: 176,
  domain: "SC",     // SC | SM | HA | NIA | PP
  q: "Question text...",
  choices: ["Option A", "Option B", "Option C", "Option D"],
  a: 1,             // index of correct answer (0-3)
  exp: "Explanation of why this is correct."
}
```
---
Good luck on your exam.
