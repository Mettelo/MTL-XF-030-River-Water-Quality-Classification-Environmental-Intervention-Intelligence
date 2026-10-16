# MTL-XF-030 — Required deliverables and metric contracts

**Decision:** Which English river water bodies warrant further environmental investigation based on ecological/chemical classifications and recorded measures, with cycle comparability and evidence gaps made explicit?  
**Business acceptance:** Director of Catchment Environment & River Improvement  
**Core scope:** Retain both agreed England exports. Freeze them within one acquisition batch with separate retrieval timestamps and checksums. Use a single latest complete published classification year/cycle for the core baseline; lock its actual value at Week 2. Core screening is limited to the surface-water category available in the export and must be labelled accurately if rivers cannot be separated from canals/transfers. Use up to ten body-level investigation cases; catchment/measure links remain at their published grain.

All artefact locations refer to the team repository. Deliver the core before optional extensions. [The source register](../data/SOURCE_REGISTER.md) documents evidence status; required field support is a G1 release condition.

## D1 — Discovery & requirements

**Due:** Week 1 · **Location:** `docs/01-discovery/` · **Owner:** Business Analyst

Map the annual classification review and quarterly catchment programme meeting, stakeholder needs, current reporting failures and target decision. Eight prioritised requirements must cover the business questions, scope gates and usable outputs.

**Pass evidence:** Each requirement has an accountable user, artefact, test and acceptance owner.

## D2 — Sources, governance & cohort contract

**Due:** Week 2 · **Location:** `data/; docs/02-data-governance/` · **Owner:** Data Governance Analyst

Complete the source-to-deliverable support matrix and classify core, fallback and optional inputs. Retain both agreed England exports. Freeze them within one acquisition batch with separate retrieval timestamps and checksums. Use a single latest complete published classification year/cycle for the core baseline; lock its actual value at Week 2. Core screening is limited to the surface-water category available in the export and must be labelled accurately if rivers cannot be separated from canals/transfers. Use up to ten body-level investigation cases; catchment/measure links remain at their published grain.

**Pass evidence:** Every used input has provenance, exact version/coverage, licence evidence and SHA-256; conditional scope cannot be signed off without supporting fields.

## D3 — Reproducible model & ingestion

**Due:** Week 3 · **Location:** `src/; sql/; docs/03-data-model/` · **Owner:** Data Engineer

Implement raw preservation, selection, schema checks, curated facts and dimensions. Classification fact: water-body identifier × year/cycle × classification level/element × status and other published dimensions. Measures fact: published measure identifier × water-body/catchment links × status/category. Link using stable identifiers with a bridge for many-to-many relationships.

**Pass evidence:** Zero unexplained duplicate keys or join inflation; every input row accounted for as retained/excluded/quarantined.

## D4 — Quality, source reconciliation & exceptions

**Due:** Week 3 · **Location:** `tests/; docs/04-data-quality/` · **Owner:** Independent reviewer + domain specialist

Execute source, denominator, missingness, boundary and linkage checks against the risk 'Cross-cycle methods, repeated elements and many-to-many measure linkage may create false deterioration, body counts or intervention coverage.'

**Pass evidence:** Reconcile five source values from at least two periods or segments; retain source coordinates, precision and explanations for non-additive totals.

## D5 — Governed metric catalogue

**Due:** Week 4 · **Location:** `docs/05-kpi-catalogue/` · **Owner:** Domain specialist + Data Governance Analyst

Implement the 8 metric contracts below; distinguish unconditional core metrics from gated extensions.

**Pass evidence:** Each core metric has purpose, raw fields, formula, grain, denominator/unit, missing/zero handling, owner, refresh and test; conditional items have explicit eligibility or unavailable status.

## D6 — Domain assessment

**Due:** Week 5 · **Location:** `analysis/; docs/06-analysis/` · **Owner:** Domain analyst

Create a classification baseline for the explicitly verified river or combined surface-water category in one declared year/cycle, keeping ecological and chemical outcomes separate. Assess change only where comparability is evidenced; otherwise deliver a single-cycle baseline and a documented comparability rejection.

**Pass evidence:** At least five supported findings answer the five questions or document a genuine evidence gap; each includes magnitude, scope, comparison and limitation.

## D7 — Investigation framework & scenarios

