---
name: verify
description: Use after generation or implementation changes to produce evidence that the repository satisfies its canonical intent.
---

# Verify

1. Read the affected intent and scenario files.
2. Run the project's native checks before inventing new commands.
3. Execute acceptance scenarios and relevant technical tests.
4. Check specification/implementation freshness and requirement traceability.
5. Record exact commands, exit status, notable output, and known gaps.
6. Distinguish passed, failed, skipped, blocked, and not-yet-specified.

## Completion

Do not say “verified” without evidence. Return a requirement-to-check table and identify any unresolved ambiguity or environmental limitation.
