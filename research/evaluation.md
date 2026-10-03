# AFGS v1.0 — Evaluation targets

**Source:** Frozen specification §18, p. 24.  
**Status:** Specified verification targets or proposed acceptance criteria. No empirical evaluation results are reported by this repository.

The following table is transcribed from the source. Numbers describe proposed thresholds or required harness outcomes, **not observed performance**.

| Metric | What it tests | Source verification position |
| --- | --- | --- |
| Material Gate Recall | Mandatory material cases reaching MDGR | Proposed benchmark threshold ≥99.9% for the defined benchmark suite; dataset and confidence interval MUST be reported. |
| Material Gate Precision | Unnecessary material escalations | Benchmark-specific target; required to prevent governance DoS. |
| Unauthorized Execution | Execution without valid authority | Required conformance-suite outcome: 0 observed unauthorized executions; not a universal 0% guarantee. |
| State Mismatch | Execution attempted under divergent state | Required harness outcome: 0 successful stale-state executions. |
| Condition Persistence | PERMIT-C conditions preserved downstream | Required harness outcome: all binding conditions preserved in tested paths. |
| Revocation Propagation Latency | Revocation event to GEG awareness | Report p50/p95/p99 against deployment-configured SLO. |
| Maximum Revocation Staleness | Longest accepted stale revocation state | MUST remain below configured maximum staleness threshold. |
| Replay Rejection | Repeated execution-token use | Required harness outcome: all defined replay attempts rejected. |
| Override Integrity | Unauthorized/unauthenticated override attempts | Required harness outcome: 0 accepted unauthorized overrides. |
| Human Review Burden | Human governance workload | Measured; no universal target. |
| Governance Latency / Cost | Additional time and compute | Measured by tier and use case; no universal target. |
| Decision Utility / False Block | Value lost through over-governance | Must be measured so safety is not achieved merely by blocking everything. |

The proposed ≥99.9% recall target must not be presented as an achieved benchmark result. “0 observed unauthorized executions” is a defined-suite acceptance requirement, not a universal safety guarantee. The existing source requires measurement of over-governance and utility loss as well as false allows.

Runtime, policy, dataset, deployment-configured bounds and measured results remain future evaluation work. Ground-truth fixtures and an executable evaluation harness are not supplied. See [test-suite status](../tests/README.md), [limitations](limitations.md) and [technical source excerpts](../provenance/AFGS-v1.0-source-excerpts.txt).
