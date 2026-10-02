# Practice Test 2: AAISM Certification Exam Prep: AI Security Management

- **Questions:** 45
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-2.md`. Track results in `score-tracker.md`.

---

**Q1.** During a NIST AI RMF implementation, which function is primarily responsible for tracking, evaluating, and responding to AI risks on an ongoing basis after a system has been deployed into production?

A) Measure
B) Map
C) Govern
D) Manage

---

**Q2.** A financial services firm wants an independently auditable framework that can result in a formal, accredited certification of its AI management system, similar to how ISO/IEC 27001 certifies information security management systems. Which framework should the firm adopt to meet this specific need?

A) ISO/IEC 42001
B) MITRE ATLAS
C) NIST AI RMF
D) OWASP Top 10 for LLM Applications

---

**Q3.** Under the EU AI Act, an organization deploys an AI system to automatically screen and rank job applicants' resumes before human recruiters review them. Under which risk classification does this system fall, and what is the PRIMARY obligation that follows?

A) Limited risk; the provider must only disclose to candidates that AI is being used
B) High risk (Annex III employment use case); the deployer must ensure human oversight, conduct a conformity assessment, and maintain technical documentation
C) Unacceptable risk; the system must be banned outright
D) Minimal risk; no specific EU AI Act obligations apply

---

**Q4.** A security team wants to systematically catalog and communicate adversary tactics and techniques that specifically target machine learning systems (e.g., model evasion, data poisoning) using the same threat-modeling discipline applied to enterprise IT via ATT&CK. Which resource should the team incorporate into the AI security program?

A) ISO/IEC 23894
B) MITRE ATLAS
C) OWASP ASVS
D) NIST AI RMF

---

**Q5.** An organization is retiring a legacy fraud-detection model that has been replaced by a newer version. Per AI asset lifecycle management best practice, which action is MOST important to include in the decommissioning procedure?

A) Leave the model endpoint active but unmonitored in case it is needed again
B) Immediately delete all model documentation to reduce storage costs
C) Revoke all API keys and access credentials tied to the model, and dispose of or retain training data and logs per the organization's data retention and legal hold policy
D) Transfer ownership of the model to the IT helpdesk team for archival

---

**Q6.** During an active incident, a customer-facing LLM chatbot is discovered to be leaking internal system prompts and confidential data due to a successful prompt injection attack via a connected plugin. Which action should the AI incident response plan direct the team to take FIRST?

A) Conduct a full root-cause analysis and publish a public post-mortem before taking any containment action
B) Disable the compromised plugin/tool integration and, if needed, roll the chatbot back to the last known-good model or configuration to contain the leakage
C) Retrain the model from scratch with updated safety filters before resuming service
D) Notify the data protection regulator within the statutory breach notification window

---

**Q7.** A multinational conglomerate operates twelve business units, each independently building and deploying machine learning models for local use cases (fraud scoring, demand forecasting, chatbots). The CISO wants a consistent AI security baseline enforced enterprise-wide but must preserve each unit's ability to move quickly on AI initiatives without waiting for central approval on every project. Which governance model BEST meets these requirements?

A) A centralized model where a single enterprise AI security team must review and approve every AI system before any business unit can deploy it
B) A decentralized model with no enterprise-level policy, allowing each business unit's risk owner to define and enforce its own AI security requirements
C) An outsourced model where a third-party managed security provider assumes full accountability for AI risk decisions across all business units
D) A federated model in which a central AI governance council sets mandatory security policy, risk thresholds, and reporting requirements, while business units implement and operate controls locally within that framework

---

**Q8.** A security team is building a threat model for an internally deployed ML-based fraud detection engine. They want a structured, publicly maintained knowledge base of adversary tactics and techniques specifically observed or demonstrated against production machine learning systems (e.g., model extraction, evasion, data poisoning), analogous in structure to a well-known enterprise threat matrix. Which resource should they use as the primary input?

A) NIST AI Risk Management Framework
B) ISO/IEC 42001
C) OWASP Top 10 for LLM Applications
D) MITRE ATLAS

---

**Q9.** An HR technology vendor plans to deploy an AI system that analyzes employee facial expressions and vocal tone during performance review meetings to infer emotional state, with results factored into manager coaching recommendations. There is no safety or medical justification for the use case. Under the EU AI Act, how should the AI governance program classify and handle this system?

A) Classify it as high-risk and proceed after completing a conformity assessment and registering it in the EU database
B) Classify it as limited-risk and satisfy obligations through a transparency notice informing employees the system is AI-driven
C) Classify it as minimal-risk since it only supports internal coaching decisions and impose no additional obligations
D) Recognize it as a prohibited AI practice under the EU AI Act and do not deploy it, regardless of proposed mitigations

---

**Q10.** An organization already certified to ISO/IEC 27001 is now scoping an ISO/IEC 42001 implementation for its AI Management System (AIMS). Which requirement is unique to ISO/IEC 42001 and NOT addressed by the existing ISO/IEC 27001 information security management system?

A) Mandatory annual penetration testing of all production systems
B) Encrypting all training data at rest and in transit
C) Establishing an AI Management System that includes AI impact assessments addressing organizational, societal, and ethical impacts of AI systems, beyond information security scope
D) Requiring an external third-party certification audit

---

**Q11.** A production fraud-detection model is being retired and replaced by a newer version. Per the organization's AI asset and data lifecycle management procedures, which action sequence BEST represents proper decommissioning?

A) Immediately delete all model artifacts and training data lineage records to reduce storage costs
B) Archive the model artifacts, retain provenance and lineage documentation per the records retention schedule, securely purge any residual personal data copies, and update the AI system inventory to reflect decommissioned status
C) Leave the retired model running in production as an undocumented fallback indefinitely in case the replacement fails
D) Transfer ownership of the model to the requesting business unit without updating the central AI inventory

---

**Q12.** An organization has an AI system in production and needs to establish continuous monitoring for model drift, along with a defined process for responding to and recovering from AI-specific incidents once detected. Under the NIST AI Risk Management Framework, which core function primarily covers these ongoing, post-deployment monitoring and incident-response activities?

A) GOVERN
B) MAP
C) MEASURE
D) MANAGE

---

**Q13.** A security leader is decommissioning a high-risk AI credit-scoring model that falls under the EU AI Act. To reduce the organization's data breach exposure, the CISO proposes immediately purging all system logs, training data, and model artifacts as soon as the model is taken out of production. Which approach BEST aligns with AI asset lifecycle management requirements and applicable regulatory obligations?

A) Transfer all model artifacts and logs to the Data Protection Officer and close out the decommissioning ticket, since regulatory retention obligations fall under privacy law rather than the AI asset inventory process
B) Retain all logs, training data, and model artifacts indefinitely in cold storage to support any future litigation, overriding the organization's standard data retention schedule
C) Retain automatically generated logs for at least six months (or longer if required by sector-specific record-keeping rules), securely destroy artifacts per the data retention policy once the period lapses, and preserve provenance metadata in the AI asset inventory to document the model's full lifecycle
D) Purge all logs, training data, and model artifacts immediately upon decommissioning to minimize residual attack surface and storage cost

---

**Q14.** A drift-monitoring alert flags anomalous output shifts in a production fraud-detection model over the past 72 hours. Forensic review finds adversarially crafted samples inside the retraining pipeline, indicating likely data poisoning. Per an AI-specific incident response runbook, what should the security leader do FIRST, before rolling back to the previous model version?

A) Isolate and quarantine the affected training data pipeline, and preserve forensic evidence (data snapshots, ingestion logs, feature-pipeline state) to support root-cause analysis and any subsequent regulatory notification, before executing the rollback
B) Delete the poisoned training dataset immediately to prevent it from contaminating any future retraining run
C) Roll back to the last known-good model version immediately to restore business operations, then investigate the poisoning afterward
D) Notify the relevant AI Act market surveillance authority immediately, since a fraud-detection model could qualify as high-risk, before completing internal impact analysis

---

**Q15.** A security manager is assessing risk for a computer-vision model licensed from a third-party vendor. The vendor discloses that the training dataset was aggregated from multiple public web scrapes with no documented chain of custody, and the vendor cannot confirm whether copyrighted or PII-containing images were filtered out. The model is scheduled for deployment in a public-facing product within 30 days. Using AI risk assessment principles, which action should the security manager prioritize BEFORE deployment?

A) Proceed with deployment since output filtering at inference time compensates for any upstream data quality issues
B) Require the vendor to provide a data provenance attestation and conduct an independent bias/PII leakage evaluation, treating the unresolved provenance gap as an unacceptable risk pending mitigation
C) Accept the risk because the vendor's contract includes a standard indemnification clause for IP infringement
D) Delay only the marketing launch while allowing internal beta testing to continue unrestricted, since beta users are not the general public

---

**Q16.** A bank's AI-based transaction fraud detection model has a documented false-negative rate that fraud rings have begun exploiting by structuring transactions just below the model's decision threshold — a classic evasion technique. The security team's risk register currently rates this threat as 'Low' because the model's overall accuracy remains above 98%. From an AI risk management perspective, what is the MOST significant flaw in this rating?

A) The rating incorrectly relies on aggregate accuracy rather than assessing adversarial robustness and targeted exploitation impact, which can be severe even when overall accuracy is high
B) The rating should be increased solely because evasion attacks are always classified as Critical severity regardless of context
C) The rating is appropriate because a 98% accuracy rate exceeds most industry benchmarks for fraud detection models
D) The rating cannot be assessed until the model is retrained, since risk scoring is only valid immediately after training

---

**Q17.** An attacker sends carefully crafted queries to a publicly exposed model-inference API, systematically varying inputs and recording outputs to reconstruct a functionally equivalent copy of the proprietary model without ever accessing the underlying weights or infrastructure. Which MITRE ATLAS-aligned threat category does this technique represent?

A) Data poisoning during the training pipeline
B) Prompt injection targeting the system instructions
C) Supply chain compromise of a third-party dependency
D) Model extraction (model theft via query-based reconstruction)

---

**Q18.** During a quarterly AI risk review, a residual risk score of 18 (on a 1–25 scale, where likelihood and impact are each rated 1–5) is calculated for an AI supply-chain compromise scenario involving a compromised open-source model repository used in the organization's ML pipeline. The organization's documented AI risk appetite threshold is 12. According to AI risk treatment principles, what is the CORRECT next step?

A) Since the residual score exceeds appetite, select and implement a formal treatment option (mitigate, transfer, avoid, or accept with documented executive sign-off) and re-score after treatment
B) Log the finding for informational purposes only, since supply-chain risks are inherently unmanageable and excluded from formal treatment
C) Automatically accept the risk because open-source components are cost-effective and widely used industry-wide
D) Reduce the impact rating to bring the score below threshold so no further action is required

---

**Q19.** A security manager is negotiating a contract with a hosted foundation-model provider that will process the organization's confidential customer data through its API for a customer-service chatbot. The vendor's standard terms are silent on whether customer inputs may be used to further train or fine-tune the provider's models. From an AI vendor risk management standpoint, which contractual requirement is MOST critical to add before signing?

A) A right-to-audit clause allowing annual on-site inspection of the vendor's data centers
B) A most-favored-customer pricing clause ensuring the organization receives the vendor's lowest published rate
C) An explicit data-usage and retention clause guaranteeing customer inputs are not used for model training and specifying retention/deletion timelines
D) A service-level agreement guaranteeing 99.99% API uptime

---

**Q20.** During threat modeling for a deployed recommendation model, an analyst distinguishes between two attack techniques: one where an adversary queries the model repeatedly to determine whether a specific individual's record was part of the training dataset, and another where an adversary manipulates input features at inference time to force a misclassification without altering the model itself. Which pairing correctly labels these two techniques?

A) First is a data poisoning attack; second is a model extraction attack
B) First is an evasion attack; second is a membership inference attack
C) First is a membership inference attack; second is an evasion attack
D) First is a model inversion attack; second is a data poisoning attack

---

**Q21.** An AI security team discovers that a competitor appears to have replicated the exact decision boundaries of the organization's proprietary fraud-detection model after months of automated, low-and-slow queries against the public-facing inference API. No credentials were compromised and the model weights were never accessed directly. Which MITRE ATLAS tactic best characterizes this activity?

A) Collection
B) Exfiltration
C) ML Attack Staging
D) Impact

---

**Q22.** A CISO is evaluating whether to approve use of a third-party foundation model API for processing regulated customer PII. The vendor's contract states model outputs may be logged 'for service improvement purposes' with no explicit retention limit or opt-out clause, and the vendor refuses to disclose whether customer data is used in future model training. Per AAISM vendor risk management guidance, what is the MOST appropriate next action before approval?

A) Approve use but require the business unit to redact PII manually before every API call
B) Accept the risk since foundation model providers rarely disclose training data practices industry-wide
C) Proceed with a signed data processing addendum template used for traditional SaaS vendors without modification
D) Require contractual amendment specifying data retention limits, training-data exclusion, and audit rights, or reject the vendor

---

**Q23.** An organization downloads open-source pre-trained model weights from a public model hub to fine-tune for an internal HR screening tool. Security cannot verify the original training data or confirm the weights haven't been tampered with post-publication. Which risk treatment is MOST appropriate given the sensitivity of the HR use case?

A) Accept the risk since open-source models are community-vetted and inherently trustworthy
B) Mitigate by validating model provenance via signed checksums/attestation and running adversarial and bias evaluation before deployment, or avoid by sourcing from a vendor offering verifiable provenance
C) Transfer the risk by purchasing cyber insurance covering model integrity failures
D) Deploy immediately behind a WAF, since network-layer controls address model supply-chain risk

---

**Q24.** An enterprise's AI risk register lists a customer-facing LLM chatbot with a documented hallucination rate of 4% on regulated financial advice queries. The organization's approved risk appetite statement caps acceptable erroneous-output rate at 1% for any customer-facing financial guidance system. Per AAISM risk threshold management principles, what should occur BEFORE this chatbot goes into production?

A) The 4% rate must be reduced to within the 1% threshold, or a formal risk exception must be obtained from the designated risk-acceptance authority with compensating controls documented
B) Deploy with a disclaimer banner stating outputs are not financial advice, satisfying the appetite requirement
C) Increase the risk appetite threshold to 5% since LLMs inherently hallucinate more than deterministic systems
D) Proceed to production and monitor the hallucination rate post-launch, adjusting appetite retroactively based on observed data

---

**Q25.** During a red-team exercise against a production LLM-based customer support agent, testers craft a multi-turn conversation that gradually convinces the model to ignore its system prompt and reveal internal API keys embedded in its context window. This is best classified as which type of AI-specific attack for risk-treatment prioritization purposes?

A) Model extraction
B) Data poisoning
C) Evasion attack
D) Jailbreak / prompt injection leading to sensitive data disclosure

---

**Q26.** An AI risk manager is prioritizing remediation across three findings: (1) a supply-chain risk from an unverified third-party training dataset, (2) a moderate-severity prompt injection vulnerability in a low-traffic internal tool, and (3) an unpatched model-serving container with a known critical CVE exposed to the internet and processing regulated PII. Applying standard AI risk prioritization principles, which should be remediated FIRST?

A) The internet-exposed container with a critical CVE processing regulated PII, based on combined likelihood, exposure, and impact
B) The training dataset issue, since data poisoning is always the highest-impact AI-specific risk
C) The internal prompt injection finding, since prompt injection is the top-ranked risk in the OWASP LLM Top 10
D) All three should be remediated simultaneously regardless of resource constraints to avoid any residual risk

---

**Q27.** A company plans to use a third-party hosted foundation-model API to process prompts containing sensitive customer PII. The vendor's contract states data 'may be used to improve services' unless the customer opts out via a support ticket, and retention is described only as 'as needed for safety and abuse monitoring,' with no defined maximum period. As part of AI vendor and third-party risk management, which is the BEST risk treatment decision before production use?

A) Require a contractual amendment specifying zero training-data use and a defined, bounded retention period before submitting PII, or apply de-identification/pseudonymization controls prior to submission
B) Accept the risk since an opt-out mechanism exists, and proceed with production deployment
C) Transfer the risk by purchasing cyber insurance that covers data privacy breaches caused by vendor mishandling
D) Mitigate the risk by scheduling API calls only during off-peak hours to reduce the number of monitoring staff with potential data access

---

**Q28.** Security telemetry shows an external consumer of your organization's fraud-detection model API submitting highly diverse, systematically varied queries designed to map decision boundaries, at low volume per source IP but distributed across many rotating IP addresses over several weeks — consistent with MITRE ATLAS reconnaissance and model-extraction techniques. Given limited security resources, which is the BEST prioritization and treatment decision?

A) Deprioritize the activity since per-IP request volume stays below existing DDoS thresholds; revisit only if volume increases
B) Prioritize as high given the model's business criticality and evidence of coordinated extraction reconnaissance; treat via behavioral-fingerprint rate limiting, output rounding/perturbation, and anomaly detection tuned to query pattern rather than raw volume
C) Prioritize as low risk because model extraction requires white-box access to the model internals, and this activity is API-only black-box access
D) Immediately take the fraud-detection model offline and rebuild it from scratch, since the model must be considered unrecoverable once extraction reconnaissance is detected

---

**Q29.** A company deploys an autonomous AI agent with access to internal HR, finance, and ticketing APIs to complete multi-step tasks on behalf of employees. Security is concerned that a prompt injection embedded in an incoming ticket could hijack the agent into exfiltrating finance data. Which architecture BEST minimizes the blast radius of such an attack?

A) Use a broker/proxy pattern that issues short-lived, per-task scoped tokens with explicit allow-lists per API, so the agent never holds a persistent broad credential
B) Give the agent a single service account with full read access across all three APIs and rely on request-level audit logging
C) Wrap every API call the agent makes in a try/except block with rate limiting to slow down any exfiltration attempt
D) Fine-tune the LLM on internal data-handling policy so it 'knows' not to access finance data without authorization

---

**Q30.** A security architect is designing the training pipeline for an LLM fine-tuned on customer support tickets containing PII. The organization must later be able to prove exactly which dataset version and which records were used to produce a specific deployed model version, in order to honor data subject deletion requests. Which control provides this capability?

A) Regular-expression-based PII scrubbing applied to the raw tickets before training begins
B) Data lineage tracking that links immutable, hashed dataset version identifiers to specific model training run IDs
C) Encrypting the training dataset at rest using customer-managed encryption keys
D) Requiring data stewards to formally re-approve the training dataset's use on a quarterly basis

---

**Q31.** A healthcare AI system generates draft treatment recommendations and, as a safety control, requires clinician sign-off before any recommendation reaches the patient record. An audit discovers clinicians are approving 98% of recommendations within seconds, effectively rubber-stamping the AI's output and negating the intended human oversight. What is the MOST effective corrective control?

A) Raise the model's confidence threshold so fewer recommendations are routed for clinician review
B) Require a documented clinical rationale field for each sign-off and periodically audit sign-off decisions against actual patient outcomes
C) Send clinicians an automated reminder email emphasizing the importance of careful review
D) Remove the human sign-off step entirely, since it is not meaningfully changing outcomes

---

**Q32.** An AI security team knows their pre-launch red team exercise on a customer-facing chatbot will not catch jailbreak techniques that emerge after deployment. Which control BEST addresses this ongoing, evolving risk once the chatbot is in production?

A) Implement a continuous automated adversarial testing pipeline integrated with production prompt/response telemetry and monitoring
B) Repeat a full manual penetration test of the chatbot once per year
C) Perform a static code review of the chatbot's application and API layer
D) Increase the model's decoding temperature so its outputs become less predictable

---

**Q33.** Before fully replacing a production LLM-based fraud-detection classifier with a newer fine-tuned version, the security team wants to evaluate the new model's real-world safety and accuracy against live traffic while ensuring zero customers are exposed to any risk from the new model's decisions. Which deployment pattern BEST achieves this?

A) Blue-green deployment with an immediate full cutover to the new model
B) Canary release exposing 5% of live customers to decisions made by the new model
C) A/B testing that splits live traffic 50/50 between the old and new models
D) Shadow deployment in which the new model scores live traffic in parallel, with its outputs logged and compared but never acted upon

---

**Q34.** Which statement BEST distinguishes a 'fairness constraint' control from a 'differential privacy' control in an AI system?

A) Fairness constraints aim to ensure equitable model performance/outcomes across protected groups, while differential privacy adds calibrated noise to limit the ability to identify or infer influence of individual training records
B) Fairness constraints protect individual training records from being identified in model outputs, while differential privacy ensures equitable outcomes across demographic groups
C) The two controls serve identical purposes and can be used interchangeably to satisfy a regulatory audit requirement covering either bias or privacy
D) Fairness constraints can only be applied at inference time, while differential privacy can only be applied to improve model explainability

---

**Q35.** An organization deploys an agentic AI system with tool-calling capabilities (code execution, API invocation, file access) inside a customer service workflow. The security team discovers that documents retrieved by the agent contain injected instructions that caused the agent to invoke unauthorized administrative APIs. Which architectural control BEST addresses this risk?

A) Enforce least-privilege, per-action authorization checks at the tool/API gateway layer, independent of the LLM's own decision-making
B) Add stricter system prompt instructions directing the agent to ignore instructions embedded in retrieved content
C) Increase the model's temperature setting to reduce susceptibility to injected instructions
D) Fine-tune the model on additional customer service examples to improve robustness against injection

---

**Q36.** A financial services firm deploys a retrieval-augmented generation (RAG) chatbot that queries a shared document repository containing both public marketing content and confidential client records. Employees using the chatbot have varying data access entitlements. Which control BEST prevents unauthorized disclosure of confidential data through the chatbot?

A) Rely on the LLM's system prompt to instruct it not to reveal confidential content to unauthorized users
B) Enforce document-level access control at retrieval time so only documents the querying user is entitled to view are returned to the LLM
C) Apply output content filtering after generation to redact strings matching confidential data patterns
D) Restrict the RAG system to index only publicly available documents

---

**Q37.** An AI security team configures a toxicity classifier as an output guardrail for a public-facing generative AI application. Setting the classifier's blocking threshold to be more aggressive (lower score required to trigger a block) produces which documented operational effect?

A) Increased false negative rate, allowing more toxic content to pass through undetected
B) Reduced model inference latency due to fewer tokens being generated
C) Increased false positive rate, causing excessive blocking of legitimate benign responses and degrading user experience
D) Elevated risk of training data leakage through the guardrail's own logs

---

**Q38.** In AI security governance, which statement correctly distinguishes data minimization from data lineage as data management controls?

A) Data minimization limits the volume, sensitivity, and retention period of data collected and used for AI purposes, while data lineage tracks the origin, movement, and transformation of data throughout the AI lifecycle
B) Data minimization tracks the origin and transformation history of data used to train a model, while data lineage limits the volume and sensitivity of data collected and retained
C) Data minimization and data lineage are interchangeable terms, both referring to encrypting data at rest and in transit
D) Data minimization applies only to inference-time data, while data lineage applies only to training-time data

---

**Q39.** A production fraud-detection model's precision has gradually declined over three months, coinciding with organic shifts in legitimate customer transaction behavior rather than any observed attack activity. Which AI security monitoring practice is BEST suited to detect and diagnose this issue?

A) Adversarial robustness testing using crafted evasion samples
B) Red-team penetration testing of the model's API endpoints
C) Model performance and data drift monitoring comparing live input/output distributions against a baseline
D) Static code analysis of the model training pipeline scripts

---

**Q40.** A healthcare organization deploys an AI system that generates treatment plan recommendations. A regulatory requirement mandates that no AI-generated recommendation may be automatically executed without a qualified clinician reviewing and approving it beforehand. Which human oversight model does this requirement describe?

A) Human-out-of-the-loop
B) Human-on-the-loop
C) Human-in-the-loop
D) Human-in-command

---

**Q41.** A multi-tenant SaaS provider offers a RAG-based assistant where each customer's proprietary documents are embedded into a shared vector store. During testing, a red team demonstrates that carefully crafted queries from one tenant occasionally retrieve embedding chunks belonging to another tenant, even though the system prompt explicitly instructs the model to 'only use context belonging to the requesting tenant.' Which architectural control BEST eliminates this cross-tenant leakage?

A) Strengthen the system prompt with additional emphasis and few-shot examples reinforcing tenant boundaries
B) Add a post-generation output filter that scans responses for another tenant's document identifiers before returning them
C) Encrypt all embeddings with a single shared key so no tenant can decrypt another tenant's vectors without the model's help
D) Enforce tenant isolation at the retrieval layer using per-tenant vector indices or hard metadata-filtered queries that are applied before results ever reach the model

---

**Q42.** A financial services firm exposes a proprietary fraud-scoring model via an API. Security monitoring detects a client account issuing an unusually high volume of queries with systematically varied, boundary-probing inputs over several weeks, consistent with an attempt to reconstruct the model's decision logic. Which control is MOST effective for detecting and mitigating this specific threat?

A) Apply differential privacy noise to the training data before the next model retraining cycle
B) Rely on the model's existing input validation to reject malformed requests
C) Increase the model's confidence threshold so only high-confidence predictions are returned to any caller
D) Deploy query-pattern anomaly detection with rate limiting and per-account query budgets that flag statistically unusual query diversity or volume indicative of model extraction

---

**Q43.** An organization deploys an autonomous agentic AI system authorized to negotiate and finalize vendor contracts up to $50,000 without further approval, and to escalate anything above that threshold. Logging captures every agent action, including completed contract submissions, for audit review the following business day. During an incident review, the security team determines the agent committed the organization to an erroneous $48,000 contract due to a manipulated data feed. Which control gap MOST directly enabled this outcome?

A) The audit logs did not capture enough metadata about the agent's decision-making process
B) The organization failed to apply differential privacy to the data feed used by the agent
C) There was no human-in-the-loop checkpoint requiring review and approval before the agent executed an irreversible, financially binding action, even one under the escalation threshold
D) The dollar threshold for escalation was set too high and should have been lowered to $10,000

---

**Q44.** A healthcare AI vendor is training a diagnostic model on data aggregated from twelve hospital systems. A new regulation requires the vendor to be able to identify, upon request, which specific source records contributed to any given model version and to remove a patient's data from future training runs. Which control BEST satisfies this requirement?

A) Encrypt all training data at rest using hospital-specific keys managed by each contributing hospital
B) Apply k-anonymity generalization to all records before ingestion into the training pipeline
C) Implement end-to-end data lineage and provenance tracking that links every training example to its originating source and dataset version across the pipeline
D) Apply differential privacy during training so individual records cannot be distinguished in the resulting model

---

**Q45.** A security leader is designing the AI red-teaming program for a customer-facing LLM chatbot that is updated with new guardrails monthly. One team member proposes running a single comprehensive adversarial test suite two weeks before the initial production launch and treating a passing result as sufficient sign-off for the program's lifetime. Which weakness in this approach is MOST significant from an AI security management perspective?

A) Adversarial testing performed by internal staff is inherently less rigorous than testing performed by any external vendor
B) The test suite should have focused exclusively on measuring model accuracy rather than security-relevant behaviors
C) A single pre-launch test suite cannot account for new jailbreak techniques and prompt injection methods that emerge after launch or that surface as guardrails and the model itself change over time
D) Pre-launch testing is unnecessary if the model provider has already published safety benchmark results for the base model

---

