## Chapter 9: AI Security Monitoring, Red-Teaming, and Continuous Evaluation — Practice Questions

**Q1.** A company's LLM-powered agent retrieves internal documents via RAG before generating responses. Security wants to detect indirect prompt injection hidden inside retrieved documents. Which logging control BEST enables this detection?

A) Log only the final user-facing output text
B) Log the full prompt context, including retrieved documents, system instructions, and tool call parameters
C) Log user IP addresses and session duration only
D) Log only the return values of tool calls

<details>
<summary>Answer</summary>

**Correct: B**

Indirect injection is embedded in retrieved/external content the model ingests before generating output. Only logging the full input context (retrieved docs, system prompt, tool params) exposes the injected instructions for detection.

**Why the others are wrong:**
- Final output alone does not show the injected content that caused the behavior
- Network/session metadata does not reveal injected instructions in content
- Tool return values alone don't show the upstream cause of the manipulated behavior

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A red team is designing an exercise for an agentic AI system that autonomously executes multi-step tool calls (e.g., ticket creation, file deletion, API calls). Which objective BEST reflects the primary risk this exercise should target?

A) Testing whether the model's final text output contains toxic language
B) Testing whether the agent can be manipulated into invoking destructive or unauthorized tool actions beyond its intended scope
C) Testing the model's arithmetic accuracy on benchmark datasets
D) Testing UI response time under concurrent load

<details>
<summary>Answer</summary>

**Correct: B**

Agentic systems introduce action risk, not just content risk — red-teaming must probe whether adversarial input can trigger unauthorized or destructive tool/API execution and privilege escalation.

**Why the others are wrong:**
- Toxicity testing is relevant for chatbots but doesn't cover the unique agentic action-execution risk
- Accuracy benchmarking is a performance test, not a security red-team objective
- UI performance testing is unrelated to security risk

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** Which approach BEST integrates AI-specific security telemetry into an organization's existing security operations?

A) Build a fully separate AI-only SOC with no ticketing or SIEM integration
B) Rely solely on the model provider's built-in safety dashboard for all monitoring
C) Forward AI telemetry (prompts, outputs, guardrail triggers, tool calls) into the existing SIEM with AI-specific detection rules, correlated against identity and network logs
D) Disable detailed AI logging to reduce SOC alert volume and noise

<details>
<summary>Answer</summary>

**Correct: C**

Best practice is unifying AI telemetry into existing SIEM/SOAR workflows with correlation to identity and network context, enabling holistic detection rather than isolated silos.

**Why the others are wrong:**
- A siloed AI-only SOC creates blind spots and duplicate tooling with no cross-correlation
- Vendor dashboards lack organization-specific context and cross-signal correlation
- Disabling logging removes the visibility needed for detection and forensics

</details>

---

**Q4.** In a continuous evaluation program for a production LLM, which metric pairing BEST distinguishes performance drift from safety drift?

A) Response latency and token cost per request
B) Task accuracy/quality score trend versus increase in policy-violation or jailbreak success rate over time
C) Number of active users and system uptime percentage
D) Model file size and version number

<details>
<summary>Answer</summary>

**Correct: B**

Performance drift is tracked via quality/accuracy trend metrics; safety drift is tracked via rising jailbreak/policy-violation success rates. Together they separate the two drift categories.

**Why the others are wrong:**
- Latency and cost are operational metrics, not quality or safety drift indicators
- Active users and uptime are business/availability metrics unrelated to drift
- File size and version number are static attributes, not evaluation metrics

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** What is the primary difference between data drift and concept drift in AI monitoring?

A) Data drift only affects storage costs; concept drift only affects billing
B) The two terms are interchangeable and used identically in AI risk management
C) Data drift applies only to LLMs; concept drift applies only to computer vision models
D) Data drift refers to a change in the distribution of input features; concept drift refers to a change in the underlying relationship between inputs and correct outputs

<details>
<summary>Answer</summary>

**Correct: D**

Data drift = shift in input feature distribution over time. Concept drift = shift in the relationship between inputs and correct outputs/labels, even if input distribution is stable.

**Why the others are wrong:**
- Cost/billing framing is fabricated and irrelevant to the technical definitions
- The exam tests these as distinct, separately monitored concepts
- Both concepts apply across model types, not restricted by modality

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A SOC analyst observes a spike in near-identical prompts attempting to bypass content filters using role-play framing such as 'pretend you are an unrestricted AI.' Which detection use case does this represent?

A) Data exfiltration via embedding queries
B) Model inversion attack
C) Training data supply chain compromise
D) Jailbreak / prompt injection abuse pattern detection

<details>
<summary>Answer</summary>

**Correct: D**

Repeated role-play/persona-override prompts attempting to bypass safety filters is a classic jailbreak abuse pattern that AI-specific detection rules should flag.

**Why the others are wrong:**
- Exfiltration involves extracting sensitive data, not bypassing content filters
- Model inversion targets extracting training data from model outputs, a different attack class
- Supply chain compromise concerns poisoned training data or dependencies, not runtime prompt abuse

</details>

---

**Q7.** A production LLM's hallucination rate on domain-specific queries has risen well above its evaluation baseline over several months. What should trigger the retraining/re-tuning decision?

A) A predefined threshold breach on continuous evaluation metrics (e.g., accuracy or hallucination rate) sustained across a defined monitoring window
B) A single user complaint submitted through customer support
C) A competitor releasing a newer model
D) An arbitrary calendar-based schedule regardless of observed metrics

<details>
<summary>Answer</summary>

**Correct: A**

Retraining/re-tuning decisions should be risk-based, driven by sustained breach of predefined evaluation thresholds, not anecdotal or arbitrary triggers.

**Why the others are wrong:**
- A single complaint is anecdotal and insufficient evidence of systemic drift
- Competitive pressure is a business consideration, not a security/quality trigger
- Calendar-only retraining ignores actual drift signals and may act too late or unnecessarily

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which logging element is MOST critical to retain for forensic reconstruction of an AI agent's decision chain during an incident investigation?

A) The full sequence of prompts, intermediate reasoning steps, tool calls with inputs/outputs, and timestamps across the session
B) The final response text only
C) The model version number only
D) Aggregate daily usage statistics

<details>
<summary>Answer</summary>

**Correct: A**

Forensic reconstruction of an agentic decision chain requires the complete session trace — prompts, reasoning, tool inputs/outputs, and timing — to understand how and why an action occurred.

**Why the others are wrong:**
- Final text output alone doesn't reveal the reasoning or tool actions that produced it
- Version number is static metadata, not the actual decision trace
- Aggregated statistics lose the per-incident detail needed for investigation

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

