## Ch.3 Cheat Sheet — AI Security Program Mgmt, Training, BCP, IR

### Governance Frameworks Reference
| Framework | Purpose | Key Fact |
|---|---|---|
| NIST AI RMF 1.0 | AI risk management | 4 functions: GOVERN, MAP, MEASURE, MANAGE |
| ISO/IEC 42001:2023 | AI management system | First intl. AI mgmt standard; complements, doesn't replace ISO 27001 |
| NIST SP 800-61 | Incident response lifecycle | 4 phases: Prep → Detect/Analyze → Contain/Eradicate/Recover → Post-Incident |
| MITRE ATLAS | AI attack technique catalog | Analogous to ATT&CK; covers poisoning, extraction, prompt injection |

### Three Lines Model for AI Risk
| Line | Owner | Function |
|---|---|---|
| 1st | Data scientists/ML engineers | Operational risk ownership |
| 2nd | AI governance/risk & compliance function | Oversight, policy, challenge |
| 3rd | Internal audit | Independent assurance |
Trap: 1st line alone owning AI risk = no accountability structure.

### AI Security Roles vs Traditional Roles
| Role | Owns |
|---|---|
| CISO | Enterprise-wide security program |
| AI Security Officer (or equivalent) | AI-lifecycle risks: data integrity, model robustness, drift, AI compliance |
| AI Governance Committee | Use-case approval, risk tolerance, board reporting |
AI roles coordinate with, not replace, existing security roles.

### KRI vs KPI (do not confuse)
| Type | Measures | Example |
|---|---|---|
| KRI | Risk exposure | % production models with unresolved high-severity adversarial finding past SLA |
| KPI | Program performance | % staff completed AI training |
Board reporting cadence: quarterly + ad hoc for major events.

### IR Playbook — AI-Specific Additions
- Model-behavior forensics (decision boundary manipulation check)
- Data/training poisoning detection
- Model extraction/theft detection
- Prompt injection response steps
- Model inversion (privacy leak) assessment
These ADD to, don't replace, the standard 4-phase NIST lifecycle.

### BCP for AI-Dependent Processes
- Trigger events: API/model outage, unacceptable drift, integrity compromise
- Required control: documented fallback (secondary model or manual process) — independent of vendor SLA
- SLA penalties ≠ continuity control (contractual deterrent only)

### Training Program Design
- Role-based, NOT one-size-fits-all
- Executives: risk/liability briefings
- Data scientists: secure model development
- General staff: prompt-injection/shadow-AI awareness
- Recurring cadence required (annual minimum; AI threat landscape evolves fast)

### Tabletop Exercises
- Minimum: annually
- Must include AI-specific scenarios, not just generic breach drills
- Additional exercises after major AI deployments/architecture changes
