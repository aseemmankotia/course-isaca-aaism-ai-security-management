## Chapter 8: Data Management, Privacy, Ethics, and Human-Oversight Controls — Practice Questions

**Q1.** A bank deploys an AI credit-scoring system classified as high-risk under the EU AI Act. Which control BEST satisfies the Article 14 human oversight requirement?

A) A human reviewer with the authority to review, override, or halt a decision before it takes effect on the applicant
B) A quarterly bias audit performed by an external firm after decisions are issued
C) A disclaimer on the loan application informing applicants that AI was used in scoring
D) Automated logging of every model inference for later compliance review

<details>
<summary>Answer</summary>

**Correct: A**

Article 14 requires that natural persons be able to understand, monitor, and intervene in or stop the system's operation before an adverse outcome is finalized — oversight must be preventive, not retrospective.

**Why the others are wrong:**
- A post-hoc audit does not allow intervention before harm occurs — it is detective, not preventive oversight
- Disclosure satisfies transparency obligations, not the oversight requirement to intervene
- Logging supports traceability but provides no human authority to stop or change the decision

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** After fine-tuning an LLM on customer support tickets containing PII, testers discover they can extract verbatim customer records using specific prompt patterns. What is this failure an example of?

A) Bias amplification from an imbalanced fine-tuning dataset
B) Concept drift caused by distribution shift in production traffic
C) Training data leakage via model memorization
D) Data poisoning introduced by a malicious fine-tuning contributor

<details>
<summary>Answer</summary>

**Correct: C**

The model memorized specific training examples and reproduces them verbatim under targeted prompting — a classic training data extraction/leakage vulnerability from fine-tuning on sensitive data.

**Why the others are wrong:**
- Bias amplification produces skewed outputs across groups, not verbatim data recall
- Drift describes performance degradation over time due to changing inputs, not extraction of memorized records
- Poisoning corrupts training data to manipulate future outputs, not to enable retrieval of legitimate records

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An AI hiring tool selects 55% of qualified female applicants and 80% of qualified male applicants for interviews. Applying the four-fifths (80%) adverse impact rule, what should the AISM conclude?

A) No adverse impact exists because both rates exceed 50%
B) Adverse impact cannot be assessed without knowing the applicants' final hire outcomes
C) The four-fifths rule does not apply to AI-driven hiring systems
D) Adverse impact is indicated because the selection ratio (55/80 = 0.6875) falls below 0.80

<details>
<summary>Answer</summary>

**Correct: D**

The four-fifths (80%) rule from the EEOC Uniform Guidelines flags adverse impact when a protected group's selection rate is less than 80% of the highest-performing group's rate; 0.6875 is below that threshold.

**Why the others are wrong:**
- Comparing to 50% is irrelevant — the rule compares group ratios, not absolute rates
- The rule is applied at the selection-rate stage; final hiring outcomes are a separate, additional check
- The rule is a widely accepted adverse-impact screening method regardless of whether selection is manual or AI-driven

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** Which technique BEST reduces the risk of membership inference attacks during model training?

A) Increasing model parameter count to improve generalization
B) Differential privacy, adding calibrated noise to training updates
C) Training for additional epochs to reduce loss
D) Removing L2 regularization to speed convergence

<details>
<summary>Answer</summary>

**Correct: B**

Differential privacy bounds how much any single training record can influence the model's outputs, directly limiting an attacker's ability to infer whether a specific record was in the training set.

**Why the others are wrong:**
- Larger models tend to memorize more, increasing membership inference risk, not decreasing it
- More training epochs increase overfitting to individual records, worsening leakage risk
- Removing regularization increases overfitting, which is a primary driver of membership inference vulnerability

</details>

---

**Q5.** An organization must document the origin, collection process, and labeling methodology of the training dataset used for a high-risk AI system under EU AI Act Article 10. Which control category does this fall under?

A) Data governance and data quality management
B) Human oversight
C) Safety guardrail
D) Ethical review board charter

<details>
<summary>Answer</summary>

**Correct: A**

Article 10 specifically addresses data and data governance requirements — provenance, quality, representativeness, and documentation of datasets used for high-risk systems.

**Why the others are wrong:**
- Human oversight (Article 14) governs intervention capability during operation, not dataset documentation
- Safety guardrails are operational/technical harm-prevention mechanisms, not data lineage requirements
- An ethics charter is a governance artifact expressing values, not a data documentation control

</details>

---

**Q6.** Which set correctly lists the four core functions of the NIST AI Risk Management Framework (AI RMF 1.0)?

A) Identify, Protect, Detect, Respond
B) Plan, Do, Check, Act
C) Govern, Map, Measure, Manage
D) Design, Develop, Deploy, Decommission

<details>
<summary>Answer</summary>

**Correct: C**

NIST AI 100-1 defines Govern, Map, Measure, and Manage as the four core functions, with Govern acting as a cross-cutting foundation for the other three.

**Why the others are wrong:**
- Identify/Protect/Detect/Respond(/Recover) is the NIST Cybersecurity Framework, not AI RMF
- Plan-Do-Check-Act is the generic ISO management-system cycle, not AI RMF-specific
- This is a generic ML lifecycle description, not the named NIST AI RMF functions

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** Which combination of controls represents a 'safety guardrail' rather than an 'ethical control' in a production LLM deployment?

A) A fairness review board evaluating quarterly bias metrics against company values
B) A published set of AI ethics principles committing to non-discrimination
C) Stakeholder consultation assessing broader societal impact of the deployment
D) An output content filter blocking hate speech combined with API rate limiting

<details>
<summary>Answer</summary>

**Correct: D**

Safety guardrails are technical, operational mechanisms that act in real time to prevent immediate harm (content filtering, rate limiting); the other options are governance/values-based processes.

**Why the others are wrong:**
- A review board evaluating metrics against values is a governance/ethics process, not a real-time technical control
- Published principles are policy statements, not enforceable technical mechanisms
- Stakeholder consultation is a deliberative ethics activity, not an operational safety mechanism

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which statement BEST distinguishes safety guardrails from ethical controls in AI governance?

A) Safety guardrails are legally mandated while ethical controls are always optional
B) Safety guardrails are technical/operational mechanisms that prevent immediate harmful outputs; ethical controls are governance-level principles guiding value-based decisions
C) The two terms are synonymous and used interchangeably in AI governance frameworks
D) Ethical controls apply only during training, while safety guardrails apply only during inference

<details>
<summary>Answer</summary>

**Correct: B**

Guardrails are enforceable technical mechanisms (filters, validators, kill switches) operating at runtime; ethical controls are broader governance principles (fairness, accountability, human rights) that inform policy and design decisions.

**Why the others are wrong:**
- Both can be either mandated or voluntary depending on jurisdiction and organizational policy — legality is not the distinguishing factor
- The terms describe different layers of control and are not interchangeable on the exam
- Both types of controls apply across the full AI lifecycle, not restricted to one phase each

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

