# Bead: bob-cli-q8.3 — Capture absorption, the plain-~ no-op, and the same-item error

[Bead Pages](../README.md) / [bob-cli-q8](README.md) / bob-cli-q8.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6f.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6f.linker.w0.md) · **Assignee:** `bob-cli-q8.3` · **Size:** medium
**Created:** 2026-11-25 18:16:42 EST · **Closed:** 2026-11-25 21:20:36 EST
**Plan:** [202611/plain\_link\_dependency\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/plain_link_dependency_ties.md)

## Description

capture-writers: & and * absorb the pair's plain links in the same staged write. A plain ~ / ~~ over a dependency becomes a reported no-op, and & plus a plain ~ to one target in a single item is a teaching error. Both report additive JSON and human output.

## Notes

[2026-11-26T02:11:15Z · bob-cli-q8.3] PROPOSED FOLLOW-UP: Add or fix the docs search-smoke entry for "- #Section" under /reference/capture-syntax/#drawer-bullets; just docs-check fails identically on clean HEAD f4da72ff. No task bead tracks this exact query; bob-cli-fo covers four other capture-token queries and is closed. The earlier stale ignored mount collision is tracked by bob-cli-it and cleared after regenerating mount copies.

[2026-11-26T02:20:36Z · bob-cli-q8.3] Implemented symmetric dependency ties for staged capture: dependencies absorb pair plain links, plain links over dependencies report a no-op, and same-item dependency plus plain link is refused. Added JSON and human output, docs, glossary, and CLI coverage. Verified cargo fmt, cargo test --test cli capture::relations:: (33 passed), cargo check --all-targets, just docs-gen, and git diff --check. just docs-check reaches the same search-smoke failure on clean base f4da72ff; the exact query follow-up is recorded on this bead. Epic-symbol audit found no leftovers.

## Dependencies

- **Depends on:** [bob-cli-q8.1](bob-cli-q8.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q8.9](bob-cli-q8.9.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.3/README.md) | [bob-cli-q8.3](bob-cli-q8.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`974129e`](https://github.com/bobs-org/bob-cli/commit/974129e55c0814d2822ab1a1b12bb278ca7f4d8e) | feat(capture): handle dependency and plain link ties | [bob-cli-q8.3](bob-cli-q8.3.md) | 2026-11-25 21:25:01 EST |
