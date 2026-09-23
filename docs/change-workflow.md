# Change Workflow

Use this sequence for most changes.

## 1. Discover

Read the issue, charter, checklist, and nearest local specifications. Ask an agent to identify contradictions, undefined terms, missing scenarios, and implementation drift.

**Done when:** affected requirement IDs and open decisions are known.

## 2. Plan

Describe the intended outcome, files to change, scenarios to add or update, constraints, and verification evidence. Keep the plan separate from generated implementation.

**Done when:** a human can approve the behavior change without reading code.

## 3. Specify

Edit intent, invariants, scenarios, terminology, and decision records. Prefer small local files over a giant specification. Assign stable requirement IDs.

**Done when:** the specification is coherent, scoped, and testable.

## 4. Generate

Ask the builder agent to implement the approved intent. Generated artifacts should carry source paths and requirement IDs.

**Done when:** implementation is fresh and no unexplained behavior was introduced.

## 5. Verify

Run native project checks, acceptance scenarios, static checks, and traceability checks. Record exact evidence.

**Done when:** every affected requirement has a pass, fail, skip, or explicit blocked status.

## 6. Review

Review the intent diff first, then generated implementation, then operational impact. A reviewer may request specification changes even when all tests pass.

**Done when:** behavior, evidence, provenance, and risk are acceptable.

## 7. Record

Update decisions, known limitations, and open questions. Keep the repository useful if the implementation is deleted and regenerated later.
