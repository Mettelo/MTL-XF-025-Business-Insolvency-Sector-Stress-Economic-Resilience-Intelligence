# MTL-XF-025 — Required deliverables and metric contracts

**Decision:** Which sectors or recorded geographic concentrations of company insolvency warrant business-support investigation, after distinguishing count growth, coverage and insolvency procedures?  
**Business acceptance:** Director of Economic Development & Business Resilience  
**Core scope:** June 2026 long-run CSV plus the agreed England/Wales/Scotland record ZIP and long-run metadata. Establish actual record-level dates, fields and event keys before sector/geographic analysis. National history and observed event history remain separate; all records with missing industry/geography stay visible in coverage diagnostics.

All artefact locations refer to the team repository. Deliver the core before optional extensions. [The source register](../data/SOURCE_REGISTER.md) documents evidence status; required field support is a G1 release condition.

## D1 — Discovery & requirements

**Due:** Week 1 · **Location:** `docs/01-discovery/` · **Owner:** Business Analyst

Map the monthly business resilience review, stakeholder needs, current reporting failures and target decision. Eight prioritised requirements must cover the business questions, scope gates and usable outputs.

**Pass evidence:** Each requirement has an accountable user, artefact, test and acceptance owner.

## D2 — Sources, governance & cohort contract

**Due:** Week 2 · **Location:** `data/; docs/02-data-governance/` · **Owner:** Data Governance Analyst

Complete the source-to-deliverable support matrix and classify core, fallback and optional inputs. June 2026 long-run CSV plus the agreed England/Wales/Scotland record ZIP and long-run metadata. Establish actual record-level dates, fields and event keys before sector/geographic analysis. National history and observed event history remain separate; all records with missing industry/geography stay visible in coverage diagnostics.

**Pass evidence:** Every used input has provenance, exact version/coverage, licence evidence and SHA-256; conditional scope cannot be signed off without supporting fields.

## D3 — Reproducible model & ingestion

**Due:** Week 3 · **Location:** `src/; sql/; docs/03-data-model/` · **Owner:** Data Engineer

Implement raw preservation, selection, schema checks, curated facts and dimensions. National fact: month × jurisdiction × procedure × adjustment basis. Record fact: published insolvency event/record × event date × jurisdiction × available company/sector/geography fields. A company identifier need not uniquely identify an insolvency event.

**Pass evidence:** Zero unexplained duplicate keys or join inflation; every input row accounted for as retained/excluded/quarantined.

## D4 — Quality, source reconciliation & exceptions

**Due:** Week 3 · **Location:** `tests/; docs/04-data-quality/` · **Owner:** Independent reviewer + domain specialist

Execute source, denominator, missingness, boundary and linkage checks against the risk 'Connected-company events and incomplete coding may be mistaken for broad local economic distress.'

**Pass evidence:** Reconcile five source values from at least two periods or segments; retain source coordinates, precision and explanations for non-additive totals.

## D5 — Governed metric catalogue

**Due:** Week 4 · **Location:** `docs/05-kpi-catalogue/` · **Owner:** Domain specialist + Data Governance Analyst

Implement the 8 metric contracts below; distinguish unconditional core metrics from gated extensions.

**Pass evidence:** Each core metric has purpose, raw fields, formula, grain, denominator/unit, missing/zero handling, owner, refresh and test; conditional items have explicit eligibility or unavailable status.

## D6 — Domain assessment

**Due:** Week 5 · **Location:** `analysis/; docs/06-analysis/` · **Owner:** Domain analyst

Produce procedure/jurisdiction trends separating seasonal adjustment bases and registration dates. Analyse industry and geography only where the record-level fields support them; quantify unmatched and uncoded records.

**Pass evidence:** At least five supported findings answer the five questions or document a genuine evidence gap; each includes magnitude, scope, comparison and limitation.

## D7 — Investigation framework & scenarios

**Due:** Week 6 · **Location:** `docs/07-decision-framework/` · **Owner:** Director of Economic Development & Business Resilience (business acceptance)

