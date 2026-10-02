# Answer Key — Practice Test 1

**Q1. Correct: C**

The EU AI Act explicitly lists credit scoring/creditworthiness assessment of natural persons in Annex III as a high-risk use case, triggering obligations including conformity assessment, technical documentation, risk management systems, logging, and human oversight before and during deployment.

---

**Q2. Correct: C**

The Govern function of the NIST AI RMF is cross-cutting and foundational — it addresses culture, policies, roles, accountability, and processes for AI risk management across the organization, and is intended to be established before or alongside the other functions.

---

**Q3. Correct: D**

AAISM guidance emphasizes integrating AI-specific incident types (data poisoning, model drift/behavior anomalies, adversarial input attacks, model theft) into the existing enterprise incident response process through dedicated playbooks and escalation criteria, rather than building a parallel, siloed process.

---

**Q4. Correct: B**

AI asset and data lifecycle management requires tracking provenance (source and history of training data), model versioning, and lineage so security teams can assess exposure to poisoning, licensing/IP risk, drift, and support incident investigation and audit trails.

---

**Q5. Correct: A**

ISO/IEC 42001 is a voluntary management system standard for AI (AIMS) that shares a common structure with other ISO management system standards, including ISO/IEC 27001, and is designed to be integrated with an organization's existing ISMS rather than replace it.

---

**Q6. Correct: A**

Effective AI governance requires balancing technical, legal, security, business, and risk perspectives; a cross-functional committee with executive sponsorship ensures accountability, appropriate authority to approve/reject deployments, and alignment with organizational risk appetite.

---

**Q7. Correct: B**

The EU AI Act explicitly lists AI systems used to evaluate creditworthiness or credit scoring of natural persons as high-risk (Annex III), which requires providers/deployers to perform a conformity assessment and maintain a continuous risk management system covering the AI lifecycle.

---

**Q8. Correct: C**

The Govern function is the cross-cutting foundation of the NIST AI RMF, addressing policies, processes, accountability, and culture that enable the other three functions (Map, Measure, Manage) to operate effectively.

---

**Q9. Correct: B**

AI asset lifecycle governance requires that decommissioning preserve auditability — model artifacts, training data lineage, and provenance must be archived or disposed of per documented retention policy so the organization can respond to future audits, disputes, or incidents tied to the model's historical decisions.

---

**Q10. Correct: D**

MITRE ATLAS is a threat-intelligence knowledge base modeled on ATT&CK, cataloging real-world adversary tactics, techniques, and case studies against AI/ML systems, whereas the OWASP Top 10 for LLM Applications is a vulnerability-focused list highlighting the most critical risks (e.g., prompt injection, insecure output handling) specific to LLM application development.

---

**Q11. Correct: B**

Provenance tracking requires recording where training data came from and a verifiable model/version hash, allowing incident responders to determine exactly which data and code produced a given model version when investigating an AI security incident such as data poisoning or model tampering.

---

**Q12. Correct: A**

Risk acceptance is a business decision that must rest with a senior, accountable executive or governance body empowered to weigh business impact against risk — not with technical staff, a single security function, or a third-party vendor — ensuring accountability aligns with organizational authority and consequence ownership.

---

**Q13. Correct: D**

AI asset lifecycle management requires that decommissioning be a governed, documented process: secure disposal or anonymization of data and model artifacts per retention policy, revocation of access/credentials tied to the asset, and an updated inventory record so the organization retains an accurate, auditable picture of what AI assets exist and what happened to retired ones. This closes the lifecycle loop that governance frameworks (e.g., NIST AI RMF, ISO/IEC 42001) expect.

---

**Q14. Correct: C**

AI incidents such as data poisoning require AI-specific response actions that generic IT incident response does not cover: the ability to roll back to a validated model version, isolate or quarantine the compromised data source/pipeline, and revalidate the model before redeployment. This is a core expectation of AI-specific business continuity and incident response planning under the domain.

