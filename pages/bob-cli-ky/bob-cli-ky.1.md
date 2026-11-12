# Bead: bob-cli-ky.1 — nav api.walkMode v1 and the walk-mode doorbell

[Bead Pages](../README.md) / [bob-cli-ky](README.md) / bob-cli-ky.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bu](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bu.md) · **Assignee:** `bob-cli-ky.1` · **Size:** small
**Created:** 2026-11-12 12:30:15 EST · **Closed:** 2026-11-12 12:45:32 EST
**Plan:** [202611/walker\_footers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/walker_footers.md)

## Description

navapi: expose the persisted bracket-repeat mode through an additive nav api namespace (current/select) plus a workspace doorbell event fired on mode change and once at setup; no visible change.

## Notes

[2026-11-12T17:45:15Z · bob-cli-ky.1] PROPOSED FOLLOW-UP: test-ledger-tools-task-tag-marks.cjs "session toggle and onload wiring" fails 2!==1 on the clean base too (already tracked by bob-cli-kw); navapi phase left the full suite otherwise green -r Recording the pre-existing clean-base test failure as follow-up instead of holding the phase open

[2026-11-12T17:45:32Z · bob-cli-ky.1] navapi done: walkMode v1 (current/select) + walk-mode doorbell firing on change and once at setup; 39/39 nav bracket tests pass; build:check and validate green; full npm test has 1 pre-existing clean-base failure (task-tag-marks session toggle, tracked by bob-cli-kw, recorded as PROPOSED FOLLOW-UP); bob plugins sync deployed nav-hotkeys, yank-flash refusal resolved via landed-commit recipe without -F

## Dependencies

- **Blocks:** [bob-cli-ky.2](bob-cli-ky.2.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ky.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.1/README.md) | [bob-cli-ky.1](bob-cli-ky.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d36acba`](https://github.com/bobs-org/bob-plugins/commit/d36acba1b09d1ae19868a467ad56c8b9e4ea9e0f) | feat(nav-hotkeys): add api.walkMode v1 and the walk-mode doorbell | [bob-cli-ky.1](bob-cli-ky.1.md) | 2026-11-12 12:47:01 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ky.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.1/README.md

<!-- sase:referenced-by:end -->
