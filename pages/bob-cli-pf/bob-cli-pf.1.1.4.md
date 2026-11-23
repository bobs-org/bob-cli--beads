# Bead: bob-cli-pf.1.1.4 — Equals arm table and drawer commands

[Bead Pages](../README.md) / [bob-cli-pf.1.1](bob-cli-pf.1.1.md) / bob-cli-pf.1.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.1.md) · **Assignee:** `bob-cli-pf.1.1.4` · **Size:** medium
**Created:** 2026-11-22 14:45:09 EST · **Closed:** 2026-11-22 18:54:17 EST
**Plan:** [202611/card\_foot\_drawer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/card_foot_drawer.md)

## Description

entrypoints: generalize the existing equals gate, add the mounted-view minus arm and palette and Command Mode toggles, retain equals behavior, and publish the tested kit integration contract.

## Notes

[2026-11-22T23:35:58Z · bob-cli-pf.1.1.4--3] PROPOSED FOLLOW-UP: stabilize full-suite performance thresholds. The same ledger timing checks failed on the phase tree (60.8 ms and 57 ms against 25 ms budgets) and clean base (38.7 ms and 263 ms), so they are not phase-specific. Evidence: file:monitor-diagnostic-manifest:kzv6j2573m7v; file:monitor-diagnostic-manifest:ae2zm8abyhr9.

[2026-11-22T23:54:17Z · bob-cli-pf.1.1.4--3] Verified mounted-view property toggling and palette/Command Mode integration while preserving == editing. npm run validate passed (12/12 plugins); docs:check passed (447 passed, 1 skipped); sync deployed ledger-tools, navigation-hotkeys, and command-mode. npm test full-suite timing failures reproduce on clean base; PROPOSED FOLLOW-UP records both monitor diagnostic refs.

## Dependencies

- **Depends on:** [bob-cli-pf.1.1.3](bob-cli-pf.1.1.3.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pf.1.1.5](bob-cli-pf.1.1.5.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.1.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.1.1.4.md) | [bob-cli-pf.1.1.4](bob-cli-pf.1.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.1.1.4--2][1] | Review the assigned phase scope and notes before recording verification and closing it | 1 |
| read-by | [agent:bob-cli-pf.1.1.4--3][1] | Confirm proposed follow-up note and phase status before closure. | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.1.1.4.md

<!-- sase:referenced-by:end -->
