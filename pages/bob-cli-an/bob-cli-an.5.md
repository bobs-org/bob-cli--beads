# Bead: bob-cli-an.5 — Preserve highlight IDs across annotation insertion

[Bead Pages](../README.md) / [bob-cli-an](README.md) / bob-cli-an.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12v.md) · **Assignee:** `bob-cli-an.5` · **Size:** medium
**Created:** 2026-10-21 12:58:23 EDT · **Closed:** 2026-10-21 13:45:33 EDT
**Plan:** [202610/backlog\_security\_and\_durability.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_security_and_durability.md)

## Description

highlight-identity: resolve bob-cli-9o by preserving existing annotation identities before allocating new IDs, including folded annotations and duplicate-text cases.

## Notes

[2026-10-21T17:45:33Z · bob-cli-an.5] Stable highlight IDs: removed ordinal from hash, reuse existing live/removed IDs via content matching with duplicate tiebreakers and prefix fallback, share host IDs for folds, thread through rendering/stubs/tasks. Verified: 2 new regression tests pass, 588 highlights_ref tests pass, just check exit=0, docs-check 447 passed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.5/README.md) | [bob-cli-an.5](bob-cli-an.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`51ad4f4`](https://github.com/bobs-org/bob-cli/commit/51ad4f4c77a318519b2039dc1e743ec9c737304f) | feat(highlights-ref): stabilize highlight IDs across sidecar order | [bob-cli-an.5](bob-cli-an.5.md) | 2026-10-21 13:47:57 EDT |
