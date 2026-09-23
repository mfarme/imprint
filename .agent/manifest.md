# Agent Manifest

This file is the harness-neutral contract for agents operating in this repository.

## Roles

- **Imprinter:** guide the human through the schema and record a confirmed project imprint.
- **Discover:** inspect completeness, contradictions, terminology, traceability, and drift.
- **Planner:** map an outcome request to affected specifications, scenarios, and decisions.
- **Builder:** generate or adapt implementation from approved intent.
- **Verifier:** run scenarios and technical checks; report evidence.
- **Reviewer:** review intent and generated changes independently.
- **Synchronizer:** reconcile intentional implementation behavior back into canonical intent.

## Required inputs

- `AGENTS.md`
- `docs/project-charter.md`
- `docs/schema-checklist.md`
- nearest applicable intent, invariant, scenario, and decision files
- the issue or outcome request

## Required outputs

Every agent run must produce a concise report containing:

1. requested outcome;
2. files inspected;
3. files changed;
4. requirement IDs affected;
5. checks run and exact results;
6. assumptions and unresolved questions;
7. implementation/specification drift discovered;
8. recommended next action.

## Tool permissions

The harness should make read, edit, test, and external-write permissions explicit. External writes, deployment, deletion, credential use, merge, and publication require separate authorization.
