# Imprint

<p align="center">
  <img src="public/imprint.png" alt="Imprint logo" width="180">
</p>

## Human intent at the source of software

Software is becoming easier to generate. As agents grow more capable, implementation becomes more replaceable, but the human contribution becomes more important.

**Imprint** is a general-purpose repository structure and agent workflow for bringing human intent, decisions, taste, and acceptance to the front of software projects. It treats the project’s human-authored meaning as durable and the generated implementation as a replaceable rendition.

The goal is not to remove engineering or code. It is to elevate the expression of human creativity in software. I think we should elevate what the project should mean, how it should feel, what trade-offs it should make, and what “good” looks like.

## The Imprint model

The repository preserves the human imprint through:

- **Intent** — what the system should achieve.
- **Commitments** — what must remain true.
- **Scenarios** — observable examples of acceptable behavior.
- **Decisions** — choices, trade-offs, and reasons.
- **Taste** — quality priorities, voice, and non-functional standards.
- **Acceptance** — the evidence required before calling the work good.
- **Implementation** — generated or adapted code, treated as a replaceable rendition.

## Start here

1. Read `AGENTS.md`.
2. Run or invoke the `imprint` skill to create the project imprint interactively.
3. Work through `docs/schema-checklist.md`.
4. Copy the relevant files from `templates/` into `domain/`, `interfaces/`, and `behavior/`.
5. Ask an agent to run `discover`, `plan`, or `review` before generating implementation.
6. Keep generated artifacts under `.implementation/` unless the project has a reason to expose them elsewhere.

## Suggested first agent prompt

> Read `AGENTS.md`, `.agent/manifest.md`, and the `imprint` skill. Interview me one question at a time to establish the project's intent, decisions, taste, commitments, scenarios, and acceptance criteria. Do not generate implementation until I confirm the imprint.

## Design principle

Natural language supplies meaning; structure supplies handles. Headings, requirement identifiers, commitments, scenarios, terminology, decisions, and manifests make the human imprint discoverable, testable, and portable across agent harnesses.

The canonical Hermes skill package lives at `skills/imprint/SKILL.md`; the `.agent/skills/` copy is retained for repository-local harness compatibility.

## Compatibility

The repository uses ordinary Markdown and folders. It is designed to work with Codex, Claude Code, Gemini CLI, Cursor, Aider, OpenCode, Hermes, and other harnesses that can read repository context files. Adapt the command names in `AGENTS.md` to the harness used by a project.

## License

This template is released under the [BSD Zero Clause License (0BSD)](LICENSE), a permissive license with no attribution or notice requirement.
