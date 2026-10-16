# MTL-XF-025 — Acceptance criteria and domain tests

**Business decision owner:** Director of Economic Development & Business Resilience. **Decision:** Which sectors or recorded geographic concentrations of company insolvency warrant business-support investigation, after distinguishing count growth, coverage and insolvency procedures?

## Delivery sign-off

| ID | Deliverables | Required pass evidence | Acceptance owner |
| --- | --- | --- | --- |
| AC1 | D1 | Eight user requirements cover the commissioned questions, named stakeholder actions and core/extension boundary. | Business Analyst / Director of Economic Development & Business Resilience |
| AC2 | D2 | 100% of used source files have approved provenance, version/coverage, licence, retrieval UTC and SHA-256. Required fields and reference versions are checked. | Data Governance Analyst |
| AC3 | D3 | Every input row is accounted for; keys and all many-to-many/hierarchy effects have explicit checks and no unexplained duplication. | Data Engineer / independent reviewer |
| AC4 | D4 | Five source cells reconcile within a declared rounding tolerance; all material differences and non-additive totals are explained. | Domain specialist |
| AC5 | D5 | All 8 metric contracts are classified core/conditional and have tested definitions; no unsupported fields or fabricated unavailable values. | Data Governance Analyst / BI Developer |
| AC6 | D6 | Five findings cover all business questions or evidence gaps; period, eligible population, magnitude, comparison and limitation are visible. | Domain analyst |
| AC7 | D7 | The project-specific baseline and alternative below are implemented; eligibility, scenario changes, reason codes and evidence requests are visible. | Director of Economic Development & Business Resilience |
| AC8 | D8 | Five BI measures reconcile to curated outputs; all filters/reset/export retain the scope, units and limitations. | BI Developer / operational UAT user |
| AC9 | D9 | DT1–DT10 have actual execution evidence and expected/actual outcomes; no unresolved critical/high defect. | Independent reviewer |
| AC10 | D10 | A distinct member's clean rerun reproduces equivalent core outputs with documented environment and checks. | Independent rerun reviewer |
| AC11 | D11 | Two-page maximum briefing and 15–20 minute presentation answer the decision and assign investigation owners without unsupported outcomes. | Director of Economic Development & Business Resilience / Mettelo panel |
| AC12 | D12 | Every member links substantive authored and reviewed work, including handover or presentation contribution. | Delivery Lead |

## Project-specific business success

1. Every trend identifies jurisdiction, procedure, date basis and seasonal-adjustment status.
2. Every sector/geographic finding reports uncoded/unmapped counts and the actual event-history window.
3. Every early-warning suggestion is labelled unvalidated unless a separate time-based backtest and denominator support it.

## Required prioritisation and sensitivity

Within each comparable jurisdiction/procedure, compare three-month and six-month count signals. For coded sectors, show event concentration with uncoded records as a separate group. Geographic candidates require documented mapping coverage; below 90% mapping coverage, label the geography result exploratory and place it in an evidence-review queue. The 90% gate is a project design choice, not an official threshold.

Record each case's entity/segment, valid period, supporting measures, reason code, scenario position, missing evidence, responsible operational role, next review and manual-review trigger. Fewer than ten cases is valid; padding unsupported cases fails acceptance.

## DT1–DT10 — minimum executed domain tests

| Test | Input / action | Expected pass evidence |
| --- | --- | --- |
| DT1 | Reconcile five monthly/procedure measures without combining seasonally adjusted and unadjusted values. | Five selected published values reproduce within declared source precision, with explicit source coordinates and scope. |
| DT2 | Show a repeated company ID with different valid events is not blindly deduplicated. | The invalid comparison, join or denominator is rejected or flagged according to the documented rule; no silent fallback. |
| DT3 | Quantify missing industry/geography records before any concentration calculation. | The edge case produces an explicit unavailable/exclusion result or a supported calculation, with affected rows quantified. |
| DT4 | Test that a missing month invalidates a three-month moving window rather than becoming zero. | The domain boundary remains visible in the analytical output and BI product; no unsupported inference. |
| DT5 | Procedure counts 10, 20 and 30 over three valid months | Trailing-three-month count = 60; it is not an average of percentages. |
| DT6 | A concentrated spike includes connected-company events | Report clustering as context; do not claim a broad sector deterioration from count alone. |
| DT7 | 20 of 100 records have no industry code | Uncoded share = 20%; concentration explicitly includes or excludes them with rationale. |
| DT8 | 85 of 100 eligible events are mapped to geography | Mapping = 85%; below the project 90% gate, geographic findings are exploratory. |
| DT9 | Monthly series and record subset use different date coverage | Do not force reconciliation; quantify scope mismatch before comparing. |
| DT10 | No compatible active-business population is registered | Output remains count/share evidence, never a risk-per-business rate. |

Worked values are **synthetic test fixtures**, not claims about the public data or simulated client. For each test retain requirement ID, source/input or fixture, expected result, actual result, evidence link, tester, independent reviewer and date. DT1–DT4 additionally require the documented project-specific rule; their general evidence descriptions do not waive the named domain condition. Add dashboard/filter tests as needed beyond these ten.

## Scope gate and unresolved issues

**Mandatory core:** June 2026 long-run CSV plus the agreed England/Wales/Scotland record ZIP and long-run metadata. Establish actual record-level dates, fields and event keys before sector/geographic analysis. National history and observed event history remain separate; all records with missing industry/geography stay visible in coverage diagnostics.

**Optional extensions:** Risk per active business, trading-site exposure, predictive early warning and causal support effectiveness require additional denominators/evaluation. If the ZIP lacks a required breakdown, use a registered official industry table for sector analysis; do not infer it from company names.

A mandatory source/field gap blocks the affected deliverable and must be resolved by a registered official replacement or approved, versioned scope change. An explicitly optional result may be unavailable with a reason and a useful evidence request. Neither missing raw data nor unexecuted tests may be marked passed.

A critical/high defect materially changes a headline value, cohort, recommendation, provenance or reproducibility and blocks release. Lower-impact issues require a named acceptance owner and disclosed impact. All panel feedback and approvals must be recorded honestly as simulated where applicable.
