---
name: imprint
description: Use when starting a project or when requirements are incomplete. Establish the human imprint through a structured interview covering intent, decisions, taste, commitments, and acceptance.
---

# Establish the Imprint

Conduct this as an interactive interview. Ask one focused question at a time, explain why it matters when the answer is non-obvious, and summarize the answer before moving on. Do not fill gaps with guesses.

## Interview order

1. **Purpose:** What outcome should exist for whom?
2. **Problem:** What happens today, and why is it insufficient?
3. **Scope:** What is in scope, explicitly out of scope, and deferred?
4. **Users and actors:** Who uses, operates, depends on, or is affected by it?
5. **Core scenarios:** What are the three most important successful interactions?
6. **Failure scenarios:** What can go wrong, and what should users observe?
7. **Invariants:** What must always remain true?
8. **Terminology:** Which words have project-specific meanings?
9. **Constraints:** What platforms, data, privacy, safety, performance, compatibility, or policy constraints apply?
10. **Quality priorities:** Which qualities matter most, and which trade-offs are acceptable?
11. **Interfaces:** What inputs, outputs, integrations, and human touchpoints exist?
12. **Evidence:** How will we know the outcome works?
13. **Decisions:** Which choices need explicit human approval?
14. **Next slice:** What is the smallest useful capability to specify and verify first?

## Interview rules

- Maintain an explicit list of answered questions, assumptions, open questions, and decisions.
- Ask follow-ups when an answer is vague, contradictory, or not observable.
- Prefer concrete examples and edge cases over implementation jargon.
- Separate desired outcomes from proposed solutions.
- Surface conflicts rather than choosing silently.
- Keep the interview bounded; pause and summarize when enough information exists for a useful first slice.

## Write-back procedure

After the user confirms the summary:

1. Fill `docs/project-charter.md`.
2. Create local `intent.md`, `invariants.md`, and scenario files from the templates.
3. Record important choices in `decisions.md`.
4. Record unresolved questions with owners in the charter or issue.
5. Run the `discover` skill against the result.
6. Do not generate implementation until the user approves the specification and the first verification plan.

## Completion report

Return:

- the agreed outcome;
- scope and non-goals;
- actors and key scenarios;
- invariants and constraints;
- terminology established;
- decisions made;
- open questions and owners;
- files written;
- recommended next step.
