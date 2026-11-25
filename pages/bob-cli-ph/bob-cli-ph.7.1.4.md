# Bead: bob-cli-ph.7.1.4 — Real Obsidian acceptance, screenshots, and documentation

[Bead Pages](../README.md) / [bob-cli-ph.7.1](bob-cli-ph.7.1.md) / bob-cli-ph.7.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.md) · **Assignee:** `bob-cli-ph.7.1.4` · **Size:** medium
**Created:** 2026-11-25 08:48:55 EST · **Closed:** 2026-11-25 12:49:33 EST
**Plan:** [202611/obsidian\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_true_case_drawers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:e9988819b2a7e52753c34291 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

obsidian-acceptance: exercise the integrated feature in an isolated Obsidian vault, inspect and publish light/dark screenshots, update the behavior docs, and record verified deployment evidence.

## Notes

[2026-11-25T17:48:32Z · bob-cli-ph.7.1.4] Acceptance: isolated Athena CDP+Xvfb e2e green, 32/32 cases (`/snap/bin/obsidian`, report pass=true). Cover autopair on/off, Vim insert, Undo/Enter/overtype/Backspace, Toggle Drawer wrap/unwrap/legacy/refusals, unchanged req typing, promote/reverse/named-refusal, and light/dark Live Preview + reading look. Visual inspect of artifacts: trays ~0.95em, hollow Empty, req diamond, unstruck Café/Same, Task Link, no leaked `**`. Artifacts on this phase and bob-cli-ph.7: report file:explicit:e9988819b2a7e52753c34291; light live file:explicit:99c1ffea61076da96225acc2; light reading file:explicit:a95e8a34e6fb850dac4ed7ce; dark live file:explicit:d0f7de1722a08229a8ef40a4; dark reading file:explicit:e51daf687f9c74c956f3709f. Markers: bob-task-drawer-bold-writes-v1, bob-task-drawer-render-v1, bob-task-drawer-typing-v1. task-status-cycler synced without -F from linked uncommitted build (apollo fdde3dc 2026-11-25T17:40:18Z, Prec.highest + deeper toggle). Land agent records host SHA after finalizers for bob-cli-ph.9. Docs: bob-cli task-drawers/projects + plugin cycler/ledger/nav. Focused: drawers e2e self-test, typing 26/26, validate 12/12, npm run build. epic-symbols: none.

[2026-11-25T17:48:47Z · bob-cli-ph.7.1.4] PROPOSED FOLLOW-UP: docs-check still red on clean-base word budgets — plugin-apis.md 9287/8000 (warning) and bob-navigation-hotkeys.md 6068/6000 (error); bob-cli-ph.4 already recorded these; this phase trimmed nav conversion to HEAD 86 words so it adds no extra overage.

[2026-11-25T17:48:54Z · bob-cli-ph.7.1.4] PROPOSED FOLLOW-UP: npm test 9509 pass / 13 fail — leftover NOTES vs **Notes** assertions in test-task-status-cycler-task-reqs-vectors.cjs, req-toggle, open-line (reproduced on clean HEAD 8d3c555c after 7.1.1 bold writers); writers emit **Notes** correctly.

[2026-11-25T17:49:02Z · bob-cli-ph.7.1.4] PROPOSED FOLLOW-UP: plugin perf flakes in npm test — event-link-times 200-link build 152.5ms vs 25ms and frees-marks 200-link/2000-task 25ms budget; test:perf 26/26 passed this run.

[2026-11-25T17:49:09Z · bob-cli-ph.7.1.4] PROPOSED FOLLOW-UP: MN click opens the source at its occurrence line (test-ledger-tools-relation-chips.cjs) expected cursor/focus and got []; unrelated to drawers, treat as flake unless it reproduces on clean HEAD.

[2026-11-25T17:49:17Z · bob-cli-ph.7.1.4] PROPOSED FOLLOW-UP: just check 4120 passed / 17 failed on capture/inbox_route, note_pull, project_note, project_note_offer, task_theme_writes, ref_library::today, and task_status_hooks grouping; this phase changed only bob-cli docs, so these are outside drawer acceptance — confirm on clean bob-cli HEAD (5c0f8160 / later origin cd594550).

[2026-11-25T17:49:33Z · bob-cli-ph.7.1.4] Athena e2e 32/32 pass; trays/empty/req/Task Link visually inspected; artifacts e9988819/99c1ffea/a95e8a34/d0f7de17/e51daf68 on this phase and bob-cli-ph.7; cycler synced Prec.highest without -F; markers bob-task-drawer-{bold-writes,render,typing}-v1; typing 26/26, validate 12/12; clean-base docs/npm/just-check leftovers recorded as PROPOSED FOLLOW-UP. epic-symbols: none. Land agent records host SHA.

## References

- file:explicit:99c1ffea61076da96225acc2
- file:explicit:a95e8a34e6fb850dac4ed7ce
- file:explicit:d0f7de1722a08229a8ef40a4
- file:explicit:e51daf687f9c74c956f3709f
- file:explicit:e9988819b2a7e52753c34291

## Dependencies

- **Depends on:** [bob-cli-ph.7.1.1](bob-cli-ph.7.1.1.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-ph.7.1.2](bob-cli-ph.7.1.2.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-ph.7.1.3](bob-cli-ph.7.1.3.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.7.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.4/README.md) | [bob-cli-ph.7.1.4](bob-cli-ph.7.1.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0742684`](https://github.com/bobs-org/bob-cli/commit/0742684de3390415ffb5dbb3423c0dbc841f4b3e) | docs(task-drawers): document Obsidian trays, typing, and conversion | [bob-cli-ph.7.1.4](bob-cli-ph.7.1.4.md) | 2026-11-25 12:51:09 EST |
| bob-plugins | [`bob-plugins@8254caa`](https://github.com/bobs-org/bob-plugins/commit/8254caa48938b49b73cd4187c216406d1e3f5fea) | feat(task-status-cycler): add Obsidian drawer acceptance and typing precedence | [bob-cli-ph.7.1.4](bob-cli-ph.7.1.4.md) | 2026-11-25 13:03:36 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.7.1.4][1] | Need notes, design, and remaining work from earlier agents | 8 |
| read-by | [agent:bob-cli-ph.7.1.land--1][2] | Re-read every child phase and its completion notes for final landing verification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.land.md

<!-- sase:referenced-by:end -->
