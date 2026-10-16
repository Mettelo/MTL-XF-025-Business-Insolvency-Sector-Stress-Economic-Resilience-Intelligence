# MTL-XF-025 — Data workspace

## Required sources and cohort

Insolvency Service long-run monthly series + record-level England/Wales/Scotland data. The long-run file goes back to 2000 and the record ZIP is only 3.97 MB.

Freeze the June 2026 long-run CSV and England/Wales/Scotland record-level ZIP. National trends use the long-run history from 2000 to the actual frozen endpoint. Record-level sector/geography analysis uses only the coverage and fields documented inside that ZIP; do not assume the entire long-run history is represented.

[Source register and exact URLs](SOURCE_REGISTER.md)

**Current state:** specification only. No raw datasets have been downloaded or uploaded in this build. Expected size, row count and history statements from the earlier agreement require verification against the actual files. Do not mark the cohort frozen until the manifest and metadata are complete.

## Controlled acquisition and preparation

1. Read [SOURCE_REGISTER.md](SOURCE_REGISTER.md); use the exact agreed URLs and official publisher documentation.
2. Validate that the response is the expected CSV/ODS/XLSX/ZIP rather than an error page. Inspect archive contents and sheet names where relevant.
3. Record resolved URL, UTC retrieval, release, coverage, filename, bytes, SHA-256 and licence evidence. Log discrepancies before changing sources.
4. Preserve original bytes in an approved immutable snapshot; later upload only where instructed and redistribution is permitted.
5. Record source fields, types, valid values, suppression, units and publisher methodology in [metadata](metadata/README.md).
6. Implement the analytical grain below, verify keys/cardinality and account for excluded/quarantined records.
7. Reconcile at least five published measures and create curated outputs reproducibly in the team repository.

## Analytical grain

National fact: month × jurisdiction × procedure × adjustment basis. Record fact: published insolvency event/record × event date × jurisdiction × available company/sector/geography fields. A company identifier need not uniquely identify an insolvency event.

## Required metric contract

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

## Mandatory quality risks

- Counts do not measure insolvency risk per business without a compatible business-population denominator.
- Public company records must not become personal profiles; omit unnecessary names and addresses from outputs.
- Retrospective insolvency indicators are not validated predictive early warnings; forecasting is optional and requires time-based evaluation.

1. Reconcile five monthly/procedure measures without combining seasonally adjusted and unadjusted values.
2. Show a repeated company ID with different valid events is not blindly deduplicated.
3. Quantify missing industry/geography records before any concentration calculation.
4. Test that a missing month invalidates a three-month moving window rather than becoming zero.

## Folder ownership

- [raw](raw/README.md): unmodified approved source snapshots; guidance only at present.
- [reference](reference/README.md): governed code lists, hierarchies and crosswalks.
- [metadata](metadata/README.md): source notices, schema, glossary, lineage and manifest evidence.

Curated data, processing code, logs and test results belong in the team delivery repository. Preserve a reproducible boundary between source inputs and generated products. Do not add personal, confidential or paid-source data.
