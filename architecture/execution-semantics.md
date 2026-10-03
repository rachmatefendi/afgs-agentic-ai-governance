# AFGS v1.0 — Execution semantics

**Document class:** Source-derived companion, not an implementation.  
**Source:** Frozen specification §§5–14.

## Conjunctive predicate

The following predicate is transcribed from §5.1:

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

Any mandatory `FALSE` or `UNRESOLVED` term prevents the current attempt from executing. `DENY`, `HOLD` and `ESCALATE` are non-execution outcomes for that attempt. A subsequent authorized transition and a fresh evaluation of the entire predicate are required before execution can occur (§5.1).

## Human approval

| Requirement state | Evaluation | Source requirement |
| --- | --- | --- |
| `NOT_REQUIRED` | TRUE | PCR/IAR explicitly declare no HITL requirement for this action class and scope. |
| `REQUIRED` + valid approval | TRUE | Approval is authenticated, jurisdiction-valid, scope-matched, current and not revoked. |
| `REQUIRED` + no valid approval | FALSE | Execution denied. |
| `UNRESOLVED` | FALSE | Fail-closed; absent or ambiguous configuration does not grant autonomous permission. |

Source: §5.2. The existence of a person's authority and that person's actual approval of an action remain different questions.

## Materiality boundary

Under §6, extraction first produces structured materiality inputs; DMI evaluates them against deterministic PCR predicates. A deterministic evaluator does not make probabilistic extraction deterministic. Consequential extraction gaps, low confidence or disagreement result in `MATERIALITY_UNKNOWN`, which cannot silently enter consequential execution.

Materiality is evaluated over policy-defined linked-decision scope, including cumulative exposure where relevant. The source does not supply a universal currency threshold, aggregation window or confidence constant.

## Validity windows

The following temporal relations are transcribed from §8.2:

```text
t_verdict_issued <= t_condition_deadline <= t_verdict_expires

t_verdict_issued <= t_conditions_satisfied <= t_token_issued < t_token_expires
```

A condition satisfied after verdict expiry requires revalidation and a renewed/new verdict before token eligibility. Timestamps are evaluated against the trusted time source described in §11.7.

## Controlled egress, PECG and PESR

GEG governs the deployment-controlled egress boundary (§11.1). The source's PECG composition includes PESR, current-state/policy/authority/condition checks, an execution lease or short-lived reservation, push-buffer plus authoritative-pull revocation checks, idempotency, replay prevention, scope matching, required human approval, and compensation/reconciliation semantics (§11.2).

PESR reads must come from the authoritative system of record or a replica with a demonstrated lag bound within the configured maximum staleness. Failure to establish freshness or trusted time prevents consequential execution (§§11.6–11.7). The source does not claim atomic control inside downstream third-party systems (§11.3).

## Revocation and overrides

A policy, authority, evidence, scope, dependency, condition or validity change can trigger re-entry (§8.1). Overrides are new auditable transitions, not in-place edits to old verdicts; a newly permissible action needs a new current token (§12.3). Ordinary overrides and break-glass cannot override non-derogable constraints (§12.1).

Policy changes that weaken the governance perimeter are themselves material governance actions, not ordinary registry edits (§10.5).

## Failure and continuity

Consequential transitions and execution fail closed when mandatory dependencies are unavailable. Policy may permit explicitly degraded read-only/advisory work. Last-Known-Good snapshots must satisfy their own integrity, trust-anchor, TTL and revocation conditions; their existence does not restore authority by default (§§10.4, 14).

The selected technical sections, including the failure matrix, are reproduced in [technical source excerpts](../provenance/AFGS-v1.0-source-excerpts.txt). This page does not add a runtime guarantee.
