## Chapter 2 Cheat Sheet — AI Asset, Data Lifecycle, and Policy Management

### Policy Hierarchy (highest → lowest)
| Level | Purpose | Mandatory? |
|---|---|---|
| Strategy | Direction/why AI is used | No (directional) |
| Policy | Mandatory rule (what must happen) | Yes |
| Standard | Specific measurable requirement | Yes |
| Procedure | Step-by-step how-to | Yes (operational) |
| Guideline | Recommended practice | No |

**Exam trap:** a numeric/field requirement (e.g., "minimum 5 fields in every risk assessment") = **Standard**, not Policy.

### AI Asset Inventory — Required Scope
| Asset Type | Examples |
|---|---|
| Models | Production, pilot, retired, third-party/embedded |
| Datasets | Training, validation, evaluation, fine-tuning sets |
| Pipelines | Orchestration/ETL, MLOps/CI-CD workflows |
| Prompts | Reusable prompt templates, system prompts |

**Exam trap:** answers scoping inventory to "models only" or "production only" are wrong — shadow/pilot assets must be included.

### Classification: Training vs. Inference Data
| Data Type | Primary Risk | Governance Focus |
|---|---|---|
| Training data | Aggregated/historical exposure, bias, reproducibility | Provenance, lineage, retention |
| Inference/prompt data | Real-time PII/sensitive exposure | Access control, DLP, logging |

### Provenance & Lineage Artifacts
| Artifact | Documents |
|---|---|
| Datasheet for Datasets | Dataset origin, collection method, known bias |
| Model Card | Trained model performance, limitations, intended use |
| Lineage graph/log | Transformation steps from raw data → deployed model |

### Retention / Decommissioning Triggers
- Regulatory or legal change creating a compliance gap
- Significant model/data drift or degraded performance
- Vendor/data source end-of-support or contract expiration
- Security incident or discovered bias/harm

### Shadow AI Remediation Sequence
1. Discover unsanctioned tool/model usage
2. Add to inventory + classify data/risk exposure
3. Apply proportionate control (block, approve with guardrails, DLP)
4. Update policy/training to prevent recurrence

### EU AI Act Quick Reference
| Tier | Examples | Obligation Level |
|---|---|---|
| Unacceptable | Social scoring, manipulative AI | Banned |
| High-risk | Hiring, credit scoring, medical devices | Strict (conformity, logging, human oversight) |
| Limited | Chatbots, deepfakes | Transparency disclosure |
| Minimal | Spam filters, AI in games | No specific obligation |

**Key dates:** In force Aug 1 2024 → Prohibitions Feb 2 2025 → GPAI rules Aug 2 2025 → Most high-risk obligations Aug 2 2026.

### NIST AI RMF Functions
Govern (continuous) → Map → Measure → Manage
