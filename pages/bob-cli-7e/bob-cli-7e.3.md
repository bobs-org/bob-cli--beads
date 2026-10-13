# Bead: bob-cli-7e.3 — Recognisers and gesture guards in nav, cycler, and block-id-prompt

[Bead Pages](../README.md) / [bob-cli-7e](README.md) / bob-cli-7e.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4d.linker.w0.md) · **Assignee:** `bob-cli-7e.3` · **Size:** medium
**Created:** 2026-10-13 11:09:49 EDT · **Closed:** 2026-10-13 12:06:35 EDT
**Plan:** [202610/prerequisite\_blocks\_lines.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prerequisite_blocks_lines.md)

## Description

plugin-guards: teach bob-navigation-hotkeys, task-status-cycler, and block-id-prompt to recognise and ignore BLOCKS lines (Pomodoro scanners, strike/restore, tree close, conversion, the hand-edit mirror) and route or refuse gestures on them, then deploy on this host.

## Notes

[2026-10-13T16:06:04Z · bob-cli-7e.3] PROPOSED FOLLOW-UP: ledger-tools unblocked-glyph suite (4 tests: Live Preview glyph, widget mousedown, rebuild triggers, Reading view) fails identically on clean base; tracked by bob-cli-6v (wall-clock daily path vs frozen 2026-10-09 fixtures)

[2026-10-13T16:06:07Z · bob-cli-7e.3] PROPOSED FOLLOW-UP: navigation decision-card Keep counts test sees review-journal missing-API notice instead of Keep notice; tracked by bob-cli-6w

[2026-10-13T16:06:11Z · bob-cli-7e.3] PROPOSED FOLLOW-UP: task-status-cycler successor-wiring Pomodoro-line close appends successor test fails identically on clean origin/master (no tracking bead found in flake/ci list); needs triage into a task bead

[2026-10-13T16:06:35Z · bob-cli-7e.3] plugin-guards done: BLOCKS recognisers in nav(081)/cycler/bip with BK1-BK21 + MC1-MC7 guards; new focused tests 20/20 pass; build+validate clean; deployed nav 2.35.0/cycler 1.40.0/bip 1.32.0 via bob plugins sync; full suite 2720 pass with 6 pre-existing failures recorded as follow-ups (6v/6w/clean-base successor-wiring)

## Dependencies

- **Depends on:** [bob-cli-7e.1](bob-cli-7e.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7e.5](bob-cli-7e.5.md) ◐ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7e.7](bob-cli-7e.7.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7e.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7e.3/README.md) | [bob-cli-7e.3](bob-cli-7e.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6aef3b6`](https://github.com/bobs-org/bob-plugins/commit/6aef3b6942ae3be0d12fa4513bee213544e8b845) | feat(blocks): add BLOCKS recognisers and gesture guards to nav, cycler, bip | [bob-cli-7e.3](bob-cli-7e.3.md) | 2026-10-13 12:07:51 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7e.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7e.3/README.md

<!-- sase:referenced-by:end -->
