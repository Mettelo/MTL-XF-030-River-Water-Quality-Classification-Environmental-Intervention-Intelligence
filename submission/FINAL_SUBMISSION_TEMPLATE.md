# MTL-XF-030 — Final submission: River Water Quality Classification & Environmental Intervention Intelligence

Complete this template in your team repository as `submission/FINAL_SUBMISSION.md`. Replace prompts with evidence; leave unavailable items explicitly unavailable with reasons. This template itself is not completed delivery evidence.

## Team and version

- Team repository URL:
- Team name and individual GitHub accounts:
- Final commit/tag and submission date:
- Master specification URL and reviewed commit:
- Delivery dates:
- Named role owners and independent reviewers:
- Engagement declaration: simulated confidential-client engagement using official public/open data; no real-client employment, endorsement or privileged access claimed.

## Commissioned decision

Which English river water bodies warrant further environmental investigation based on ecological/chemical classifications and recorded measures, with cycle comparability and evidence gaps made explicit?

State the answer, confidence, principal limitation and proposed investigation action.

## Actual cohort and provenance

Agreed boundary: Use the agreed Environment Agency England classifications.csv and measures.csv endpoints. They are mutable exports: freeze both at one recorded retrieval timestamp before team analysis. Filter to England river water bodies using actual type codes; include other water-body types only as separately labelled context. Compare classification years/cycles only when methodologically compatible. No raw Water Quality Explorer observations are required.

Record actual frozen files/versions, manifest/checksums, source-register link, licence evidence, retrieval timestamp, schema/coverage validation, inclusions/exclusions and approved deviations. Do not mark acquisition complete without evidence.

## Evidence index

| Deliverable | Artefact link | Owner / reviewer | Status / limitation |
| --- | --- | --- | --- |
| D1 — Discovery & decision requirements | To complete | To complete | To complete |
| D2 — Governed sources & cohort | To complete | To complete | To complete |
| D3 — Reproducible analytical model | To complete | To complete | To complete |
| D4 — Quality & reconciliation | To complete | To complete | To complete |
| D5 — KPI catalogue | To complete | To complete | To complete |
| D6 — Domain analytical assessment | To complete | To complete | To complete |
| D7 — Investigation decision framework | To complete | To complete | To complete |
| D8 — BI decision-support product | To complete | To complete | To complete |
| D9 — Independent assurance & UAT | To complete | To complete | To complete |
| D10 — Technical & operational handover | To complete | To complete | To complete |
| D11 — Executive recommendation | To complete | To complete | To complete |
| D12 — Contribution & delivery record | To complete | To complete | To complete |

## Governed measures

| Required measure | Definition/source/test link | Result / unavailable reason |
| --- | --- | --- |
| Ecological status distribution | To complete | To complete |
| Good-or-better ecological share | To complete | To complete |
| Chemical status distribution | To complete | To complete |
| Comparable deterioration count | To complete | To complete |
| Recorded measure coverage | To complete | To complete |
| Measure status distribution | To complete | To complete |
| Classification completeness | To complete | To complete |
| Join coverage | To complete | To complete |

## Business questions and five findings

1. Which river water bodies have the weakest ecological or chemical status in a comparable assessment cycle?
2. Which apparent changes may reflect methodology rather than environmental change?
3. Where are recorded measures linked to weaker classifications?
4. Which bodies have missing classification or measure evidence?
5. Which cases require field sampling, pressure assessment or delivery-status investigation?

For each question record the finding, quantitative evidence, period/grain, comparison, uncertainty, limitation and artefact link. Record an evidenced gap where the data cannot answer it.

## Investigation shortlist and sensitivity

Provide up to ten supported cases. For each: entity/segment, signal and magnitude, eligibility, reason code, scenario membership, proposed investigation, responsible role, missing evidence and review trigger. Compare at least two scenarios and explain membership/rank changes. Include a case where evidence is insufficient for action.

## Acceptance and assurance

| Criterion | Pass/fail / evidence / reviewer |
| --- | --- |
| AC1 (D1) | To complete |
| AC2 (D2) | To complete |
| AC3 (D3) | To complete |
| AC4 (D4) | To complete |
| AC5 (D4–D5) | To complete |
| AC6 (D5) | To complete |
| AC7 (D6) | To complete |
| AC8 (D7) | To complete |
| AC9 (D8) | To complete |
| AC10 (D9) | To complete |
| AC11 (D10–D11) | To complete |
| AC12 (D12) | To complete |

Record at least ten executed UAT scenarios, expected/actual results, defect severity/disposition and five reconciled BI measures. Mandatory cases:

1. Reconcile distinct-body status counts for five selected classifications/catchments.
2. Show a multi-measure join cannot inflate the count of water bodies.
3. Reject a cross-cycle deterioration comparison lacking comparability evidence.
4. Test unknown status, an unmatched body ID and a non-river exclusion.

## Reproducible handover

- Environment/tool versions and dependencies:
- Input snapshot location and checksum verification:
- Clean run instructions and output locations:
- Independent rerun reviewer/date/duration/results:
- Reconciliation evidence and permitted rounding:
- Refresh/change process and known failure modes:

## Executive delivery

- Two-page briefing link:
- Presentation link and 15–20 minute duration:
- Dashboard/free access instructions and static export:
- Recommendations, missing evidence, responsible roles and next review:

## Contributions

For every member link authored artefacts, review work, issues/PRs/commits and presentation/handover contribution. Link `CONTRIBUTIONS.md`; commit count alone is insufficient.

## Limitations and review decision

- Measures recorded in an administrative dataset do not prove implementation or ecological effectiveness.
- Do not average ordinal status labels into a continuous pollution score or combine chemical and ecological scales.
- Classification changes can reflect monitoring and method changes; these files do not supply raw chemical sampling histories.

Add actual limitations, optional extensions, unresolved accepted issues and their impacts. Record simulated panel review date, reviewers and decision only after review occurs. Do not claim real operational savings or outcome improvements.
