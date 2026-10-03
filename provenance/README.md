# AFGS v1.0 — Source provenance and artifact identity

**Publication paper and non-normative documentation. The canonical DOCX is not included and its declared hash is not verified.**

## Distinct artifacts

| Object | Identity | Distribution status |
| --- | --- | --- |
| Canonical normative specification | `AFGS_v1.0_Frozen_Normative_Baseline.docx`; identified on the publication paper's cover. | Original bytes not included; declared hash not verified. |
| Publication paper | [14-page PDF](../paper/AFGS-v1.0.pdf). | Original bytes preserved; a separate measured checksum. |
| Technical source excerpts | [Selected passages](AFGS-v1.0-source-excerpts.txt) from a retrieved-text representation of the 33-page specification. | Non-normative reference; not a complete transcript or an authenticated canonical copy. |
| Companion documentation and JSON examples | Source-derived descriptions, tables and illustrative contract objects. | No independent baseline authority or execution permission. |

## Declared canonical identity

```text
SHA-256: cce49a17697e91aefa409c28c6650d79aeca1dba3cb01deea4838abbf72d32a6
```

This identity is **source-declared**, not verified against original DOCX bytes. The paper, source excerpts and companion pages are different objects and do not replace that file. Do not cite them as a byte-verified canonical baseline.

## Scope of the excerpts

| Source section | Included material |
| --- | --- |
| §§1–18 | Definitions, jurisdictions, architecture, state, execution, materiality, contracts, controls, invariants, threats, conformance and evaluation criteria. |
| §19.3 | Controlled amendment procedure. |
| §20.4 | Selected limitation and consequence passages; the organizational-taxonomy implementation requirement is retained. |
| §21 | Implementation roadmap, steps 1–7. |
| Appendix A | Minimum contract set and reference URI schemes. |

Source numbering and source-page references are preserved. Running headers are removed; line wrapping and flattened table extraction are otherwise retained. Only the listed passages are included. The excerpts do not purport to reproduce the entire 33-page document or amend it.

Companion tables normalize layout for readability. The six JSON examples preserve the source's keys and values. Their identifiers, timestamps and permissions are illustrative, not live state.

## Integrity and evidence boundaries

[manifest.json](manifest.json) distinguishes the source-declared canonical identity, the source-text representation used for the excerpts, and the measured identities of the included artifacts. [SHA256SUMS](../SHA256SUMS) covers repository files except itself.

Checksums identify file bytes; they do not authenticate source assertions, grant authority, establish peer review, or demonstrate SC1/SC2/SC3 conformance. See [conformance](../specification/conformance.md) and [limitations](../research/limitations.md).

The [paper](../paper/README.md) retains its original license. Source excerpts, examples and companion documentation receive no additional license grant; see [LICENSE.md](../LICENSE.md).
