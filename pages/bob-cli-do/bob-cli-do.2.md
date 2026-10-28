# Bead: bob-cli-do.2 — Save before the review walk switches notes

[Bead Pages](../README.md) / [bob-cli-do](README.md) / bob-cli-do.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.157.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.157.f0.md) · **Assignee:** `bob-cli-do.2` · **Size:** medium
**Created:** 2026-10-28 10:46:06 EDT · **Closed:** 2026-10-28 11:07:47 EDT
**Plan:** [202610/clobbered\_note\_repair\_and\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/clobbered_note_repair_and_guards.md)

## Description

walk-save-guard: in bob-navigation-hotkeys, flush and verify the active note before any same-pane note switch, add a clobber tripwire on landing, test, build, deploy.

## Notes

[2026-10-28T15:07:47Z · bob-cli-do.2] Implemented the shared save-and-verify guard and immediate/delayed clobber tripwire across the planned same-pane switches; verified npm test (3,911 passed), docs:check, and athena deployment of bob-navigation-hotkeys 2.56.5 plus bob-ledger-tools. Mac deployment remains for Bryan after these uncommitted source changes land on origin.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-do.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-do.2/README.md) | [bob-cli-do.2](bob-cli-do.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a182635`](https://github.com/bobs-org/bob-plugins/commit/a1826356cbcbdbef67902d685ab481f61b45969e) | fix(navigation-hotkeys): guard same-pane note switches | [bob-cli-do.2](bob-cli-do.2.md) | 2026-10-28 11:08:46 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-do.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-do.2/README.md

<!-- sase:referenced-by:end -->
