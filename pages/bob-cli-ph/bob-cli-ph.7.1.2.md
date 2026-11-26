# Bead: bob-cli-ph.7.1.2 — Task drawer marks in Live Preview and reading view

[Bead Pages](../README.md) / [bob-cli-ph.7.1](bob-cli-ph.7.1.md) / bob-cli-ph.7.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.md) · **Assignee:** `bob-cli-ph.7.1.2` · **Size:** medium
**Created:** 2026-11-25 08:48:55 EST · **Closed:** 2026-11-25 10:55:37 EST
**Plan:** [202611/obsidian\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_true_case_drawers.md)

## Description

drawer-rendering: render the approved tray and verbatim title using source-backed attributes, owner ink, folded counts, empty and closed states, and a persistent marks toggle.

## Notes

[2026-11-25T15:47:00Z · bob-cli-ph.7.1.2--3] PROPOSED FOLLOW-UP: Reconcile task-status-cycler fixtures with canonical Notes drawers. Clean-tree tests reproduce 10 assertions expecting NOTES while the writer emits **Notes**; those tests and writer files are unchanged from the pre-phase tree (2796d63d^), so this is outside drawer-marks scope.

[2026-11-25T15:55:12Z · bob-cli-ph.7.1.2--4] Verified bob-ledger-tools deployment: npm run build passed; node --test scripts/test-ledger-tools-task-tag-marks.cjs passed 53/53; npm test had only the 10 known clean-base task-status-cycler NOTES expectation failures, while perf passed 26/26. Deployed with bob plugins sync --repo <linked bob-plugins checkout> --no-pull -p bob-ledger-tools.

[2026-11-25T15:55:37Z · bob-cli-ph.7.1.2--4] Closed after bob-ledger-tools deployment; build and focused 53/53 test passed, full suite showed only the 10 documented clean-base NOTES expectation failures, and performance tests passed 26/26.

## Dependencies

- **Depends on:** [bob-cli-ph.7.1.1](bob-cli-ph.7.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.7.1.3](bob-cli-ph.7.1.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.7.1.4](bob-cli-ph.7.1.4.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.2.md) | [bob-cli-ph.7.1.2](bob-cli-ph.7.1.2.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@2796d63`](https://github.com/bobs-org/bob-plugins/commit/2796d63dc79b3c5e44d113a5b2aae4bbc2ee4ad8) | feat(drawers): add task drawer marks in Obsidian | [bob-cli-ph.7.1.2](bob-cli-ph.7.1.2.md) | 2026-11-25 10:11:25 EST |
| bob-plugins | [`bob-plugins@5ed3bd2`](https://github.com/bobs-org/bob-plugins/commit/5ed3bd22603800d8d2c73f4a2b0ddeb2b494206c) | fix(bob-ledger-tools): export task drawer helpers after initialization | [bob-cli-ph.7.1.2](bob-cli-ph.7.1.2.md) | 2026-11-25 10:25:15 EST |
| bob-plugins | [`bob-plugins@1753d73`](https://github.com/bobs-org/bob-plugins/commit/1753d730133fd125e4b32cd53bd8223efc4ff47b) | docs(bob-ledger-tools): list task drawer marks command | [bob-cli-ph.7.1.2](bob-cli-ph.7.1.2.md) | 2026-11-25 10:33:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.7.1.2--1][1] | Need the phase scope, decisions, and current status before completing its verification | 1 |
| read-by | [agent:bob-cli-ph.7.1.2--2][1] | Confirm assigned scope and existing verification notes before continuing | 1 |
| read-by | [agent:bob-cli-ph.7.1.3][2] | Check what drawer-rendering phase landed to build typing on top | 1 |
| read-by | [agent:bob-cli-ph.7.1.4][3] | Need prior phase notes, markers, deploy evidence, and remaining work | 1 |
| read-by | [agent:bob-cli-ph.7.1.land--1][4] | Re-read every child phase and its completion notes for final landing verification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.land.md

<!-- sase:referenced-by:end -->
