# AFGS v1.0 — Illustrative contract examples

**Status: ILLUSTRATIVE SOURCE EXAMPLES — NOT LIVE STATE, NOT TEST RESULTS.**

These six JSON objects are extracted from the frozen specification with keys and values preserved; indentation is normalized. No new example entities, thresholds, timestamps or permissions have been added.

| File | Source section | Object |
| --- | --- | --- |
| [stack-governance-envelope.json](stack-governance-envelope.json) | §9.1 | Stack Governance Envelope |
| [mdgr-verdict.json](mdgr-verdict.json) | §9.2 | MDGR Verdict Contract |
| [error-timeout-envelope.json](error-timeout-envelope.json) | §9.3 | Error & Timeout Envelope |
| [execution-token.json](execution-token.json) | §11.4 | Execution Token Contract |
| [human-override.json](human-override.json) | §12.3 | Human Override Contract |
| [shared-event.json](shared-event.json) | §13 | Shared Event Model |

## Interpretation boundary

The objects are individual illustrative snapshots, not a complete executable end-to-end fixture. Different state versions and object scopes must not be treated as automatically reconciled. Reference URIs, actors, amounts, nonces and statuses are source-example values, not real connected services or authorizations. `AUTHORIZED`, `VALID` and `PERMIT_WITH_CONDITIONS` inside an example are data strings, not approvals to act.

A source example may omit fields needed by the minimum contract inventory or a real implementation. The objects are preserved rather than silently enriched. Parseability does not establish schema completeness, registry resolution, authority validity, temporal completeness or AFGS conformance.

See [contract inventory](../schemas/README.md) and [technical source excerpts](../provenance/AFGS-v1.0-source-excerpts.txt).
