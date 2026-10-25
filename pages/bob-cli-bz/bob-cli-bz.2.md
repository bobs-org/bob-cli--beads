# Bead: bob-cli-bz.2 — Mount the strip under the bob-plan badges and delete the end-of-note mount

[Bead Pages](../README.md) / [bob-cli-bz](README.md) / bob-cli-bz.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.143](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.143.md) · **Assignee:** `bob-cli-bz.2` · **Size:** medium
**Created:** 2026-10-25 07:46:43 EDT · **Closed:** 2026-10-25 08:36:47 EDT
**Plan:** [202610/day\_strip\_under\_the\_badges.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/day_strip_under_the_badges.md)

## Description

strip-home: in bob-plugins' bob-ledger-tools, host the Day strip inside the rendered `bob-plan` block of canonical daily notes, after the badges, in Live Preview and Reading view. The plan block's 5 s repaint must never touch the strip host. Delete the CodeMirror StateField mount. Rewire `Toggle Day stats`, `stats.day_strip`, and rollover to plan-block hosts. Replace the mount tests with plan-host tests, update the plugin docs and manifest, then sync.

## Notes

[2026-10-25T12:36:47Z · bob-cli-bz.2] strip-home done: plan-block host ships under badges, mount deleted. Verified: npm run build, build:check, validate, docs:check (447 passed), preview-day-strip (84 cells 0 failures), day-strip suites 10+29+8 pass, full npm test 3649 pass, bob plugins sync 3 copied.

## Dependencies

- **Depends on:** [bob-cli-bz.1](bob-cli-bz.1.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-bz.3](bob-cli-bz.3.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-bz.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-bz.2/README.md) | [bob-cli-bz.2](bob-cli-bz.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8388ef2`](https://github.com/bobs-org/bob-plugins/commit/8388ef20bd96e984668f969eef95b69ef5005f8f) | feat(ledger-tools): host Day strip under bob-plan badges | [bob-cli-bz.2](bob-cli-bz.2.md) | 2026-10-25 08:37:41 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bz.2][1] | Check phase notes before closing strip-home work | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-bz.2/README.md

<!-- sase:referenced-by:end -->
