# Practice Test 1: AAISM Certification Exam Prep: AI Security Management

- **Questions:** 45
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-1.md`. Track results in `score-tracker.md`.

---

**Q1.** A financial services firm deploys an AI system in the EU that evaluates consumers' creditworthiness and determines loan eligibility. Under the EU AI Act, how should this AI system be classified, and what does that classification require?

A) Unacceptable risk — the system must be banned outright because it makes automated decisions about individuals
B) Minimal risk — no specific obligations apply beyond voluntary adherence to codes of conduct
C) High-risk — Annex III designates credit scoring/creditworthiness systems as high-risk, requiring conformity assessment, a risk management system, technical documentation, and human oversight
D) Limited risk — only a transparency notice disclosing AI use to the consumer is required

---

**Q2.** A CISO wants to first establish organizational culture, roles, accountability structures, and policies for managing AI risk before conducting detailed risk identification for specific AI systems. Which NIST AI Risk Management Framework function does this activity primarily belong to?

A) Manage
B) Map
C) Govern
D) Measure

---

**Q3.** During a model retraining cycle, a security team discovers that a portion of the training dataset was subtly manipulated by an external contributor, causing the model to misclassify a specific category of inputs. Which approach BEST supports organizational readiness to respond to this type of AI-specific incident?

A) Limit incident response scope to only availability incidents affecting the model's inference endpoints
B) Rely solely on the third-party AI vendor's incident response team, since the model was trained using vendor-supplied tooling
C) Stand up a wholly separate AI incident response function that operates independently of the enterprise security operations center
D) Extend the existing enterprise incident response plan with AI-specific playbooks covering data poisoning, model behavior anomalies, and adversarial inputs, with clear escalation criteria

---

**Q4.** A security program manager is designing the data fields to capture in the organization's AI asset inventory to support security risk assessment and audit readiness. Which element is MOST important to include?

A) The number of end users licensed to access the AI application
B) Training data provenance, model version, and lineage information
C) Marketing copy describing the model's business capabilities
D) The business unit's budget allocated to the AI project

---

**Q5.** How does ISO/IEC 42001 relate to ISO/IEC 27001 within an organization's AI security program?

A) ISO/IEC 42001 establishes an AI management system (AIMS) intended to be integrated with, not replace, an existing ISO/IEC 27001 information security management system (ISMS)
B) ISO/IEC 42001 is a legal requirement enforceable under the EU AI Act
C) ISO/IEC 42001 replaces ISO/IEC 27001 for any organization that deploys AI systems
D) ISO/IEC 42001 only applies to vendors that build AI models, not organizations that consume third-party AI services

---

**Q6.** An organization is forming a governance body to oversee decisions about AI risk acceptance, policy exceptions, and deployment approvals. Which committee composition BEST supports effective AI governance oversight?

A) Cross-functional membership including security, legal/compliance, data science, risk management, and business unit representatives, with executive sponsorship
B) A single AI Risk Officer with sole decision-making authority, reporting directly into IT operations
C) A committee composed solely of data scientists and ML engineers who build and train the models
D) Full delegation of all AI governance decisions to the organization's primary AI model vendor

---

**Q7.** A bank deploys an AI system that automatically scores consumer loan applications for creditworthiness, with the score directly determining approval or denial. Under the EU AI Act, how should this system be classified, and what is the PRIMARY governance obligation this classification triggers?

A) Limited-risk system requiring only a user-facing disclosure that AI is being used
B) High-risk system requiring a conformity assessment and an ongoing risk management system prior to and during deployment
C) Unacceptable-risk system that must be banned from use in financial services
D) Minimal-risk system with no additional obligations beyond existing banking regulation

---

**Q8.** Which function of the NIST AI Risk Management Framework is PRIMARILY focused on establishing organizational culture, policies, roles, and accountability structures for managing AI risk before systems are mapped or measured?

A) Measure
B) Map
C) Govern
D) Manage

---

**Q9.** An organization is decommissioning a legacy fraud-detection model that was trained on years of historical customer transaction data. Which action is MOST critical to include in the decommissioning procedure to satisfy AI asset and data lifecycle governance requirements?

A) Immediately delete all training data and model artifacts to reduce storage costs
B) Archive the model artifacts and document data provenance, lineage, and retention disposition in accordance with policy
C) Redeploy the model in a test environment indefinitely without further documentation
D) Notify only the IT infrastructure team that the server hosting the model can be reclaimed

---

**Q10.** Which statement BEST differentiates MITRE ATLAS from the OWASP Top 10 for Large Language Model Applications?

A) ATLAS is a regulatory compliance checklist, while OWASP Top 10 for LLM is a certification standard
B) ATLAS only applies to generative AI, while OWASP Top 10 for LLM applies to all machine learning systems
C) They are functionally identical frameworks published by the same organization for redundancy
D) ATLAS catalogs adversary tactics and techniques against AI systems in an ATT&CK-style knowledge base, while OWASP Top 10 for LLM identifies the most critical application-level vulnerability categories specific to LLM-based applications

---

**Q11.** An organization is building the AI model registry that forms the core of its AI asset inventory. Which field is REQUIRED in each registry entry to support incident response and provenance tracking as part of the AI security program?

A) The model's current accuracy score only
B) Training data lineage and model/version hash
C) The internal project codename only
D) The name of the cloud vendor hosting the model only

---

**Q12.** An organization has established a dedicated AI governance committee to oversee its AI security program. According to AI security program management best practice, who should hold ultimate accountability for accepting residual risk on a high-impact AI system?

A) A designated senior business risk owner accountable through the AI governance structure (e.g., committee chair or accountable executive)
B) The individual data scientist who built the model
C) The CISO alone, without business input
D) The cloud service provider hosting the AI infrastructure

---

**Q13.** A financial services firm is decommissioning a credit-scoring model that was trained on customer PII and is being replaced by a newer version. The AI security program requires a formal decommissioning procedure before the model is removed from production. Which action BEST satisfies this requirement?

A) Archive the model artifact and the full training dataset indefinitely in cold storage in case the model needs to be retrained later
B) Remove the model from the production inference servers only, leaving all copies of the training data in the data lake for future audits
C) Transfer the model and its training data to the original technology vendor for off-site storage without creating internal documentation
D) Follow the documented AI asset decommissioning procedure: securely delete or anonymize the model weights and training data per retention policy, revoke associated access and API keys, and update the AI asset inventory with the disposal date and justification

---

**Q14.** An organization's AI security program is updating its incident response plan to address AI-specific incidents. Post-deployment monitoring reveals that a production model's behavior has degraded because part of its training data was poisoned before deployment. Which element should the AI incident response plan include to address this AI-unique scenario, beyond standard IT incident response procedures?

A) A defined escalation path to the security operations center for triage
B) Standard patch management windows for underlying operating system updates
C) A defined procedure for rolling the model back to a validated last-known-good version and revoking or quarantining the compromised training data pipeline
D) Documented network segmentation zones separating the data center from the corporate network

---

**Q15.** An enterprise risk appetite statement states that risks rated 'Low' are accepted without additional controls, while risks rated 'Medium' or higher require documented treatment before go-live. A pre-deployment AI risk assessment rates a customer-facing LLM chatbot's exposure to prompt injection leading to sensitive data disclosure as 'Medium.' Which treatment approach BEST aligns with the stated risk appetite?

A) Mitigate the risk by implementing input sanitization, output filtering, and system-prompt hardening, then re-assess before launch
B) Accept the risk as-is since the chatbot only serves external customers and not internal systems
C) Transfer the risk entirely by purchasing a cyber-insurance rider covering AI incidents
D) Avoid the risk by canceling the chatbot project until a zero-risk architecture is found

---

**Q16.** During a security review, an attacker submits thousands of carefully varied queries to a deployed image-classification API and uses the returned confidence scores to reconstruct a functionally equivalent copy of the underlying proprietary model. Which adversarial technique does this describe?

A) Data poisoning
B) Model extraction
C) Evasion attack
D) Prompt injection

---

**Q17.** A security manager is negotiating a contract with a foundation-model provider that will host the organization's fine-tuning workloads. From a security-risk perspective, which contractual clause is MOST important to secure before onboarding?

A) A committed monthly service-level uptime percentage
B) An explicit data-usage clause specifying whether customer prompts and fine-tuning data will be used to further train the vendor's models
C) A guaranteed model-versioning and deprecation notice schedule
D) A tiered pricing structure based on token consumption volume

---

**Q18.** An organization operates a recommendation model that retrains nightly on unvalidated user click-feedback data with no anomaly screening or human review of the training set. The security team must prioritize which threat to address first. Which threat should receive the HIGHEST priority?

A) Model theft through unauthorized API scraping
B) Evasion of the model's output through adversarial perturbation of a single query
C) Prompt injection targeting the model's system instructions
D) Data poisoning via manipulated feedback signals injected by malicious users

---

**Q19.** According to AAISM guidance, what is the KEY distinction between defining risk appetite for AI systems versus for traditional deterministic IT systems?

A) AI risk appetite must always be set lower than traditional IT risk appetite regardless of use case
B) AI risk appetite requires no board-level approval since AI risk is purely technical
C) AI risk appetite is identical to traditional IT risk appetite since both are ultimately measured in financial loss terms
D) AI risk appetite must account for probabilistic, non-deterministic model behavior, meaning static pass/fail thresholds are often replaced with tolerance bands around output drift, confidence, and error rates

---

**Q20.** A security team wants cryptographic assurance of the lineage of a third-party open-source model and its training dataset before approving it for production use. Which artifact provides this assurance?

A) A machine learning bill of materials (ML-BOM) containing signed hashes of model weights and dataset components
B) The model card published by the model's authors
C) The vendor's publicly available README documentation
D) A general SOC 2 Type II report covering the vendor's cloud infrastructure

---

**Q21.** A bank's AI security team discovers that a third-party model hub hosting a pre-trained transformer used in their fraud-detection pipeline had a backdoor trigger embedded in the model weights before the bank downloaded and fine-tuned it. In the MITRE ATLAS framework, which tactic best describes this attack?

A) Defense Evasion
B) ML Attack Staging
C) Initial Access
D) Exfiltration

---

**Q22.** An AI security manager is finalizing a contract with a foundation-model API provider. The organization plans to submit regulated customer PII in prompts for a customer-service chatbot. Which contract clause is MOST critical to negotiate before signing?

A) A service-level agreement guaranteeing 99.9% API uptime
B) An explicit clause prohibiting the vendor from using submitted prompts and outputs to train or fine-tune their models
C) A right to audit the vendor's physical data center security controls annually
D) A discount clause tied to monthly API call volume

---

**Q23.** An organization's AI risk register lists a threat: 'Adversary submits crafted training examples through a public data-labeling crowdsourcing pipeline to bias the model's decision boundary.' Which specific vulnerability class does this threat exploit?

A) Model extraction
B) Prompt injection
C) Membership inference
D) Data poisoning

---

**Q24.** During AI risk treatment planning, a security leader determines that the residual risk of a customer-facing generative AI chatbot leaking proprietary system prompts through jailbreak attempts remains above the organization's defined risk appetite even after adding output filtering. Leadership decides to proceed anyway because the chatbot is core to the product launch timeline. Which risk treatment strategy has been applied?

A) Risk avoidance
B) Risk transfer
C) Risk mitigation
D) Risk acceptance

---

**Q25.** An AI security team is prioritizing remediation across several identified threats to a production LLM system: (1) a jailbreak technique that occasionally bypasses content filters, (2) a model-extraction risk via high-volume API querying, (3) an unpatched dependency in the inference server with a known critical CVE, and (4) a theoretical membership-inference risk requiring white-box model access the attacker does not have. Using a risk-based prioritization approach, which threat should receive the HIGHEST remediation priority?

A) The unpatched critical CVE in the inference server, because it has a known exploit, high likelihood, and severe potential impact with no attacker-access barrier
B) The theoretical membership-inference risk, because privacy violations carry the largest regulatory fines
C) The occasional jailbreak bypass, because generative AI content risks always outrank infrastructure risks
D) The model-extraction risk, because intellectual property loss is inherently worse than any infrastructure vulnerability

---

**Q26.** A company is evaluating two AI model vendors for a high-risk hiring-decision use case. Vendor A provides a signed model card with training data lineage, evaluation results, and known limitations, but offers no source data samples. Vendor B provides no documentation but allows full API access for internal testing. From an AI risk-management due-diligence perspective, which factor should carry the MOST weight in the vendor risk assessment?

A) Whether the vendor offers the lowest per-query API pricing
B) Whether the vendor's marketing materials claim state-of-the-art accuracy benchmarks
C) The availability of verifiable model documentation and data provenance artifacts that support accountability and bias evaluation
D) The speed of the vendor's customer support response time

---

**Q27.** An organization is evaluating a third-party foundation-model provider to process regulated customer data through a hosted inference API. The security team's primary concern is that submitted prompts and documents could be retained and used to fine-tune the vendor's future models. Which control BEST addresses this risk before onboarding the vendor?

A) Require the vendor to provide a SOC 2 Type II report and consider the review complete
B) Accept the vendor's published privacy policy as sufficient assurance of data-handling practices
C) Negotiate and execute a data processing addendum with an explicit contractual clause prohibiting use of submitted data for model training or fine-tuning, with audit rights to verify compliance
D) Require the vendor's staff to sign a mutual non-disclosure agreement covering the engagement

---

**Q28.** A security team notices a threat actor sending an unusually large volume of systematically varied queries to an organization's public-facing ML prediction API. Analysis suggests the actor is attempting to reconstruct a functionally equivalent copy of the proprietary model by observing its outputs. Which MITRE ATLAS-aligned classification and PRIMARY treatment are appropriate?

A) Classify as model extraction/theft via inference API querying; prioritize query rate limiting, output perturbation, and anomaly detection on query patterns
B) Classify as prompt injection; prioritize input sanitization and system-prompt hardening
C) Classify as data poisoning; prioritize retraining the model on a cleansed dataset
D) Classify as an evasion attack; prioritize adversarial training of the model

---

**Q29.** A company deploys a RAG-based chatbot that retrieves from multiple internal data sources with different sensitivity levels, including HR salary records and public product documentation. Employees without HR clearance report receiving salary data in chatbot answers. Which control BEST addresses this issue?

A) Increase the LLM's context window so it can better distinguish document types
B) Fine-tune the model to refuse any question containing the word 'salary'
C) Add API rate limiting to reduce the number of queries per user
D) Implement document-level access control filtering during retrieval so only authorized documents are passed to the model for a given user

---

**Q30.** An agentic AI assistant has been granted a single service account with broad administrative permissions across ticketing, email, and cloud infrastructure so it can complete multi-step tasks autonomously. The security team wants to reduce the blast radius if the agent is manipulated through prompt injection. Which control is MOST appropriate?

A) Increase the model's temperature setting so its behavior is less predictable to attackers
B) Move the agent to a fully air-gapped network with no external connectivity
C) Enforce least-privilege, per-tool scoped credentials for the agent, with human approval required before high-impact actions execute
D) Encrypt the agent's conversation logs at rest

---

**Q31.** Which control is MOST effective at detecting and blocking adversarial prompt injection attempts before they reach the underlying LLM in a production deployment?

A) An input guardrail layer that inspects and sanitizes incoming prompts prior to model invocation
B) Vector database encryption at rest
C) Model weight quantization to reduce inference latency
D) An output content filter applied only after the model generates its response

---

**Q32.** An AI system autonomously approves loan applications under $5,000 but organizational policy requires human review for higher-risk decisions. Which configuration best implements risk-tiered human oversight at critical decision points?

A) Disable human review entirely once model accuracy exceeds 95% on validation data
B) Route decisions above a defined risk/dollar threshold to mandatory human review, allowing autonomous approval below that threshold
C) Require human sign-off on every single decision regardless of amount
D) Trigger human review only after a customer files a complaint about a decision

---

**Q33.** Which statement correctly distinguishes AI red-teaming from continuous production monitoring as security controls?

A) Red-teaming and continuous monitoring are the same control, simply executed by different teams
B) Red-teaming applies only to training data, while monitoring applies only to model weights
C) Red-teaming is a point-in-time adversarial evaluation used to discover vulnerabilities before or periodically during deployment, while continuous monitoring provides ongoing detection of drift, misuse, and anomalies in live production traffic
D) Red-teaming is passive log collection, while continuous monitoring is active penetration testing of the model

---

**Q34.** A regulator requires an organization to explain why its hiring model denies certain demographic groups at a disproportionately higher rate and to show the provenance of the data used to train it. Which control should the organization have implemented to support this requirement?

A) Encryption of all model outputs before storage
B) Data lineage and documentation tracking data sources, transformations, and demographic composition throughout the pipeline
C) Increasing the number of parameters in the model to improve overall accuracy
D) API throttling to limit the number of external inference requests

---

**Q35.** A security architect is designing controls for an agentic AI system that can autonomously call external APIs to execute financial transactions. Which control BEST mitigates the risk of excessive agency leading to unauthorized high-value transactions?

A) Enforce scoped, least-privilege tool permissions with mandatory human approval for transactions above a defined risk threshold
B) Increase the context window size so the agent has more information before acting
C) Log all agent actions in a centralized SIEM for retrospective review only
D) Require the agent to explain its reasoning in natural language before each action

---

**Q36.** An organization is fine-tuning a large language model on internal customer support transcripts. Which control BEST reduces the risk of sensitive customer PII being memorized and later regurgitated by the model?

A) Apply data minimization and automated PII redaction/tokenization to the transcripts before they enter the fine-tuning pipeline
B) Increase the number of training epochs to improve model generalization
C) Restrict maximum model output length to reduce the chance of verbose leakage
D) Encrypt the training dataset at rest using AES-256

---

**Q37.** A managed AI service provider hosts fine-tuned models for multiple enterprise customers on shared infrastructure. Which architectural control BEST prevents cross-tenant data leakage between customer-specific models?

A) Apply API rate limiting per tenant
B) Use a single shared model with prompt-based tenant identifiers
C) Provision logically and physically segmented model instances and vector stores per tenant with strict IAM boundaries
D) Rely on output content filtering to strip other tenants' data

---

**Q38.** Which configuration BEST supports continuous security assurance for a production LLM-based application over its full lifecycle?

A) A one-time red team assessment performed before initial deployment
B) Automated adversarial testing and red-teaming integrated into the CI/CD pipeline, combined with periodic manual adversarial exercises post-deployment
C) Manual penetration testing conducted annually by an external vendor
D) Static code analysis of the application's backend service only

---

**Q39.** In AI security architecture, what is the PRIMARY distinction between a 'guardrail' and an 'evaluation' control?

A) Guardrails are applied only during model training, while evaluations are applied only during inference
B) Guardrails and evaluations are interchangeable terms for the same control type
C) Guardrails are a compliance-only requirement, while evaluations are a purely technical requirement
D) Guardrails run in real time to prevent or constrain harmful model behavior at inference, while evaluations assess model quality and safety through structured testing, typically before or periodically after deployment

---

**Q40.** An AI-powered loan approval system shows statistically significant disparate approval rates across demographic subgroups during production monitoring. Which control BEST addresses this finding while maintaining operational continuity?

A) Immediately decommission the model and revert to manual underwriting for all applications
B) Suppress the demographic subgroup fields from the monitoring dashboard to avoid raising further concerns
C) Retrain the model exclusively on synthetic data to eliminate historical bias
D) Implement subgroup-level fairness monitoring thresholds that trigger mandatory human review of flagged decisions before final approval

---

**Q41.** A company deploys an agentic AI system that can autonomously call internal APIs and execute code to complete multi-step tasks. Security leadership is concerned that a successful prompt injection could cause the agent to take destructive actions across multiple internal systems. Which architectural control BEST mitigates this risk?

A) Grant the agent a single service account with broad API access and enable verbose logging of all actions for later audit
B) Rely on the system prompt to instruct the agent never to perform destructive actions
C) Apply output content filtering only after the agent's actions have already been executed against downstream systems
D) Execute agent tool calls within an isolated, sandboxed execution environment using short-lived, least-privilege scoped credentials per task

---

**Q42.** An organization is building a training dataset for a customer service LLM that will ingest historical support tickets, some of which contain customer PII. Which control MOST directly reduces the risk of that PII being memorized and later leaked in the model's inference outputs?

A) Encrypting the training dataset at rest using AES-256
B) Applying data minimization and PII redaction/anonymization to the dataset before it is used for training
C) Rate limiting the number of API calls each end user can make to the deployed model
D) Restricting network access to the training environment using a private VPC

---

**Q43.** An AI system generates automated recommendations for loan approvals and denials. Per AI security management best practice for human oversight at critical decision points, which implementation is MOST appropriate for adverse actions such as a loan denial?

A) A qualified human reviewer must evaluate and approve the AI's recommendation before the denial is finalized, with authority to override it
B) The AI automatically issues the denial and a human reviewer audits a random sample of denials each quarter
C) A human reviewer is notified of the denial after it has been sent to the customer, for record-keeping purposes
D) The AI automatically approves or denies all loans without human involvement, since the model has passed accuracy validation

---

**Q44.** Before releasing a new generative AI model to production, the security team conducts structured adversarial red-teaming exercises. What is the PRIMARY purpose of this activity?

A) To proactively discover jailbreaks, prompt injection paths, and harmful output generation techniques before real attackers exploit them
B) To benchmark the model's response latency and token throughput under load
C) To validate the infrastructure's uptime against its service level agreement
D) To calculate the per-token inference cost for budgeting purposes

---

**Q45.** A generative AI chatbot has been running in production for several months. Which monitoring approach BEST detects degradation in model behavior, such as data drift or a gradual increase in unsafe outputs, over time?

A) A one-time evaluation performed before the model was deployed to production
B) A manual quarterly review of the application's source code repository
C) Continuous monitoring of input and output distributions and quality/safety metrics, with automated alerting on statistically significant deviations
D) Infrastructure monitoring limited to server CPU and memory utilization

---

