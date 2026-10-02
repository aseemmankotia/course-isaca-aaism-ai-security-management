## Chapter 6: AI Vendor, Third-Party, and Supply-Chain Risk Management — Practice Questions

**Q1.** A company is negotiating a contract with a foundation-model provider to power a customer support chatbot that will process proprietary customer data via API. Which contract term is MOST critical to include to prevent the vendor from using customer inputs to improve their foundation model?

A) A service-level agreement guaranteeing 99.9% uptime
B) An explicit data-usage and training opt-out clause prohibiting use of submitted data for model training or fine-tuning
C) A most-favored-customer pricing clause
D) A liability cap limiting vendor damages to fees paid in the prior 12 months

<details>
<summary>Answer</summary>

**Correct: B**

Only an explicit training opt-out / data-usage clause directly restricts the vendor from using customer data to improve or retrain its model.

**Why the others are wrong:**
- Uptime SLAs address availability, not data confidentiality or training usage.
- Pricing clauses are commercial terms unrelated to data protection.
- A liability cap limits financial exposure after a breach but does not prevent the underlying data usage from occurring.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** During due diligence, a security team discovers that their AI vendor's foundation model is actually hosted and fine-tuned by an undisclosed fourth-party cloud subprocessor. What is the GREATEST risk this introduces?

A) Increased latency in API responses
B) Higher subscription costs due to additional infrastructure layers
C) Loss of visibility and control over data handling and security controls applied by the undisclosed subprocessor
D) Reduced model accuracy due to multi-tenant hosting

<details>
<summary>Answer</summary>

**Correct: C**

Undisclosed subprocessors create a supply-chain blind spot — the organization cannot verify what controls, retention practices, or access policies apply to its data at the fourth-party level.

**Why the others are wrong:**
- Latency is an operational concern, not the primary security/compliance risk.
- Cost is a commercial concern, not a supply-chain security risk.
- Accuracy degradation is a performance concern, unrelated to visibility/control gaps.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An AI security manager reviewing a vendor's model card notices it lists only aggregate performance metrics with no information on training data sources or licensing. What critical gap does this represent for supply-chain risk assessment?

A) Inability to verify the model's inference latency benchmarks
B) Inability to configure API rate limits for the service
C) Inability to determine the model's supported programming languages
D) Inability to verify data provenance, licensing terms, and potential bias or IP-infringement exposure from training data sources

<details>
<summary>Answer</summary>

**Correct: D**

Model cards describe model behavior, but provenance and licensing details belong in dataset documentation (e.g., a datasheet); their absence blocks verification of legal and bias risk.

**Why the others are wrong:**
- Latency is a performance metric unrelated to provenance review.
- Rate limits are an operational/API configuration matter.
- Supported languages are a feature detail, not a supply-chain risk indicator.

</details>

---

**Q4.** A regulated financial institution wants a right-to-audit clause in its contract with a foundation-model API provider. The provider refuses direct on-site audits, citing shared multi-tenant infrastructure, but offers to share independent audit reports instead. What is the BEST risk-based path for the institution?

A) Require current SOC 2 Type II reports and/or ISO/IEC 42001 certification, plus a contractual right to review findings and remediation plans
B) Accept the vendor's verbal assurance of compliance with no supporting documentation
C) Terminate the vendor relationship because audit rights cannot be negotiated with multi-tenant providers
D) Rely solely on the vendor's public marketing claims about its security posture

<details>
<summary>Answer</summary>

**Correct: A**

Third-party attestations combined with a contractual right to review results and remediation are the accepted substitute when direct audits of shared infrastructure are impractical.

**Why the others are wrong:**
- Verbal assurance provides no verifiable evidence and fails due-diligence standards.
- Termination is an overreaction — negotiated attestation-based alternatives are standard industry practice.
- Marketing claims are not independently verified and are unacceptable as sole assurance.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which contract clause type specifically addresses financial responsibility if a foundation-model provider's training data is later found to infringe third-party intellectual property rights, resulting in claims against the customer?

A) Indemnification clause
B) Service Level Agreement (SLA)
C) Data Processing Addendum (DPA)
D) Non-disclosure Agreement (NDA)

<details>
<summary>Answer</summary>

**Correct: A**

Indemnification clauses allocate liability for third-party claims, including IP infringement arising from vendor-supplied training data.

**Why the others are wrong:**
- SLAs govern availability and performance metrics, not legal liability.
- A DPA governs personal data processing obligations under privacy law, not IP claims.
- An NDA protects confidential information exchange, not liability allocation.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** An organization wants third-party assurance that a foundation-model vendor operates a mature AI risk management system, beyond general information security controls. Which certification BEST demonstrates this?

A) ISO/IEC 27001
B) SOC 1 Type I
C) ISO/IEC 42001
D) PCI DSS

<details>
<summary>Answer</summary>

**Correct: C**

ISO/IEC 42001:2023 is the international standard specifically for AI management systems, covering AI-specific governance, risk, and lifecycle controls.

**Why the others are wrong:**
- ISO/IEC 27001 certifies general information security management, not AI-specific risk practices.
- SOC 1 Type I addresses financial reporting controls at a single point in time and is unrelated to AI risk maturity.
- PCI DSS applies to payment card data handling and is irrelevant to AI supply-chain assurance.

</details>

---

**Q7.** When drafting SLA requirements for a foundation-model vendor, which requirement is MOST important to ensure timely response to AI-specific harms such as data leakage through model outputs?

A) A guaranteed maximum API response time of 200ms
B) Unlimited free retraining requests included in the base subscription
C) A defined security-incident notification window with escalation procedures specific to data exposure and anomalous model behavior
D) A fixed monthly cost regardless of usage volume

<details>
<summary>Answer</summary>

**Correct: C**

A defined notification and escalation timeline for AI-specific incidents (data leakage, anomalous outputs) ensures the customer can act quickly to contain and report harm.

**Why the others are wrong:**
- Response-time guarantees address performance, not incident response for security harms.
- Free retraining is a commercial perk unrelated to incident handling.
- Fixed pricing is a cost-control term, not a risk-response mechanism.

</details>

---

**Q8.** What is the KEY difference between a 'model card' and a 'dataset datasheet' in AI vendor due diligence?

A) A model card documents infrastructure costs while a dataset datasheet documents API endpoints
B) A model card documents a trained model's intended use, performance, and limitations, while a dataset datasheet documents the provenance, composition, and collection methodology of the training data
C) They are interchangeable terms for the same document
D) A model card is required only for open-source models, while dataset datasheets are required only for proprietary models

<details>
<summary>Answer</summary>

**Correct: B**

Model cards (Mitchell et al.) describe the trained model's behavior and limitations; dataset datasheets (Gebru et al.) describe the training data's origin, composition, and licensing — two distinct artifacts serving different due-diligence purposes.

**Why the others are wrong:**
- Neither document addresses infrastructure cost or API endpoints.
- They are not interchangeable — one covers the model, the other the data.
- Both concepts apply regardless of open-source or proprietary status.

</details>

---

