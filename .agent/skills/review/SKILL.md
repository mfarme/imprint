---
name: review
description: Use when reviewing an intent-native change or generated implementation for behavioral correctness and traceability.
---

# Review

Review in this order:

1. Does the intent express the requested outcome clearly?
2. Are invariants, terminology, non-goals, and failure behavior complete?
3. Do scenarios cover success, boundary, retry, and failure paths that matter?
4. Is the generated implementation justified by the intent?
5. Is every changed requirement verified by evidence?
6. Is any implementation behavior unexplained or any intent stale?
7. Are security, privacy, accessibility, and operational risks addressed where relevant?

## Completion

Report blocking findings first, with file and requirement IDs. Separate specification defects from implementation defects. Approve only when the change is coherent, traceable, and verified.
