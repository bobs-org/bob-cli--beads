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
- **Blocks:** [bob-cli-ph.7.1.4](bob-cli-ph.7.1.4.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.2.md) | [bob-cli-ph.7.1.2](bob-cli-ph.7.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.7.1.2--1][1] | Need the phase scope, decisions, and current status before completing its verification | 1 |
| read-by | [agent:bob-cli-ph.7.1.2--2][1] | Confirm assigned scope and existing verification notes before continuing | 1 |
| read-by | [agent:bob-cli-ph.7.1.3][2] | Check what drawer-rendering phase landed to build typing on top | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.1.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.7.1.3/README.md

<!-- sase:referenced-by:end -->
