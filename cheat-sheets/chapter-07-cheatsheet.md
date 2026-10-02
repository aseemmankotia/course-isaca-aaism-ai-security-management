## Chapter 7 Cheat Sheet: AI Security Architecture & Secure Deployment Patterns

### Secure ML Pipeline Stages (Isolation Zones)
| Stage | Trust Boundary Purpose |
|---|---|
| Data ingestion | Validate source, quarantine untrusted data |
| Data validation | Detect poisoning/anomalies before use |
| Feature store | Curated, access-controlled features |
| Training environment | Isolated compute; may be air-gapped for sensitive data |
| Model registry | **Gate**: validation/approval before promotion |
| Staging | Pre-prod testing, red-teaming |
| Production serving | Locked-down inference endpoint |

### Guardrail Layers (Processing Order)
1. **Input filtering** — prompt injection, jailbreak, PII detection
2. **Model inference**
3. **Output filtering** — toxicity, hallucination, data leakage
4. **Policy enforcement / escalation** — block, redact, or route to human review for high-risk results

### Secure RAG Pattern
- Enforce **document/row-level ACLs at retrieval**, matched to requesting user identity (never rely on the LLM to withhold unauthorized content).
- Treat retrieved content as **untrusted data** — use delimiters/instruction-hierarchy to block indirect prompt injection.
- Segment vector stores by tenant/classification; encrypt embeddings at rest.
- Monitor the index for data poisoning.

### Agentic AI Tool-Use Isolation
| Control | Purpose |
|---|---|
| Least-privilege tool scoping | Limit each tool to only required actions |
| Sandboxed execution | Contain code/tool execution blast radius |
| Short-lived, session-scoped credentials | Reduce impact of leaked tokens |
| Allow-list of permitted actions | Prevent unauthorized tool invocation |
| Human-in-the-loop approval | Required for high-risk/irreversible actions |
| Full tool-call logging | Auditability and forensic traceability |

### Network & Identity Controls
- Private endpoints for model APIs; mutual TLS between components
- Separate network segments: training vs. inference
- Egress filtering — prevent exfiltration via model outputs or agent calls
- Managed identity/service principal > shared static API keys
- Just-in-time access + secrets vault for API keys/tokens

### OWASP Top 10 for LLM Applications (2025) — Know These
| Code | Risk |
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

**Common mistake:** confusing detective controls (logging, monitoring) with preventive controls (approval gates, retrieval ACLs, input filtering) — the exam tests whether you pick the control that stops the harmful action *before* it occurs, not after.