**Due:** Week 6 · **Location:** `docs/07-decision-framework/` · **Owner:** Director of Catchment Environment & River Improvement (business acceptance)

First compare an ecological-status-led queue with an evidence-gap-led queue within the same eligible body set. Preserve status/potential distinctions for modified/artificial bodies. Do not use an all-fail chemical status as if it independently differentiates priority. Catchment-level measures must not be attributed to every body as a proven body-level intervention.

**Pass evidence:** Publish eligibility, component definitions, scenario differences and up to ten supported cases; every case names a service role, evidence request and review trigger.

## D8 — Decision-support BI

**Due:** Draft Week 6; final Week 7 · **Location:** `dashboard/` · **Owner:** BI Developer

Build overview, diagnostic and quality pages for the annual classification review and quarterly catchment programme meeting. Show period, units, definitions, missingness and core/extension status.

**Pass evidence:** Five headline values reconcile; every visible filter and reset tested; accessible static export plus free review/build path.

## D9 — Assurance & simulated UAT

**Due:** Week 7 · **Location:** `docs/08-assurance-uat/` · **Owner:** Independent reviewer

Execute DT1–DT10 below, plus any tool-specific calculations and filter tests. Record expected/actual evidence, requirement links and defects.

**Pass evidence:** All ten mandatory domain cases evidenced; no critical/high issue remains; accepted lower-impact limitations have named review.

## D10 — Technical & operational handover

**Due:** Week 8 · **Location:** `docs/09-technical-handover/` · **Owner:** Data Engineer + a second-member reviewer

Provide environment, immutable manifest, end-to-end run, output checks, troubleshooting and refresh/change process.

**Pass evidence:** A second member regenerates equivalent core outputs without undocumented edits and records checks, environment, duration and result.

## D11 — Executive briefing & presentation

**Due:** Week 8 · **Location:** `deliverables/` · **Owner:** Business Analyst + specialist service roles

Deliver maximum two-page briefing and 15–20 minute presentation to Director of Catchment Environment & River Improvement: decision, five findings, scenario comparison, investigation actions, evidence gaps and next review.

**Pass evidence:** Every numeric claim links to tested evidence; explicitly show a case where action is not yet supported.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8 · **Location:** `CONTRIBUTIONS.md` · **Owner:** Delivery Lead

Link actual authored work, reviews, issues/PRs/commits and presentation/handover contributions for every member.

**Pass evidence:** All responsibilities have owners and evidence; commit count alone is insufficient.

## Metric contracts — authoritative definitions

| Metric | Definition / support condition |
| --- | --- |
| Ecological status distribution | Distinct eligible water bodies by published ecological status within one assessment year/cycle. |
| Good-or-better ecological share | 100 × eligible bodies with good/high ecological status / bodies with valid comparable ecological status. |
| Chemical status distribution | Distinct bodies by chemical status, kept separate from ecological status. |
| Deterioration count — optional extension | Only after a documented comparability assessment passes; otherwise report unavailable and complete the single-cycle core. |
| Recorded-measure linkage — conditional | Report body-level coverage only where a valid body link exists; otherwise summarise measures at their published catchment grain. |
| Measure status distribution | Distinct measures by available published implementation/status categories; preserve unknowns. |
| Classification completeness | 100 × bodies with valid target classification / expected eligible bodies. |
| Join coverage | Matched distinct water bodies / eligible bodies, plus unmatched and multiply linked measure counts. |

For each metric add source ID and actual raw fields, business purpose, formula, grain, valid population, unit, numerator/denominator, hierarchy, suppression/zero/missing handling, owner, refresh and test evidence. Verify source rounding before setting a reconciliation tolerance. A conditional item is not silently promoted into core; a core requirement is not silently waived.

## Project-specific outcomes

1. Exactly one declared classification year/cycle drives the core baseline and denominator.
2. Distinct body counts remain unchanged after linking classification elements and measures.
3. Each investigation distinguishes weak condition, missing evidence and recorded measure status without claiming ecological effectiveness.

See [DT1–DT10 and investigation rules](ACCEPTANCE_CRITERIA.md) for worked pass/fail cases. Source schemas, specific period selections and reference versions must be signed at G1. Keep calculation definitions here; other guidance pages link to this contract rather than maintaining competing copies.
