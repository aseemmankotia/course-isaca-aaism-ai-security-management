## Chapter 4: AI Risk Assessment, Appetite, and Treatment — Practice Questions

**Q1.** A healthcare provider's diagnostic-support AI model has a false negative rate that exceeds the risk appetite threshold set for patient safety. The vendor cannot remediate the model within the required timeframe. Which treatment strategy should the AI risk committee select?

A) Accept the risk since the model still provides clinical value
B) Avoid the risk by halting deployment until the false negative rate is remediated
C) Transfer the risk by purchasing malpractice insurance and continuing deployment
D) Mitigate the risk by adding a disclaimer for clinicians

<details>
<summary>Answer</summary>

**Correct: B**

When a risk exceeds the defined appetite for a high-criticality, safety-related use case and cannot be reduced through available controls, avoidance (halting deployment) is the correct treatment.

**Why the others are wrong:**
- Accepting a risk that exceeds the stated appetite threshold violates the governance decision already made about tolerable patient-safety risk.
- Transfer (insurance) addresses financial liability, not the underlying likelihood or clinical impact of missed diagnoses.
- A disclaimer is a superficial control that does not reduce the false negative rate below the required threshold.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** An organization is defining risk thresholds across three AI use-case tiers: low (internal productivity tools), moderate (customer-facing recommendation engine), and high (autonomous credit-decisioning model). Which approach correctly aligns risk appetite with use-case criticality?

A) Set the lowest risk tolerance for the credit-decisioning model and progressively higher tolerance for lower-criticality use cases
B) Apply the same risk threshold across all AI use cases for consistency
C) Set the highest risk tolerance for the credit-decisioning model since it delivers the most business value
D) Base thresholds solely on model accuracy metrics regardless of use case

<details>
<summary>Answer</summary>

**Correct: A**

Risk appetite must be inversely proportional to potential harm; the highest-criticality use case (autonomous credit decisions, regulatory/fairness exposure) requires the lowest tolerance for risk.

**Why the others are wrong:**
- A uniform threshold over-controls low-risk tools and under-controls high-risk ones, wasting resources and exposing the organization.
- Higher business value does not offset the harm potential of a high-impact, high-autonomy decisioning system.
- Accuracy alone ignores impact, autonomy, and reach dimensions used to set appetite.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An organization maintains a portfolio of 40 AI models with limited resources for in-depth assessment this quarter. Which prioritization approach BEST allocates assessment effort?

A) Assess models in the order they were deployed, oldest first
B) Assess models alphabetically by model name
C) Assess only models that have had a reported incident in the past
D) Prioritize models using a combined score of business impact, autonomy level, and data sensitivity

<details>
<summary>Answer</summary>

**Correct: D**

Portfolio-level prioritization should be risk-based, combining impact, autonomy, and data sensitivity to focus effort where potential harm is greatest.

**Why the others are wrong:**
- Deployment date has no correlation to current risk level.
- Alphabetical order is arbitrary and ignores risk entirely.
- Limiting review to models with prior incidents is reactive and misses undiscovered high-risk models.

</details>

---

**Q4.** Which risk register entry reflects a risk that is specific to AI systems rather than traditional IT infrastructure?

A) Unpatched operating system vulnerability on the model-serving host
B) Unauthorized network access to the production environment
C) Model performance degradation caused by data drift over time
D) Expired TLS certificate causing a service outage

<details>
<summary>Answer</summary>

**Correct: C**

Data drift causing silent performance degradation is a risk unique to statistical/ML models and requires ongoing monitoring not present in traditional IT risk registers.

**Why the others are wrong:**
- Unpatched OS vulnerabilities are generic infrastructure risks applicable to any server.
- Unauthorized network access is a standard IT security risk.
- Certificate expiration is a common IT operations risk unrelated to model behavior.

</details>

---

**Q5.** A CISO wants to adopt a structured, function-based approach organized around Govern, Map, Measure, and Manage specifically for AI risk. Which framework should be referenced?

A) NIST AI Risk Management Framework (AI RMF 1.0)
B) ISO/IEC 27001
C) COBIT 2019
D) PCI DSS

<details>
<summary>Answer</summary>

**Correct: A**

NIST AI RMF 1.0 is organized into the four functions Govern, Map, Measure, and Manage, purpose-built for AI risk.

**Why the others are wrong:**
- ISO/IEC 27001 is a general information security management system standard, not AI-specific and not organized by these functions.
- COBIT 2019 is a general IT governance and management framework, not AI risk-specific.
- PCI DSS is a payment card data security standard unrelated to AI risk functions.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** An enterprise integrates a third-party foundation model API for customer support and identifies risk of vendor model deprecation and unpredictable pricing affecting business continuity. Which treatment strategy is MOST appropriate for this specific risk?

A) Accept the risk because the vendor has a strong market reputation
B) Avoid the risk entirely by never using third-party AI models
C) Mitigate by negotiating contractual SLAs and maintaining a fallback model
D) Transfer the risk fully to the vendor through indemnification clauses alone

<details>
<summary>Answer</summary>

**Correct: C**

Mitigation through contractual SLAs plus a technical fallback directly reduces the likelihood and impact of continuity disruption.

**Why the others are wrong:**
- Reputation does not address deprecation or pricing volatility exposure.
- Avoidance forgoes legitimate business value disproportionate to a manageable, addressable risk.
- Indemnification transfers financial liability but leaves operational continuity risk unaddressed since it doesn't guarantee service availability.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** An organization uses a 5x5 risk matrix (likelihood 1-5, impact 1-5) and its risk appetite statement requires executive sign-off for any AI use case scoring above 15. A new generative AI use case scores likelihood=4, impact=5 (score=20). What is the correct next step?

A) Deploy immediately since the model passed technical testing
B) Automatically reject the use case without further review
C) Lower the impact score to bring the total under the threshold
D) Escalate to executive leadership for risk acceptance sign-off before deployment

<details>
<summary>Answer</summary>

**Correct: D**

The defined appetite threshold requires escalation to executives when the score exceeds 15; this is a governance gate, not an automatic pass or fail.

**Why the others are wrong:**
- Technical testing does not substitute for the governance escalation required by the risk appetite policy.
- Exceeding the threshold triggers escalation, not automatic rejection; executives may accept with compensating controls.
- Adjusting scores to avoid escalation is gaming the risk criteria and violates governance integrity.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which characteristic MOST distinguishes AI risk assessment from traditional IT risk assessment?

A) AI risk assessment does not require documentation of findings
B) AI risk assessment only applies to models trained on unstructured data
C) AI risk assessment must additionally account for emergent behaviors, model drift, and non-deterministic outputs beyond standard confidentiality/integrity/availability risks
D) AI risk assessment eliminates the need for a risk register

<details>
<summary>Answer</summary>

**Correct: C**

AI risk assessment extends traditional IT/CIA-based assessment to cover behaviors unique to learning systems: drift, non-determinism, and emergent outputs.

**Why the others are wrong:**
- Documentation is still required and arguably more critical for AI due to explainability needs.
- AI risk applies equally to structured-data models (e.g., credit scoring) and unstructured-data models (e.g., LLMs).
- A risk register is still required; AI risk simply adds new fields and risk types to it.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

