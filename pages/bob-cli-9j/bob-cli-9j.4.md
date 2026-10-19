# Bead: bob-cli-9j.4 — Mac: override banner and orange Return

[Bead Pages](../README.md) / [bob-cli-9j](README.md) / bob-cli-9j.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.91](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.91.md) · **Assignee:** `bob-cli-9j.4` · **Size:** medium
**Created:** 2026-10-18 16:26:21 EDT · **Closed:** 2026-10-18 19:06:58 EDT
**Plan:** [202610/eq\_overrides\_running\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/eq_overrides_running_pomodoro.md)

## Description

mac-warning: add the override banner to the start card, tint the Return button orange for overrides, respell `==` copy to `=`, drop the idle and parse-flag leftovers, regenerate fixtures from the new bob, and update tests and README.

## Notes

[2026-10-18T23:06:14Z · bob-cli-9j.4] PROPOSED FOLLOW-UP: skipped decisions-web record — epic DECISIONS set decision_record=no; land agent should file a memory task if a record for `=` overriding the running Pomodoro is still wanted

[2026-10-18T23:06:19Z · bob-cli-9j.4] PROPOSED FOLLOW-UP: capture-complete omits override on empty `=#` — real bob returns override only once a destination name exists (`=#bugs`); empty `=#` while running lists names with override=None. Mac picker override tests use FAKE_BOB_OVERRIDE. Land agent should decide whether complete should emit override on the incomplete empty `=#` draft.

[2026-10-18T23:06:58Z · bob-cli-9j.4] athena just portable-check: 1379 tests, 0 failures. Override banner + orange Return on restart/swap; leftover idle/parse fixtures dropped; == retired teaching fixtures; fixtures regenerated from this tree's bob. Mac compile unverified (ssh mac timed out). CI Lint/Build/Test not run (no push yet). Recorded PROPOSED FOLLOW-UPs: skipped decisions-web record (decision_record=no); capture-complete omits override on empty =#.

## Dependencies

- **Depends on:** [bob-cli-9j.2](bob-cli-9j.2.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9j.5](bob-cli-9j.5.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-9j.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-9j.4/README.md) | [bob-cli-9j.4](bob-cli-9j.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@4c391eb`](https://github.com/bobs-org/bob-mac-capture/commit/4c391eb3263e4a407459b4acffca439a91bab9d2) | feat(capture): show orange override banner when \`=\` restarts or swaps | [bob-cli-9j.4](bob-cli-9j.4.md) | 2026-10-18 19:08:57 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9j.4][1] | Need the phase scope and design file | 5 |
| read-by | [agent:bob-cli-9j.land--1][2] | Need unchanged phase verification notes and prior commit references for final epic closure. | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-9j.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-9j.land.md

<!-- sase:referenced-by:end -->