---

**Q15. Correct: A**

The appetite statement requires documented treatment for Medium+ risks. Mitigation via layered controls (input/output filtering, prompt hardening) directly reduces likelihood/impact of prompt injection to bring residual risk within tolerance, which is the standard treatment path an AI security manager applies before acceptance.

---

**Q16. Correct: B**

Model extraction (query-synthesis/model-stealing) involves systematically querying an exposed inference API to reconstruct model parameters or a functional surrogate, matching the MITRE ATLAS technique 'Exfiltration via ML Model Inference API' — a core mapped threat in AAISM threat-and-vulnerability content.

---

**Q17. Correct: B**

The data-usage/training-data clause directly governs whether confidential or regulated organizational data could leak into the vendor's shared model weights or be exposed to other tenants, making it the primary security-relevant term in AI vendor risk management per AAISM guidance on foundation-model provider evaluation.

---

**Q18. Correct: D**

The described architecture — automated nightly retraining on unvalidated, user-controllable feedback with no anomaly screening — creates a direct, low-effort attack surface for data poisoning, where adversaries can persistently and cumulatively corrupt the model's behavior. This is the most exploitable and highest-impact threat given the described control gap, so it should be prioritized first per AAISM threat-prioritization guidance.

---

**Q19. Correct: D**

AI systems behave probabilistically rather than deterministically, so a fixed pass/fail control test (common in traditional IT risk) is insufficient. AAISM guidance emphasizes tolerance bands (e.g., acceptable ranges for model drift, false-positive/negative rates, hallucination frequency) as the appropriate risk-appetite construct for AI, reflecting the statistical nature of model outputs.

---

**Q20. Correct: A**

An ML-BOM with cryptographically signed hashes of model weights and dataset components provides verifiable, tamper-evident provenance — confirming the exact artifacts used and detecting substitution or unauthorized modification, which is the assurance mechanism AAISM's AI supply-chain guidance calls for.

---

**Q21. Correct: C**

Compromising a model before it enters the organization's pipeline (via a public model hub) maps to the Initial Access tactic, specifically the 'ML Supply Chain Compromise' technique, which covers tainted pre-trained models, datasets, or ML libraries obtained from external sources.

---

**Q22. Correct: B**

When regulated PII is sent to a third-party foundation-model provider, the single highest-risk exposure is that the vendor could retain, log, or use that data to train future models, permanently embedding sensitive data into a shared model. A binding data-usage exclusion clause is the primary safeguard the security manager must obtain before onboarding.

---

**Q23. Correct: D**

Injecting malicious or mislabeled samples into the training data pipeline to intentionally skew the learned decision boundary is the definition of data poisoning, a training-time integrity attack.

---

**Q24. Correct: D**

When residual risk exceeds appetite but leadership consciously chooses to proceed without further reducing, transferring, or eliminating the risk, this is a formal risk acceptance decision, which should be documented with sign-off from an authorized risk owner.

---

**Q25. Correct: A**

Risk-based prioritization weighs likelihood and impact together. A known, actively exploitable critical CVE in production infrastructure has high likelihood (public exploit available) and severe impact (full system compromise), and requires no special access, making it the clear top priority over speculative or access-constrained threats.

---

**Q26. Correct: C**

For a high-risk use case like hiring, provenance and documentation (model cards, data lineage, known limitations) directly support the organization's ability to assess bias, explainability, and regulatory compliance obligations, which is the core purpose of AI vendor due diligence in this domain.

---

**Q27. Correct: C**

A binding contractual data-usage clause in the data processing addendum, paired with audit rights, is the only control that creates enforceable obligations on the vendor and verifiable evidence of compliance -- this is the core AI vendor/third-party risk management practice AAISM tests for foundation-model providers.

---

**Q28. Correct: A**

