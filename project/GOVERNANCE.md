# MTL-XF-025 — Governance and decision controls

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Authority and accountability

**Director of Economic Development & Business Resilience** owns business scope, prioritisation assumptions, accepted analytical limitations and investigation recommendations. The Mettelo review panel owns programme acceptance. Operational responsibilities are in [business context](BUSINESS_CONTEXT.md); delivery-role artefacts are in [the project brief](PROJECT_BRIEF.md).

The Data Governance Analyst approves source identity, metadata, licence evidence and field support. The Data Engineer owns transformations and reruns. Domain specialists approve interpretation; a distinct reviewer checks critical calculations and executes or reviews DT1–DT10. Combining delivery roles does not remove review accountability.

## Stage gates

| Gate | Accountability | Required review |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Release resources and metadata link verified; ZIP members, event coverage, sector/location schema and frozen checksums pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Economic Development & Business Resilience + operational stakeholders | Within each comparable jurisdiction/procedure, compare three-month and six-month count signals. For coded sectors, show event concentration with uncoded records as a separate group. Geographic candidates require documented mapping coverage; below 90% mapping coverage, label the geography result exploratory and place it in an evidence-review queue. The 90% gate is a project design choice, not an official threshold. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

## Data/source control

Use the [source register](../data/SOURCE_REGISTER.md) as the authoritative evidence record. Preserve agreed URLs and explicitly label new required references, supplements and fallbacks. Record each actual file's resolved URL, retrieval UTC, release, scope, bytes, checksum and licence notices. Public access alone is not proof of unrestricted redistribution. No raw-data upload is part of this update.

Freeze input files only after the source-to-deliverable matrix passes; retain original bytes in an approved location and never overwrite a snapshot. A fallback must have a documented activation reason, compatible coverage and version-selection rule. Do not stack overlapping combined and fallback inputs.

## Domain interpretation

- Counts do not measure insolvency risk per business without a compatible business-population denominator.
- Public company records must not become personal profiles; omit unnecessary names and addresses from outputs.
- Retrospective insolvency indicators are not validated predictive early warnings; forecasting is optional and requires time-based evaluation.

**Primary risk:** Connected-company events and incomplete coding may be mistaken for broad local economic distress.

The [metric contract](DELIVERABLES.md) and [domain tests](ACCEPTANCE_CRITERIA.md) govern calculations. Thresholds/weights that are project choices must be labelled as such, with baseline and alternative scenarios; they are not official service standards. No automatic allocation or regulatory/professional certification is implied.

## Core and extension change control

Risk per active business, trading-site exposure, predictive early warning and causal support effectiveness require additional denominators/evaluation. If the ZIP lacks a required breakdown, use a registered official industry table for sector analysis; do not infer it from company names.

Every source/scope change records requester, date, reason, old/new requirement, coverage/schema impact, affected KPIs/artefacts/tests, owner, reviewer and decision. Missing mandatory evidence blocks the dependent release; it is not resolved by relabelling a promised deliverable unavailable. Optional models need a naive baseline, appropriate holdout, leakage checks, uncertainty and a named reviewer.

## Reuse, information and repository controls

Never commit secrets, private correspondence or unnecessary personal details. Preserve suppression and publication notices. Check screenshots and exports for permitted publication. The team repository must be under Mettelo with individual member accounts, evidence-linked contributions and reviews. Record environment, manifest and final commit/tag so reviewers can reproduce results without paid-only access. Accurately describe verified participation; do not claim real-client employment, endorsement, operational adoption or achieved savings.
