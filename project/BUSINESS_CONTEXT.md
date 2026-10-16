# MTL-XF-030 — Business context

## Organisation and decision owner

**Simulated client:** Confidential Catchment Environment & River Improvement Authority. **Accountable executive:** Director of Catchment Environment & River Improvement. **Review cadence:** annual classification review and quarterly catchment programme meeting.

This fictional directorate/board is an engagement scenario, not an assertion of a real client's circumstances. The source data remains official public/open data.

## Business setting and immediate planning need

The simulated catchment environment authority coordinates a quarterly programme meeting and an annual classification review. It has to choose where to commission evidence gathering and measure-delivery checks before a river-improvement proposal is advanced.

## Business problem

The Director of Catchment Environment & River Improvement needs a practical investigation agenda from a complex classification and measures register. A water body may have many element records, while one measure may relate to multiple places; a flat report can make documentation density look like a larger environmental problem. A broad chemical-failure label may also provide little distinction between competing cases.

The authority needs to distinguish three operational questions: where ecological condition merits specialist review, where classification evidence is incomplete, and where recorded measures need delivery-status clarification. The commission is a transparent same-cycle baseline and investigation queue that helps programme managers assign those questions without claiming that a listed measure has been implemented or has improved a river.

## Why the current process is insufficient

Classification summaries and measures lists are reviewed separately, so a weak status does not arrive with a clear evidence request or responsible programme role. Cross-cycle changes may be interpreted as deterioration before comparability is checked. The replacement must preserve distinct body counts, keep ecological and chemical assessments separate, and connect records only at their supported grain.

## Stakeholders and decisions

| Simulated stakeholder | Decision / review responsibility |
| --- | --- |
| Director of Catchment Environment & River Improvement | Accountable for scope, investigation priorities, accepted limitations and final business sign-off. |
| Catchment Programme Manager | Select evidence-gathering and delivery-status investigations. |
| Environmental Classification Specialist | Approve classification level, status order and within-cycle comparability. |
| Catchment / GIS Data Steward | Validate water-body IDs, categories and links between bodies and measures. |
| Environmental Assurance Lead | Challenge deterioration and measure-effectiveness claims. |

## Commissioned decision

Which English river water bodies warrant further environmental investigation based on ecological/chemical classifications and recorded measures, with cycle comparability and evidence gaps made explicit?

## Practical management use case

In the quarterly meeting, the Programme Manager opens the declared classification-year/cycle baseline and reviews two queues: ecological-condition cases and evidence-gap cases. The Classification Specialist checks status versus potential and the water-body category, while the Data Steward confirms whether a recorded measure is linked to that body or only to the wider catchment.

The Director commissions a specialist evidence review or a measure-delivery-status enquiry, naming an owner and required evidence. A uniform chemical-failure result is explained rather than used as a spurious tie-breaker. Where cross-cycle comparability cannot be established, the decision uses the valid single-cycle baseline and records the limitation.

## Current-to-target workflow

**Target management handover:** A catchment review pack containing a single-cycle body baseline, distinct ecological/chemical views, a verified measures linkage, two investigation queues and an evidence-request register for condition or delivery-status checks.

The meeting's decision record must contain: the selected case and reporting period; the source-backed finding; the decision to investigate, watch, clarify or close; the responsible stakeholder role; the specific additional evidence requested; and the next review point. Add the evidence that would reverse or narrow the recommendation. A watchlist or no-action conclusion is valid when supported; do not fill the shortlist simply to reach ten cases.

## Required analytical response

- Create a classification baseline for the explicitly verified river or combined surface-water category in one declared year/cycle, keeping ecological and chemical outcomes separate.
- Assess change only where comparability is evidenced; otherwise deliver a single-cycle baseline and a documented comparability rejection.
- Shortlist up to ten water bodies for investigation using classification weakness, missingness and recorded-measure context; test at least two classification/missingness priority rules.

## Measurable project outcomes

1. Exactly one declared classification year/cycle drives the core baseline and denominator.
2. Distinct body counts remain unchanged after linking classification elements and measures.
3. Each investigation distinguishes weak condition, missing evidence and recorded measure status without claiming ecological effectiveness.

## Proposed benefit monitoring

Measure whether every selected case cites a classification cycle, eligible body identifier, supported measure-link level and investigation owner; target 100%. Simulated users must distinguish poor condition from missing evidence and recorded measures from confirmed delivery. Ecological recovery requires later comparable monitoring and evaluation.

Record the preparation and review baseline at kickoff, then measure evidence-pack regeneration during the independent rerun. No pre-project time saving or achieved operational benefit is assumed. The eight-week engagement is assessed on the usability and traceability of the decision pack; later service outcomes require separate follow-up.

## Scope and evidence limits

**Core:** Retain both agreed England exports. Freeze them within one acquisition batch with separate retrieval timestamps and checksums. Use a single latest complete published classification year/cycle for the core baseline; lock its actual value at Week 2. Core screening is limited to the surface-water category available in the export and must be labelled accurately if rivers cannot be separated from canals/transfers. Use up to ten body-level investigation cases; catchment/measure links remain at their published grain.

**Extensions:** Cross-cycle deterioration, raw nutrient time series, causal measure effectiveness and a GIS map needing an additional boundary file are extensions. Cross-cycle change is blocked unless a comparability assessment explicitly passes; a valid single-cycle baseline fully satisfies core delivery.

- Measures recorded in an administrative dataset do not prove implementation or ecological effectiveness.
- Do not average ordinal status labels into a continuous pollution score or combine chemical and ecological scales.
- Classification changes can reflect monitoring and method changes; these files do not supply raw chemical sampling histories.

## Risks, mitigations and escalation

- **Interpretation risk:** Cross-cycle methods, repeated elements and many-to-many measure linkage may create false deterioration, body counts or intervention coverage. The domain specialist reviews definitions and DT1–DT10 before sign-off.
- **Source risk:** Classification/methodology pages and endpoint documentation verified; export schema, actual cycle, body-type filter, measure-link grain and checksums pending. The steward records unresolved items at G1; mandatory gaps block dependent outputs.
- **Decision risk:** prioritisation assumptions may affect which cases appear. Show alternative scenarios, excluded cases and evidence that could change a recommendation.
- **Delivery risk:** limited time or skills can leave undocumented manual steps. Assign a second-member rerun and retain contribution/review evidence throughout the eight weeks.

## Evidence chain

Stakeholder requirement → registered source and valid cohort → governed field/metric → tested transformation → reconciled finding → scenario reason code → investigation owner/evidence request → simulated UAT and sign-off.

Every major recommendation must be traceable through this chain.
