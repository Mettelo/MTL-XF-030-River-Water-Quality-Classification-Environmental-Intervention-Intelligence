# MTL-XF-030 — Reference mappings

References support the approved [model and cohort](../README.md). Do not assume a mapping exists solely because entity names look similar.

Required acquisition checks: Identify actual body ID, body category, year/cycle, classification level/element, ecological status or potential, chemical status, measure identifier and published linkage keys. Never assume all measures have a direct body ID or implemented status. Record each export's own retrieval timestamp within one batch.

For each mapping record source/version, licence, key, definition, valid dates, uniqueness, relationship cardinality, unmatched coverage and responsible domain steward. Quantify every unmapped category/entity. Keep totals distinct from components and do not multiply fact rows through many-to-many crosswalks.

Analyst-created groupings and eligibility thresholds are labelled project assumptions. If they affect case selection, show their effect in [the scenario comparison](../../project/ACCEPTANCE_CRITERIA.md). Candidate raw field names or download references in the source register still require actual version validation.
