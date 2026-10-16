# MTL-XF-030 — Acceptance criteria and domain tests

**Business decision owner:** Director of Catchment Environment & River Improvement. **Decision:** Which English river water bodies warrant further environmental investigation based on ecological/chemical classifications and recorded measures, with cycle comparability and evidence gaps made explicit?

## Delivery sign-off

| ID | Deliverables | Required pass evidence | Acceptance owner |
| --- | --- | --- | --- |
| AC1 | D1 | Eight user requirements cover the commissioned questions, named stakeholder actions and core/extension boundary. | Business Analyst / Director of Catchment Environment & River Improvement |
| AC2 | D2 | 100% of used source files have approved provenance, version/coverage, licence, retrieval UTC and SHA-256. Required fields and reference versions are checked. | Data Governance Analyst |
| AC3 | D3 | Every input row is accounted for; keys and all many-to-many/hierarchy effects have explicit checks and no unexplained duplication. | Data Engineer / independent reviewer |
| AC4 | D4 | Five source cells reconcile within a declared rounding tolerance; all material differences and non-additive totals are explained. | Domain specialist |
| AC5 | D5 | All 8 metric contracts are classified core/conditional and have tested definitions; no unsupported fields or fabricated unavailable values. | Data Governance Analyst / BI Developer |
| AC6 | D6 | Five findings cover all business questions or evidence gaps; period, eligible population, magnitude, comparison and limitation are visible. | Domain analyst |
| AC7 | D7 | The project-specific baseline and alternative below are implemented; eligibility, scenario changes, reason codes and evidence requests are visible. | Director of Catchment Environment & River Improvement |
| AC8 | D8 | Five BI measures reconcile to curated outputs; all filters/reset/export retain the scope, units and limitations. | BI Developer / operational UAT user |
| AC9 | D9 | DT1–DT10 have actual execution evidence and expected/actual outcomes; no unresolved critical/high defect. | Independent reviewer |
| AC10 | D10 | A distinct member's clean rerun reproduces equivalent core outputs with documented environment and checks. | Independent rerun reviewer |
| AC11 | D11 | Two-page maximum briefing and 15–20 minute presentation answer the decision and assign investigation owners without unsupported outcomes. | Director of Catchment Environment & River Improvement / Mettelo panel |
| AC12 | D12 | Every member links substantive authored and reviewed work, including handover or presentation contribution. | Delivery Lead |

## Project-specific business success

1. Exactly one declared classification year/cycle drives the core baseline and denominator.
2. Distinct body counts remain unchanged after linking classification elements and measures.
3. Each investigation distinguishes weak condition, missing evidence and recorded measure status without claiming ecological effectiveness.

## Required prioritisation and sensitivity

First compare an ecological-status-led queue with an evidence-gap-led queue within the same eligible body set. Preserve status/potential distinctions for modified/artificial bodies. Do not use an all-fail chemical status as if it independently differentiates priority. Catchment-level measures must not be attributed to every body as a proven body-level intervention.

Record each case's entity/segment, valid period, supporting measures, reason code, scenario position, missing evidence, responsible operational role, next review and manual-review trigger. Fewer than ten cases is valid; padding unsupported cases fails acceptance.

## DT1–DT10 — minimum executed domain tests

| Test | Input / action | Expected pass evidence |
| --- | --- | --- |
| DT1 | Reconcile distinct-body status counts for five selected classifications/catchments. | Five selected published values reproduce within declared source precision, with explicit source coordinates and scope. |
| DT2 | Show a multi-measure join cannot inflate the count of water bodies. | The invalid comparison, join or denominator is rejected or flagged according to the documented rule; no silent fallback. |
| DT3 | Reject a cross-cycle deterioration comparison lacking comparability evidence. | The edge case produces an explicit unavailable/exclusion result or a supported calculation, with affected rows quantified. |
| DT4 | Test unknown status, an unmatched body ID and exclusion of water-body categories outside the explicitly approved river or combined category. | The domain boundary remains visible in the analytical output and BI product; no unsupported inference. |
| DT5 | One water body has five classification elements and three linked measures | The linked diagnostic may expand, but the body count remains one. |
| DT6 | A chemical status is identical for every eligible body | Show no discriminatory power; do not manufacture a ranking from tied values. |
| DT7 | A modified body reports ecological potential | Preserve potential rather than relabel as natural-body status without a rule. |
| DT8 | The source groups rivers, canals and transfers | Label the group honestly or register a verified river-only filter; no unsupported river-only claim. |
| DT9 | A measure links only to a catchment | Keep that link at catchment grain; no automatic implemented-measure flag for every body. |
| DT10 | Two classification cycles lack method comparability | No deterioration conclusion; core single-cycle baseline remains complete. |

Worked values are **synthetic test fixtures**, not claims about the public data or simulated client. For each test retain requirement ID, source/input or fixture, expected result, actual result, evidence link, tester, independent reviewer and date. DT1–DT4 additionally require the documented project-specific rule; their general evidence descriptions do not waive the named domain condition. Add dashboard/filter tests as needed beyond these ten.

## Scope gate and unresolved issues

**Mandatory core:** Retain both agreed England exports. Freeze them within one acquisition batch with separate retrieval timestamps and checksums. Use a single latest complete published classification year/cycle for the core baseline; lock its actual value at Week 2. Core screening is limited to the surface-water category available in the export and must be labelled accurately if rivers cannot be separated from canals/transfers. Use up to ten body-level investigation cases; catchment/measure links remain at their published grain.

**Optional extensions:** Cross-cycle deterioration, raw nutrient time series, causal measure effectiveness and a GIS map needing an additional boundary file are extensions. Cross-cycle change is blocked unless a comparability assessment explicitly passes; a valid single-cycle baseline fully satisfies core delivery.

A mandatory source/field gap blocks the affected deliverable and must be resolved by a registered official replacement or approved, versioned scope change. An explicitly optional result may be unavailable with a reason and a useful evidence request. Neither missing raw data nor unexecuted tests may be marked passed.

A critical/high defect materially changes a headline value, cohort, recommendation, provenance or reproducibility and blocks release. Lower-impact issues require a named acceptance owner and disclosed impact. All panel feedback and approvals must be recorded honestly as simulated where applicable.
