# MTL-XF-030 — Source register

**Project:** River Water Quality Classification & Environmental Intervention Intelligence  
**Register date:** 16 October 2026  
**Status:** agreed source references recovered; acquisition, payload verification and freeze approval pending.

## Cohort contract

Use the agreed Environment Agency England classifications.csv and measures.csv endpoints. They are mutable exports: freeze both at one recorded retrieval timestamp before team analysis. Filter to England river water bodies using actual type codes; include other water-body types only as separately labelled context. Compare classification years/cycles only when methodologically compatible. No raw Water Quality Explorer observations are required.

## Source entries

### S1 — classifications.csv

Exact agreed download URL (copy verbatim):

```text
https://environment.data.gov.uk/catchment-planning/England/classifications.csv
```

- Publisher/source: Environment Agency Catchment Data Explorer — England classifications and measures CSVs. These are direct machine-readable endpoints maintained by the Environment Agency.
- Intended role: required core input.
- Access expectation from agreement: £0, public download, no paid API required.
- Verification state: URL recovered from the final agreed conversation; browser-only retrieval on 16 October 2026 could not validate the file contents. This is not a completed download/schema/licence check.
- File acquisition state: **not downloaded or uploaded in this master-pack build**.
- Actual release/coverage, retrieval UTC, resolved URL, filename, bytes, SHA-256, sheet/archive members, row counts and schema: **pending controlled acquisition**.
- Licence and redistribution evidence: **pending inspection of the official publication and file notices**. Public accessibility alone does not establish reuse rights.
- Required before analysis: metadata and coverage validation; freeze approval by Data Governance Analyst and domain analyst.

### S2 — measures.csv

Exact agreed download URL (copy verbatim):

```text
https://environment.data.gov.uk/catchment-planning/England/measures.csv
```

- Publisher/source: Environment Agency Catchment Data Explorer — England classifications and measures CSVs. These are direct machine-readable endpoints maintained by the Environment Agency.
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
