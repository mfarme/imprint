# Intent Schema Checklist

Use this as a gate before generation and before review. Mark each item `[x]`, `[ ]`, or `[N/A]`; explain exceptions.

## Repository shape

- [ ] The project charter states purpose, users, scope, priorities, and constraints.
- [ ] Each major domain area has a local `intent.md`.
- [ ] Non-negotiable behavior is recorded in `invariants.md`.
- [ ] Observable behavior is represented in scenarios or examples.
- [ ] Important architectural or product choices have a dated decision record.
- [ ] The nearest local instructions are discoverable by the chosen agent harness.

## Intent quality

- [ ] Requirements describe outcomes, not merely implementation tasks.
- [ ] Every requirement has a stable identifier, such as `BILLING-REFUND-001`.
- [ ] Ambiguous terms are defined in the terminology table.
- [ ] Positive behavior is stated; prohibitions are used only for real guardrails.
- [ ] Scope and non-goals are explicit.
- [ ] Requirements do not contradict one another.
- [ ] Assumptions are labeled as assumptions.
- [ ] Open questions are visible and owned.

## Verifiability

- [ ] Every important requirement has at least one scenario or check.
- [ ] Scenarios include relevant preconditions, action, and observable result.
- [ ] Failure modes and boundary cases are represented.
- [ ] Security, privacy, accessibility, and operational behavior are considered where relevant.
- [ ] A reviewer can distinguish “not implemented” from “not yet specified.”
- [ ] The project can report exact verification commands and results.

## Generation and traceability

- [ ] Generated files identify their source specifications.
- [ ] The generation toolchain and model/agent metadata are recorded when practical.
- [ ] Implementation changes without intent changes are reviewed as possible drift.
- [ ] Intent changes without implementation regeneration are rejected or clearly marked stale.
- [ ] Regeneration is repeatable enough to diagnose differences.
- [ ] Human-written escape hatches are labeled, tested, and documented.

## Agent readiness

- [ ] A new agent can discover the repository workflow from `AGENTS.md`.
- [ ] The task can be decomposed into bounded local changes.
- [ ] The agent knows which files are authoritative.
- [ ] The agent knows what it may edit and what requires approval.
- [ ] The agent has a completion report format.
- [ ] The agent is instructed to surface ambiguity instead of inventing policy.

## Final gate

- [ ] A human can explain the intended behavior without reading generated code.
- [ ] An agent can identify the affected specifications from a plain-language issue.
- [ ] A verifier can determine whether the result satisfies the intent.
- [ ] The repository would remain useful if the current implementation were deleted.
