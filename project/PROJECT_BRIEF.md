# MTL-XF-025 — Project brief

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

**Client:** Confidential Economic Development & Business Resilience Directorate. **Decision owner:** Director of Economic Development & Business Resilience. **Team:** 3–5. **Duration:** 8 weeks. **Review:** monthly business resilience review.

## Business problem and commission

The simulated economic-development directorate runs a monthly business-resilience meeting with its intelligence and business-support teams. The meeting must decide which sectors or supported recorded-location clusters warrant a deeper enquiry before support resources are redirected.

The Director of Economic Development & Business Resilience needs a defensible response when company insolvency counts rise. Headline national totals do not identify the local support question, and a cluster of recorded events may reflect one procedure, connected companies or incomplete sector/location coverage rather than widespread trading distress.

Acting too quickly could divert outreach towards a misleading cluster; waiting for an unambiguous headline could leave a credible sector concern unexplored. The commission is a monthly evidence pack that distinguishes sustained procedure-level movement from record-level concentration and turns supported signals into targeted intelligence requests. It is not a predictive company failure model.

> Which sectors or recorded geographic concentrations of company insolvency warrant business-support investigation, after distinguishing count growth, coverage and insolvency procedures?

**Required management handover:** A monthly resilience pack containing procedure/jurisdiction trends, event coverage diagnostics, three-/six-month investigation comparisons and a sector/location enquiry register. Each case must distinguish observed count concentration from a risk-rate or trading-footprint claim.

See [the management use case](BUSINESS_CONTEXT.md#practical-management-use-case) for how the review meeting uses this evidence.

## Core deliverable boundary

June 2026 long-run CSV plus the agreed England/Wales/Scotland record ZIP and long-run metadata. Establish actual record-level dates, fields and event keys before sector/geographic analysis. National history and observed event history remain separate; all records with missing industry/geography stay visible in coverage diagnostics.

**Optional / out of core:** Risk per active business, trading-site exposure, predictive early warning and causal support effectiveness require additional denominators/evaluation. If the ZIP lacks a required breakdown, use a registered official industry table for sector analysis; do not infer it from company names.

File availability does not prove dimensional support. Before analytical build, the team completes the source→field→metric→deliverable matrix in [data guidance](../data/README.md). Missing mandatory support blocks the gate and requires an approved official replacement or scope decision.

## Analytical model

National fact: month × jurisdiction × procedure × adjustment basis. Record fact: published insolvency event/record × event date × jurisdiction × available company/sector/geography fields. A company identifier need not uniquely identify an insolvency event.

The source contract above controls where a general grain description is conditional. Do not create dimensions absent from the approved input.

## Objectives

1. Every trend identifies jurisdiction, procedure, date basis and seasonal-adjustment status.
2. Every sector/geographic finding reports uncoded/unmapped counts and the actual event-history window.
3. Every early-warning suggestion is labelled unvalidated unless a separate time-based backtest and denominator support it.

## Business questions

1. Which insolvency procedures drive recent changes within each jurisdiction?
2. Which sectors concentrate observed records, where industry coding exists?
3. Are recorded geographic concentrations robust to missing or ambiguous addresses?
4. Do recent trends persist under three- versus six-month smoothing?
5. What business-population denominator and support-service evidence are needed before an early-warning claim?

## Cross-functional delivery model

| Delivery role | Required project contribution |
| --- | --- |
| Business Analyst / Delivery Lead | Map the monthly business resilience review, document eight prioritised user requirements and maintain requirement→deliverable→test links; Director of Economic Development & Business Resilience owns business approval. |
| Data Governance Analyst | Own the MTL-XF-025 source/metadata register, cohort decision, licence evidence and 100% headline-measure lineage; resolve the specific risk: Connected-company events and incomplete coding may be mistaken for broad local economic distress. |
| Data Engineer | Implement the declared facts, keys, hierarchy and join controls; account for every source row and deliver a second-member reproducible run at the chosen MTL-XF-025 scope. |
| BI Developer | Implement the monthly business resilience review overview, diagnostic and quality pages; reconcile five measures and ensure cohort/extension warnings survive filters and export. |
| Economic & Business Resilience Analyst | Own procedure/jurisdiction comparability and explain five reconciled monthly measures. |
| Industry & Geographic Data Steward | Document industry mapping, event keys and the percentage of uncoded/unmapped records. |
| Model & Decision Assurance Analyst | Review smoothing sensitivity and any optional backtest; block unsupported predictive-risk claims. |

Assign named team members and review partners at kickoff; roles may be combined, but a distinct member must review critical calculations and perform the final clean rerun. The executive and operational stakeholder roles are specified in [business context](BUSINESS_CONTEXT.md).

## Required investigation approach

Within each comparable jurisdiction/procedure, compare three-month and six-month count signals. For coded sectors, show event concentration with uncoded records as a separate group. Geographic candidates require documented mapping coverage; below 90% mapping coverage, label the geography result exploratory and place it in an evidence-review queue. The 90% gate is a project design choice, not an official threshold.

## Milestones and acceptance

| Gate | Reviewers | Evidence / decision |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Release resources and metadata link verified; ZIP members, event coverage, sector/location schema and frozen checksums pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Economic Development & Business Resilience + operational stakeholders | Within each comparable jurisdiction/procedure, compare three-month and six-month count signals. For coded sectors, show event concentration with uncoded records as a separate group. Geographic candidates require documented mapping coverage; below 90% mapping coverage, label the geography result exploratory and place it in an evidence-review queue. The 90% gate is a project design choice, not an official threshold. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

D1–D12 are defined in [deliverables](DELIVERABLES.md). AC1–AC12 and DT1–DT10 are defined in [acceptance criteria](ACCEPTANCE_CRITERIA.md). No real production deployment, automatic funding/service allocation, private-client data or paid-source dependency is required.

## Team organisation

The recommended team size is **3–5 people**. Delivery roles describe responsibilities, not separate positions: members can combine complementary business analysis, governance, engineering, analysis/modelling, BI and domain responsibilities. Assign a named owner to each deliverable and use a different team member to review critical calculations and perform the final clean rerun.
