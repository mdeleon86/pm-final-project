# A/B Experiment Brief, RouteLogic (B2B)

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Step Progress Indicator for dispatch coordinator compliance checksd |
| Persona | Dispatch coordinators responsible for completing compliance checks and managing daily delivery operations. |
| Expected outcome | Higher compliance-check completion rates |
| Primary success metric | Compliance-check completion rate (% of eligible coordinator compliance checks successfully completed). |
| Baseline rate | 48% |
| Guardrail metric | Compliance accuracy (percentage of completed compliance checks that satisfy all required validation rules). |
| Guardrail boundary | 0 percentage points |
| Second guardrail | · |
| Minimum Detectable Effect | 12 |
| Sample size per arm | 270 |
| Traffic split | 50/50 |
| Test duration | 14 days |
| Significance threshold | p < 0.05 |

## Control vs. Variant
- **Control (A):** Dispatch coordinators use the existing RouteLogic compliance-check workflow without a Step Progress Indicator. They must navigate the current process without a visual display of completed, current, and remaining steps. Existing required fields, validation rules, and submission behavior remain unchanged.
- **Variant (B):** Dispatch coordinators use the existing compliance-check workflow with one added feature: the Step Progress Indicator. It visually displays completed, current, and remaining required steps and updates automatically as each step is completed. All existing required fields, validation rules, and submission behavior remain unchanged.
- **Held constant (isolation check):** Both groups use the same RouteLogic application, compliance-check steps, required fields, validation rules, submission process, and completion confirmation. User permissions, notifications, onboarding, and access to existing features remain identical. The only difference is that Variant B displays the Step Progress Indicator.

## Hypothesis
> I believe that Step Progress Indicator for dispatch coordinator compliance checksd for Dispatch coordinators responsible for completing compliance checks and managing daily delivery operations. will result in Higher compliance-check completion rates, as measured by a 12 change in Compliance-check completion rate (% of eligible coordinator compliance checks successfully completed). within 14 days. We will protect Compliance accuracy (percentage of completed compliance checks that satisfy all required validation rules). throughout the test.

## Shipping criteria
> We will **ship** if Compliance-check completion rate (% of eligible coordinator compliance checks successfully completed). improves by ≥ 12 at p < 0.05 and Compliance accuracy (percentage of completed compliance checks that satisfy all required validation rules). does not reach 0 percentage points after 14 days.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14 days, no results reviewed before this date.
