# MTL-XF-025 — Submission guide

## What to submit

Submit the Mettelo organisation team repository URL, final commit/tag, completed `submission/FINAL_SUBMISSION.md`, and links to D1–D12. Use the provided [template](FINAL_SUBMISSION_TEMPLATE.md). The final version must remain reproducible after review; record changes made after submission.

## Before submitting

1. Confirm the repository README states the simulated engagement and commissioned decision: Which sectors or recorded geographic concentrations of company insolvency warrant business-support investigation, after distinguishing count growth, coverage and insolvency procedures?
2. Complete the source manifest and cohort sign-off. Freeze the June 2026 long-run CSV and England/Wales/Scotland record-level ZIP. National trends use the long-run history from 2000 to the actual frozen endpoint. Record-level sector/geography analysis uses only the coverage and fields documented inside that ZIP; do not assume the entire long-run history is represented.
3. Link the requirements matrix, model, field lineage, quality/reconciliation evidence and all 8 metric definitions.
4. Link at least five findings and the up-to-ten-case investigation shortlist, including owners, evidence gaps and two compared scenarios.
5. Reconcile at least five headline dashboard measures and test all visible filters; provide a free review path and static export.
6. Execute ten or more UAT scenarios, including all domain cases below. Resolve critical/high defects and disclose any accepted remaining limitations.
7. Have another member reproduce the core outputs using documented steps; retain the run environment, checks and results.
8. Complete contribution evidence for each member and prepare the two-page briefing and 15–20 minute presentation.

## Required domain checks

1. Reconcile five monthly/procedure measures without combining seasonally adjusted and unadjusted values.
2. Show a repeated company ID with different valid events is not blindly deduplicated.
3. Quantify missing industry/geography records before any concentration calculation.
4. Test that a missing month invalidates a three-month moving window rather than becoming zero.

## Panel presentation

Explain the decision, actual cohort and limitations; demonstrate one source-to-KPI-to-dashboard chain; present five findings; compare two prioritisation scenarios; justify the investigation cases; show one case where action is not supported; describe next evidence-gathering steps and named role ownership.

Expect challenges on definitions, denominators, exclusions, comparability, threshold choices, sensitivity, reproducibility and contribution. Label feedback and approvals as simulated where appropriate. Do not invent contact with real stakeholders.

## Acceptance and changes

Use [AC1–AC12](../project/ACCEPTANCE_CRITERIA.md) to record pass/fail, evidence and reviewer. An unavailable conditional analysis needs a supported explanation and alternative; it cannot be disguised as a result. Source changes require registration, impact review and rerun. Final acceptance is recorded by the simulated Mettelo review panel, not self-certified as a real-client outcome.
