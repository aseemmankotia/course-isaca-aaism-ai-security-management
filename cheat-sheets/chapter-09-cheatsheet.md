## Chapter 9 Cheat Sheet: AI Security Monitoring, Red-Teaming, Continuous Evaluation

### NIST AI RMF 1.0 — 4 Functions
| Function | Focus |
|---|---|
| Govern | Policy, accountability, culture |
| Map | Context, risk identification |
| Measure | Continuous evaluation, metrics, monitoring |
| Manage | Response, retraining, remediation |

### Drift Types Comparison
| Type | Definition | Detection Signal |
|---|---|---|
| Data drift | Input feature distribution shifts | Input stats diverge from training baseline |
| Concept drift | Input→correct-output relationship shifts | Accuracy/hallucination rate rises on stable inputs |
| Model drift (umbrella) | General performance decay over time | Combined quality + safety metric decline |

### OWASP Top 10 for LLM Applications (2025)
| ID | Risk |
|---|---|
| LLM01 | Prompt Injection |
| LLM02 | Sensitive Information Disclosure |
| LLM03 | Supply Chain |
| LLM04 | Data and Model Poisoning |
| LLM05 | Improper Output Handling |
| LLM06 | Excessive Agency |
| LLM07 | System Prompt Leakage |
| LLM08 | Vector and Embedding Weaknesses |
| LLM09 | Misinformation |
| LLM10 | Unbounded Consumption |

### Minimum Audit Log Fields (Prompt/Response/Tool Chain)
| Field | Why It Matters |
|---|---|
| Timestamp + Session ID | Session reconstruction |
| User/service identity | Attribution |
| System prompt (or hash) | Integrity check w/o exposure |
| Full user prompt + retrieved context | Detects indirect injection |
| Tool calls (name, params, result) | Detects unauthorized agent actions |
| Model + version | Correlate incidents to model release |
| Guardrail/filter decision | Shows what was blocked/allowed |

### Red-Team Exercise Phases
1. Scoping & threat modeling (map to MITRE ATLAS TTPs)
2. Adversarial prompt / attack generation (direct + indirect injection, jailbreaks)
3. Execution — including agentic tool-abuse and privilege escalation attempts
4. Impact assessment
5. Reporting & remediation tracking

### Continuous Evaluation — Metric Categories
| Category | Example Metrics |
|---|---|
| Performance | Accuracy, task success rate, hallucination rate |
| Safety | Jailbreak success rate, policy-violation rate, toxic output rate |
| Operational (context only) | Latency, cost — NOT drift indicators alone |

### SOC Integration Rules
- Forward AI telemetry into existing SIEM/SOAR — do not build a silo
- Correlate AI logs with identity + network logs
- Add AI-specific detection rules (injection patterns, abuse spikes, tool-call anomalies)
- Retraining trigger = sustained threshold breach on defined metrics, not anecdote or calendar alone
