# Bead: bob-cli-9u.1 — Classify, match, and fold underlines into their highlights

[Bead Pages](../README.md) / [bob-cli-9u](README.md) / bob-cli-9u.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4z.linker.w0.md) · **Assignee:** `bob-cli-9u.1` · **Size:** medium
**Created:** 2026-10-19 11:48:18 EDT · **Closed:** 2026-10-19 12:24:59 EDT
**Plan:** [202610/underline\_emphasis.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/underline_emphasis.md)

## Description

fold-render: add underline.rs (classifier, match key, host predicate, word-snapped runs), plan underlines before continuations in one shared fold plan, render runs, comments, image notes, and task links into the host block, absorb underline IDs with link-aware Merged emphasis stubs, heal standalone underlines, and rehearse the rollout on a scratch copy of the affected notes.

## Notes

[2026-10-19T16:24:59Z · bob-cli-9u.1] Implemented underline folding, standalone healing, emphasis rendering, annotation routing, and merge-stub behavior; just check passed (3,022 unit tests and 1,839 CLI tests), targeted underline tests passed, and scratch-vault scans were idempotent with no new tombstones. epic-symbols was empty.

## Dependencies

- **Blocks:** [bob-cli-9u.2](bob-cli-9u.2.md) ◐ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9u.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9u.1/README.md) | [bob-cli-9u.1](bob-cli-9u.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a2638aa`](https://github.com/bobs-org/bob-cli/commit/a2638aa92e4da62e6733af86fcc01708df7da1ef) | feat(highlights): fold underlines into highlight quotes | [bob-cli-9u.1](bob-cli-9u.1.md) | 2026-10-19 12:25:38 EDT |
