# MTL-XF-030 — Metadata, lineage and freeze evidence

Metadata makes river water quality classification & environmental intervention intelligence reproducible. This folder currently contains guidance; no acquisition manifest or source sign-off is claimed.

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

Classification fact: water-body identifier × year/cycle × classification level/element × status and other published dimensions. Measures fact: published measure identifier × water-body/catchment links × status/category. Link using stable identifiers with a bridge for many-to-many relationships.

## Metric definition coverage

- Ecological status distribution: Distinct eligible water bodies by published ecological status within one assessment year/cycle.
- Good-or-better ecological share: 100 × eligible bodies with good/high ecological status / bodies with valid comparable ecological status.
- Chemical status distribution: Distinct bodies by chemical status, kept separate from ecological status.
- Comparable deterioration count: Bodies moving to a worse ordered ecological class between compatible cycles; chemical status uses its own rules.
- Recorded measure coverage: 100 × eligible bodies linked to at least one recorded measure / eligible bodies; no effectiveness claim.
- Measure status distribution: Distinct measures by available published implementation/status categories; preserve unknowns.
- Classification completeness: 100 × bodies with valid target classification / expected eligible bodies.
- Join coverage: Matched distinct water bodies / eligible bodies, plus unmatched and multiply linked measure counts.

Every listed metric needs source fields, transformation/formula, valid grain, unit, numerator/denominator, exclusions, zero/missing behaviour, refresh expectation, owner and test reference. Mark conditional metrics unavailable if the actual source cannot support them.

Store actual evidence only; never invent publisher schema, a completed licence review, a checksum or a stakeholder approval. See [source register](../SOURCE_REGISTER.md) and [acceptance criteria](../../project/ACCEPTANCE_CRITERIA.md).
