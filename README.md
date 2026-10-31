# TryHackMe Notes — Penetration Testing Learning Journey

> A structured knowledge base of my hands-on cybersecurity practice on [TryHackMe](https://tryhackme.com/), covering offensive security fundamentals, web application pentesting, and AI/ML security threats.

![Status](https://img.shields.io/badge/status-actively%20learning-blue)
![Focus](https://img.shields.io/badge/focus-penetration%20testing-red)
![Platform](https://img.shields.io/badge/platform-TryHackMe-212C42)
![License](https://img.shields.io/badge/license-MIT-green)

---

## About

This repository documents my self-paced journey toward becoming a penetration tester. Each note is a **structured write-up** of a TryHackMe room or module — not just answers, but methodology, commands used, key takeaways, and lessons learned.

**Purpose**
- Reinforce knowledge through documentation.
- Build a reusable personal knowledge base for real engagements.
- Demonstrate consistent, hands-on practice to potential employers.

**Scope**
- Cyber Security fundamentals
- Junior Penetration Tester learning path
- Web Application Pentesting (advanced)
- AI/ML security threats

---

## 🛠️ Skills & Tools Covered

| Category | Skills / Tools |
|---|---|
| **Reconnaissance** | Nmap (SYN/version/OS/script scans), service enumeration |
| **Web Pentesting** | Burp Suite, OWASP Top 10 (2025), SQLMap, authentication & MFA testing, injection attacks |
| **Advanced Web Attacks** | Server-Side & Client-Side attacks, HTTP Request Smuggling |
| **Networking** | TCP/IP, protocols, packet analysis |
| **Cryptography** | Hashing, encryption fundamentals |
| **Defensive Security** | Security tooling, blue-team fundamentals, security solutions |
| **AI/ML Security** | AI fundamentals, ML threat modeling |
| **Methodology** | PTES-style enumeration, exploit basics, vulnerability analysis |

---

## Repository Structure

```text
tryhackme-notes/
├── AI/                          # AI fundamentals & AI/ML security threats
├── Cyber-Security-101/          # Core security fundamentals
│   ├── Cryptography/
│   ├── Networking/
│   ├── Web-Hacking/
│   ├── Defensive-Security/
│   ├── Exploitation-Basics/
│   └── ...
├── Jr-Penetration-Tester/       # Jr Pentester learning path
│   ├── 01-Introduction-to-Pentesting/
│   ├── 02-Introduction-to-Web-Hacking/
│   ├── 04-Network-Reconnaissance/
│   ├── 07-Burp-Suite/
│   ├── 11-OWASP-Top-10/
│   └── ...
├── Nmap/                        # Nmap deep-dive + post-scan analysis
├── Web-Application-Pentesting/  # Advanced web attack techniques
│   ├── 01-Authentication/
│   ├── 02-Injection-Attacks/
│   ├── 03-Advanced-Server-Side-Attacks/
│   ├── 04-Advanced-Client-Side-Attacks/
│   └── 05-HTTP-Request-Smuggling/
└── images/                      # Screenshots & diagrams used in write-ups
```

Each folder contains its own `README.md` (module overview + room list) and individual room write-ups.

---

## Learning Paths & Progress

| Path | Description | Progress |
|---|---|---|
| **Cyber Security 101** | Foundational security concepts | 🟢 Completed |
| **Jr Penetration Tester** | Core pentesting methodology | 🟡 In progress |
| **Web Application Pentesting** | Advanced web attack techniques | 🟡 In progress |
| **AI Security** | AI fundamentals & ML threats | 🟡 In progress |

---

## Featured Write-ups

A few notes that best represent my workflow and depth of understanding:

- **[Nmap — Post Scan Analysis](./Nmap/)** — Service enumeration, scripting, and result interpretation.
- **[Burp Suite](./Jr-Penetration-Tester/)** — Intercepting, replaying, and manipulating HTTP traffic.
- **[OWASP Top 10 (2025)](./Jr-Penetration-Tester/)** — Practical walkthroughs of the most common web vulnerabilities.
- **[HTTP Request Smuggling](./Web-Application-Pentesting/)** — Advanced desync attacks and exploitation.
- **[Authentication & MFA Bypass](./Web-Application-Pentesting/)** — Logic flaws and authentication bypass techniques.

---

## Note Conventions

- **One room = one file**.
- Each write-up follows a consistent template:
  - Objectives
  - Key concepts
  - Walkthrough (commands + screenshots)
  - Takeaways / lessons learned
- **Flags and credentials are redacted** before publishing.
- Screenshots stored in `images/` and referenced with relative paths.
- Commands are always in fenced code blocks for reproducibility.

---

## How to Use

1. Clone the repo:
   ```bash
   git clone https://github.com/ngngocatr/tryhackme-notes.git
   ```
2. Open in any Markdown editor (VSCode, Obsidian) for best readability.
3. Navigate via the folder structure above or through each module's `README.md`.

---

## Disclaimer

All notes and techniques documented here are for **educational purposes only** and were performed in **legal, controlled lab environments on TryHackMe**. Do not use these techniques against systems you do not own or have explicit permission to test.

---

## Contact

- **GitHub:** [@ngngocatr](https://github.com/ngngocatr)
- **TryHackMe:** [THM profile](https://tryhackme.com/p/daq)
- **Email:** *ngocdz2006@gmail.com*

---

## License

Released under the [MIT License](./LICENSE). Feel free to reference and learn from these notes.