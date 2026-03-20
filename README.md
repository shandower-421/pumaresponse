# PumaResponse

> **Status: Unfinished Prototype** — This project is an early-stage prototype under active development. Features may be incomplete, scenarios may change, and rough edges are expected.

PumaResponse is an incident response edutainment game that puts you in the seat of a cybersecurity analyst at a Managed Security Service Provider (MSSP). Make critical decisions across realistic incident scenarios and see how your choices affect the outcome.

## What Is This?

An interactive, browser-based simulator where you work through the six phases of incident response — Triage, Containment, Investigation, Eradication, Recovery, and Post-Incident — making branching decisions that are scored on response time, containment effectiveness, evidence preservation, and thoroughness.

The game features a retro CRT terminal aesthetic with a live SIEM feed, dynamic scoring, and a final performance grade (A–F).

## Scenarios

Seven incident scenarios are currently included (randomly selected each playthrough):

- **Ransomware Outbreak (LockBit 3.0)** — Multiple endpoints encrypted at a financial services firm. Active Directory potentially compromised. Data exfiltration detected. *CRITICAL severity.*
- **Business Email Compromise (BEC/CEO Fraud)** — $340K wire transfer initiated via spoofed CEO email. Within the recall window. Credential compromise confirmed. *HIGH severity.*
- **Supply Chain Compromise** — Trusted RMM vendor pushes backdoored update to 340+ endpoints at a healthcare organization. Patient data at risk. HIPAA implications. *CRITICAL severity.*
- **Insider Threat** — Departing engineer exfiltrates ITAR-controlled avionics designs to a foreign-owned competitor. FBI referral and defense contractor compliance at stake. *HIGH severity.*
- **Cloud Infrastructure Breach** — AWS access keys leaked in a public GitHub repo. Crypto miners, IAM privilege escalation, and 2.1M payment card records exposed. PCI-DSS breach. *CRITICAL severity.*
- **DDoS Smokescreen** — Volumetric DDoS attack masks a simultaneous SQL injection and POS malware deployment across 52 retail locations on Black Friday weekend. *CRITICAL severity.*
- **Web Application RCE** — Zero-day deserialization exploit on a law firm's client portal. Attacker gains root, dumps attorney-client privileged case files. Legal ethics crisis. *CRITICAL severity.*

Each scenario includes realistic IOCs, forensic evidence, and consequences tied to your decisions.

## How to Run

No build step, no dependencies — just open the file:

```bash
# Option 1: Open directly
open index.html

# Option 2: Local server (recommended)
python3 -m http.server 8000
# Then visit http://localhost:8000
```

Works in any modern browser (Chrome, Firefox, Safari, Edge). Responsive on mobile/tablet.

## Controls

- **Mouse**: Click choices and buttons
- **Keyboard**: `A`/`B`/`C` or `1`/`2`/`3` to select choices, `Enter`/`Space` to advance

## Tech Stack

- Vanilla HTML, CSS, and JavaScript (single `index.html` file)
- No frameworks or external dependencies
- CRT terminal aesthetic with CSS animations and custom properties

## Scoring

Decisions are rated as good, partial, or bad across four metrics. Your final grade reflects professional incident response standards:

| Grade | Score | Meaning |
|-------|-------|---------|
| A | 80%+ | Outstanding response |
| B | 60–79% | Solid response |
| C | 40–59% | Contained with gaps |
| D | 20–39% | Barely contained |
| F | <20% | Response failure |

## Educational Value

The simulator teaches real-world incident response trade-offs grounded in NIST/SANS frameworks:

- Speed vs. evidence preservation
- Scope of containment vs. business disruption
- Depth of investigation vs. timeline pressure
- Post-incident documentation and regulatory obligations

## Project Structure

```
pumaresponse/
└── index.html    # Single-file application (~87 KB)
```

## License

Not yet specified.
