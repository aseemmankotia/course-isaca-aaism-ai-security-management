# Answer Key — Practice Test 2

**Q1. Correct: D**

The Manage function covers prioritizing, responding to, and continuously monitoring AI risks, including allocating resources to treat residual risk throughout deployment and operation.

---

**Q2. Correct: A**

ISO/IEC 42001 defines requirements for an AI management system (AIMS) and is the standard organizations can be certified against by accredited third-party certification bodies.

---

**Q3. Correct: B**

The EU AI Act's Annex III explicitly classifies AI systems used in recruitment, including resume screening and candidate ranking, as high-risk, triggering obligations such as human oversight, conformity assessment, risk management, and technical documentation.

---

**Q4. Correct: B**

MITRE ATLAS is a knowledge base of adversary tactics, techniques, and case studies specifically targeting AI/ML systems, modeled on the structure of MITRE ATT&CK.

---

**Q5. Correct: C**

Proper decommissioning requires revoking access to eliminate shadow AI and attack surface, plus disposing of or retaining associated data in accordance with retention and legal hold requirements to avoid compliance violations or data leakage.

---

**Q6. Correct: B**

Immediate containment—disabling the compromised integration and rolling back to a known-good configuration—stops active data leakage first, consistent with containment-before-eradication IR principles applied to an AI-specific attack vector.

---

**Q7. Correct: D**

A federated governance structure balances enterprise consistency with business agility: the central council defines non-negotiable policy, risk tolerance, and metrics reporting, while operational implementation stays close to the business units that understand their own use cases. This is the recommended structure when speed and local context matter but consistent risk posture is required.

---

**Q8. Correct: D**

MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems) is structured like ATT&CK, cataloging real-world and demonstrated adversary tactics and techniques against ML systems, making it the correct input for adversarial threat modeling of a production ML system.

---

**Q9. Correct: D**

The EU AI Act explicitly prohibits AI systems used to infer emotions of natural persons in the workplace (and in education), except for narrow medical or safety purposes. No risk-tier mitigation, conformity assessment, or transparency notice can make this use case legal — it must not be deployed.

---

**Q10. Correct: C**

ISO/IEC 42001 extends beyond information security into the broader responsible-AI domain, requiring organizations to assess and manage the wider organizational, societal, and ethical impacts of AI systems (e.g., fairness, transparency, human oversight) as part of the AIMS — scope that ISO/IEC 27001 does not cover.

---

**Q11. Correct: B**

Proper decommissioning under AI asset lifecycle management requires preserving provenance/lineage records for audit and regulatory traceability, purging personal data no longer needed to satisfy data minimization requirements, and updating the central inventory so the organization retains an accurate, current record of all AI assets and their status.

---

**Q12. Correct: D**

The MANAGE function addresses allocating resources to identified risks on an ongoing basis, including responding to, recovering from, and communicating about AI incidents post-deployment — the operational risk-treatment activities that follow risk identification and measurement.

---

**Q13. Correct: C**

The EU AI Act requires providers of high-risk AI systems to retain automatically generated logs for a minimum period (at least six months, longer if other Union/national law or sector rules require it) before destruction, and AI asset lifecycle management practices require provenance metadata to persist in the inventory even after the model itself is retired, so the decommissioning trail remains auditable.

---

**Q14. Correct: A**

AI-specific incident response procedures require containment and evidence preservation of the poisoning source before remediation actions like rollback, so root-cause analysis, chain-of-custody, and any downstream regulatory notification obligations remain supportable.

---

**Q15. Correct: B**

AI risk assessment requires treating provenance gaps in training data as a distinct risk category from output-level controls; when provenance cannot be verified and legal/privacy exposure exists, the correct treatment is to obtain attestation and independently verify before accepting residual risk, especially given a hard deployment deadline.

---

**Q16. Correct: A**

AI risk assessment for adversarial threats must evaluate targeted, exploitable weaknesses (evasion at the decision boundary) rather than relying on aggregate performance metrics; a high overall accuracy figure can mask a systematically exploitable blind spot with significant financial impact — this is a core AAISM distinction between traditional model performance metrics and security-relevant robustness metrics.

---

