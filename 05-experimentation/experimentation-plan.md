A/B Experiment Brief, RouteLogic (B2B)
Parameters
Parameter	Decision
Feature under test	Step Progress Indicator for dispatch coordinator compliance checks
Persona	Dispatch coordinators responsible for completing compliance checks and managing daily delivery operations.
Expected outcome	Higher compliance-check completion rates
Primary success metric	Compliance-check completion rate (% of eligible coordinator compliance checks successfully completed).
Baseline rate	48%
Guardrail metric	Compliance accuracy (percentage of completed compliance checks that satisfy all required validation rules).
Guardrail boundary	No decline in compliance accuracy relative to control (0 percentage-point permitted decrease); no invalid submissions accepted
Second guardrail	None selected
Minimum Detectable Effect	12 percentage points
Sample size per arm	270
Traffic split	50/50
Test duration	14 days
Significance threshold	p < 0.05


Control vs. Variant
- Control (A): Dispatch coordinators use the existing RouteLogic compliance-check workflow without a Step Progress Indicator. They must navigate the current process without a visual display of completed, current, and remaining steps. Existing required fields, validation rules, and submission behavior remain unchanged.
- Variant (B): Dispatch coordinators use the existing compliance-check workflow with one added feature: the Step Progress Indicator. It visually displays completed, current, and remaining required steps and updates automatically as each step is completed. All existing required fields, validation rules, and submission behavior remain unchanged.
- Held constant (isolation check): Both groups use the same RouteLogic application, compliance-check steps, required fields, validation rules, submission process, and completion confirmation. User permissions, notifications, onboarding, and access to existing features remain identical. The only difference is that Variant B displays the Step Progress Indicator.
Hypothesis
I believe adding a Step Progress Indicator to the existing compliance-check workflow for dispatch coordinators will increase compliance-check completion by making completed, current, and remaining steps visible. We aim to improve the completion rate from the observed 48% baseline to at least 60%, a proposed 12-percentage-point increase, during a 14-day experiment. Compliance accuracy must not decline relative to the control group, and invalid submissions must remain blocked.

Shipping criteria
- Ship: The variant demonstrates an improvement of at least 12 percentage points versus the control group, with p < 0.05, while compliance accuracy does not decline and no invalid submissions are accepted. Confirm the planned sample size and valid randomization before interpreting the result.
- Iterate: Results suggest a positive effect, but the lift is below 12 percentage points or evidence is inconclusive, with no safety violation. Investigate what to improve and test again; do not treat this as a confirmed win.
- Kill: The feature shows no useful improvement or a negative effect after a sufficiently powered, valid experiment. Do not equate a nonsignificant result from an underpowered test with proof of no effect.
- Investigate / pause: Any compliance guardrail breach, unexpected segment differences, instrumentation problems, contamination, or insufficient independent participants requires review before a shipping decision.
- Read date: Evaluate the pre-specified results at the end of 14 days, provided the planned sample and data-quality conditions are met. Do not make an early shipping decision based on interim results.
Assumptions to verify before running
- Metric definition: Confirm the original 48% funnel baseline uses the same denominator and definition as the experiment's completed-check rate.
- Sample feasibility: The builder estimates 270 independent coordinators per arm (540 total) at 80% power and 5% significance for a 12-percentage-point effect. The three-account pilot has not been shown to provide this many independent participants; account-level clustering or cross-group contamination may require a different design or larger sample.
- Duration: The 14-day measurement period can fit inside the previously proposed four-week pilot window, but duration alone does not guarantee enough data.
- Guardrail measurement: Establish an auditable compliance-accuracy measurement and confirm that all existing validation rules remain enforced in both groups.
