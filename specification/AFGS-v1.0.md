# AFGS v1.0 — Specification reading guide

**Document class:** Non-normative companion / source navigation  
**Source:** AFGS v1.0 Frozen Normative Baseline, Normative Integration & Conformance Specification  
**Author:** Rachmat Efendi  
**Source date:** August 2026  
**Current source conformance claim:** SC0 / SC1-capable

This guide does not replace the frozen specification. Selected technical passages are available in [the source excerpts](../provenance/AFGS-v1.0-source-excerpts.txt). They are not a complete transcript or an authenticated canonical copy; see [artifact identity](../provenance/README.md).

## Canonical definition

> AI Founder Governance Stack is a three-pillar architecture composed of AI Founder OS, EASGF, and MDGR, bound by a shared integration, state, authority, evidence, execution, and assurance substrate.

Source: frozen specification §1.1.

## Boundaries that determine interpretation

AFGS is not a monolithic agent, a universal autonomous system, a substitute for human professional or organizational authority, or a claim that model reasoning is sufficient for execution (§1.4). The terms MUST, MUST NOT and SHALL are mandatory in the source; SHOULD is the recommended default and MAY is optional where justified and auditable (§1.5).

The separation is explicit: skill activation, tool authorization, source authorization, decision approval, human authority and execution permission are distinct (§2). The actual external enforcement boundary is the deployment-controlled egress point, not a guarantee of atomicity in a bank, counterparty or external API (§3.1 and §11.1).

The model-assisted reasoning plane may propose findings. It cannot independently establish the binding state, authority or constraint satisfaction on which its own verdict depends (§7; GS-I12).

## Technical source index

| Section | Source heading |
| --- | --- |
| 1 | Canonical Definition, Scope & Terminology |
| 2 | Architectural Thesis & Jurisdiction |
| 3 | Reference Architecture & Shared Governance Substrate |
| 4 | Unified State Model & State Precedence |
| 5 | Effective Execution Predicate & Human Approval Semantics |
| 6 | Material Decision Gate, DMI & Linked-Decision Aggregation |
| 7 | MDGR Hybrid Trust Boundary |
| 8 | Re-Entry & Normative Temporal Consistency |
| 9 | Integration Protocol & Error Semantics |
| 10 | Core Registries, LKG Snapshots & Material Policy Mutation |
| 11 | Governed Execution Gateway, PECG/PESR & Revocation |
| 12 | Human Governance, Override & Break-Glass |
| 13 | Shared Event Model & Auditability |
| 14 | Substrate Failure & Degraded-Mode Policy |
| 15 | Cross-Pillar Hard Invariants GS-I1–GS-I12 |
| 16 | Threat Model & Traceability Matrix |
| 17 | Stack Conformance Criteria SC0–SC3 |
| 18 | Assurance, Metrics & Proposed Acceptance Criteria |
| 19.3 | Controlled Amendment Flow |
| 20.4 | Known-Limitations Register — selected passages |
| 21 | Post-Freeze Implementation Roadmap — steps 1–7 |
| Appendix A | Canonical Contract Schemas |

The Appendix A heading describes the source contract inventory; it does not indicate that executable JSON Schema files are supplied. Formal contracts remain implementation work under §21.

## Focused reading paths

| Question | Source sections | Companion |
| --- | --- | --- |
| Who owns which state? | §§2–4 | [Architecture](../architecture/README.md) |
| When can an action execute? | §§5, 8, 11–14 | [Execution semantics](../architecture/execution-semantics.md) |
| What makes a decision material? | §6 | [Execution semantics](../architecture/execution-semantics.md) |
| Which invariants and threats apply? | §§15–16 | [Invariants](invariants.md), [threat matrix](threat-model.md) |
| What can this documentation support? | §17; paper §§10–12 | [Conformance](conformance.md), [limitations](../research/limitations.md) |
| What remains to be implemented? | §21; Appendix A | [Roadmap](../research/roadmap.md), [contract inventory](../schemas/README.md) |

## Version and authority

This guide describes AFGS v1.0, including GS-I1–GS-I12, T01–T15 and PECG/PESR. It is a non-normative companion. Changes to normative meaning require the controlled process in §19.3; an edit to this guide does not amend the baseline.
