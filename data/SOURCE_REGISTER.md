# MTL-XF-030 — Source register and verification record

**Project:** River Water Quality Classification & Environmental Intervention Intelligence  
**Documentation review:** 16 October 2026  
**State:** official documentation checked; acquired-file validation and freeze approval pending.  
**Steward:** Data Governance Analyst, with the project domain specialist.

## Source/cohort decision

Retain both agreed England exports. Freeze them within one acquisition batch with separate retrieval timestamps and checksums. Use a single latest complete published classification year/cycle for the core baseline; lock its actual value at Week 2. Core screening is limited to the surface-water category available in the export and must be labelled accurately if rivers cannot be separated from canals/transfers. Use up to ten body-level investigation cases; catchment/measure links remain at their published grain.

**Outside core:** Cross-cycle deterioration, raw nutrient time series, causal measure effectiveness and a GIS map needing an additional boundary file are extensions. Cross-cycle change is blocked unless a comparability assessment explicitly passes; a valid single-cycle baseline fully satisfies core delivery.

## Official publication and methodology references

| Official reference | URL |
| --- | --- |
| Classification overview and historic comparability warning | https://environment.data.gov.uk/catchment-planning/England/classifications |
| Export endpoint documentation | https://environment.data.gov.uk/catchment-planning/api/docs |
| Definitions and chemical-status guidance | https://environment.data.gov.uk/catchment-planning/help/usage |

References above were inspected for this revision. They establish only the evidence described below; they are not a completed file acquisition, licence clearance or signed freeze.

## Verification findings

The official classification page warns that cycles can be incomparable and groups rivers, canals and transfers together in its summary. CDE guidance explains the 2019 chemical-method change and widespread failures associated with ubiquitous pollutants. The API documents both agreed England CSV endpoints. These facts support a single-cycle core and a requirement to validate water-body and measure-link grain.

**Field/reference mapping and acquisition instructions:** Identify actual body ID, body category, year/cycle, classification level/element, ecological status or potential, chemical status, measure identifier and published linkage keys. Never assume all measures have a direct body ID or implemented status. Record each export's own retrieval timestamp within one batch.

**Remaining status:** Classification/methodology pages and endpoint documentation verified; export schema, actual cycle, body-type filter, measure-link grain and checksums pending.

## Exact copyable file URLs

Original agreed URLs are retained. Entries labelled required supplement/reference or fallback are explicit changes from the initial pack. Do not silently replace an input with a newer release.

### S1 — Agreed core input 1

```text
https://environment.data.gov.uk/catchment-planning/England/classifications.csv
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

### S2 — Agreed core input 2

```text
https://environment.data.gov.uk/catchment-planning/England/measures.csv
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

## File validation and licence record

For every actually used input record:

`source_id, role_core_reference_fallback_extension, original_url, resolved_url, retrieved_utc, actual_release, filename, bytes, sha256, format, sheets_or_members, rows, geography, period_start, period_end, grain, schema_version, methodology_evidence, licence_notice, attribution, redistribution_conditions, approved_by, approval_date`

Retain the relevant publication/file notices, including exceptions and third-party conditions. Do not assume all publishers use the same licence. A stated publication licence does not remove the need to check file-specific terms. Keep unverified values pending; never invent a hash or approval.

## Support and freeze decision

Complete the [source-to-deliverable matrix](README.md). The domain specialist verifies actual grain, units, period comparability and supported metrics; the steward verifies identity and reuse terms. Required missing fields block dependent core outputs. Every activated extension is separately registered. Where a fallback is used, record why, which original it replaces, overlap handling and impact on outputs.

If an agreed URL fails, seek the same official archived release and record evidence. A browser format limitation does not prove a file is unavailable, and a successful page fetch does not prove payload integrity. Preserve the frozen version and metadata in the approved location so future website changes do not silently alter the cohort.
