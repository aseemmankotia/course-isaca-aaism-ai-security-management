# Chapter 5 Cheat Sheet: Adversarial ML & ATLAS Mapping

## Adversarial ML Taxonomy
| Attack | When | Goal | Example |
|---|---|---|---|
| Evasion | Inference time | Force misclassification | Adversarial pixel perturbation on stop sign |
| Poisoning | Training/fine-tuning time | Corrupt behavior via bad data | Backdoor trigger phrase in fine-tuning set |
| Extraction | Inference time (repeated queries) | Steal model, data, or IP | Cloning a model via 500K API queries |

## Prompt Injection vs. Jailbreak
| Aspect | Prompt Injection | Jailbreak |
|---|---|---|
| Vector | Hijacked instructions (input or retrieved content) | Bypasses safety alignment directly |
| Direct form | Attacker types payload into input | Role-play / persona framing (e.g., DAN) |
| Indirect form | Payload hidden in doc/webpage/tool output (RAG) | N/A — jailbreak is inherently direct |
| Goal | Hijack task/output | Unlock disallowed content/behavior |

## MITRE ATLAS — Key Tactics (ML-specific additions to ATT&CK)
| Tactic | Description | Example Technique |
|---|---|---|
| Reconnaissance | Learn about target ML system | Discover model ontology |
| ML Model Access | Gain query/white-box/black-box access | API access, model file access |
| ML Attack Staging | Build attack assets using target model | Train substitute/surrogate model |
| Defense Evasion | Evade detection/model defenses | Evade ML Model (adversarial example) |
| Exfiltration | Remove stolen model/data/capability | Exfiltrate via ML inference API |
| Impact | Achieve attacker's end goal | Erode model integrity, denial of service |

## OWASP Top 10 for LLM Applications (2025)
| ID | Category |
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

## Exam Gotchas
- Evasion ≠ Poisoning: evasion = inference-time input attack; poisoning = training-time data attack. Exam loves swapping these.
- Jailbreak can occur with NO external data — pure conversational manipulation. Don't confuse with indirect injection.
- Model extraction control = rate limiting + query anomaly detection, NOT bigger models or more logging alone.
- Supply-chain (LLM03) = compromised model/library provenance; Poisoning (LLM04) = compromised training data. Exam tests this distinction directly.
- ATLAS reuses ATT&CK tactic names but adds ML-specific stages (ML Model Access, ML Attack Staging) — map attacker technique to the specific ML-lifecycle stage, not just generic IT kill-chain stage.
