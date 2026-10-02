## Chapter 1 Cheat Sheet: AI Governance Frameworks as Program Inputs

### NIST AI RMF — Four Core Functions
| Function | Focus | Exam Cue |
|---|---|---|
| Govern | Culture, policy, accountability | Cross-cutting — applies continuously, not a phase |
| Map | Context, intended use, stakeholders | Must happen before risk can be measured |
| Measure | Analyze, benchmark, track risk | Requires mapped context as input |
| Manage | Resource allocation, risk treatment | Prioritization and response to identified risk |

Voluntary. Not certifiable. No accredited 'NIST AI RMF certification' exists.

### ISO/IEC 42001 (AIMS)
- Certifiable AI Management System standard.
- Built on Annex SL high-level structure (same skeleton as ISO 27001/9001) — integrates with existing ISO management systems.
- Includes Annex A controls covering AI lifecycle, data governance, and impact assessment.
- Exam cue: question mentions 'audit,' 'certification,' or 'external assessor' → ISO 42001.

### Threat-Input vs. Program Frameworks
| Framework | Type | Purpose |
|---|---|---|
| MITRE ATLAS | Threat-input | ATT&CK-style catalog of adversarial ML tactics/techniques; feeds Map/Measure |
| OWASP Top 10 for LLM | Threat-input / AppSec checklist | Ranked LLM app vulnerabilities (prompt injection, insecure output handling, excessive agency, training data poisoning, etc.) |
| NIST AI RMF | Program framework | Organization-wide voluntary risk process |
| ISO/IEC 42001 | Program framework | Certifiable management system |

Exam cue: ATLAS and OWASP Top 10 are **inputs consumed by** a program framework — never the answer to 'which framework structures your governance program.'

### EU AI Act — Risk Tiers
| Tier | Obligation | Example |
|---|---|---|
| Unacceptable | Prohibited | Social scoring, manipulative subliminal techniques |
| High-risk | Conformity assessment, risk mgmt, human oversight, documentation | Employment screening, credit scoring, biometrics, education access (Annex III) |
| Limited | Transparency disclosure only | Chatbots, deepfake generators |
| Minimal | No mandatory obligations | Spam filters, AI-enabled games |

Key timeline: Prohibited practices applicable Feb 2, 2025 → GPAI model obligations Aug 2, 2025 → High-risk system obligations generally applicable Aug 2, 2026 (extended timelines apply to certain Annex I regulated products).

### Selecting Frameworks: Mandate vs. Voluntary
- Regulation (EU AI Act) = legally binding **what** must be done.
- NIST AI RMF / ISO 42001 = voluntary **how** to structure the program.
- Choose ISO 42001 when certification/audit is required; NIST AI RMF for internal, non-certified risk process; ATLAS/OWASP as technical inputs, never as the program's structural foundation.

### Stakeholder Roles (EU AI Act)
Provider (builds the system) · Deployer (uses it operationally) · Importer · Distributor — each carries distinct obligations; map these alongside internal roles (legal, security, ML teams, execs) when scoping a governance program.
