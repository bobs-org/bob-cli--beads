# Bead: bob-cli-60.1 — Salvage PR

[Bead Pages](../README.md) / [bob-cli-60](README.md) / bob-cli-60.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.61.w1.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.61.w1.f0.md) · **Assignee:** `bob-cli-60.1` · **Size:** medium
**Created:** 2026-10-09 14:20:00 EDT · **Closed:** 2026-10-09 14:25:46 EDT
**Plan:** [202610/mac\_capture\_auto\_comma\_land.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_auto_comma_land.md)

## Description

land-assist: cherry-pick PR #4 (3842ee9) without committing onto fresh master, rename the colliding CapturePomodoroEntry model, trigger the assist parse from the digit key event, prefetch the count in CapturePanelController.show(), guard refresh races, extend fake-bob and tests, and land it through the /sase_final commit decision rather than a branch or PR.

## Notes

[2026-10-09T18:25:46Z · bob-cli-60.1] Salvaged PR #4 (3842ee9) onto fresh master via cherry-pick --no-commit, then fixed per plan: renamed colliding model to CapturePomodorosListEntry (Decodable/Equatable, exactly one CapturePomodoroEntry left), key-driven assist trigger (requestCloseListAssistParse + pending flag, deleted caret trigger), count prefetch moved to CapturePanelController.show(), generation-guarded refresh, fake-bob capture-pomodoros + =x1 parse cases, 10 new model/controller tests, README entry-point wording. Verified: git status dirty with 16 salvaged+fixed files, single struct decl, bash -n clean, fake-bob serves count/fail/parse cases live, decode bound is Decodable. No Swift toolchain on Linux and CI has NOT run yet; phase ci-green drives CI. No commit pushed by hand; changes staged for the sase_final commit decision (feat(close): auto-insert commas between close task numbers).

## Dependencies

- **Blocks:** [bob-cli-60.2](bob-cli-60.2.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-60.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-60.1/README.md) | [bob-cli-60.1](bob-cli-60.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-60.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-60.1/README.md

<!-- sase:referenced-by:end -->
