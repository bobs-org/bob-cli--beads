# Bead: bob-cli-px.3 — Mail Close Card and guard API in Bob Navigation Hotkeys

[Bead Pages](../README.md) / [bob-cli-px](README.md) / bob-cli-px.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fs](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fs.md) · **Assignee:** `bob-cli-px.3` · **Size:** medium
**Created:** 2026-11-24 12:22:30 EST · **Closed:** 2026-11-24 14:48:37 EST
**Plan:** [202611/email\_task\_close\_confirmation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/email_task_close_confirmation.md)

## Description

navcard: model twin, the card modal, nav api.mailCloseGuard v1, and guarding every nav-owned close path including review-walk landings.

## Notes

[2026-11-24T19:47:55Z · bob-cli-px.3--4] PROPOSED FOLLOW-UP: scripts/test-ledger-tools-frees-marks.cjs intermittently misses its 25 ms budget for the 200-link / 2,000-task synthetic build. The full suite failed twice: first at 32 ms, then reported 25 ms against the 25 ms budget (42.2 ms TAP duration); the isolated run passed at 19.5 ms. The test and ledger implementation are unchanged in this phase.

[2026-11-24T19:48:37Z · bob-cli-px.3--4] Verified the Mail Close Card model, nav API, guards, and docs: npm run build passed; npm run docs:check passed against this workspace (447 documentation tests passed, 1 skipped); bob plugins sync completed. Full npm test repeatedly hit the unchanged scripts/test-ledger-tools-frees-marks.cjs 25 ms synthetic-build budget; it passed in isolation, and the observed full-suite timings are recorded in the PROPOSED FOLLOW-UP note. sase bead epic-symbols found no remaining symbols.

## Dependencies

- **Depends on:** [bob-cli-px.1](bob-cli-px.1.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-px.4](bob-cli-px.4.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-px.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-px.3.md) | [bob-cli-px.3](bob-cli-px.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@06f236c`](https://github.com/bobs-org/bob-plugins/commit/06f236c21942d7f42bf6445832d0b7afdd337f79) | feat(navigation): guard Gmail task closes with Mail Close Card | [bob-cli-px.3](bob-cli-px.3.md) | 2026-11-24 14:50:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-px.3--4][1] | Review the assigned Bob Navigation Hotkeys phase before recording verification findings and resolving symbols | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-px.3.md

<!-- sase:referenced-by:end -->
