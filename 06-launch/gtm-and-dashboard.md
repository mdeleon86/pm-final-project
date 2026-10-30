# GTM Launch Plan, RouteLogic (B2B)

| Field | Value |
|---|---|
| Feature | Step Progress Indicator for dispatch coordinator compliance checks |
| Goal | Engagement |
| Launch tier | M, Targeted |

## Goal & Audience
- **Goal:** Engagement, RouteLogic already serves dispatch coordinators, so the priority is improving engagement with the existing compliance-check workflow rather than acquiring new users. Module 3 identified a 48% compliance-check completion baseline. The Step Progress Indicator aims to improve workflow clarity and increase completion to a proposed 60%, provided the experiment validates its effectiveness without reducing compliance accuracy.
- **Target audience:** Primary audience: Existing RouteLogic dispatch coordinators responsible for completing compliance checks and managing daily delivery operations.

Secondary audience: Customer success leads and operations managers at participating enterprise accounts who support coordinator adoption, monitor compliance performance, and provide feedback during rollout.

## Launch Tier
- **M, Targeted**, A targeted (M) launch is appropriate because the Step Progress Indicator is a focused workflow improvement for existing RouteLogic customers, not a new product or market expansion. Coordinated email, in-app messaging, and customer success outreach can reach dispatch coordinators without the expense of a broad marketing campaign. The rollout will remain conditional on successful experiment results and compliance safeguards.

## Channels
1. **Owned: In-app messaging (Owned): Display a contextual announcement and brief walkthrough when dispatch coordinators open the compliance-check workflow, explaining the new Step Progress Indicator and how to use it.**
2. **Owned: Targeted Email (Owned): Send a focused product update to dispatch coordinators and operations managers at participating RouteLogic accounts. Explain the Step Progress Indicator's benefits, provide a short walkthrough, and direct users to the updated compliance-check workflow.**
3. **Owned: Customer Success Outreach (Owned): Have RouteLogic customer success leads coordinate short demonstrations and onboarding sessions with operations managers and dispatch coordinators at participating accounts. Collect feedback, address adoption barriers, and reinforce proper use of the Step Progress Indicator.**

## Enablement & Assets
Prepare a short feature walkthrough, in-app announcement, targeted email template, and one-page quick-start guide for dispatch coordinators. Equip Customer Success with a demonstration script, FAQ, and feedback collection template. Provide Support with troubleshooting guidance and an escalation process. Confirm all materials accurately explain the Step Progress Indicator, required compliance steps, and submission validation rules before launch.

## Ownership, Budget & Timeline
- **Ownership & budget:** Product Manager: Own launch coordination, go/no-go decision, success metrics, and stakeholder alignment. Engineering (2 engineers): Own feature readiness, instrumentation, and technical support. Product Designer (1 designer): Own in-app messaging and walkthrough assets. Customer Success Lead (1 lead): Own targeted email outreach, account onboarding, demonstrations, and feedback collection. Support: Own troubleshooting documentation and issue escalation.

Budget: No paid advertising planned. Use existing internal resources and customer communication channels. Confirm staff availability, asset production effort, and any incremental costs before launch. Individual owners to be assigned.
- **Timeline:** Phase 1: Beta (Weeks 1–2, provisional): Conduct the planned A/B experiment with participating RouteLogic accounts. Before starting, verify that the pilot can provide the required 540 eligible, independently measured coordinators and reliable instrumentation. Run the planned 14-day measurement period only if feasible; otherwise, revise the experiment timeline or recruitment plan before making a launch decision.

Phase 2: Launch (Week 3, conditional): If experiment results meet the predefined shipping criteria, release the Step Progress Indicator to the approved audience. Activate in-app messaging, targeted email communication, and Customer Success onboarding. If results are inconclusive or safeguards fail, delay launch and investigate.

Phase 3: Post-Launch (Week 4 and ongoing): Monitor feature adoption, compliance-check completion, and compliance accuracy. Collect coordinator feedback, resolve issues, and decide whether to expand, iterate, or pause the rollout.

## Success Metrics
- **Metrics:** 1. Compliance-check completion rate (primary): Percentage of eligible compliance-check workflows started by dispatch coordinators that reach successful, valid submission. Compare the observed 48% baseline with the proposed 60% target (+12 percentage points), using consistent eligibility criteria, event definitions, and denominators. Confirm the historical baseline matches this definition before interpreting experiment results.

2. Feature adoption: Track the percentage of eligible dispatch coordinators who use the Step Progress Indicator after launch. Establish the adoption baseline and target during rollout planning.

3. Compliance-check task time: Reduce median completion time from the observed 14.6 minutes toward the proposed target of 11.7 minutes or less.

Guardrail: Compliance accuracy must not decline relative to the control group, and no invalid submissions may be accepted.
- **Bad signal to watch for:** Watch for declining compliance accuracy, invalid submissions, low feature adoption, increased task completion time, or coordinator feedback indicating confusion. A completion-rate improvement accompanied by compliance errors is not a successful outcome. Also monitor insufficient sample size or unreliable experiment data, which would prevent a confident launch decision.
- **Likely post-launch decision:** The most likely decision is to iterate based on coordinator feedback and observed adoption, unless the experiment demonstrates a clear reason to expand or pause.  Double down if a valid A/B test shows at least a 12-percentage-point improvement in compliance-check completion (p < 0.05) with no decline in compliance accuracy. Iterate if results are positive but below the target or inconclusive. Investigate and delay expansion if sample size or data quality is insufficient. Pause or roll back if compliance safeguards fail. Deprioritize if a sufficiently powered experiment shows no meaningful benefit.
