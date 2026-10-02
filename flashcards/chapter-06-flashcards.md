## Chapter 6: AI Vendor, Third-Party, and Supply-Chain Risk Management — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | What does a 'model card' document? | Intended use cases, performance across subgroups, limitations, and ethical considerations of a trained model (Mitchell et al.). Exam tip: absence of a model card during vendor review = red flag. |
| 2 | What does a 'dataset datasheet' document? | Provenance, collection methodology, composition, and intended uses of a training dataset (Gebru et al., 'Datasheets for Datasets'). Used to assess licensing and bias risk. |
| 3 | Model card vs. dataset datasheet — key distinction | Model card = about the trained MODEL (performance/limitations). Dataset datasheet = about the DATA used to train it (provenance/licensing). Exam frequently swaps these terms. |
| 4 | Which ISO standard certifies an organization's AI management system? | ISO/IEC 42001:2023 — first international AI Management System (AIMS) standard. Distinct from ISO/IEC 27001, which covers general information security. |
| 5 | SOC 2 Type I vs Type II — which is stronger evidence for AI vendor due diligence? | Type II — assesses control effectiveness over an observation period (commonly 6-12 months). Type I is a point-in-time design snapshot only. |
| 6 | Best contract clause to stop a foundation-model vendor from training on your submitted data | An explicit data-usage / training opt-out clause stating customer inputs and outputs are NOT used for model training or fine-tuning by default. |
| 7 | Which clause allocates liability for IP-infringement claims from vendor training data? | Indemnification clause — distinct from SLA (availability/performance) and DPA (personal data processing obligations). |
| 8 | Fourth-party AI risk — definition | Risk from a vendor's subcontractors/subprocessors (e.g., undisclosed cloud host or fine-tuning partner) with no direct contractual relationship to the customer. Must be disclosed in a subprocessor list. |
| 9 | Right-to-audit alternative when a multi-tenant vendor denies direct audits | Accept independent third-party attestations (SOC 2 Type II, ISO/IEC 42001, ISO/IEC 27001) plus a contractual right to review findings and remediation plans. |
| 10 | GDPR breach-notification timeline referenced in vendor SLA negotiations | GDPR Art. 33 requires controllers to notify the supervisory authority within 72 hours of becoming aware of a personal data breach — vendor SLAs should require faster upstream notification to allow this. |
| 11 | NIST AI RMF (2023) core functions | Govern, Map, Measure, Manage — used as a baseline framework to evaluate a vendor's AI risk management maturity. |
| 12 | Key due-diligence question on vendor data retention | Ask: how long are API inputs/outputs retained, for what purpose (abuse monitoring vs. training), and can retention be contractually shortened or set to zero? |
