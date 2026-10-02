## Chapter 4 Cheat Sheet — AI Risk Assessment, Appetite, and Treatment

### AI Risk Assessment vs. Traditional IT Risk Assessment
| Dimension | Traditional IT | AI-Specific Addition |
|---|---|---|
| Core risk model | Confidentiality/Integrity/Availability | + Drift, emergent behavior, non-determinism, bias |
| Register fields | Asset, vulnerability, threat | + Model lineage, training data provenance, retraining trigger |
| Change trigger | Patch/config change | + Data drift, prompt/context change, model version update |
| Monitoring | Uptime, logs | + Output quality, hallucination rate, fairness metrics |

### NIST AI RMF 1.0 — Four Functions
| Function | Purpose |
|---|---|
| Govern | Culture, policy, accountability (continuous, underpins all) |
| Map | Context and risk identification |
| Measure | Analyze and quantify risk |
| Manage | Prioritize and respond (treatment) |

### Risk Treatment Options
| Option | Definition | AI Example |
|---|---|---|
| Avoid | Discontinue/don't launch use case | Halt biased hiring model |
| Mitigate | Reduce likelihood/impact via controls | Add RAG grounding, guardrails, HITL review |
| Transfer | Shift impact to third party | Vendor indemnification, cyber/AI insurance |
| Accept | Formally sign off residual risk | Low-impact internal chatbot with monitoring |

### Risk Appetite Alignment by Criticality
| Use-Case Tier | Example | Risk Tolerance |
|---|---|---|
| Low | Internal productivity tool | Higher tolerance |
| Moderate | Customer-facing recommender | Medium tolerance |
| High | Autonomous credit/medical decisioning | Lowest tolerance |

### Appetite vs. Tolerance vs. Capacity
- **Appetite:** strategic amount of risk willing to pursue.
- **Tolerance:** acceptable operational variance around appetite.
- **Capacity:** absolute max risk before organizational failure.

### Risk Scoring & Escalation
- Standard matrix: Likelihood (1-5) × Impact (1-5) = Score (1-25).
- Appetite statement defines escalation threshold (e.g., score >15 = executive sign-off).
- Residual Risk = Inherent Risk − Control Effectiveness; compare to appetite before acceptance.

### Portfolio Prioritization Criteria
Business impact + Autonomy level + Data sensitivity + Reach/scale → combined risk score drives assessment order. Never prioritize by deployment date or alphabetically.

### Relevant Standards
| Standard | Type | Note |
|---|---|---|
| NIST AI RMF 1.0 | Voluntary framework | Govern/Map/Measure/Manage |
| ISO/IEC 23894:2023 | Guidance | AI risk management, extends ISO 31000 |
| ISO/IEC 42001:2023 | Certifiable | AI management system standard |

### Exam Traps
- Transfer ≠ full risk resolution (residual operational/ethical risk often remains).
- Uniform thresholds across all use cases = common wrong answer.
- Exceeding appetite triggers escalation, not automatic rejection.
- Don't confuse NIST AI RMF (framework) with ISO 42001 (certifiable management system).
