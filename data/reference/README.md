# MTL-XF-025 — Reference data and mappings

## Purpose

Maintain the code lists and crosswalks needed to implement this analytical grain:

National fact: month × jurisdiction × procedure × adjustment basis. Record fact: published insolvency event/record × event date × jurisdiction × available company/sector/geography fields. A company identifier need not uniquely identify an insolvency event.

Potential references are the publisher's geography/entity identifiers, category hierarchies, period definitions, units, status codes and revision markers. Include only references actually needed by the model. Register any separately downloaded official file as an additional source.

## Required mapping evidence

Each reference needs source/version, licence, valid-from/to dates, key uniqueness, allowed values, business meaning, owner and transformation use. For each crosswalk record source key, target key, relationship cardinality, rationale and treatment of unmapped or changed entities. Quantify 100% of unmatched keys; do not silently drop them or infer a mapping from similar names.

Avoid multiplying facts when a reference is many-to-many. Keep parent totals distinct from child categories. Non-official analyst-created groupings must be labelled as project assumptions and sensitivity-tested where they affect the investigation shortlist.

## Domain constraints

- Counts do not measure insolvency risk per business without a compatible business-population denominator.
- Public company records must not become personal profiles; omit unnecessary names and addresses from outputs.
- Retrospective insolvency indicators are not validated predictive early warnings; forecasting is optional and requires time-based evaluation.

The domain specialist approves category meaning and comparability. The Data Engineer supplies uniqueness, join-cardinality and coverage checks before the reference enters the curated model.
