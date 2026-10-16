# MTL-XF-025 — Project brief

## Engagement

This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

**Simulated sponsor:** Confidential Economic Development & Business Resilience Directorate. **Duration:** 8 weeks. **Team:** 6–8 members. **Track:** Cross-Functional. **Sector:** Business Resilience / Economic Development.

## Commission

Which sectors or recorded geographic concentrations of company insolvency warrant business-support investigation, after distinguishing count growth, coverage and insolvency procedures?

**Business Insolvency, Sector Stress & Economic Resilience Intelligence.** An economic-development team needs earlier warning of where business distress is rising by insolvency type, sector and geography so business-support resources can be investigated before pressure becomes more severe.

## Outcomes and boundaries

- Produce procedure/jurisdiction trends separating seasonal adjustment bases and registration dates.
- Analyse industry and geography only where the record-level fields support them; quantify unmatched and uncoded records.
- Shortlist up to ten sector/geographic investigation cases with three-/six-month sensitivity and explicit denominator gaps.

Deliver evidence for a management investigation decision, with an auditable shortlist of up to ten cases and at least two alternative prioritisation scenarios. Do not manufacture a full shortlist where the data supports fewer cases. Findings may conclude that evidence is insufficient.

**Data boundary:** Freeze the June 2026 long-run CSV and England/Wales/Scotland record-level ZIP. National trends use the long-run history from 2000 to the actual frozen endpoint. Record-level sector/geography analysis uses only the coverage and fields documented inside that ZIP; do not assume the entire long-run history is represented.

**Model boundary:** National fact: month × jurisdiction × procedure × adjustment basis. Record fact: published insolvency event/record × event date × jurisdiction × available company/sector/geography fields. A company identifier need not uniquely identify an insolvency event.

**Out of scope:** real operational deployment, confidential case-level data, guaranteed savings/outcome improvements, paid-source dependencies and automatic allocation of services or funding. Optional modelling or enriched sources must not delay or replace the core D1–D12 pack.

## Users and acceptance owners

- Simulated sponsor/review panel: approves commissioned question, changes and final investigation recommendation.
- Domain service/planning user: checks whether diagnostic evidence supports the proposed review action.
- Data steward: verifies source/version, licence, definitions, quality and retention evidence.
- BI user: tests overview, drill-down, filters and limitations.
- Independent reviewer: verifies calculations, rerun and requirement-to-test traceability.

These are simulated stakeholder roles, not claims of access to a real organisation.

## Work allocation

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential Economic Development & Business Resilience Directorate; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 025 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 025 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 025 dashboard measures and test every visible filter. |
| Economic & Business Resilience Analyst | Own procedure/jurisdiction comparability and explain five reconciled monthly measures. |
| Industry & Geographic Data Steward | Document industry mapping, event keys and the percentage of uncoded/unmapped records. |
| Model & Decision Assurance Analyst | Review smoothing sensitivity and any optional backtest; block unsupported predictive-risk claims. |

At kickoff, replace role ownership with named team members and record review partners in `CONTRIBUTIONS.md`. Multiple roles per member are permitted, but critical calculations need a reviewer distinct from their author.

## Working stages

1. Week 1: agree at least eight requirements and define expected decisions.
2. Week 2: inspect actual file schemas, establish available coverage and approve cohort freeze.
3. Week 3: implement and reconcile analytical facts, keys and exclusions.
4. Week 4: approve the 8-measure KPI catalogue and denominator rules.
5. Week 5: complete five supported findings and domain comparisons.
6. Week 6: compare two decision scenarios, produce the investigation shortlist and BI draft.
7. Week 7: execute ten or more assurance/UAT scenarios, including project-specific edge cases.
8. Week 8: independent rerun, executive briefing, presentation and final handover.

## Sign-off

Follow [D1–D12](DELIVERABLES.md) and [AC1–AC12](ACCEPTANCE_CRITERIA.md). Approve only with reproducible evidence, no unresolved critical/high defects and transparent conditional-data limitations. A change in source availability must be logged; do not silently substitute a newer release.