**Q17. Correct: D**

Systematic input/output querying to reverse-engineer or clone a model's functionality is the defining pattern of model extraction (model theft), a technique explicitly cataloged in the MITRE ATLAS matrix under exfiltration/theft of ML artifacts via API abuse.

---

**Q18. Correct: A**

When a residual risk score exceeds the defined risk appetite threshold, governance requires formal treatment selection from the standard options (mitigate, transfer, avoid, or accept), with acceptance requiring explicit documented approval at an appropriate authority level — simply logging or ignoring the exceedance violates the risk management lifecycle.

---

**Q19. Correct: C**

For hosted/foundation-model vendors, the highest-priority security and privacy risk is unauthorized use of confidential inputs for further model training or retention beyond need, which can lead to data leakage into future model outputs served to other customers; an explicit data-usage and retention clause directly addresses this AI-specific supply-chain risk and is a core AAISM vendor-management concern.

---

**Q20. Correct: C**

Membership inference determines whether a specific data record was used in training by analyzing model confidence/output patterns on queries — a privacy attack. Evasion involves crafting inputs at inference time to cause misclassification without modifying the model — an integrity attack against the deployed model's decision boundary. This distinction is a core part of the AI threat taxonomy tested in AAISM.

---

**Q21. Correct: B**

Reconstructing a model's parameters or decision logic purely through repeated inference queries maps to the ATLAS technique 'Exfiltration via ML Inference API,' which falls under the Exfiltration tactic — the attacker is extracting the model's intellectual property (its learned behavior) without ever touching the underlying artifact.

---

**Q22. Correct: D**

AI-specific vendor due diligence requires explicit contractual terms addressing data usage for model training, retention limits, and audit rights — generic SaaS terms are insufficient because AI vendors have a unique additional risk vector (customer data leaking into future model weights). Without these terms, the risk must be treated (via contract negotiation) or the engagement rejected.

---

**Q23. Correct: B**

For an unverifiable, high-sensitivity model source, the correct treatment combines mitigation (provenance verification, integrity checks, and pre-deployment adversarial/bias testing) with the option to avoid entirely by choosing a provider with verifiable supply-chain assurances — this directly addresses the unverified provenance risk rather than sidestepping it.

---

**Q24. Correct: A**

When a measured risk metric exceeds the board-approved risk appetite threshold, governance requires either remediation to bring the metric within tolerance or a formal, documented exception approved by the appropriate risk-acceptance authority with compensating controls — this preserves the integrity of the risk appetite framework.

---

**Q25. Correct: D**

Manipulating conversational context across turns to bypass the system prompt's restrictions and exfiltrate embedded secrets is a jailbreak achieved through prompt injection — it directly targets the model's instruction-following behavior at inference time, not its training data or classification boundary.

---

**Q26. Correct: A**

Risk prioritization is driven by the combination of likelihood (internet exposure, known exploitable CVE), impact (regulated PII exposure, critical severity), and business context — not by the AI-specific nature of a finding alone. An internet-facing critical vulnerability on regulated data outranks a lower-traffic, moderate-severity internal finding and an unquantified supply-chain concern.

---

**Q27. Correct: A**

Undefined retention and default opt-in-to-training terms are unacceptable for processing PII under most risk appetites. The correct treatment addresses the root cause through contract negotiation (defined retention, no training use) and/or technical mitigation (de-identification before data leaves the trust boundary), reducing exposure rather than merely accepting or financially transferring it.

---

**Q28. Correct: B**

Risk prioritization must weigh asset criticality and threat likelihood/intent, not raw volume alone. Distributed, low-and-slow, boundary-mapping queries are a documented black-box extraction technique; the proportionate treatment combines behavioral detection and output-based mitigations (e.g., confidence rounding) that reduce information leakage without disrupting the business.

---

**Q29. Correct: A**

A broker/proxy issuing scoped, short-lived, per-task credentials enforces least privilege and segmentation at the identity/access layer, so even a successfully hijacked agent cannot reach systems outside its authorized task scope — this is the core secure-agentic-architecture control (tool/permission isolation).

---

**Q30. Correct: B**

