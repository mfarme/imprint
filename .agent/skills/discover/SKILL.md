---
name: discover
description: Use when assessing an Imprint repository before planning or editing. Find missing, contradictory, stale, or untestable specifications.
---

# Discover

1. Read `AGENTS.md`, `docs/project-charter.md`, and `docs/schema-checklist.md`.
2. Map the repository's intent, invariants, scenarios, decisions, interfaces, and implementation.
3. Build a requirement table: ID, source, affected area, verification, status.
4. Flag undefined terms, contradictions, missing edge cases, stale generated files, and unowned open questions.
5. Do not edit files unless explicitly requested.

## Completion

Report findings by severity, cite exact files, and recommend the smallest next action. Never claim the repository is ready if a critical requirement lacks an observable verification path.