High-volume, systematically varied querying of a public inference endpoint to reverse-engineer model behavior matches the ATLAS technique for model extraction/theft via inference API exfiltration. The correct treatment targets the attack vector directly -- rate limiting, output perturbation, and query-pattern anomaly detection -- rather than controls aimed at a different threat category.

---

**Q29. Correct: D**

Retrieval-time access control filtering (retrieval-augmented generation authorization) ensures the model only ever receives documents the requesting user is authorized to see, eliminating the leakage path regardless of prompt content.

---

**Q30. Correct: C**

Least-privilege, scoped credentials per tool combined with human-in-the-loop approval for high-impact actions directly limits what a compromised or manipulated agent can do, which is the core mitigation for excessive agency in agentic AI systems.

---

**Q31. Correct: A**

An input guardrail/prompt-shield layer intercepts and inspects prompts before they reach the model, allowing detection and blocking of injection patterns pre-execution, which is the recommended defensive layer for this threat.

---

**Q32. Correct: B**

A risk-tiered oversight model routes higher-consequence decisions to human reviewers while allowing automation for low-risk cases, balancing efficiency with accountability at genuinely critical decision points, which is the AAISM-recommended approach to human oversight.

---

**Q33. Correct: C**

Red-teaming is a deliberate, time-bound adversarial exercise to surface weaknesses, whereas continuous monitoring is an always-on detective control observing live behavior for drift, abuse, and anomalies — they are complementary but distinct controls across the AI lifecycle.

---

**Q34. Correct: B**

Data lineage and documentation capture where training data came from, how it was transformed, and its demographic makeup, which is exactly what is needed to investigate disparate outcomes and satisfy regulatory transparency requirements around fairness.

---

**Q35. Correct: A**

Scoped least-privilege tool access combined with human-in-the-loop approval for high-risk actions directly limits the blast radius of excessive agency before harm occurs — this is the core guardrail pattern for autonomous agents.

---

**Q36. Correct: A**

Removing or tokenizing PII before it enters the fine-tuning pipeline is a foundational data management control that prevents the sensitive information from ever being available for the model to memorize.

---

**Q37. Correct: C**

Segmentation and isolation of model instances, data stores, and access boundaries per tenant is the core architectural control for preventing cross-tenant leakage in multi-tenant AI environments.

---

**Q38. Correct: B**

Integrating automated adversarial testing into CI/CD along with periodic manual red-teaming provides continuous, lifecycle-wide monitoring that keeps pace with model updates, drift, and evolving attack techniques.

---

**Q39. Correct: D**

Guardrails are real-time, preventive/constraining controls acting on live inference traffic, whereas evaluations are structured, often periodic assessments of model behavior, quality, and safety conducted before or after deployment.

---

**Q40. Correct: D**

Subgroup-level fairness monitoring with a human review trigger for flagged decisions is a proportionate control that addresses the identified disparity while keeping the system operational, consistent with human oversight at critical decision points.

---

**Q41. Correct: D**

Sandboxed execution with least-privilege, task-scoped credentials limits the blast radius of a compromised or manipulated agent, containing damage before it can propagate across systems — a core secure deployment pattern for agentic AI.

---

**Q42. Correct: B**

Removing or anonymizing sensitive data before it enters the training pipeline prevents the model from ever learning to reproduce that PII, addressing the root cause of memorization-based leakage rather than a downstream symptom.

---

**Q43. Correct: A**

For high-stakes, adverse decisions that materially affect individuals, effective human oversight requires a human-in-the-loop with meaningful review and override authority BEFORE the decision takes effect, not after.

---

**Q44. Correct: A**

Red-teaming simulates adversarial behavior specifically to surface security and safety weaknesses — jailbreaks, prompt injection, unsafe content generation — so they can be remediated prior to production exposure.

---

**Q45. Correct: C**

Ongoing, continuous monitoring of input/output distributions and safety metrics with automated deviation alerting is the control that detects drift and emerging unsafe behavior in near real time throughout the AI system's operational lifecycle.

---

