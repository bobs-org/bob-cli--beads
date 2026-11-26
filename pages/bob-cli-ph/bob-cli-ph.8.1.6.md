# Bead: bob-cli-ph.8.1.6 — Mac drawer acceptance, screenshots, and documentation

[Bead Pages](../README.md) / [bob-cli-ph.8.1](bob-cli-ph.8.1.md) / bob-cli-ph.8.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.6` · **Size:** small
**Created:** 2026-11-25 20:56:01 EST · **Closed:** 2026-11-26 03:20:54 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

## Description

mac-acceptance: verify the integrated feature on exact-SHA macOS CI, publish the drawer render screenshots, reconcile Mac and bob-cli docs with what shipped, and run every repo gate.

## Notes

[2026-11-26T08:19:42Z · bob-cli-ph.8.1.6--1] --list

[2026-11-26T08:20:33Z · bob-cli-ph.8.1.6--1] PROPOSED FOLLOW-UP: migrate remaining drawer test goldens to ph.10 bold-only behavior (just check red on clean master: ~25 lib + 55 cli failures, e.g. REQUIREMENTS vs Requirements, __AGENDA__ vs AGENDA; ph.10 commits 9573ff86/46aba677 changed behavior, c3a9bdd9 migrated only task-requirements vectors; master CI runs 45758122303 45763997268 45755965376 45752393102 all failure) -r "Acceptance gate just check fails on the clean base tree; needs a ci-type task bead"

[2026-11-26T08:20:42Z · bob-cli-ph.8.1.6--1] PROPOSED FOLLOW-UP: finish mac-acceptance remainder blocked by red gate (Mac commit a2e79f65 unpushed: 4-word model-binding test fix + draft-paint docs; push master, watch exact-SHA macOS run green, download render-fixtures artifact, inspect drawer PNGs, publish via sase artifact create, attach refs to bob-cli-ph.8.1.6 and bob-cli-ph.8) -r "Push was gated on both acceptance gates passing; just check failed so no push per phase instructions"

[2026-11-26T08:20:54Z · bob-cli-ph.8.1.6--1] Acceptance docs landed (631a49d5 docs-only; Mac a2e79f65 committed unpushed). just check on clean tree fails in -p bob-obsidian lib (~25) + cli (55) drawer goldens caused by ph.10 9573ff86/46aba677, pre-existing vs 8.1.6 base (recorded as PROPOSED FOLLOW-UP); master CI runs 45758122303/45763997268/45755965376/45752393102 failure corroborate. epic-symbols clean. Mac push+screenshots recorded as PROPOSED FOLLOW-UP, push gated on green gates.

[2026-11-26T11:36:53Z · bob-cli-ph.8.1.land--4] Mac drawer acceptance screenshots verified. Green exact-SHA gate: https://github.com/bobs-org/bob-mac-capture/actions/runs/45806522346 snapshot SHA 3635cbfe169a86820f970ef09615ae573159e7d2 (Lint/Build/Test 5297 tests 0 failures/Bundle/plist/launch-smoke/install all ok). Inspected all 16 drawer-headers PNGs (edge+real x 620/760 x light/dark/high-contrast): tray distinct from checkbox and requirement diamond; true-case verbatim semibold titles (Requirements, Perf Budget; legacy FUTURE WORK as-sent); empty Drafts muted; removed Old Drawer struck+dimmed; no ** on drawer rows; **Just bold** stays verbatim; requirement Scope-it keeps diamond; long title wraps cleanly. Registered as file:explicit artifacts (16 refs attached).

## References

- file:explicit:92ac260b4e11d2084e051d00
- file:explicit:8cf8d08357d505985cc67004
- file:explicit:5922d9f1d9d98925f294a512
- file:explicit:57de71e8ea3f5dfdd5a934a5
- file:explicit:ce0a9003fdbdfdde5cb94511
- file:explicit:6d35dc2d9c381c63545fba03
- file:explicit:44ec5c8cb0a0d2c38aa6a3de
- file:explicit:719de2e5996765b69febd0f5
- file:explicit:8264c29c8718f9462fc51b5e
- file:explicit:15c959fa575be4f8bc1408f5
- file:explicit:22075c1c60e8fbe071b26a35
- file:explicit:08ba10fc00da9e997f951646
- file:explicit:180759c7af703517f7b40435
- file:explicit:59ba2549dd929ad4a04196da
- file:explicit:8c8d339af7b68f9fa19bdf3b
- file:explicit:0ba25b1607cc2ca3dde68e7a

## Dependencies

- **Depends on:** [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-ph.8.1.2](bob-cli-ph.8.1.2.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-ph.8.1.3](bob-cli-ph.8.1.3.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-ph.8.1.4](bob-cli-ph.8.1.4.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-ph.8.1.5](bob-cli-ph.8.1.5.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.6.md) | [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`631a49d`](https://github.com/bobs-org/bob-cli/commit/631a49d5d55f18ea6b343ce778f6148e457e1bf1) | docs(drawers): reconcile Mac Capture section with shipped true-case behavior | [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) | 2026-11-26 03:03:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.8.1.land--4][1] | Land tale: need drawer test bead for screenshot refs | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.land.md

<!-- sase:referenced-by:end -->
