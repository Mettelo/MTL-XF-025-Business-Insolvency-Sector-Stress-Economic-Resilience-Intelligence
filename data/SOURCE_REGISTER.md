# MTL-XF-025 — Source register and verification record

**Project:** Business Insolvency, Sector Stress & Economic Resilience Intelligence  
**Documentation review:** 16 October 2026  
**State:** official documentation checked; acquired-file validation and freeze approval pending.  
**Steward:** Data Governance Analyst, with the project domain specialist.

## Source/cohort decision

June 2026 long-run CSV plus the agreed England/Wales/Scotland record ZIP and long-run metadata. Establish actual record-level dates, fields and event keys before sector/geographic analysis. National history and observed event history remain separate; all records with missing industry/geography stay visible in coverage diagnostics.

**Outside core:** Risk per active business, trading-site exposure, predictive early warning and causal support effectiveness require additional denominators/evaluation. If the ZIP lacks a required breakdown, use a registered official industry table for sector analysis; do not infer it from company names.

## Official publication and methodology references

| Official reference | URL |
| --- | --- |
| June 2026 official release and methodology links | https://www.gov.uk/government/statistics/company-insolvencies-june-2026 |

References above were inspected for this revision. They establish only the evidence described below; they are not a completed file acquisition, licence clearance or signed freeze.

## Verification findings

The official release lists the long-run CSV, separate metadata, record-level ZIP and industry tables. It notes that connected-company administrations can affect a monthly movement. Registration counts and population-based insolvency rates are different measures; the release does not verify every field or historical span inside the ZIP.

**Field/reference mapping and acquisition instructions:** Required metadata reference: https://assets.publishing.service.gov.uk/media/6a5798509e6315445441375c/Metadata_for_Long-Run_Series_in_CSV_Format_-_Company_Insolvency_Statistics_June_2026.csv . Read ZIP documentation to establish event date, procedure, jurisdiction, company identifier and any industry/location fields; do not treat company identifier alone as an event key.

**Remaining status:** Release resources and metadata link verified; ZIP members, event coverage, sector/location schema and frozen checksums pending.

## Exact copyable file URLs

Original agreed URLs are retained. Entries labelled required supplement/reference or fallback are explicit changes from the initial pack. Do not silently replace an input with a newer release.

### S1 — Agreed core input 1

```text
https://assets.publishing.service.gov.uk/media/6a57978e31fb6daf3141374b/Long-Run_Series_in_CSV_Format_-_Company_Insolvency_Statistics_June_2026.csv
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S2 — Agreed core input 2

```text
https://assets.publishing.service.gov.uk/media/6a57978e31fb6daf3141374c/Record-level_data_for_England_Wales_and_Scotland_-_Company_Insolvency_Statistics_June_2026.zip
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### R1 — Required long-run series metadata

```text
https://assets.publishing.service.gov.uk/media/6a5798509e6315445441375c/Metadata_for_Long-Run_Series_in_CSV_Format_-_Company_Insolvency_Statistics_June_2026.csv
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Reference metadata; match its version to the analytical input.

## File validation and licence record

For every actually used input record:

`source_id, role_core_reference_fallback_extension, original_url, resolved_url, retrieved_utc, actual_release, filename, bytes, sha256, format, sheets_or_members, rows, geography, period_start, period_end, grain, schema_version, methodology_evidence, licence_notice, attribution, redistribution_conditions, approved_by, approval_date`

Retain the relevant publication/file notices, including exceptions and third-party conditions. Do not assume all publishers use the same licence. A stated publication licence does not remove the need to check file-specific terms. Keep unverified values pending; never invent a hash or approval.

## Support and freeze decision

Complete the [source-to-deliverable matrix](README.md). The domain specialist verifies actual grain, units, period comparability and supported metrics; the steward verifies identity and reuse terms. Required missing fields block dependent core outputs. Every activated extension is separately registered. Where a fallback is used, record why, which original it replaces, overlap handling and impact on outputs.

If an agreed URL fails, seek the same official archived release and record evidence. A browser format limitation does not prove a file is unavailable, and a successful page fetch does not prove payload integrity. Preserve the frozen version and metadata in the approved location so future website changes do not silently alter the cohort.
