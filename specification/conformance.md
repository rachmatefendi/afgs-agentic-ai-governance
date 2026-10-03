# AFGS v1.0 — Stack conformance: SC0–SC3

**Source:** Specification §17; publication paper §§10–12.  
**Repository status:** Documentation distribution; no conformance level beyond the source's SC0 / SC1-capable statement is demonstrated here.

## Criteria transcribed from §17.2

| Level | Minimum substrate | Required evidence | Defensible claim |
| --- | --- | --- | --- |
| SC0 | Architecture / specification artifacts | Named components, jurisdictions, invariants, contracts, and declared implementation boundaries. | Governance architecture documented. |
| SC1 | Prompt / in-context orchestration | Behavioral tests for routing, source discipline, output form, escalation, and claimed limitations; failures recorded. | Best-effort behavioral compliance only. |
| SC2 | External registries + validators | External IAR/EPS/PCR or equivalents; schema/constraint validation; rejection of unresolved authority/evidence/state references; independent validation evidence. | Invalid or unbound governance artifacts can be externally rejected. |
| SC3 | External state machine + controlled egress / GEG | Externally enforced legal transitions; PECG/PESR; token checks; revocation; replay prevention; bypass testing; consequential mutation cannot reach controlled egress without current authorization. | Invalid state, phase, authority, or token cannot pass the deployment-controlled execution boundary. |

## Claim rule

> A deployment MAY claim only the highest level for which every required control is actually implemented and supported by conformance evidence. Passing a prompt-level test does not establish SC2 or SC3.

Source: §17.3.

## Conformance is not certification

The specification defines technical conformance criteria. It does not establish a certification authority or scheme (§17.1). An internal consistency check, an AI-assisted paper walkthrough, a formatted JSON example or a file-integrity check is not external validation or a production safety result.

| Object or assertion | Status of this repository |
| --- | --- |
| Normative architecture described | Yes, source-derived documentation and publication paper. |
| Canonical normative DOCX byte identity verified locally | No; original DOCX bytes not included. |
| SC1-capable source baseline | Reported by the source; not a newly run SC1 evaluation. |
| SC2 reference implementation | Not supplied or demonstrated. |
| SC3 controlled-egress enforcement | Not supplied or demonstrated. |
| Executable conformance suite | Not supplied; KL-R5 remains open implementation work. |
| Empirical metrics | Not reported as measured results in this repository. |
| External certification / independent human peer review | Not established. |

See [source identity](../provenance/README.md), [limitations](../research/limitations.md) and [evaluation targets](../research/evaluation.md).
