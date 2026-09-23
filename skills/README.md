# Imprint skills

This directory contains the marketplace-facing Hermes skills for Imprint.

- `skills/imprint/SKILL.md` is the canonical skill package for Hermes skill taps and direct GitHub installation.
- `.agent/skills/` contains harness-local companion skills (`discover`, `plan`, `review`, and `verify`) plus a compatibility copy of the Imprint skill.

Keep the two Imprint skill copies synchronized until the repository adopts a single harness convention across all consumers.

Install from Hermes:

```bash
hermes skills tap add mfarme/imprint
hermes skills install mfarme/imprint/imprint
```
