# MTL-XF-030 — River Water Quality Classification & Environmental Intervention Intelligence

**Mettelo Project Studio** · Cross-Functional · Master project specification  
**Client:** Confidential Catchment Environment & River Improvement Authority  
**Accountable simulated executive:** Director of Catchment Environment & River Improvement  
**Sector:** Environment / Water / Catchment Planning  
**Team:** 6–8 people · **Window:** 8 weeks  
**Status:** documentation revised; file acquisition and cohort freeze pending  
**Review cadence:** annual classification review and quarterly catchment programme meeting

> This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Business setting

The simulated catchment environment authority coordinates a quarterly programme meeting and an annual classification review. It has to choose where to commission evidence gathering and measure-delivery checks before a river-improvement proposal is advanced.

## Business problem

The Director of Catchment Environment & River Improvement needs a practical investigation agenda from a complex classification and measures register. A water body may have many element records, while one measure may relate to multiple places; a flat report can make documentation density look like a larger environmental problem. A broad chemical-failure label may also provide little distinction between competing cases.

The authority needs to distinguish three operational questions: where ecological condition merits specialist review, where classification evidence is incomplete, and where recorded measures need delivery-status clarification. The commission is a transparent same-cycle baseline and investigation queue that helps programme managers assign those questions without claiming that a listed measure has been implemented or has improved a river.

## Commissioned decision

> Which English river water bodies warrant further environmental investigation based on ecological/chemical classifications and recorded measures, with cycle comparability and evidence gaps made explicit?

## Practical use

In the quarterly meeting, the Programme Manager opens the declared classification-year/cycle baseline and reviews two queues: ecological-condition cases and evidence-gap cases. The Classification Specialist checks status versus potential and the water-body category, while the Data Steward confirms whether a recorded measure is linked to that body or only to the wider catchment.

The Director commissions a specialist evidence review or a measure-delivery-status enquiry, naming an owner and required evidence. A uniform chemical-failure result is explained rather than used as a spurious tie-breaker. Where cross-cycle comparability cannot be established, the decision uses the valid single-cycle baseline and records the limitation.

**Management handover:** A catchment review pack containing a single-cycle body baseline, distinct ecological/chemical views, a verified measures linkage, two investigation queues and an evidence-request register for condition or delivery-status checks.

The full [business context](project/BUSINESS_CONTEXT.md) sets out stakeholders, decisions, evidence limits and proposed benefit measures.

## What must be delivered

1. Create a classification baseline for the explicitly verified river or combined surface-water category in one declared year/cycle, keeping ecological and chemical outcomes separate.
2. Assess change only where comparability is evidenced; otherwise deliver a single-cycle baseline and a documented comparability rejection.
3. Shortlist up to ten water bodies for investigation using classification weakness, missingness and recorded-measure context; test at least two classification/missingness priority rules.

The complete D1–D12 pack includes discovery, source governance, ingestion/model, quality, metric catalogue, analysis, investigation scenarios, BI, assurance/UAT, independent handover, executive briefing and contribution evidence. A dashboard by itself does not satisfy the commission.

## Fixed core and optional work

**Core:** Retain both agreed England exports. Freeze them within one acquisition batch with separate retrieval timestamps and checksums. Use a single latest complete published classification year/cycle for the core baseline; lock its actual value at Week 2. Core screening is limited to the surface-water category available in the export and must be labelled accurately if rivers cannot be separated from canals/transfers. Use up to ten body-level investigation cases; catchment/measure links remain at their published grain.

**Extensions:** Cross-cycle deterioration, raw nutrient time series, causal measure effectiveness and a GIS map needing an additional boundary file are extensions. Cross-cycle change is blocked unless a comparability assessment explicitly passes; a valid single-cycle baseline fully satisfies core delivery.

Source support is checked at the Week 2 gate. A required output is blocked until its fields and cohort are verified; it cannot pass acceptance through a generic “data unavailable” disclaimer. An explicitly optional extension may remain unavailable with a reason. See [exact source URLs and verification evidence](data/SOURCE_REGISTER.md).

## Measurable project outcomes

1. Exactly one declared classification year/cycle drives the core baseline and denominator.
2. Distinct body counts remain unchanged after linking classification elements and measures.
3. Each investigation distinguishes weak condition, missing evidence and recorded measure status without claiming ecological effectiveness.

All headline metrics require field lineage; five source values and five BI measures must reconcile. DT1–DT10 must be executed, a second member must reproduce the core outputs, and no critical/high defect may remain. These assess delivery quality; real-world savings or service improvement are not claimed.

## Investigation rules

First compare an ecological-status-led queue with an evidence-gap-led queue within the same eligible body set. Preserve status/potential distinctions for modified/artificial bodies. Do not use an all-fail chemical status as if it independently differentiates priority. Catchment-level measures must not be attributed to every body as a proven body-level intervention.

- Measures recorded in an administrative dataset do not prove implementation or ecological effectiveness.
- Do not average ordinal status labels into a continuous pollution score or combine chemical and ecological scales.
- Classification changes can reflect monitoring and method changes; these files do not supply raw chemical sampling histories.

## Team and stakeholder ownership

Director of Catchment Environment & River Improvement approves business scope and the investigation recommendation. The Business Analyst, Data Governance Analyst, Data Engineer and BI Developer work with the specialist roles in the [project brief](project/PROJECT_BRIEF.md). Assign individual owners at kickoff and record substantive work and independent reviews in `CONTRIBUTIONS.md`.

## Delivery plan

Weeks 1–2: decision requirements and verified cohort. Weeks 3–4: model, reconciliation and metric definitions. Weeks 5–6: analytical findings, alternative investigation scenarios and BI draft. Weeks 7–8: simulated UAT, independent rerun, executive briefing and handover.

## Start here

1. [Project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. [D1–D12 deliverables and metric contracts](project/DELIVERABLES.md).
3. [AC1–AC12 and DT1–DT10 acceptance tests](project/ACCEPTANCE_CRITERIA.md).
4. [Governance and sign-off](project/GOVERNANCE.md).
5. [Data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw](data/raw/README.md), [reference](data/reference/README.md) and [metadata](data/metadata/README.md) guidance.
6. [Team repository standard](submission/TEAM_REPOSITORY_STANDARD.md), [submission guide](submission/SUBMISSION_GUIDE.md) and [final template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master repository holds the Mettelo-controlled specification. Create `MTL-XF-030-<team-name>` under the **Mettelo GitHub organisation** and add every member's individual account. Delivery analysis, code, tests, BI and contribution evidence belong in that team repository. Use issues, branches, meaningful commits, PRs and reviews where practical.

The required master areas are `project/`, `data/` (including raw/reference/metadata guidance) and `submission/`; [the documentation index](project/README.md) explains their authority and current revision.

**Mettelo — Built for What’s Next**
