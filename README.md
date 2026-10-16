# MTL-XF-025 — Business Insolvency, Sector Stress & Economic Resilience Intelligence

**Mettelo Project Studio** · Cross-Functional · Master specification  
**Client:** Confidential Economic Development & Business Resilience Directorate  
**Sector:** Business Resilience / Economic Development  
**Status:** Pre-launch; documentation ready, data acquisition/freeze pending  
**Recommended team:** 6–8 people · **Delivery window:** 8 weeks  
**Master repository:** `Mettelo/MTL-XF-025-Business-Insolvency-Sector-Stress-Economic-Resilience-Intelligence`

> This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

## Business challenge

**Business Insolvency, Sector Stress & Economic Resilience Intelligence.** An economic-development team needs earlier warning of where business distress is rising by insolvency type, sector and geography so business-support resources can be investigated before pressure becomes more severe.

Current reporting fragments the evidence needed for a repeatable management review. The team must explain which signals are reliable, which comparisons are valid and where further investigation is needed. No budget, operational failure or improvement outcome is asserted as an observed client fact.

## Commissioned decision

> Which sectors or recorded geographic concentrations of company insolvency warrant business-support investigation, after distinguishing count growth, coverage and insolvency procedures?

The product supports a simulated stakeholder review. A dashboard alone is insufficient: the recommendation must be traceable to governed definitions, a reproducible model, reconciled analysis and a transparent investigation framework.

## Business questions

- Which insolvency procedures drive recent changes within each jurisdiction?
- Which sectors concentrate observed records, where industry coding exists?
- Are recorded geographic concentrations robust to missing or ambiguous addresses?
- Do recent trends persist under three- versus six-month smoothing?
- What business-population denominator and support-service evidence are needed before an early-warning claim?

## Approved data and cohort

Insolvency Service long-run monthly series + record-level England/Wales/Scotland data. The long-run file goes back to 2000 and the record ZIP is only 3.97 MB.

Freeze the June 2026 long-run CSV and England/Wales/Scotland record-level ZIP. National trends use the long-run history from 2000 to the actual frozen endpoint. Record-level sector/geography analysis uses only the coverage and fields documented inside that ZIP; do not assume the entire long-run history is represented.

Exact copyable URLs and acquisition gates are in [SOURCE_REGISTER.md](data/SOURCE_REGISTER.md). No raw data is uploaded by this build. Source coverage and size statements inherited from the agreement are expected values until controlled acquisition verifies them; current URLs are not a substitute for a frozen file manifest.

## What the team must build

1. Produce procedure/jurisdiction trends separating seasonal adjustment bases and registration dates.
2. Analyse industry and geography only where the record-level fields support them; quantify unmatched and uncoded records.
3. Shortlist up to ten sector/geographic investigation cases with three-/six-month sensitivity and explicit denominator gaps.

Produce the full D1–D12 delivery pack: discovery, governance, ingestion/model, quality, KPI catalogue, analysis, decision framework, BI, assurance/UAT, handover, executive briefing and contribution record. [Deliverables](project/DELIVERABLES.md) defines locations, dates and evidence for each.

## Core measures

| Metric | Required definition / calculation |
| --- | --- |
| Monthly insolvency events | Published count by procedure, jurisdiction and adjustment basis. |
| Year-on-year change | 100 × (monthly count / same month previous year − 1), only with positive comparable base. |
| Three-month moving count | Trailing three-month sum; require all three months. |
| Procedure share | 100 × procedure count / compatible jurisdiction total. |
| Observed sector share | 100 × coded sector events / all observed eligible events; display uncoded share separately. |
| Geographic coding coverage | 100 × valid mapped records / eligible record-level records. |
| Record-to-series reconciliation gap | Record aggregate minus compatible published count; report scope and timing differences. |
| Concentration | Sum of squared sector shares at a declared mutually exclusive industry level; report uncoded treatment. |

## Cross-functional ownership

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential Economic Development & Business Resilience Directorate; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 025 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 025 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 025 dashboard measures and test every visible filter. |
| Economic & Business Resilience Analyst | Own procedure/jurisdiction comparability and explain five reconciled monthly measures. |
| Industry & Geographic Data Steward | Document industry mapping, event keys and the percentage of uncoded/unmapped records. |
| Model & Decision Assurance Analyst | Review smoothing sensitivity and any optional backtest; block unsupported predictive-risk claims. |

Roles may be combined by a smaller team, but each responsibility needs a named owner. A different member reviews critical calculations and final evidence wherever practical.

## Interpretation rules

- Counts do not measure insolvency risk per business without a compatible business-population denominator.
- Public company records must not become personal profiles; omit unnecessary names and addresses from outputs.
- Retrospective insolvency indicators are not validated predictive early warnings; forecasting is optional and requires time-based evaluation.

## Measurable success

- All source files and transformations have provenance and licence evidence; approved inputs have SHA-256 manifests.
- All headline metrics have tested definitions and source-field lineage.
- At least five published values and five dashboard measures reconcile with declared source rounding.
- At least five findings address the business questions and quantify materiality.
- Up to ten investigation cases have evidence, reason codes, owners and limitations; at least two priority scenarios are compared.
- At least ten UAT scenarios pass or have explicitly accepted low-impact limitations; no critical/high defect remains.
- A second member reproduces the core outputs from the same frozen inputs.

These are delivery acceptance thresholds, not promises of real-world service improvement. See [acceptance criteria](project/ACCEPTANCE_CRITERIA.md).

## Delivery sequence

Weeks 1–2: decision requirements, source inspection and freeze approval. Weeks 3–4: model, reconciliation and KPI definitions. Weeks 5–6: analysis, investigation framework and BI draft. Weeks 7–8: UAT, independent rerun, briefing and handover.

## Start here

1. Read the [project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. Review [deliverables](project/DELIVERABLES.md), [acceptance criteria](project/ACCEPTANCE_CRITERIA.md) and [governance](project/GOVERNANCE.md).
3. Inspect the [data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw guidance](data/raw/README.md), [reference guidance](data/reference/README.md) and [metadata guidance](data/metadata/README.md).
4. Create `MTL-XF-025-<team-name>` under the **Mettelo GitHub organisation**, add each member's individual account and follow the [team repository standard](submission/TEAM_REPOSITORY_STANDARD.md).
5. Use the [submission guide](submission/SUBMISSION_GUIDE.md) and [final submission template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master holds the challenge specification. Teams deliver their analysis and artefacts in their own Mettelo organisation repository. Do not submit team work by replacing this master specification. Use issues, branches, meaningful commits, PRs and reviews to demonstrate actual collaboration.

## Specification map

```text
README.md
project/README.md
project/PROJECT_BRIEF.md
project/BUSINESS_CONTEXT.md
project/DELIVERABLES.md
project/ACCEPTANCE_CRITERIA.md
project/GOVERNANCE.md
data/README.md
data/SOURCE_REGISTER.md
data/raw/README.md
data/reference/README.md
data/metadata/README.md
submission/README.md
submission/TEAM_REPOSITORY_STANDARD.md
submission/SUBMISSION_GUIDE.md
submission/FINAL_SUBMISSION_TEMPLATE.md
```

**Mettelo — Built for What’s Next**
