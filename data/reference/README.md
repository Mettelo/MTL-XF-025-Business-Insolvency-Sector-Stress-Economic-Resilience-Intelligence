# MTL-XF-025 — Reference mappings

References support the approved [model and cohort](../README.md). Do not assume a mapping exists solely because entity names look similar.

Required acquisition checks: Required metadata reference: https://assets.publishing.service.gov.uk/media/6a5798509e6315445441375c/Metadata_for_Long-Run_Series_in_CSV_Format_-_Company_Insolvency_Statistics_June_2026.csv . Read ZIP documentation to establish event date, procedure, jurisdiction, company identifier and any industry/location fields; do not treat company identifier alone as an event key.

For each mapping record source/version, licence, key, definition, valid dates, uniqueness, relationship cardinality, unmatched coverage and responsible domain steward. Quantify every unmapped category/entity. Keep totals distinct from components and do not multiply fact rows through many-to-many crosswalks.

Analyst-created groupings and eligibility thresholds are labelled project assumptions. If they affect case selection, show their effect in [the scenario comparison](../../project/ACCEPTANCE_CRITERIA.md). Candidate raw field names or download references in the source register still require actual version validation.
