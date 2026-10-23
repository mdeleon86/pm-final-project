# Step Progress Indicator, Simplified PRD (RouteLogic)

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** Dispatch coordinators responsible for completing compliance checks and managing daily delivery operations.

## 1. The Big Picture
- **Vision:** Enable dispatch coordinators to complete compliance checks with greater clarity and confidence by making workflow progress and remaining requirements visible at every step.
- **Press release:** RouteLogic introduces a Step Progress Indicator to help dispatch coordinators navigate compliance checks more clearly. The feature shows completed, current, and remaining steps, helping users understand what still needs attention. The initial pilot will evaluate whether this visibility improves completion rates and reduces workflow friction without compromising compliance accuracy.
- **Success metric:** Compliance-check completion rate: 48% baseline → 60% proposed target (25% relative improvement).
- **Guardrail:** Compliance accuracy must not decline compared with the pre-pilot baseline; establish the baseline and measurement method before testing.

## 2. The Details
### User stories
- As a dispatch coordinator, I want to see my progress through a compliance check so that I know which steps are complete and which remain.
- As a dispatch coordinator, I want to identify incomplete required steps so that I can finish the check without overlooking information.
- As a dispatch coordinator, I want clear confirmation when a compliance check is submitted so that I know the process is complete.
### Screens to build
- 1. Compliance Check Start: Display the checklist and a progress indicator showing current and remaining steps.
- 2. Compliance Check In Progress: Show completed steps, current step, and remaining required actions.
- 3. Incomplete Step: Highlight missing required information and prevent invalid submission.
- 4. Completion Confirmation: Confirm successful submission and display completed status.
### Functional requirements
- 1. Display completed, current, and remaining compliance-check steps.
- 2. Update progress immediately when a required step is completed.
- 3. Visually distinguish completed, active, and incomplete steps.
- 4. Identify missing required fields before allowing submission.
- 5. Preserve existing compliance validation rules.
- 6. Display a clear confirmation after successful completion.
### Smart behaviors (Situation → Outcome)
- If a coordinator completes a required step, the progress indicator updates automatically.
- If required information is missing, the interface highlights the incomplete step and explains what needs attention.
- If the coordinator attempts to submit an incomplete check, submission is blocked until required information is provided.
- If all required steps pass validation, the coordinator can submit and receives completion confirmation.
### Technical constraints
- Build a clickable prototype using representative sample data. No production integrations or external APIs are required. Preserve existing compliance validation logic conceptually; the prototype must not be used for real compliance submissions. Keep the design focused on the existing coordinator workflow and support desktop use.

## 3. The Logistics
### Features out
- AI-powered compliance auto-fill; full coordinator dashboard redesign; automated daily reporting; new external compliance integrations; changes to compliance policies or validation requirements.
### Edge cases & safety guard
- Missing required information: Highlight the incomplete step and block submission. Incorrect progress state: Do not mark steps complete until required fields pass validation. Interrupted workflow: Do not falsely display completion. Compliance safety: Preserve existing validation requirements and prevent submission of incomplete checks.
### Decision log
- 1. Prioritize a lightweight progress indicator instead of a full compliance workflow redesign to test whether improved visibility increases completion.
- 2. Exclude AI automation and external integrations from the initial prototype to reduce implementation complexity and focus validation on the core hypothesis.
### Evals
- 1. Accuracy: 100% of tested progress states correctly reflect required-step completion and validation status.
- 2. Time-on-task: Target at least a 20% reduction in median compliance-check duration from the 14.6-minute baseline (to 11.7 minutes or less).
- 3. Safety: Zero invalid compliance submissions accepted during prototype testing; no decline in compliance accuracy during the pilot.

## MoSCoW scope
- **Must:** Display completed, current, and remaining compliance-check steps.; Update progress when each required step is completed.; Clearly identify incomplete required steps.; Preserve existing compliance validation rules.; Show confirmation after successful submission.
- **Should:** Show a simple progress count (e.g., Step 2 of 5).; Highlight the next required action.; Provide concise guidance when a step is incomplete.
- **Could:** Estimated time remaining for each step.; Optional contextual help tooltips.; Subtle visual confirmation when a step is completed.
- **Won't (now):** AI-powered compliance auto-fill.; Full coordinator dashboard redesign.; Automated daily reporting.; New integrations with external compliance systems.; Changes to compliance policies or validation requirements.

---
**Builder hook:** Build a working prototype based on this PRD. Use the User Story as the core flow, Functional Requirements as build constraints, and prioritize speed and clarity over visual complexity.
