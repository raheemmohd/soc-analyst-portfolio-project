# SOC Analyst Project — Alert to Resolution

An interactive walkthrough of a Security Operations Center analyst's workflow — from raw log to detection rule to a triaged, investigated, and closed incident. Built as a single self-contained web page, no backend or build step required.

**[▶ Live demo](https://claude.ai/artifact/EADZLLJquGJ6W8vVM4goV1)**

![status](https://img.shields.io/badge/status-complete-brightgreen) ![type](https://img.shields.io/badge/type-portfolio%20project-blue) ![stack](https://img.shields.io/badge/stack-HTML%2FCSS%2FJS-informational)

---

## Why I built this

I wanted a way to show SOC workflow knowledge that goes beyond a bullet point on a resume — something a reviewer can actually click through instead of just reading about. So instead of writing another study-notes doc, I built a page that documents the full alert lifecycle *and* lets you interact with a simulated alert queue the same way a Tier 1 analyst would: open an alert, pull the evidence, decide false positive / escalate / contain.

It's organized around two fully worked case studies — a brute-force SSH compromise and a phishing-to-malware-execution chain — plus the frameworks a real SOC runs on: the NIST incident response lifecycle, MITRE ATT&CK, the cyber kill chain, and a detection-engineering pipeline showing how an alert gets built in the first place.

## What's inside

| Section | What it covers |
|---|---|
| SOC roles & tiers | L1 triage, L2 incident response, L3 threat hunting, plus shift structure and severity-based SLAs |
| Tool stack & sample queries | SIEM/EDR/IDS/SOAR/threat-intel categories, with Splunk SPL, Microsoft Sentinel KQL, and a Sigma detection rule |
| Detection engineering pipeline | How a raw log becomes a firing alert — collection → parsing → normalization → correlation rule → alert → analyst feedback loop |
| Alert severity scoring model | A concrete formula (asset criticality × threat confidence × potential impact) with a worked scoring table |
| Alert triage flowchart | The decision path every alert goes through: false-positive check → context gathering → confirmation → severity scoring → escalation |
| Incident response lifecycle | The NIST IR model — Preparation, Detection & Analysis, Containment, Eradication, Recovery, Lessons Learned |
| Case study 1 | Brute-force SSH login → compromised account, with log excerpts at every step |
| Case study 2 | Phishing attachment → macro execution → PowerShell → C2 callback, resolved at the endpoint |
| MITRE ATT&CK mapping | Both case studies mapped to specific ATT&CK tactics/techniques, plus the Lockheed Martin Cyber Kill Chain |
| **Live demo — alert queue** | 5 alerts of varying severity; click "Investigate" to pull evidence, then classify each one |
| KPIs | MTTD, MTTR, false-positive rate, dwell time, alert volume, ATT&CK coverage |
| Where SOC work is heading | AI-assisted triage, SOAR automation, XDR, autonomous threat hunting |

## Skills demonstrated

`Log analysis` · `SIEM query writing (SPL / KQL)` · `Detection engineering (Sigma rules)` · `Alert triage` · `Incident response (NIST lifecycle)` · `MITRE ATT&CK mapping` · `Threat intelligence` · `Network & endpoint forensics` · `Malware triage basics`

## Tech stack & approach

Pure HTML, CSS, and vanilla JavaScript — no frameworks, no dependencies, no build tooling. All diagrams are hand-built inline SVG rather than screenshots, and the alert queue is a small state machine in plain JS. I kept it dependency-free on purpose: it's trivial to host anywhere (GitHub Pages, any static host, or just opening the file locally), and anyone reviewing it can read the whole source in one sitting.

## Repository structure

```
soc-analyst-portfolio-project/
├── index.html          # the entire project — open this in a browser
└── README.md            # this file
```

## Running it locally

No install required.

```bash
git clone https://github.com/<your-username>/soc-analyst-portfolio-project.git
cd soc-analyst-portfolio-project
open index.html          # macOS
# or just double-click index.html / drag it into a browser tab
```

## Hosting it for free (GitHub Pages)

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, select the `main` branch and `/ (root)`.
4. The project's HTML file is already named `index.html`, so Pages will pick it up automatically.
5. The live link will be `https://<your-username>.github.io/soc-analyst-portfolio-project/`.

I link the Pages URL — not the repo itself — in my resume and portfolio, so people land straight on the interactive alert queue instead of a code view.

## A note on the data

The logs, alert queue, IPs, hostnames, and usernames throughout are synthetic — written to model a realistic investigation rather than to represent any real organization or incident.

## License

MIT

## Author

[MOHAMMED ABDUL RAHEEM] · [raheemmohd0000@gmail.com] 
