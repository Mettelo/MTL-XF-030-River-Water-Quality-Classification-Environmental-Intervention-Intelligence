# MTL-XF-030 — Project brief

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

**Client:** Confidential Catchment Environment & River Improvement Authority. **Decision owner:** Director of Catchment Environment & River Improvement. **Team:** 6–8. **Duration:** 8 weeks. **Review:** annual classification review and quarterly catchment programme meeting.

## Business problem and commission

The simulated catchment environment authority coordinates a quarterly programme meeting and an annual classification review. It has to choose where to commission evidence gathering and measure-delivery checks before a river-improvement proposal is advanced.

The Director of Catchment Environment & River Improvement needs a practical investigation agenda from a complex classification and measures register. A water body may have many element records, while one measure may relate to multiple places; a flat report can make documentation density look like a larger environmental problem. A broad chemical-failure label may also provide little distinction between competing cases.

The authority needs to distinguish three operational questions: where ecological condition merits specialist review, where classification evidence is incomplete, and where recorded measures need delivery-status clarification. The commission is a transparent same-cycle baseline and investigation queue that helps programme managers assign those questions without claiming that a listed measure has been implemented or has improved a river.

> Which English river water bodies warrant further environmental investigation based on ecological/chemical classifications and recorded measures, with cycle comparability and evidence gaps made explicit?

**Required management handover:** A catchment review pack containing a single-cycle body baseline, distinct ecological/chemical views, a verified measures linkage, two investigation queues and an evidence-request register for condition or delivery-status checks.

See [the management use case](BUSINESS_CONTEXT.md#practical-management-use-case) for how the review meeting uses this evidence.

## Core deliverable boundary

Retain both agreed England exports. Freeze them within one acquisition batch with separate retrieval timestamps and checksums. Use a single latest complete published classification year/cycle for the core baseline; lock its actual value at Week 2. Core screening is limited to the surface-water category available in the export and must be labelled accurately if rivers cannot be separated from canals/transfers. Use up to ten body-level investigation cases; catchment/measure links remain at their published grain.

**Optional / out of core:** Cross-cycle deterioration, raw nutrient time series, causal measure effectiveness and a GIS map needing an additional boundary file are extensions. Cross-cycle change is blocked unless a comparability assessment explicitly passes; a valid single-cycle baseline fully satisfies core delivery.

File availability does not prove dimensional support. Before analytical build, the team completes the source→field→metric→deliverable matrix in [data guidance](../data/README.md). Missing mandatory support blocks the gate and requires an approved official replacement or scope decision.

## Analytical model

Classification fact: water-body identifier × year/cycle × classification level/element × status and other published dimensions. Measures fact: published measure identifier × water-body/catchment links × status/category. Link using stable identifiers with a bridge for many-to-many relationships.

The source contract above controls where a general grain description is conditional. Do not create dimensions absent from the approved input.

## Objectives

1. Exactly one declared classification year/cycle drives the core baseline and denominator.
2. Distinct body counts remain unchanged after linking classification elements and measures.
3. Each investigation distinguishes weak condition, missing evidence and recorded measure status without claiming ecological effectiveness.

## Business questions

1. Which river water bodies have the weakest ecological or chemical status in a comparable assessment cycle?
2. Which apparent changes may reflect methodology rather than environmental change?
3. Where are recorded measures linked to weaker classifications?
4. Which bodies have missing classification or measure evidence?
5. Which cases require field sampling, pressure assessment or delivery-status investigation?

## Cross-functional delivery model

| Delivery role | Required project contribution |
| --- | --- |
| Business Analyst / Delivery Lead | Map the annual classification review and quarterly catchment programme meeting, document eight prioritised user requirements and maintain requirement→deliverable→test links; Director of Catchment Environment & River Improvement owns business approval. |
| Data Governance Analyst | Own the MTL-XF-030 source/metadata register, cohort decision, licence evidence and 100% headline-measure lineage; resolve the specific risk: Cross-cycle methods, repeated elements and many-to-many measure linkage may create false deterioration, body counts or intervention coverage. |
| Data Engineer | Implement the declared facts, keys, hierarchy and join controls; account for every source row and deliver a second-member reproducible run at the chosen MTL-XF-030 scope. |
| BI Developer | Implement the annual classification review and quarterly catchment programme meeting overview, diagnostic and quality pages; reconcile five measures and ensure cohort/extension warnings survive filters and export. |
| Environmental Classification Analyst | Validate status orders and cycle comparability, and reconcile five body/classification counts. |
| Catchment / GIS Data Steward | Own river-type filters, stable water-body identifiers and many-to-many measure linkage; quantify all unmatched records. |
| Environmental Programme & Assurance Analyst | Review up to ten investigation cases and prevent recorded measures being presented as proven effectiveness. |

Assign named team members and review partners at kickoff; roles may be combined, but a distinct member must review critical calculations and perform the final clean rerun. The executive and operational stakeholder roles are specified in [business context](BUSINESS_CONTEXT.md).

## Required investigation approach

First compare an ecological-status-led queue with an evidence-gap-led queue within the same eligible body set. Preserve status/potential distinctions for modified/artificial bodies. Do not use an all-fail chemical status as if it independently differentiates priority. Catchment-level measures must not be attributed to every body as a proven body-level intervention.

## Milestones and acceptance

| Gate | Reviewers | Evidence / decision |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Classification/methodology pages and endpoint documentation verified; export schema, actual cycle, body-type filter, measure-link grain and checksums pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of Catchment Environment & River Improvement + operational stakeholders | First compare an ecological-status-led queue with an evidence-gap-led queue within the same eligible body set. Preserve status/potential distinctions for modified/artificial bodies. Do not use an all-fail chemical status as if it independently differentiates priority. Catchment-level measures must not be attributed to every body as a proven body-level intervention. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

D1–D12 are defined in [deliverables](DELIVERABLES.md). AC1–AC12 and DT1–DT10 are defined in [acceptance criteria](ACCEPTANCE_CRITERIA.md). No real production deployment, automatic funding/service allocation, private-client data or paid-source dependency is required.
