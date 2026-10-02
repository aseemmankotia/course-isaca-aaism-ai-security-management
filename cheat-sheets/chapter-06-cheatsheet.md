## Chapter 6 Cheat Sheet: AI Vendor & Supply-Chain Risk

### Vendor Due-Diligence Checklist
| Area | Ask For |
|---|---|
| Data usage | Written confirmation inputs/outputs excluded from training |
| Provenance | Model card + dataset datasheet (or equivalent) |
| Attestation | SOC 2 Type II, ISO/IEC 42001, ISO/IEC 27001 |
| Subprocessors | Current fourth-party / subprocessor list |
| Retention | Data retention period, purpose, deletion rights |
| Audit | Right-to-audit clause or attestation substitute |

### Key Contract Clauses
| Clause | Purpose | Common Confusion |
|---|---|---|
| Data-usage / training opt-out | Blocks vendor from training on customer data | Confused with DPA |
| Indemnification | Allocates liability for IP/third-party claims | Confused with liability cap |
| DPA (Data Processing Addendum) | Governs personal data processing per privacy law | Confused with indemnification |
| Right-to-audit | Enables direct/independent verification of controls | Assumed impossible for SaaS — attestations are the accepted substitute |
| SLA | Availability + incident notification timelines | Focused only on uptime, ignoring incident response |

### Model Card vs. Dataset Datasheet
| | Model Card | Dataset Datasheet |
|---|---|---|
| Describes | Trained model behavior, performance, limitations | Training data provenance, composition, licensing |
| Origin | Mitchell et al., 2019 | Gebru et al., 'Datasheets for Datasets' |
| Exam use | Verify performance/bias disclosure | Verify data provenance/IP risk |

### Attestation Comparison
| Standard | Focus | Notes |
|---|---|---|
| ISO/IEC 42001:2023 | AI management system | AI-specific governance/risk |
| ISO/IEC 27001 | General infosec management | Not AI-specific |
| SOC 2 Type I | Point-in-time control design | Weaker evidence |
| SOC 2 Type II | Control effectiveness over a period (typ. 6-12 mo) | Stronger evidence |

### Fourth-Party / Supply-Chain Risk
- Foundation-model vendors often rely on subcontracted hosting, fine-tuning, or moderation providers.
- Undisclosed subprocessors = loss of visibility/control over data handling.
- Require a maintained subprocessor list + notification of changes.

### Right-to-Audit Alternatives (multi-tenant vendors)
1. Independent attestation reports (SOC 2 Type II, ISO/IEC 42001)
2. Contractual right to review findings + remediation plans
3. Pooled/consortium audits where available

### Frameworks to Reference
- **NIST AI RMF 1.0 (2023):** Govern, Map, Measure, Manage
- **ISO/IEC 23894:** AI risk management guidance
- **GDPR Art. 33:** 72-hour breach notification benchmark for SLA design

### Exam Traps
- Confusing DPA (personal data) with indemnification (IP/liability).
- Assuming termination is required when direct audit is refused — attestations are acceptable.
- Treating model card and dataset datasheet as interchangeable.
- Overlooking fourth-party subprocessors during vendor onboarding.
