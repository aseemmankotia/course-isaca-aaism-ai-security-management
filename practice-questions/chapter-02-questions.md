## Chapter 2: AI Asset, Data Lifecycle, and Policy Management — Practice Questions

**Q1.** An AI governance team is updating its data retention policy for a fraud-detection model. The model was trained on customer transaction data 18 months ago, a new regulatory guidance now requires justification for any model in production beyond 12 months without revalidation, and the model has not been retrained since deployment. Which trigger should MOST directly initiate the decommissioning/retraining review process?

A) The original training dataset has grown by 10% since collection
B) A regulatory change created a new compliance requirement the deployed model does not meet
C) The vendor released a newer version of the underlying framework
D) The model owner requested a cosmetic dashboard update

<details>
<summary>Answer</summary>

**Correct: B**

Regulatory/legal change is a core decommissioning-retention trigger in AI governance frameworks — it creates a compliance gap that must be remediated regardless of model performance.

**Why the others are wrong:**
- Dataset growth alone is not a retention trigger unless it affects representativeness or introduces drift
- Framework/vendor version changes are operational maintenance items, not governance decommissioning triggers
- A cosmetic UI change has no bearing on retention or decommissioning decisions

</details>

---

**Q2.** During an internal audit, the governance office discovers that a marketing team has been using a public generative AI web tool to draft customer emails, uploading customer segment data in the process. This tool was never registered in the AI asset inventory. What is the FIRST governance action that should be taken?

A) Add the tool retroactively to the inventory and classify the data exposure risk before deciding on remediation
B) Immediately terminate the marketing employees involved
C) Ignore it since the tool is free and low-risk
D) Escalate directly to the regulator without internal investigation

<details>
<summary>Answer</summary>

**Correct: A**

Shadow AI remediation begins with discovery and inventory capture plus risk/data classification, which informs proportionate next steps (policy enforcement, DLP controls, training).

**Why the others are wrong:**
- Termination is a disproportionate first step and not a governance control action
- Ignoring the finding contradicts the purpose of shadow AI discovery programs
- External escalation before internal risk assessment skips required incident triage steps

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A healthcare organization must respond to an auditor's request to show exactly which dataset version, preprocessing steps, and hyperparameters produced a currently deployed diagnostic model. Which capability is being tested?

A) Data classification
B) Provenance and lineage tracking
C) Access control management
D) Model explainability

<details>
<summary>Answer</summary>

**Correct: B**

Provenance and lineage tracking captures the full chain of data sources, transformations, and training parameters across the model lifecycle so it can be reconstructed for audit.

**Why the others are wrong:**
- Data classification labels sensitivity, not the transformation history
- Access control governs who can touch the asset, not how it was built
- Explainability addresses why a model produced a specific output, not its build history

</details>

---

**Q4.** A governance team wants a single documentation artifact that describes a training dataset's composition, collection methodology, known biases, and intended/excluded uses so downstream teams can assess suitability before reuse. Which artifact BEST fits this need?

A) A model card
B) A software bill of materials (SBOM)
C) A datasheet for the dataset
D) A data classification label

<details>
<summary>Answer</summary>

**Correct: C**

Datasheets for datasets (Gebru et al.) are the standard artifact documenting dataset composition, collection process, and appropriate use, supporting provenance and reuse governance.

**Why the others are wrong:**
- Model cards document a trained model's performance and limitations, not the raw dataset
- An SBOM documents software components/dependencies, not dataset provenance
- A classification label is a single sensitivity tag, not a full provenance description

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which classification approach is MOST appropriate for distinguishing AI data risk at the point of use?

A) Classify all AI-related data identically regardless of lifecycle stage
B) Classify training data by sensitivity/provenance and separately classify inference/input data by real-time exposure risk
C) Classify only inference data since training data is discarded after use
D) Classify data solely by file size

<details>
<summary>Answer</summary>

**Correct: B**

Training data and inference/prompt data carry different risk profiles (aggregated historical exposure vs. live/real-time PII exposure), so mature governance schemes classify each separately.

**Why the others are wrong:**
- Uniform classification ignores that training and inference data have different lifecycle risks
- Training data is frequently retained for retraining/audit and cannot be assumed discarded
- File size has no relationship to sensitivity or risk

</details>

---

**Q6.** An organization's AI governance program includes: (1) a board-approved statement that AI must be used responsibly and aligned to business objectives, (2) a mandatory rule that all production models require a documented risk assessment before deployment, (3) a mandatory minimum set of fields required in every risk assessment, and (4) a step-by-step guide for filling out the risk assessment form. In the policy hierarchy, item (3) is best classified as which document type?

A) Standard
B) Strategy
C) Policy
D) Procedure

<details>
<summary>Answer</summary>

**Correct: A**

A standard specifies mandatory, measurable requirements that support a policy (e.g., the exact minimum fields required), sitting between the policy (the rule) and the procedure (the how-to steps).

**Why the others are wrong:**
- Strategy is the high-level directional statement (item 1), not a mandatory requirement set
- Policy is the mandatory rule itself (item 2: risk assessment is required), not the specific field requirements
- Procedure is the step-by-step instructions (item 4), not the mandatory requirement list

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** Which set of items should be included in the scope of an organization's AI asset inventory?

A) Only production models that generate revenue
B) Only datasets classified as confidential
C) Only third-party vendor AI tools, since internally built models are already tracked in the CMDB
D) Models, training/evaluation datasets, pipelines/orchestration code, and reusable prompt templates

<details>
<summary>Answer</summary>

**Correct: D**

A complete AI asset inventory must capture the full ecosystem — models, datasets, pipelines, and prompts/templates — since each carries distinct governance and risk obligations.

**Why the others are wrong:**
- Limiting to revenue-generating production models excludes shadow AI, pilots, and internal-use models that still carry risk
- Limiting to confidential datasets ignores models, pipelines, and prompt assets entirely
- Excluding internally built models assumes CMDB coverage, which typically does not capture AI-specific lifecycle attributes like lineage and training data

</details>

---

**Q8.** Which statement BEST describes the difference between a policy and a standard in an AI governance hierarchy?

A) A policy is optional guidance while a standard is legally binding
B) A policy and a standard are interchangeable terms for the same document
C) A policy states the mandatory rule (the 'what'), while a standard defines the specific mandatory requirements that operationalize the policy (the measurable 'how much/which')
D) A standard is set by regulators while a policy is set only by internal management

<details>
<summary>Answer</summary>

**Correct: C**

In governance hierarchies, the policy establishes the mandatory rule, and the standard provides the specific, measurable requirements needed to comply with that policy.

**Why the others are wrong:**
- Both policy and standard are mandatory, not optional — guidelines are the optional layer
- The two terms serve distinct, non-interchangeable purposes in the hierarchy
- Standards can originate internally or externally (e.g., regulatory); the distinction is about specificity, not source

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

