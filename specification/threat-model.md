# AFGS v1.0 — Threat model and traceability

**Source:** Frozen specification §16, pp. 21–22.  
**Representation:** Source-text table transcription; layout normalized.

The register contains **15 threats**. It defines control boundaries and verification targets, not results from an executed attack campaign.

| ID | Threat | Invariants | Primary control boundary | Verification metric / hook |
| --- | --- | --- | --- | --- |
| T01 | Material-Gate Miss | GS-I4, GS-I11 | Extraction layer + DMI + materiality-unknown routing | Material Gate Recall; miss analysis |
| T02 | Material-Gate Overreach | GS-I11 | MDGR triage de-escalation + precision testing | Material Gate Precision; unnecessary escalation rate |
| T03 | State Divergence | GS-I2, GS-I10 | Versioned state + event sourcing + PECG/PESR | State mismatch incidents; divergence detection latency |
| T04 | Authority Spoofing | GS-I1, GS-I8 | IAR validation; authenticated authority references | Authority-spoof detection; unauthorized execution attempts rejected |
| T05 | Evidence Semantic Drift | GS-I5 | EPS canonical semantics; provenance/version checks | Evidence binding accuracy; stale/superseded evidence detection |
| T06 | Condition Stripping | GS-I6 | Verdict/token binding; downstream schema validation | Condition persistence rate |
| T07 | Phase Laundering | GS-I3, GS-I9, GS-I12 | MDGR control-plane phase validation | Illegal phase-transition rejection |
| T08 | Execution Bypass | GS-I3, GS-I7, GS-I9 | GEG controlled egress; least privilege | Bypass attempts; ungoverned execution count |
| T09 | TOCTOU Drift | GS-I7 | PECG + PESR + lease/reservation + revocation checks + trusted time (§11.7) | Stale-state execution rejection; revalidation latency |
| T10 | Token Replay | GS-I7 | Single-use nonce + idempotency + token status | Replay rejection rate |
| T11 | Cross-Project Leakage | GS-I2, GS-I5 | Workstream isolation; scoped references; EASGF source policy | Cross-project leakage incidents |
| T12 | Direct Rule / Prompt Injection | GS-I2, GS-I9 | External state/policy precedence; context sanitization | Governance-state mutation attempts blocked |
| T13 | Policy Capture / Staleness | GS-I9, GS-I10 | PCR provenance; versioning; expiry; appeal; LKG constraints; material policy mutation gate (§10.5) | Policy-drift incidents; time to revalidation |
| T14 | Validator Circularity | GS-I12 | Reasoning/control-plane separation; independent deterministic/human control | Validator-independence compliance |
| T15 | Ceremonial Human Rubber Stamp | GS-I8 | Risk-tier HITL; SoD; rationale and review requirements | Approval quality review; override/approval anomaly rate |

## Cross-cutting scope-splitting

The source treats scope-splitting as a cross-cutting variant of Material-Gate Miss and Execution Bypass. Linked-decision aggregation must consider policy-defined relationships and cumulative exposure, not just single transactions or a universal fixed time window (§16.1; §6.4).

The controls and hooks above are specified requirements and evaluation targets, not measurements or evidence of deployed protection. Source text: [technical source excerpts](../provenance/AFGS-v1.0-source-excerpts.txt).
