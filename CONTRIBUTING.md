# AFGS v1.0 — Review and contribution

The source record identifies AFGS v1.0 as a frozen normative baseline. This repository distributes the paper and non-normative supporting documentation; it does not supply the byte-verified canonical DOCX. A review contribution is a proposal, not an approval, a certification, a license grant or an amendment.

## Useful submissions

Report a concrete contradiction, ambiguous contract, missing enforcement boundary, source/claim mismatch, or counterexample. Identify the artifact and section, the affected invariant or threat where relevant, the evidence, and the smallest correction or clarification that would resolve the issue. Distinguish a documentary observation from a result obtained on a real implementation.

The [specification-review template](.github/ISSUE_TEMPLATE/specification-review.md) captures those fields. Stylistic suggestions and optional extensions should not be presented as acceptance blockers.

## Frozen baseline versus companion documentation

Do not overwrite or regenerate an original canonical artifact as a documentation cleanup. Publication-paper revisions, normative amendments, implementation profiles and companion-document corrections remain separate change objects.

Material changes follow the source's §19.3 flow:

```text
Change Request -> Impact Classification -> Architecture / Security /
Governance Review -> Schema & Test Impact -> Red-Team / Regression Update
-> Approval Record -> Versioned Release -> Migration / Deprecation Notice
where required
```

This is the source procedure. A written contribution process does not itself enforce branch protection, required review or approval authority.

## Evidence and claims

Label tests as proposed or executed. Executed results need an identifiable implementation, test inputs and actual output; do not infer enforcement from a prompt or formatted example. Source-reported historical validation is not independent replication. Do not add “passing” badges without corresponding test evidence.

## Rights and sensitive material

Read [LICENSING.md](LICENSING.md) before reproducing or redistributing source text. The paper and source excerpts are licensed under CC BY-ND 4.0 (no public sharing of adaptations); companion documentation and examples are licensed under CC BY 4.0. By submitting a contribution to companion material, you agree that it may be distributed under CC BY 4.0. Prefer review commentary and clearly separate proposals written in your own words. Do not submit credentials, customer records, private corporate approvals or material you lack permission to share.

The specification owner identified by the source is Rachmat Efendi. A pull request, reviewer comment or AI recommendation does not exercise that owner's approval authority.
