## Chapter 3: AI Security Program Management, Training, BCP, and Incident Response — Practice Questions

**Q1.** A large bank plans to deploy an internal generative AI assistant for customer service. The CISO proposes that existing security operations staff absorb all AI-specific security responsibilities without adding new roles or committees. Which risk is MOST likely to result from this approach?

A) Lack of accountability for AI-specific risks such as model drift, data poisoning, and training data provenance because no one owns these risks explicitly
B) Increased licensing costs for security tooling
C) Slower deployment of the chatbot due to additional change management overhead
D) Reduced visibility into network-layer attacks against the API gateway

<details>
<summary>Answer</summary>

**Correct: A**

AI-specific risks (drift, poisoning, provenance) fall outside traditional SOC/IR skillsets and require explicitly assigned ownership; absorbing them into existing roles without new accountability creates gaps.

**Why the others are wrong:**
- Cost is a secondary business concern, not the governance risk being tested.
- Deployment speed is not the accountability issue described in the scenario.
- Network-layer visibility is unrelated to adding AI duties to existing staff; it is a traditional concern, not AI-specific.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** An enterprise relies on a third-party large language model API for a critical claims-processing workflow. The vendor experiences an extended outage with no committed restoration timeline. Which control should have been established during business continuity planning to prevent workflow disruption?

A) A quarterly penetration test of the vendor's API
B) An annual AI ethics review of the vendor's training data sources
C) A service-level agreement requiring 99.9% uptime with financial penalties
D) A documented fallback procedure, such as a secondary model or manual review process, activated when the primary AI service becomes unavailable

<details>
<summary>Answer</summary>

**Correct: D**

BCP for AI-dependent processes requires a defined fallback or degraded-mode procedure so operations continue when AI availability fails, regardless of vendor contract terms.

**Why the others are wrong:**
- A pentest addresses security testing, not operational continuity.
- An ethics review addresses data governance, not continuity of operations.
- An SLA with penalties is a contractual deterrent, not an operational continuity control — it does not restore service during an outage.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** During an investigation of a fraud-detection ML model, analysts find attacker-crafted inputs causing consistent misclassification, but no unauthorized data access occurred. Which adaptation to the standard IR playbook is MOST necessary for this AI incident?

A) Adding a model-behavior forensics step to determine whether the model's decision boundary was manipulated via adversarial inputs, versus a data breach
B) Immediate rotation of all API keys used by the fraud team
C) Notifying customers under standard breach-notification requirements
D) Escalating to legal for a suspected insider threat investigation

<details>
<summary>Answer</summary>

**Correct: A**

AI incidents often involve model manipulation (adversarial/evasion attacks) rather than classic exfiltration; IR playbooks must add model-behavior forensics steps distinct from traditional network/data forensics.

**Why the others are wrong:**
- Key rotation addresses credential compromise, which is not indicated here.
- No data breach occurred, so breach notification is not yet triggered.
- No evidence points to an insider; the scenario describes external adversarial inputs.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** An organization is establishing AI governance and needs a body that reviews high-risk AI use cases before deployment, sets risk tolerance, and reports AI risk posture to the board. Which structure BEST fulfills this role?

A) A dedicated AI governance committee with cross-functional representation from security, legal, data science, and risk management
B) The existing Change Advisory Board (CAB)
C) The Security Operations Center (SOC) shift lead
D) The vendor management office

<details>
<summary>Answer</summary>

**Correct: A**

Cross-functional AI governance committees are the standard structure for AI risk oversight, use-case review, and board reporting.

**Why the others are wrong:**
- A CAB handles IT change control, not AI risk tolerance decisions.
- The SOC is operational/tactical, not a governance body.
- Vendor management focuses on procurement/contracts, not AI risk oversight.

</details>

---

**Q5.** Which metric is the BEST Key Risk Indicator (KRI) to report to the board regarding AI model security posture, as opposed to a Key Performance Indicator (KPI)?

A) Percentage of production AI models with an unresolved high-severity adversarial-robustness finding past the remediation SLA
B) Number of AI models deployed this quarter
C) Average model inference latency
D) Number of employees who completed AI awareness training

<details>
<summary>Answer</summary>

**Correct: A**

A KRI measures exposure to risk; unresolved high-severity findings past SLA directly indicates risk exposure, appropriate for board-level reporting.

**Why the others are wrong:**
- Deployment count is an operational volume metric, not a risk indicator.
- Latency is a performance metric unrelated to risk exposure.
- Training completion is a KPI (program effectiveness), commonly mistaken for a KRI, but it does not measure risk exposure itself.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** An AI security awareness training program is being designed for three audiences: executives, developers/data scientists, and general staff using AI tools. Which approach reflects best practice for this program's design?

A) Deliver one identical annual training module to all three audiences to ensure consistency
B) Require only developers to complete AI security training since they build the models
C) Provide role-based, differentiated content — e.g., prompt-injection awareness for general staff, secure model development practices for data scientists, and risk/liability briefings for executives
D) Deliver training once at hire with no recurring refresher

<details>
<summary>Answer</summary>

**Correct: C**

Role-based, differentiated training is best practice because different roles face different AI risks and need tailored content.

**Why the others are wrong:**
- A one-size-fits-all module fails to address role-specific risks.
- General staff and executives also face AI risk (e.g., shadow AI use, oversight duties) and need training.
- Recurring training is required given the fast-evolving AI threat landscape.

</details>

---

**Q7.** How frequently should AI security KRIs and KPIs typically be reported to the board or senior executive committee to satisfy oversight expectations?

A) Only when a major incident occurs
B) Annually, aligned with the enterprise risk assessment
C) At a regular cadence (e.g., quarterly), supplemented by ad hoc reporting for significant risk events
D) Daily, as part of SOC shift reports

<details>
<summary>Answer</summary>

**Correct: C**

Governance best practice calls for regular periodic board reporting (commonly quarterly) plus event-driven reporting for significant risk events.

**Why the others are wrong:**
- Reactive-only reporting fails oversight and accountability expectations.
- Annual-only reporting is too infrequent given the rapidly evolving nature of AI risk.
- Daily board reporting is operationally impractical; that granularity belongs at the SOC/operational level.

</details>

---

**Q8.** Which statement BEST describes how the 'AI Security Officer' (or equivalent AI security governance role) differs from the traditional CISO role?

A) The AI Security Officer replaces the CISO and assumes all security responsibilities enterprise-wide
B) The AI Security Officer owns risks specific to the AI lifecycle — training data integrity, model behavior, adversarial robustness, and AI-specific compliance — often coordinating with, not replacing, the CISO's broader security mandate
C) The AI Security Officer focuses exclusively on network and infrastructure security, while the CISO focuses on application security
D) The AI Security Officer role is identical to the CISO role but reports to a different executive

<details>
<summary>Answer</summary>

**Correct: B**

The exam-tested distinction is risk-domain based: AI-specific roles address novel lifecycle risks traditional security roles are not equipped to fully own, coordinating with rather than replacing existing security governance.

**Why the others are wrong:**
- The role does not replace the CISO; both roles coexist.
- This reverses/misstates the actual distinction being tested.
- If the roles were identical, there would be no rationale for creating a distinct role; the exam tests differentiation by risk domain, not reporting line.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