Within each comparable jurisdiction/procedure, compare three-month and six-month count signals. For coded sectors, show event concentration with uncoded records as a separate group. Geographic candidates require documented mapping coverage; below 90% mapping coverage, label the geography result exploratory and place it in an evidence-review queue. The 90% gate is a project design choice, not an official threshold.

**Pass evidence:** Publish eligibility, component definitions, scenario differences and up to ten supported cases; every case names a service role, evidence request and review trigger.

## D8 — Decision-support BI

**Due:** Draft Week 6; final Week 7 · **Location:** `dashboard/` · **Owner:** BI Developer

Build overview, diagnostic and quality pages for the monthly business resilience review. Show period, units, definitions, missingness and core/extension status.

**Pass evidence:** Five headline values reconcile; every visible filter and reset tested; accessible static export plus free review/build path.

## D9 — Assurance & simulated UAT

**Due:** Week 7 · **Location:** `docs/08-assurance-uat/` · **Owner:** Independent reviewer

Execute DT1–DT10 below, plus any tool-specific calculations and filter tests. Record expected/actual evidence, requirement links and defects.

**Pass evidence:** All ten mandatory domain cases evidenced; no critical/high issue remains; accepted lower-impact limitations have named review.

## D10 — Technical & operational handover

**Due:** Week 8 · **Location:** `docs/09-technical-handover/` · **Owner:** Data Engineer + a second-member reviewer

Provide environment, immutable manifest, end-to-end run, output checks, troubleshooting and refresh/change process.

**Pass evidence:** A second member regenerates equivalent core outputs without undocumented edits and records checks, environment, duration and result.

## D11 — Executive briefing & presentation

**Due:** Week 8 · **Location:** `deliverables/` · **Owner:** Business Analyst + specialist service roles

Deliver maximum two-page briefing and 15–20 minute presentation to Director of Economic Development & Business Resilience: decision, five findings, scenario comparison, investigation actions, evidence gaps and next review.

**Pass evidence:** Every numeric claim links to tested evidence; explicitly show a case where action is not yet supported.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8 · **Location:** `CONTRIBUTIONS.md` · **Owner:** Delivery Lead

Link actual authored work, reviews, issues/PRs/commits and presentation/handover contributions for every member.

**Pass evidence:** All responsibilities have owners and evidence; commit count alone is insufficient.

## Metric contracts — authoritative definitions

| Metric | Definition / support condition |
| --- | --- |
| Monthly insolvency events | Published count by procedure, jurisdiction and adjustment basis. |
| Year-on-year change | 100 × (monthly count / same month previous year − 1), only with positive comparable base. |
| Three-month moving count | Trailing three-month sum; require all three months. |
| Procedure share | 100 × procedure count / compatible jurisdiction total. |
| Observed sector share | 100 × coded sector events / all observed eligible events; display uncoded share separately. |
| Geographic coding coverage | 100 × valid mapped records / eligible record-level records. |
| Record-to-series reconciliation gap | Record aggregate minus compatible published count; report scope and timing differences. |
| Concentration | Sum of squared sector shares at a declared mutually exclusive industry level; report uncoded treatment. |

For each metric add source ID and actual raw fields, business purpose, formula, grain, valid population, unit, numerator/denominator, hierarchy, suppression/zero/missing handling, owner, refresh and test evidence. Verify source rounding before setting a reconciliation tolerance. A conditional item is not silently promoted into core; a core requirement is not silently waived.

## Project-specific outcomes

1. Every trend identifies jurisdiction, procedure, date basis and seasonal-adjustment status.
2. Every sector/geographic finding reports uncoded/unmapped counts and the actual event-history window.
3. Every early-warning suggestion is labelled unvalidated unless a separate time-based backtest and denominator support it.

See [DT1–DT10 and investigation rules](ACCEPTANCE_CRITERIA.md) for worked pass/fail cases. Source schemas, specific period selections and reference versions must be signed at G1. Keep calculation definitions here; other guidance pages link to this contract rather than maintaining competing copies.
