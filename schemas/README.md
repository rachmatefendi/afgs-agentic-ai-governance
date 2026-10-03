# AFGS v1.0 — Contract inventory and formal-schema status

**Status: FORMAL SCHEMAS NOT INCLUDED.**

The frozen source contains a minimum contract set and illustrative JSON objects. Formal JSON Schema / Protobuf contracts are explicitly post-freeze implementation work (§21, Step 2). The examples below do not define a formal contract for types, required fields, enums, reference resolution, cross-object constraints or version semantics.

## Minimum contract set

Transcribed from Appendix A.1:

| Contract | Minimum purpose |
| --- | --- |
| Stack Governance Envelope | Cross-pillar request, scoped state refs, materiality state, policy/authority/evidence refs. |
| MDGR Verdict | Bounded outcome, state version, policy snapshot, authority refs, findings, conditions, validity, re-entry triggers. |
| Execution Token | Actor, action, scope, state/policy/authority bindings, issue/expiry, nonce, idempotency key, status. |
| Human Override Event | Override class, actors, authority, justification, scope, validity, review requirements, new-verdict requirement. |
| Revocation Event | Token/verdict/decision refs, revocation reason, authority, timestamp, state version, acknowledgement state. |
| Error & Timeout Envelope | Failure class, component, retryability, mutation state, execution allowance, fallback mode, next action. |
| IAR Object | Identity, roles, delegated authority, SoD, conflicts, expiry, vetoes. |
| EPS Object | Evidence ID, source, issuer, hash, version, effective/retrieval dates, authority/freshness/verification, derivation. |
| PCR Object | Constraint ID, issuer, authority, jurisdiction, version, effective window, type, priority, evaluation mode. |
| Shared Event | Event type, origin, actor, prior/new state refs, triggers, policy/authority refs, reason code. |

## Source URI schemes

| Scheme | Source use |
| --- | --- |
| `afos://` | AI Founder OS business and operating-state references. |
| `easgf://` | EASGF runtime, capability, routing and validation references. |
| `mdgr://` | MDGR decision, verdict, finding and governance-state references. |
| `iar://` | Identity and authority references. |
| `eps://` | Evidence and provenance references. |
| `pcr://` | Policy and constraint references. |
| `sub://` | Shared substrate state/event/internal service references. |

Source: Appendix A.2. These are specification reference schemes, not live network endpoints.

The [six extracted JSON examples](../examples/README.md) can be parsed as JSON. That does not make them a formal schema, a complete interoperable contract, a validated authority record, or an executable permission. Future formalization belongs to a separately reviewed implementation/profile change, not a silent rewrite of v1.0.
