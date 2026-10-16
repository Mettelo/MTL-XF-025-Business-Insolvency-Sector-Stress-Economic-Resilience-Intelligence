# MTL-XF-025 — Business Insolvency, Sector Stress & Economic Resilience Intelligence

**Mettelo Project Studio** · Cross-Functional · Master project specification  
**Client:** Confidential Economic Development & Business Resilience Directorate  
**Accountable simulated executive:** Director of Economic Development & Business Resilience  
**Sector:** Business Resilience / Economic Development  
**Team:** 6–8 people · **Window:** 8 weeks  
**Status:** documentation revised; file acquisition and cohort freeze pending  
**Review cadence:** monthly business resilience review

> This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Business problem

The economic-development team must decide where additional business-support intelligence is needed when insolvency counts move sharply. A spike may reflect connected companies entering a procedure rather than a broad rise in business failure. National monthly totals, event records and registered company locations also do not necessarily describe the same population or trading footprint.

## Commissioned decision

> Which sectors or recorded geographic concentrations of company insolvency warrant business-support investigation, after distinguishing count growth, coverage and insolvency procedures?

## Practical use

At the monthly review, the Director sees the procedure driving a count increase, checks whether the movement persists across three- and six-month windows, then reviews available sector coding. If a cluster appears linked to one corporate group or has poor geographic coverage, the team requests corroborating evidence before targeting an area-wide support response.

The full [business context](project/BUSINESS_CONTEXT.md) names operational stakeholders, decisions, risks and proposed benefit measures.

## What must be delivered

1. Produce procedure/jurisdiction trends separating seasonal adjustment bases and registration dates.
2. Analyse industry and geography only where the record-level fields support them; quantify unmatched and uncoded records.
3. Shortlist up to ten sector/geographic investigation cases with three-/six-month sensitivity and explicit denominator gaps.

The complete D1–D12 pack includes discovery, source governance, ingestion/model, quality, metric catalogue, analysis, investigation scenarios, BI, assurance/UAT, independent handover, executive briefing and contribution evidence. A dashboard by itself does not satisfy the commission.

## Fixed core and optional work

**Core:** June 2026 long-run CSV plus the agreed England/Wales/Scotland record ZIP and long-run metadata. Establish actual record-level dates, fields and event keys before sector/geographic analysis. National history and observed event history remain separate; all records with missing industry/geography stay visible in coverage diagnostics.

**Extensions:** Risk per active business, trading-site exposure, predictive early warning and causal support effectiveness require additional denominators/evaluation. If the ZIP lacks a required breakdown, use a registered official industry table for sector analysis; do not infer it from company names.

Source support is checked at the Week 2 gate. A required output is blocked until its fields and cohort are verified; it cannot pass acceptance through a generic “data unavailable” disclaimer. An explicitly optional extension may remain unavailable with a reason. See [exact source URLs and verification evidence](data/SOURCE_REGISTER.md).

## Measurable project outcomes

1. Every trend identifies jurisdiction, procedure, date basis and seasonal-adjustment status.
2. Every sector/geographic finding reports uncoded/unmapped counts and the actual event-history window.
3. Every early-warning suggestion is labelled unvalidated unless a separate time-based backtest and denominator support it.

All headline metrics require field lineage; five source values and five BI measures must reconcile. DT1–DT10 must be executed, a second member must reproduce the core outputs, and no critical/high defect may remain. These assess delivery quality; real-world savings or service improvement are not claimed.

## Investigation rules

Within each comparable jurisdiction/procedure, compare three-month and six-month count signals. For coded sectors, show event concentration with uncoded records as a separate group. Geographic candidates require documented mapping coverage; below 90% mapping coverage, label the geography result exploratory and place it in an evidence-review queue. The 90% gate is a project design choice, not an official threshold.

- Counts do not measure insolvency risk per business without a compatible business-population denominator.
- Public company records must not become personal profiles; omit unnecessary names and addresses from outputs.
- Retrospective insolvency indicators are not validated predictive early warnings; forecasting is optional and requires time-based evaluation.

## Team and stakeholder ownership

Director of Economic Development & Business Resilience approves business scope and the investigation recommendation. The Business Analyst, Data Governance Analyst, Data Engineer and BI Developer work with the specialist roles in the [project brief](project/PROJECT_BRIEF.md). Assign individual owners at kickoff and record substantive work and independent reviews in `CONTRIBUTIONS.md`.

## Delivery plan

Weeks 1–2: decision requirements and verified cohort. Weeks 3–4: model, reconciliation and metric definitions. Weeks 5–6: analytical findings, alternative investigation scenarios and BI draft. Weeks 7–8: simulated UAT, independent rerun, executive briefing and handover.

## Start here

1. [Project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. [D1–D12 deliverables and metric contracts](project/DELIVERABLES.md).
3. [AC1–AC12 and DT1–DT10 acceptance tests](project/ACCEPTANCE_CRITERIA.md).
4. [Governance and sign-off](project/GOVERNANCE.md).
5. [Data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw](data/raw/README.md), [reference](data/reference/README.md) and [metadata](data/metadata/README.md) guidance.
6. [Team repository standard](submission/TEAM_REPOSITORY_STANDARD.md), [submission guide](submission/SUBMISSION_GUIDE.md) and [final template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master repository holds the Mettelo-controlled specification. Create `MTL-XF-025-<team-name>` under the **Mettelo GitHub organisation** and add every member's individual account. Delivery analysis, code, tests, BI and contribution evidence belong in that team repository. Use issues, branches, meaningful commits, PRs and reviews where practical.

The required master areas are `project/`, `data/` (including raw/reference/metadata guidance) and `submission/`; [the documentation index](project/README.md) explains their authority and current revision.

**Mettelo — Built for What’s Next**
