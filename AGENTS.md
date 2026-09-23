# Agent Instructions

## Purpose

This repository uses the Imprint workflow. Bring human intent, decisions, taste, and acceptance to the front of the project. Treat the human-authored specification as canonical and `.implementation/` as generated or derived unless a file explicitly says otherwise.

## Project initialization

When the user is starting a project, defining a product, or has incomplete requirements, read `skills/imprint/SKILL.md` and conduct the Imprint interview one question at a time before generating implementation. Summarize the confirmed imprint and wait for approval before building.

## Before changing anything

1. Read `docs/project-charter.md`.
2. Read `docs/schema-checklist.md`.
3. Read the nearest applicable `intent.md`, `invariants.md`, `scenarios/`, and `decisions.md` files.
4. Inspect the current implementation and verification commands instead of guessing.
5. Identify ambiguity and contradictions before editing.

## Change protocol

1. Start from a plain-language issue or user outcome.
2. Make the smallest necessary change to the canonical intent files.
3. Update invariants, scenarios, terminology, and decisions when affected.
4. Generate or update implementation only after the intent is coherent.
5. Run the project's checks and report exact commands and results.
6. Show intent changes separately from generated implementation changes.
7. Do not silently resolve meaningful ambiguity. Ask, record an assumption, or leave an explicit open question.

## Source-of-truth rules

- Intent, invariants, scenarios, and decisions are authoritative for behavior.
- Configuration and package manifests are authoritative for commands and dependencies.
- Generated files must identify their source specifications and generator metadata.
- If implementation behavior is not justified by a specification, flag it as drift.
- If a specification cannot be verified, flag it as incomplete rather than claiming success.

## Harness interface

Use the repository's native commands when they exist. If no commands exist yet, propose them before inventing a toolchain. Recommended conceptual commands:

```text
agent imprint    # interview the human and establish the project's imprint
agent discover   # inspect completeness, terms, contradictions, and drift
agent plan       # map a requested outcome to affected intent and checks
agent generate   # compile intent into implementation
agent verify     # run scenarios, tests, static checks, and traceability checks
agent review     # review a change against intent and repository policy
agent sync       # reconcile intentional implementation changes back into intent
```

These names are conventions, not mandatory executables. A harness may expose them as slash commands, skills, scripts, or prompts.

## Completion report

Every completed change must state:

- outcome requested;
- canonical files changed;
- implementation files generated or adapted;
- verification performed and exact results;
- assumptions, unresolved questions, and known drift;
- whether a human decision is still required.

## Safety

Do not deploy, delete data, rotate credentials, merge, or make irreversible external changes without explicit authorization. Never place secrets in specification files, issues, manifests, or logs.
