# Harness Integration Guide

The repository is harness-neutral by default. Keep project meaning in the canonical Markdown files and adapt only the invocation layer for each agent.

## Universal contract

Every harness should be able to discover:

1. `AGENTS.md` — repository operating rules;
2. `docs/project-charter.md` — project context;
3. `docs/schema-checklist.md` — quality gate;
4. `.agent/manifest.md` — roles, inputs, outputs, and permissions;
5. `.agent/skills/<name>/SKILL.md` — reusable procedures.

## Adapter strategy

- **Codex, Gemini CLI, Cursor, Aider, OpenCode, and similar tools:** configure them to load `AGENTS.md` and follow its context pointers.
- **Claude Code:** optionally add a thin `CLAUDE.md` that points to `AGENTS.md`; do not duplicate the rules.
- **Hermes:** expose the repository's `.agent/skills/` as project skills or invoke the skill files directly; keep durable project facts in the repository, not in personal memory.
- **CI or custom harness:** implement `discover`, `plan`, `generate`, `verify`, `review`, and `sync` as scripts or jobs while preserving the report contract in `.agent/manifest.md`.

## Prompt adapter pattern

A harness-specific wrapper should be short:

```text
Read AGENTS.md first. Then load .agent/manifest.md and the skill for this task.
Use the canonical intent files as the source of truth. Follow context pointers.
Return the required completion report. Surface ambiguity; do not invent policy.
```

## Context rules

Load progressively:

- always: `AGENTS.md`;
- per task: the manifest and one relevant skill;
- per area: nearest intent, invariants, scenarios, and decisions;
- on demand: architecture, operations, security, or deployment references.

Do not create parallel copies of project rules for each harness. Duplicated instructions drift.

## Model and generator portability

Record the generator, model, tool version, source revision, and verification results in generated metadata when practical. The specifications must remain understandable and usable if the current model or harness is replaced.
