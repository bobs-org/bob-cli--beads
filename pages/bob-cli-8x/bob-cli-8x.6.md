# Bead: bob-cli-8x.6 — README, manifests, glossary, and the final sweep

[Bead Pages](../README.md) / [bob-cli-8x](README.md) / bob-cli-8x.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.117](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.117.md) · **Assignee:** `bob-cli-8x.6` · **Size:** small
**Created:** 2026-10-17 17:11:59 EDT · **Closed:** 2026-10-17 20:07:53 EDT
**Plan:** [202610/ctrl\_shift\_alt\_b\_blocks\_stage.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_alt_b_blocks_stage.md)

## Description

publish: document Ctrl+Shift+Alt+B and ⇧B in the bob-plugins README, deduplicating it first if it still repeats. Finalize the manifest descriptions, apply the glossary_dep_link memory decision, run the full suites and bob plugins sync, and check the docs against the shipped behavior.

## Notes

[2026-10-18T00:07:48Z · bob-cli-8x.6] PROPOSED FOLLOW-UP: Investigate six unrelated bob-plugins test failures observed in the full suite: four unblocked-glyph rendering cases, Keep counts once and saturates at 999 without reset, and forward conversion carries a Depends-On line and reverse restores it. Their source and test files were untouched by this phase; full suite rerun reproduced the same failures.

[2026-10-18T00:07:53Z · bob-cli-8x.6] Published the reverse Blocks stage and ⇧B in the plugin README and manifests, corrected the authorized dependency-link glossary, validated all 7 plugin manifests, and synced the updated plugin. Full suite ran 2,990 tests with 2,984 passing and six unrelated failures recorded as a proposed follow-up; docs show no stale later-epic or dependent-only wording. No epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-8x.4](bob-cli-8x.4.md) ✓ · ⧖ 2026-10-17
- **Depends on:** [bob-cli-8x.5](bob-cli-8x.5.md) ✓ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-8x.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-8x.6/README.md) | [bob-cli-8x.6](bob-cli-8x.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3ec4d0d`](https://github.com/bobs-org/bob-cli/commit/3ec4d0d232dbb178e01d0b4fe0761a66323f547f) | docs(dependencies): clarify editing from both ends | [bob-cli-8x.6](bob-cli-8x.6.md) | 2026-10-17 20:08:44 EDT |
| bob-plugins | [`bob-plugins@96a42c5`](https://github.com/bobs-org/bob-plugins/commit/96a42c56e9d338c0fd013cce4c1187bcba8b2b04) | docs(plugins): publish reverse Blocks stage gestures | [bob-cli-8x.6](bob-cli-8x.6.md) | 2026-10-17 20:09:51 EDT |
