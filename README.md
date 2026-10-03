# AI Founder Governance Stack (AFGS) v1.0

> **Status: publication paper and non-normative companion documentation only; not a verified canonical frozen-baseline distribution or an implementation release.**

**Author:** Rachmat Efendi · **Version:** v1.0

Documentation of an architecture that separates AI-supported business operations, AI-system governance, material decisions, and consequential execution.

The source baseline declares **SC0 / SC1-capable**. This repository does not demonstrate deployed SC1 compliance, SC2/SC3 enforcement, empirical effectiveness, external certification, or independent human peer review.

## Start here

[Paper](paper/AFGS-v1.0.pdf) · [Specification guide](specification/AFGS-v1.0.md) · [Architecture](architecture/README.md) · [Conformance](specification/conformance.md) · [Source identity](provenance/README.md)

## The problem

AFGS addresses the conflation of analytical quality with authority to act. A convincing recommendation is not an approval, and an approval is not permission for an arbitrary action at a later time. The specification assigns these questions to separate components and binds consequential execution to current governance state. Source: paper, §§1–4.

## Three pillars, distinct jurisdictions

| Component | Responsibility | Must not become |
| --- | --- | --- |
| **AI Founder OS** | Business objectives, workstreams, lifecycle and operating state. | A source of tool permission, MDGR verdicts, or self-created authority. |
| **EASGF** | AI capability, source, tool, context, routing and validation governance. | A substitute for organizational approval or material-decision authority. |
| **MDGR** | Material-decision eligibility, binding constraints, verdicts and token eligibility. | A self-validating reasoning component or a second business operating layer. |
| **Shared governance substrate** | State, identity/authority, evidence, policy, events, controlled egress and audit. | Evidence that enforcement exists merely because it is specified. |

Source: specification §§2–4, reproduced in the [technical source excerpts](provenance/AFGS-v1.0-source-excerpts.txt).

## Execution permission is conjunctive

```text
Execution_Eligible =
    Business_Stage_Ready
AND Runtime_Authorized
AND Governance_Verdict_Allows
AND Authority_Valid
AND Policy_Current
AND Evidence_Preconditions_Valid
AND Human_Approval_Valid_If_Required
AND Execution_Token_Valid
AND PECG_Passed
```

Under the specified semantics, a mandatory term that is **FALSE or UNRESOLVED** prevents the current attempt from executing. A missing human-approval requirement is not equivalent to `NOT_REQUIRED`. These are design requirements; their enforcement depends on implementation and evidence. Source: specification §5; see [execution semantics](architecture/execution-semantics.md).

## Contents

| Path | Contents |
| --- | --- |
| `paper/` | Original 14-page publication PDF and bibliographic information. |
| `specification/` | Reading guide, GS-I1–GS-I12, SC0–SC3 criteria and T01–T15. |
| `architecture/` | Architecture overview and execution semantics using PECG/PESR. |
| `schemas/` | Minimum contract inventory; formal schemas are not supplied. |
| `examples/` | Six illustrative JSON contract objects; not live permissions. |
| `research/` | Implementation roadmap, evaluation targets and limitations. |
| `tests/`, `reference-implementation/` | Availability statements; no executable conformance suite or runtime. |
| `provenance/` | Selected technical source passages and distinct artifact identities. |
| `.github/` | Public issue and pull-request templates. |
| `release/` | Public release description for `v1.0-spec`. |

## Artifact identity

The paper identifies a canonical normative DOCX by SHA-256:

```text
cce49a17697e91aefa409c28c6650d79aeca1dba3cb01deea4838abbf72d32a6
```

**The canonical DOCX is not included, and its declared hash has not been verified.** The 14-page publication PDF and technical excerpts from the 33-page source are separate artifacts. The excerpts are not the complete source transcript or an authenticated copy of the DOCX. Neither their checksums nor this repository establish canonical equivalence. **Do not cite the excerpts or companion pages as a verified canonical baseline.**

See [artifact provenance](provenance/README.md), [manifest](provenance/manifest.json) and [SHA256SUMS](SHA256SUMS).

## Review

Report contradictions, ambiguous interfaces, unsupported claims or concrete counterexamples using [CONTRIBUTING.md](CONTRIBUTING.md). A review, issue, fork or pull request does not amend the normative baseline or confer approval authority.

## Citation and licensing

Cite the paper using [CITATION.cff](CITATION.cff) or [CITATION.bib](CITATION.bib).

The paper retains **CC BY-ND 4.0**. **No separate license grant is made for the source excerpts, examples or companion documentation.** This is not a repository-wide open-source or modifiable-specification license. Existing license rights, applicable exceptions and GitHub platform rights remain unaffected. See [LICENSE.md](LICENSE.md).
