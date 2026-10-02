## Chapter 7: AI Security Architecture and Secure Deployment Patterns — Practice Questions

**Q1.** An agentic AI assistant has a tool that can initiate wire transfers. The tool currently executes any transfer the model requests without further review, and losses have occurred from manipulated prompts. Which control BEST addresses this under a least-privilege agentic design?

A) Lower the model's temperature setting to make outputs more deterministic
B) Log all completed transactions to a SIEM for after-the-fact review
C) Retrain the model on a larger, more diverse transaction dataset
D) Require human approval for transactions above a defined risk threshold before execution

<details>
<summary>Answer</summary>

**Correct: D**

This maps to OWASP LLM06 (Excessive Agency). A preventive human-in-the-loop approval gate for high-risk, irreversible actions is the standard least-privilege control for agentic tool use.

**Why the others are wrong:**
- Temperature affects output variability, not authorization or agency scope — it doesn't prevent unauthorized actions.
- Logging is a detective control; the transfer has already occurred, so damage is not prevented.
- More training data addresses model accuracy/bias, not the authorization boundary of the tool itself.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A RAG-based internal knowledge assistant retrieves and summarizes documents from a shared vector store containing files with different confidentiality levels. Users report seeing summarized content from documents they should not have access to. What is the ROOT cause and BEST fix?

A) The retrieval layer does not enforce document-level access control matching the querying user's identity; add identity-aware access control at retrieval time
B) The output filter fails to redact keywords; add a stronger keyword-based redaction list
C) The vector database is unencrypted at rest; enable encryption
D) Chunk sizes are too large; reduce chunk size to limit exposure per retrieval

<details>
<summary>Answer</summary>

**Correct: A**

In secure RAG architecture, authorization must be enforced at the retrieval layer (row/document-level ACLs tied to the requesting user's identity), not left to the generation model or output filter.

**Why the others are wrong:**
- Keyword redaction is unreliable and treats a symptom, not the missing authorization check.
- Encryption at rest protects against storage theft, not against an authorized-looking query returning unauthorized content.
- Chunk size affects granularity of leakage, not whether the user was authorized to see the content at all.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An organization is designing a secure ML pipeline and wants to prevent a compromised training environment from directly affecting production inference. Which architecture decision BEST achieves this?

A) Separate training and production into distinct isolation zones connected only through a governed model registry that gates promotion after validation
B) Run training and inference in the same network segment with shared credentials for simplicity
C) Allow the training pipeline to write directly to the production model endpoint for faster deployment
D) Use the same service account for both training jobs and inference API calls

<details>
<summary>Answer</summary>

**Correct: A**

Reference secure ML pipeline architecture segments training and production into separate trust zones, with a model registry acting as a controlled gate that enforces validation/approval before promotion.

**Why the others are wrong:**
- Shared network segments and credentials remove the isolation boundary entirely, defeating the purpose of segmentation.
- Direct writes to production bypass validation and approval gates, increasing the blast radius of a compromised training pipeline.
- Shared service accounts violate least-privilege identity design and make it impossible to scope or revoke access independently.

</details>

---

**Q4.** Which OWASP Top 10 for LLM Applications (2025) risk category specifically describes an AI agent being granted more functionality, permissions, or autonomy than necessary for its task, resulting in unintended or harmful actions?

A) LLM02: Sensitive Information Disclosure
B) LLM09: Misinformation
C) LLM10: Unbounded Consumption
D) LLM06: Excessive Agency

<details>
<summary>Answer</summary>

**Correct: D**

LLM06: Excessive Agency directly addresses agents with overly broad permissions, functions, or autonomy that lead to unintended actions — the core issue in agentic tool-use isolation.

**Why the others are wrong:**
- LLM02 concerns leakage of confidential data through model outputs, not excessive permissions.
- LLM09 concerns the model generating false or misleading content, unrelated to permission scope.
- LLM10 concerns resource exhaustion (e.g., denial of wallet/service), not permission scope.

</details>

---

**Q5.** A security architect must choose a defense against indirect prompt injection, where malicious instructions are embedded inside documents retrieved by a RAG pipeline. Which pattern is MOST effective?

A) Increase the model's context window so more of the document can be reviewed
B) Treat retrieved content strictly as untrusted data using delimiters and instruction-hierarchy enforcement so it cannot override system instructions
C) Disable retrieval logging to reduce the attack surface
D) Fine-tune the model exclusively on the organization's trusted documents

<details>
<summary>Answer</summary>

**Correct: B**

The core secure RAG pattern for indirect prompt injection is to structurally separate trusted system/developer instructions from untrusted retrieved data, enforcing an instruction hierarchy the model cannot bypass.

**Why the others are wrong:**
- A larger context window does not prevent malicious instructions embedded in the additional content from being processed as commands.
- Disabling logging removes visibility needed for detection and forensics — it does not stop the injection.
- Fine-tuning does not eliminate runtime injection risk from documents ingested after training and does not enforce trust boundaries.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** In a layered guardrail architecture for an LLM application, which is the CORRECT processing order for a user request through the system?

A) Output filtering → model inference → input filtering → policy enforcement
B) Policy enforcement → output filtering → model inference → input filtering
C) Model inference → input filtering → output filtering → policy enforcement
D) Input filtering → model inference → output filtering → policy enforcement/escalation for high-risk results

<details>
<summary>Answer</summary>

**Correct: D**

Standard guardrail architecture screens the request first (input filtering for prompt injection, PII, jailbreak attempts), runs inference, screens the response (output filtering for toxicity, leakage, hallucination), and finally applies policy enforcement or human escalation for high-risk outputs.

**Why the others are wrong:**
- Filtering output before inference is logically impossible — there is no output to filter yet.
- Enforcing policy before any input or output has been generated or evaluated provides no basis for a decision.
- Running inference before input filtering allows unfiltered malicious input to reach the model unchecked.

</details>

---

**Q7.** For agentic AI systems that call external tools/APIs on behalf of users, which credential management approach BEST supports least-privilege and auditability?

A) A single long-lived API key shared across all agents and sessions
B) Hardcoded credentials embedded in the agent's system prompt
C) A shared service account with administrator-level access to all connected tools
D) Short-lived, session-scoped credentials issued per agent invocation with permissions limited to the specific tool call

<details>
<summary>Answer</summary>

**Correct: D**

Least-privilege agentic design requires short-lived, narrowly scoped, session-bound credentials so that a compromised agent session or leaked token has minimal blast radius and actions remain individually auditable.

**Why the others are wrong:**
- Shared long-lived keys cannot be scoped per session and create a large blast radius if leaked.
- Prompt-embedded credentials are exposed to prompt injection and leakage risks (e.g., system prompt leakage).
- Broad admin-level shared accounts violate least privilege and make it impossible to attribute actions to a specific agent session.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** What is the primary purpose of establishing 'isolation zones' in a secure ML architecture?

A) To increase model accuracy by separating training data by geography
B) To reduce cloud compute costs by consolidating resources
C) To separate components with different trust levels or data sensitivity so a compromise in one zone does not automatically compromise others
D) To simplify deployment by removing the need for access control

<details>
<summary>Answer</summary>

**Correct: C**

Isolation zones enforce trust boundaries between components (e.g., raw data, feature store, training, model registry, inference) so that compromise, misconfiguration, or excessive access in one zone is contained and does not propagate.

**Why the others are wrong:**
- Geographic separation of data is a data residency/sovereignty concern, not the security purpose of isolation zones.
- Isolation zones typically add architectural overhead rather than reduce cost — cost reduction is not their purpose.
- Isolation zones exist specifically to enforce access control between boundaries, not remove it.

</details>

---

