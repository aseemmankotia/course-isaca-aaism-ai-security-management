## Chapter 1: AI Governance Foundations: Frameworks as Program Inputs — Practice Questions

**Q1.** A financial services firm wants to build an internal AI governance program that can be independently audited and certified to demonstrate AI risk maturity to enterprise clients. Which framework should form the foundation of this program?

A) NIST AI RMF
B) ISO/IEC 42001
C) MITRE ATLAS
D) OWASP Top 10 for LLM Applications

<details>
<summary>Answer</summary>

**Correct: B**

ISO/IEC 42001 is the only framework listed that is structured as a certifiable AI management system (AIMS), built on the Annex SL structure, allowing third-party audit and certification.

**Why the others are wrong:**
- NIST AI RMF is a voluntary, non-certifiable risk management framework — no accredited certification body issues 'NIST AI RMF certification.'
- MITRE ATLAS is a threat/adversarial tactics knowledge base, not a management system framework — it has no certification scope at all.
- OWASP Top 10 for LLM is a technical vulnerability checklist for LLM applications, not an enterprise governance/management system.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A US federal contractor needs to establish a voluntary, internal risk management practice for its AI systems organized around continuous, cross-functional processes, without pursuing external certification. Which framework best fits this need?

A) NIST AI RMF
B) ISO/IEC 42001
C) EU AI Act
D) MITRE ATLAS

<details>
<summary>Answer</summary>

**Correct: A**

NIST AI RMF is explicitly designed as a voluntary framework organized around Govern/Map/Measure/Manage, suited for internal risk practice without certification overhead.

**Why the others are wrong:**
- ISO/IEC 42001 is built for formal certification/audit, adding overhead beyond what a purely internal, non-certified practice requires.
- The EU AI Act is a binding regulation, not a voluntary management framework — it defines legal obligations, not a process structure.
- MITRE ATLAS is a threat catalog, not a risk management process framework.

</details>

---

**Q3.** A company deploys an AI system in the EU that automatically screens job applicant resumes to shortlist candidates for interviews. Under the EU AI Act, how is this system classified?

A) High-risk — subject to conformity assessment and risk management obligations
B) Unacceptable risk — prohibited
C) Limited risk — transparency obligations only
D) Minimal risk — no mandatory obligations

<details>
<summary>Answer</summary>

**Correct: A**

Employment and worker management use cases, including resume screening, are explicitly listed under Annex III as high-risk, triggering conformity assessment, risk management, human oversight, and documentation obligations.

**Why the others are wrong:**
- Unacceptable risk is reserved for practices like social scoring or manipulative subliminal techniques — resume screening is not banned outright.
- Limited risk (transparency-only) applies to systems like chatbots or deepfake generators, not Annex III high-risk use cases such as employment screening.
- Minimal risk applies to low-impact systems like spam filters or AI-enabled video games — misclassifying employment AI here would miss mandatory obligations.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A red team needs a resource that catalogs known adversarial tactics and techniques used to attack machine learning systems, modeled after an ATT&CK-style matrix, to inform threat modeling. Which resource should they use?

A) OWASP Top 10 for LLM Applications
B) ISO/IEC 42001
C) MITRE ATLAS
D) NIST AI RMF

<details>
<summary>Answer</summary>

**Correct: C**

MITRE ATLAS is purpose-built as an ATT&CK-style knowledge base of adversarial tactics and techniques across the ML attack lifecycle, ideal for red-team threat modeling.

**Why the others are wrong:**
- OWASP Top 10 for LLM is a ranked vulnerability list scoped to LLM applications, not a full tactics-and-techniques matrix across the ML lifecycle.
- ISO/IEC 42001 is a management system standard focused on organizational governance, not adversarial technique cataloging.
- NIST AI RMF is a risk management process framework, not a threat intelligence resource.

</details>

---

**Q5.** An application security team is reviewing a customer-facing LLM chatbot and needs a prioritized, practical checklist of common LLM-specific vulnerabilities such as prompt injection and insecure output handling. Which resource should they consult first?

A) MITRE ATLAS
B) OWASP Top 10 for LLM Applications
C) ISO/IEC 42001
D) NIST AI RMF

<details>
<summary>Answer</summary>

**Correct: B**

OWASP Top 10 for LLM Applications is a practical, ranked vulnerability list specifically addressing LLM application risks like prompt injection and insecure output handling.

**Why the others are wrong:**
- MITRE ATLAS covers broader ML adversarial tactics and techniques, useful for threat modeling but less actionable for day-to-day AppSec checklist review.
- ISO/IEC 42001 addresses organizational AI management processes, not application-level vulnerability guidance.
- NIST AI RMF is a program-level risk management framework, not a technical vulnerability checklist.

</details>

---

**Q6.** Under NIST AI RMF, an organization is establishing context, categorizing intended system use, and identifying relevant stakeholders before assessing risk. Which core function does this activity belong to?

A) Govern
B) Measure
C) Manage
D) Map

<details>
<summary>Answer</summary>

**Correct: D**

Map is the function focused on establishing context, categorizing intended use, and identifying stakeholders — it must occur before meaningful risk measurement can happen.

**Why the others are wrong:**
- Govern is cross-cutting and establishes policies/accountability structures, not context-setting for a specific system.
- Measure involves analyzing, benchmarking, and tracking identified risks, which requires Map to have already occurred.
- Manage involves allocating resources to treat prioritized risks, a later-stage activity.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** Which NIST AI RMF function is described as cross-cutting, applying continuously across all other functions to embed accountability, culture, and policy?

A) Map
B) Measure
C) Manage
D) Govern

<details>
<summary>Answer</summary>

**Correct: D**

Govern is explicitly cross-cutting in the NIST AI RMF, informing and being applied throughout Map, Measure, and Manage rather than acting as a sequential phase.

**Why the others are wrong:**
- Map is a discrete function focused on context and categorization, not a continuous cross-cutting activity.
- Measure is focused on analyzing and tracking risk metrics for a specific mapped context.
- Manage is focused on resourcing and treating prioritized risks, not embedding organization-wide accountability.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** What is the key conceptual distinction between a 'program framework' like NIST AI RMF or ISO/IEC 42001 and a 'threat-input framework' like MITRE ATLAS?

A) Program frameworks define organizational processes for managing AI risk; threat-input frameworks catalog specific attack techniques that feed into those processes
B) Program frameworks are legally mandated while threat-input frameworks are always voluntary
C) Threat-input frameworks replace the need for a program framework entirely
D) There is no meaningful distinction — both serve identical purposes in an AI governance program

<details>
<summary>Answer</summary>

**Correct: A**

Program frameworks (NIST AI RMF, ISO 42001) structure the organizational lifecycle and processes for managing AI risk, while threat-input frameworks like MITRE ATLAS supply specific adversarial technique data that informs the Map/Measure functions within that program.

**Why the others are wrong:**
- Neither category is inherently tied to legal mandate status — both NIST AI RMF and MITRE ATLAS are voluntary; mandate status depends on regulation, not framework type.
- Threat-input frameworks do not replace program frameworks — they are inputs consumed by a governance program, not substitutes for one.
- The two categories serve fundamentally different purposes: one structures governance process, the other supplies threat intelligence content.

</details>

---

