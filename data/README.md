# MTL-XF-030 — Data workspace

## Required sources and cohort

Environment Agency Catchment Data Explorer — England classifications and measures CSVs. These are direct machine-readable endpoints maintained by the Environment Agency.

Use the agreed Environment Agency England classifications.csv and measures.csv endpoints. They are mutable exports: freeze both at one recorded retrieval timestamp before team analysis. Filter to England river water bodies using actual type codes; include other water-body types only as separately labelled context. Compare classification years/cycles only when methodologically compatible. No raw Water Quality Explorer observations are required.

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

Classification fact: water-body identifier × year/cycle × classification level/element × status and other published dimensions. Measures fact: published measure identifier × water-body/catchment links × status/category. Link using stable identifiers with a bridge for many-to-many relationships.

## Required metric contract

| Metric | Required definition / calculation |
| --- | --- |
| Ecological status distribution | Distinct eligible water bodies by published ecological status within one assessment year/cycle. |
| Good-or-better ecological share | 100 × eligible bodies with good/high ecological status / bodies with valid comparable ecological status. |
| Chemical status distribution | Distinct bodies by chemical status, kept separate from ecological status. |
| Comparable deterioration count | Bodies moving to a worse ordered ecological class between compatible cycles; chemical status uses its own rules. |
| Recorded measure coverage | 100 × eligible bodies linked to at least one recorded measure / eligible bodies; no effectiveness claim. |
| Measure status distribution | Distinct measures by available published implementation/status categories; preserve unknowns. |
| Classification completeness | 100 × bodies with valid target classification / expected eligible bodies. |
| Join coverage | Matched distinct water bodies / eligible bodies, plus unmatched and multiply linked measure counts. |

## Mandatory quality risks

- Measures recorded in an administrative dataset do not prove implementation or ecological effectiveness.
- Do not average ordinal status labels into a continuous pollution score or combine chemical and ecological scales.
- Classification changes can reflect monitoring and method changes; these files do not supply raw chemical sampling histories.

1. Reconcile distinct-body status counts for five selected classifications/catchments.
2. Show a multi-measure join cannot inflate the count of water bodies.
3. Reject a cross-cycle deterioration comparison lacking comparability evidence.
4. Test unknown status, an unmatched body ID and a non-river exclusion.

## Folder ownership

- [raw](raw/README.md): unmodified approved source snapshots; guidance only at present.
- [reference](reference/README.md): governed code lists, hierarchies and crosswalks.
- [metadata](metadata/README.md): source notices, schema, glossary, lineage and manifest evidence.

Curated data, processing code, logs and test results belong in the team delivery repository. Preserve a reproducible boundary between source inputs and generated products. Do not add personal, confidential or paid-source data.
