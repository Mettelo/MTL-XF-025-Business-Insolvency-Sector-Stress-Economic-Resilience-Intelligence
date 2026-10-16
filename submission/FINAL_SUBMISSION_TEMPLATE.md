# MTL-XF-025 — Final submission: Business Insolvency, Sector Stress & Economic Resilience Intelligence

Complete this template in your team repository as `submission/FINAL_SUBMISSION.md`. Replace prompts with evidence; leave unavailable items explicitly unavailable with reasons. This template itself is not completed delivery evidence.

## Team and version

- Team repository URL:
- Team name and individual GitHub accounts:
- Final commit/tag and submission date:
- Master specification URL and reviewed commit:
- Delivery dates:
- Named role owners and independent reviewers:
- Engagement declaration: simulated confidential-client engagement using official public/open data; no real-client employment, endorsement or privileged access claimed.

## Commissioned decision

Which sectors or recorded geographic concentrations of company insolvency warrant business-support investigation, after distinguishing count growth, coverage and insolvency procedures?

State the answer, confidence, principal limitation and proposed investigation action.

## Actual cohort and provenance

Agreed boundary: Freeze the June 2026 long-run CSV and England/Wales/Scotland record-level ZIP. National trends use the long-run history from 2000 to the actual frozen endpoint. Record-level sector/geography analysis uses only the coverage and fields documented inside that ZIP; do not assume the entire long-run history is represented.

Record actual frozen files/versions, manifest/checksums, source-register link, licence evidence, retrieval timestamp, schema/coverage validation, inclusions/exclusions and approved deviations. Do not mark acquisition complete without evidence.

## Evidence index

| Deliverable | Artefact link | Owner / reviewer | Status / limitation |
| --- | --- | --- | --- |
| D1 — Discovery & decision requirements | To complete | To complete | To complete |
| D2 — Governed sources & cohort | To complete | To complete | To complete |
| D3 — Reproducible analytical model | To complete | To complete | To complete |
| D4 — Quality & reconciliation | To complete | To complete | To complete |
| D5 — KPI catalogue | To complete | To complete | To complete |
| D6 — Domain analytical assessment | To complete | To complete | To complete |
| D7 — Investigation decision framework | To complete | To complete | To complete |
| D8 — BI decision-support product | To complete | To complete | To complete |
| D9 — Independent assurance & UAT | To complete | To complete | To complete |
| D10 — Technical & operational handover | To complete | To complete | To complete |
| D11 — Executive recommendation | To complete | To complete | To complete |
| D12 — Contribution & delivery record | To complete | To complete | To complete |

## Governed measures

| Required measure | Definition/source/test link | Result / unavailable reason |
| --- | --- | --- |
| Monthly insolvency events | To complete | To complete |
| Year-on-year change | To complete | To complete |
| Three-month moving count | To complete | To complete |
| Procedure share | To complete | To complete |
| Observed sector share | To complete | To complete |
| Geographic coding coverage | To complete | To complete |
| Record-to-series reconciliation gap | To complete | To complete |
| Concentration | To complete | To complete |

## Business questions and five findings

1. Which insolvency procedures drive recent changes within each jurisdiction?
2. Which sectors concentrate observed records, where industry coding exists?
3. Are recorded geographic concentrations robust to missing or ambiguous addresses?
4. Do recent trends persist under three- versus six-month smoothing?
5. What business-population denominator and support-service evidence are needed before an early-warning claim?

For each question record the finding, quantitative evidence, period/grain, comparison, uncertainty, limitation and artefact link. Record an evidenced gap where the data cannot answer it.

## Investigation shortlist and sensitivity

Provide up to ten supported cases. For each: entity/segment, signal and magnitude, eligibility, reason code, scenario membership, proposed investigation, responsible role, missing evidence and review trigger. Compare at least two scenarios and explain membership/rank changes. Include a case where evidence is insufficient for action.

## Acceptance and assurance

| Criterion | Pass/fail / evidence / reviewer |
| --- | --- |
| AC1 (D1) | To complete |
| AC2 (D2) | To complete |
| AC3 (D3) | To complete |
| AC4 (D4) | To complete |
| AC5 (D4–D5) | To complete |
| AC6 (D5) | To complete |
| AC7 (D6) | To complete |
| AC8 (D7) | To complete |
| AC9 (D8) | To complete |
| AC10 (D9) | To complete |
| AC11 (D10–D11) | To complete |
| AC12 (D12) | To complete |

Record at least ten executed UAT scenarios, expected/actual results, defect severity/disposition and five reconciled BI measures. Mandatory cases:

1. Reconcile five monthly/procedure measures without combining seasonally adjusted and unadjusted values.
2. Show a repeated company ID with different valid events is not blindly deduplicated.
3. Quantify missing industry/geography records before any concentration calculation.
4. Test that a missing month invalidates a three-month moving window rather than becoming zero.

## Reproducible handover

- Environment/tool versions and dependencies:
- Input snapshot location and checksum verification:
- Clean run instructions and output locations:
- Independent rerun reviewer/date/duration/results:
- Reconciliation evidence and permitted rounding:
- Refresh/change process and known failure modes:

## Executive delivery

- Two-page briefing link:
- Presentation link and 15–20 minute duration:
- Dashboard/free access instructions and static export:
- Recommendations, missing evidence, responsible roles and next review:

## Contributions

For every member link authored artefacts, review work, issues/PRs/commits and presentation/handover contribution. Link `CONTRIBUTIONS.md`; commit count alone is insufficient.

## Limitations and review decision

- Counts do not measure insolvency risk per business without a compatible business-population denominator.
- Public company records must not become personal profiles; omit unnecessary names and addresses from outputs.
- Retrospective insolvency indicators are not validated predictive early warnings; forecasting is optional and requires time-based evaluation.

Add actual limitations, optional extensions, unresolved accepted issues and their impacts. Record simulated panel review date, reviewers and decision only after review occurs. Do not claim real operational savings or outcome improvements.