Only immutable version-hashed lineage that maps dataset versions to specific training run/model IDs creates a verifiable, record-level traceability chain, which is required to determine which model versions were built from data that must later be removed or retrained.

---

**Q31. Correct: B**

Requiring a documented rationale forces clinicians to actively engage with each recommendation rather than passively approve it, and outcome-based auditing gives measurable evidence of whether oversight is genuine — this restores the substance of 'human oversight at critical decision points' rather than its mere appearance.

---

**Q32. Correct: A**

Continuous automated red-teaming tied to live telemetry detects new jailbreak patterns as they emerge in production, closing the gap left by a point-in-time pre-launch test — this is the intended continuous evaluation/monitoring control for deployed generative AI systems.

---

**Q33. Correct: D**

Shadow deployment scores real traffic to validate the new model's behavior but never surfaces its decisions to end users, giving the security team true real-world evaluation data with zero customer risk exposure.

---

**Q34. Correct: A**

Fairness constraints are performance-equity controls that target disparate outcomes across protected groups, whereas differential privacy is a data-protection technique that mathematically bounds how much any single training record can influence or be inferred from the model's output — the two address distinct risk categories.

---

**Q35. Correct: A**

Because the LLM's reasoning can be manipulated via prompt injection, security must be enforced at an external control point (the tool/API gateway) that authorizes each action independently of the model's own judgment, applying least-privilege regardless of what the model 'decides' to do.

---

**Q36. Correct: B**

Filtering by the user's entitlements at retrieval time ensures the model never receives unauthorized confidential content in its context window, addressing the root cause of the disclosure risk through proper data segmentation.

---

**Q37. Correct: C**

A more aggressive (lower) blocking threshold causes the classifier to flag more borderline content as violating, which increases false positives and unnecessarily blocks legitimate responses.

---

**Q38. Correct: A**

This is the accurate distinction: minimization is a scope/retention control limiting what data is collected and kept, while lineage is a traceability control documenting where data came from and how it was transformed across the AI lifecycle.

---

**Q39. Correct: C**

Gradual performance decline tied to organic changes in input data distribution is a classic concept/data drift scenario, which is specifically detected and diagnosed through ongoing performance and drift monitoring against a defined baseline.

---

**Q40. Correct: C**

Human-in-the-loop describes a control model where a qualified human must review and approve each individual AI-generated output before it is acted upon, matching the mandatory pre-execution review requirement described.

---

**Q41. Correct: D**

Prompt-level instructions are advisory, not enforced access control, and can be bypassed by prompt injection or retrieval quirks. Segmentation must occur structurally at the retrieval layer — separate indices per tenant or mandatory, non-bypassable metadata filters applied by the retrieval system itself — so the model architecturally cannot receive another tenant's chunks, regardless of prompt content.

---

**Q42. Correct: D**

Model extraction/inversion attacks are characterized by abnormal querying behavior — high volume, systematic boundary probing, or unusual input diversity from a single source. Detecting and throttling this behavior in real time through anomaly detection and rate/query limits is the direct operational control for this threat, and it acts during the active attack rather than after the fact.

---

**Q43. Correct: C**

The core control failure is architectural: irreversible, binding actions (executed contracts) were allowed to proceed autonomously with only after-the-fact logging, rather than requiring a human approval gate before execution. Human oversight at critical decision points means placing the checkpoint BEFORE high-impact or irreversible actions occur, not merely reviewing logs afterward — post-hoc audit cannot undo an already-signed contract.

---

**Q44. Correct: C**

The requirement is traceability and the ability to act on specific source records (identify and remove them from future training) — this is a data lineage/provenance problem. Only end-to-end lineage tracking that records the source, transformations, and dataset version tied to each training example enables the vendor to answer 'which records contributed to this model' and to exclude specific records going forward.

---

**Q45. Correct: C**

AI red-teaming for LLM/agentic systems must be continuous and lifecycle-based, not a one-time gate. New attack techniques (jailbreaks, prompt injections), model updates, and guardrail changes continuously alter the attack surface, so a point-in-time test cannot represent ongoing risk. Effective programs schedule recurring adversarial testing tied to model and guardrail updates, not a single pre-launch checkpoint treated as permanent sign-off.

---

