## Chapter 8 Cheat Sheet: Data, Privacy, Ethics & Human Oversight

### Data Governance Controls
| Control | Purpose | Key Reference |
|---|---|---|
| Data minimization | Limit data to what's necessary for the purpose | GDPR Art. 5(1)(c) |
| Data lineage/provenance | Track origin, transformations, labeling of training data | EU AI Act Art. 10 |
| Purpose limitation | Prevent reuse of data beyond original consent scope | GDPR Art. 5(1)(b) |

### Leakage Vectors Across the AI Lifecycle
| Stage | Leakage Risk | Primary Mitigation |
|---|---|---|
| Training | Model memorizes sensitive records | Differential privacy, data de-identification |
| Fine-tuning | Small, sensitive datasets get memorized easily | PII scrubbing, synthetic data, DP-SGD |
| Inference | Prompt injection / extraction attacks reveal training data or system prompts | Output filtering, rate limiting, input sanitization |

**Attack types:** Membership inference (was record X in training set?) vs. Model inversion (reconstruct record X from outputs).

### Bias & Fairness Testing
- **Four-fifths (80%) rule:** selection ratio < 0.80 between groups signals adverse impact (EEOC).
- **Common fairness metrics:** demographic parity, equalized odds, equal opportunity.
- Test bias at **data, model, and decision-output** stages — not just one point.

### Transparency & Explainability
- **SHAP** — global, additive, game-theoretic attribution.
- **LIME** — local linear surrogate explanation per prediction.
- EU AI Act high-risk systems require **technical documentation + user-facing transparency** on capabilities/limitations.

### Human Oversight Thresholds
- EU AI Act Art. 14: human must be able to **understand, monitor, intervene, override, stop** — oversight must occur **before** harm, not only in retrospective audits.
- GDPR Art. 22: right against solely automated decisions with legal/significant effect; exceptions require safeguards (human review, right to contest).
- High-risk domains needing oversight: credit scoring, employment, biometric ID, law enforcement, critical infrastructure, education admissions.

### Safety Guardrails vs Ethical Controls
| Guardrail (technical/operational) | Ethical Control (governance/values) |
|---|---|
| Content filters | Published AI ethics principles |
| Rate limiting | Ethics review boards |
| Output validators / kill switches | Stakeholder impact consultations |
| Real-time, enforceable | Deliberative, policy-level |

### Key Frameworks
- **NIST AI RMF 1.0:** Govern, Map, Measure, Manage (Govern is cross-cutting).
- **ISO/IEC 42001:2023:** AI Management System (AIMS) standard.
- **EU AI Act risk tiers:** Unacceptable (banned) → High-risk (strict obligations) → Limited (transparency duties) → Minimal (no obligations).

### Exam Traps
- Post-hoc audits ≠ human oversight (oversight must allow intervention *before* harm).
- Disclosure of AI use ≠ satisfying oversight or fairness obligations.
- Guardrails and ethical controls are frequently confused — guardrails are technical/real-time; ethics controls are governance/values-based.
