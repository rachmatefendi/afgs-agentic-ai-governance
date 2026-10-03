# AFGS v1.0 — Implementation roadmap

**Source:** Frozen specification §21.  
**Status:** Existing roadmap, not a commitment that any step has been implemented or authorized for execution in this repository.

| Step | Source work item | Outcome described by the source |
| --- | --- | --- |
| 1 | Materiality Policy & Canonical State Machine | Production-grade policy objects, legal transitions, linked-decision scope and state invariants. |
| 2 | Formal JSON Schema / Protobuf Contracts | Machine-validated envelope, verdict, token, IAR/EPS/PCR, override, revocation and error objects. |
| 3 | SC2 Reference Implementation | External validator middleware, registries and state engine. |
| 4 | Conformance Test Suite & Adversarial Benchmark | Ground-truth fixtures and scope-splitting, authority, staleness, revocation, bypass and circularity tests; addresses KL-R5. |
| 5 | SC3 Enforcement Implementation | GEG, PECG/PESR, tokens, revocation, controlled egress, resilience, idempotency, reconciliation and trusted time. |
| 6 | Empirical Evaluation | Measured false allow/block, materiality precision/recall, latency, cost, human burden and utility loss. |
| 7 | External Validation / Independent Certification, if established | A separate assurance milestone, not implied by conformance. |


These are implementation and evaluation work items, not delivered capabilities. See [limitations](limitations.md), [conformance](../specification/conformance.md) and the selected §21 steps in [the source excerpts](../provenance/AFGS-v1.0-source-excerpts.txt).
