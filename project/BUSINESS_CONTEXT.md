# MTL-XF-030 — Business context

## Organisation and decision owner

**Simulated client:** Confidential Catchment Environment & River Improvement Authority. **Accountable executive:** Director of Catchment Environment & River Improvement. **Review cadence:** annual classification review and quarterly catchment programme meeting.

This fictional directorate/board is an engagement scenario, not an assertion of a real client's circumstances. The source data remains official public/open data.

## Business problem

The authority must prioritise catchment investigations while classification records repeat each water body across elements and assessments, and measures may link to several places. A flat join can make heavily documented bodies look like more water bodies. Historical method changes and widespread chemical failures also mean a simple worst-status ranking may provide little practical differentiation.

## Why the current process is insufficient

The current scenario relies on separately prepared reports without a common source/metric contract. The material failure to prevent is specific: Cross-cycle methods, repeated elements and many-to-many measure linkage may create false deterioration, body counts or intervention coverage.

This creates uncertainty over which cases need investigation and which comparisons should be rejected. No quantified loss, backlog, budget deficit or service failure is invented as a client fact.

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

In the programme meeting, the Director starts with a single-cycle ecological baseline, selects a catchment/body and checks the underlying classification level and recorded measures. Where chemical status is uniformly failing, the team explains that limitation rather than inventing a finer ranking. The Programme Manager assigns a field-evidence or measure-delivery-status check; recorded measures are not presented as completed remediation.

## Current-to-target workflow

1. **Before review:** analyst registers the approved files, coverage and definitions; steward checks the cohort and unresolved exceptions.
2. **At review:** Director of Catchment Environment & River Improvement opens the overview, then inspects diagnostics and the underlying eligible population before considering a case.
3. **Challenge:** the relevant stakeholder compares the alternative scenario and asks whether the signal survives missingness, comparability and denominator checks.
4. **Action:** each accepted case records investigation type, responsible service role, missing evidence, next review and what finding would reverse the recommendation.
5. **Follow-up:** the next annual classification review and quarterly catchment programme meeting records evidence received and the decision, without claiming the analytical signal itself caused an improvement.

## Required analytical response

- Create a classification baseline for the explicitly verified river or combined surface-water category in one declared year/cycle, keeping ecological and chemical outcomes separate.
- Assess change only where comparability is evidenced; otherwise deliver a single-cycle baseline and a documented comparability rejection.
- Shortlist up to ten water bodies for investigation using classification weakness, missingness and recorded-measure context; test at least two classification/missingness priority rules.

## Measurable project outcomes

1. Exactly one declared classification year/cycle drives the core baseline and denominator.
2. Distinct body counts remain unchanged after linking classification elements and measures.
3. Each investigation distinguishes weak condition, missing evidence and recorded measure status without claiming ecological effectiveness.

## Proposed benefit monitoring

At kickoff, record a baseline review process and propose measures for: time to regenerate the agreed evidence pack; proportion of agenda recommendations with a complete evidence chain; and proportion of accepted investigations with a role owner and next review. The target for recommendation traceability and ownership is 100%; regeneration time is measured during the independent rerun, with no fabricated pre-project baseline or claimed reduction. These are proposed management measures, not achieved service benefits.

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
