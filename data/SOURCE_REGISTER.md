# MTL-XF-025 — Source register

**Project:** Business Insolvency, Sector Stress & Economic Resilience Intelligence  
**Register date:** 16 October 2026  
**Status:** agreed source references recovered; acquisition, payload verification and freeze approval pending.

## Cohort contract

Freeze the June 2026 long-run CSV and England/Wales/Scotland record-level ZIP. National trends use the long-run history from 2000 to the actual frozen endpoint. Record-level sector/geography analysis uses only the coverage and fields documented inside that ZIP; do not assume the entire long-run history is represented.

## Source entries

### S1 — Long-Run_Series_in_CSV_Format_-_Company_Insolvency_Statistics_June_2026.csv

Exact agreed download URL (copy verbatim):

```text
https://assets.publishing.service.gov.uk/media/6a57978e31fb6daf3141374b/Long-Run_Series_in_CSV_Format_-_Company_Insolvency_Statistics_June_2026.csv
```

- Publisher/source: Insolvency Service long-run monthly series + record-level England/Wales/Scotland data. The long-run file goes back to 2000 and the record ZIP is only 3.97 MB.
- Intended role: required core input.
- Access expectation from agreement: £0, public download, no paid API required.
- Verification state: URL recovered from the final agreed conversation; browser-only retrieval on 16 October 2026 could not validate the file contents. This is not a completed download/schema/licence check.
- File acquisition state: **not downloaded or uploaded in this master-pack build**.
- Actual release/coverage, retrieval UTC, resolved URL, filename, bytes, SHA-256, sheet/archive members, row counts and schema: **pending controlled acquisition**.
- Licence and redistribution evidence: **pending inspection of the official publication and file notices**. Public accessibility alone does not establish reuse rights.
- Required before analysis: metadata and coverage validation; freeze approval by Data Governance Analyst and domain analyst.

### S2 — Record-level_data_for_England_Wales_and_Scotland_-_Company_Insolvency_Statistics_June_2026.zip

Exact agreed download URL (copy verbatim):

```text
https://assets.publishing.service.gov.uk/media/6a57978e31fb6daf3141374c/Record-level_data_for_England_Wales_and_Scotland_-_Company_Insolvency_Statistics_June_2026.zip
```

- Publisher/source: Insolvency Service long-run monthly series + record-level England/Wales/Scotland data. The long-run file goes back to 2000 and the record ZIP is only 3.97 MB.
- Intended role: required core input.
- Access expectation from agreement: £0, public download, no paid API required.
- Verification state: URL recovered from the final agreed conversation; browser-only retrieval on 16 October 2026 could not validate the file contents. This is not a completed download/schema/licence check.
- File acquisition state: **not downloaded or uploaded in this master-pack build**.
- Actual release/coverage, retrieval UTC, resolved URL, filename, bytes, SHA-256, sheet/archive members, row counts and schema: **pending controlled acquisition**.
- Licence and redistribution evidence: **pending inspection of the official publication and file notices**. Public accessibility alone does not establish reuse rights.
- Required before analysis: metadata and coverage validation; freeze approval by Data Governance Analyst and domain analyst.

## Acquisition manifest requirements

Create one row per acquired file, including archive members and all eight months where applicable:

`source_id, original_url, resolved_url, retrieved_utc, publisher_release, filename, bytes, sha256, format, sheets_or_members, row_count, coverage_start, coverage_end, geography, schema_version, licence_evidence_path, approved_by, approval_date`

Never enter guessed values. A missing field remains pending with an owner and reason. Source IDs above are local to this project. Preserve the actual publisher metadata and notices alongside the manifest.

## Validation and fallback

Browser checks during this build could not inspect downloadable payloads consistently; unsupported download formats and retrieval failures do not prove a URL is broken. They also do not verify schema, current availability, advertised history, size or redistribution rights. Perform a controlled file acquisition before team analysis.

If the exact link fails, locate the same release through the official publisher's publication series, record the replacement URL and compare version/coverage. Escalate any change to cohort, dimensions or reporting window through the project change log. No paid source or live API is required by the agreed design. No guarantee is made that a publisher URL will remain unchanged indefinitely.

## Data sign-off

The Data Governance Analyst and domain analyst sign the actual manifest after checking file identity, licence, coverage and definitions. Ingest only the signed cohort. Every headline metric must trace through transformations back to a registered source and field.
