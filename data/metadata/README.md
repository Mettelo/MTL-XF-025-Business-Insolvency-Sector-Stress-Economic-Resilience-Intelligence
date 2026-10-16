# MTL-XF-025 — Metadata, lineage and freeze evidence

Metadata makes business insolvency, sector stress & economic resilience intelligence reproducible. This folder currently contains guidance; no acquisition manifest or source sign-off is claimed.

## Required records after acquisition

- Source manifest: source ID, exact/resolved URL, retrieval UTC, actual release, filename, bytes, SHA-256, archive members/sheets and coverage.
- Publisher methodology and licence/attribution evidence with provenance and retrieval date.
- Schema and field dictionary: name, type, meaning, units, key role, missing/suppression markers and valid values.
- Business glossary and critical data elements, with named steward and approved definitions.
- Grain, hierarchy and join-cardinality documentation.
- Field-level lineage from raw fields through transformations to each headline metric/dashboard measure.
- Quality profile, row-accounting reconciliation, exclusions, unresolved exceptions and their decision impact.
- Freeze approval, change log and later revision comparisons.

## Model contract

National fact: month × jurisdiction × procedure × adjustment basis. Record fact: published insolvency event/record × event date × jurisdiction × available company/sector/geography fields. A company identifier need not uniquely identify an insolvency event.

## Metric definition coverage

- Monthly insolvency events: Published count by procedure, jurisdiction and adjustment basis.
- Year-on-year change: 100 × (monthly count / same month previous year − 1), only with positive comparable base.
- Three-month moving count: Trailing three-month sum; require all three months.
- Procedure share: 100 × procedure count / compatible jurisdiction total.
- Observed sector share: 100 × coded sector events / all observed eligible events; display uncoded share separately.
- Geographic coding coverage: 100 × valid mapped records / eligible record-level records.
- Record-to-series reconciliation gap: Record aggregate minus compatible published count; report scope and timing differences.
- Concentration: Sum of squared sector shares at a declared mutually exclusive industry level; report uncoded treatment.

Every listed metric needs source fields, transformation/formula, valid grain, unit, numerator/denominator, exclusions, zero/missing behaviour, refresh expectation, owner and test reference. Mark conditional metrics unavailable if the actual source cannot support them.

Store actual evidence only; never invent publisher schema, a completed licence review, a checksum or a stakeholder approval. See [source register](../SOURCE_REGISTER.md) and [acceptance criteria](../../project/ACCEPTANCE_CRITERIA.md).
