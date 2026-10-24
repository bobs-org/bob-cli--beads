# Bead: bob-cli-bp.5 — Virtual Live Preview mount, controls, and plugin docs

[Bead Pages](../README.md) / [bob-cli-bp](README.md) / bob-cli-bp.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2f.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2f.linker.w1.md) · **Assignee:** `bob-cli-bp.5` · **Size:** medium
**Created:** 2026-10-24 16:30:45 EDT · **Closed:** 2026-10-24 18:21:34 EDT
**Plan:** [202610/daily\_note\_day\_strip.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_note_day_strip.md)

## Description

strip-mount: mount the strip as a CodeMirror StateField block widget after the last line of canonical daily notes in Live Preview. Add the `stats.day_strip` config switch, the session `Toggle Day stats` command, per-device collapse, fence stand-down, and the optional Reading view host. Then update plugin docs and the manifest, and sync to the vault.

## Notes

[2026-10-24T22:09:47Z · bob-cli-bp.5] PROPOSED FOLLOW-UP: Add the accepted Day strip placement and facts-only decision record for bob-ledger-tools and bob-cli — deferred by the epic decision_record=false branch.

[2026-10-24T22:09:53Z · bob-cli-bp.5] PROPOSED FOLLOW-UP: Add a Day Strip glossary term (alias day stats) distinguishing the daily-note receipt from the Morning GTD Review Footer — deferred by the epic glossary_term=false branch.

[2026-10-24T22:09:58Z · bob-cli-bp.5] Manual Mac checks for Bryan: open today warm and cold to check first-frame geometry; type and use vim G/o and confirm tile clicks preserve vim; compare spawn counts while scrolled off screen; verify Stats opens with the day pinned and time mix opens homes; check a past-day receipt, light/dark themes, 410 px split, and 200% zoom.

[2026-10-24T22:21:13Z · bob-cli-bp.5--1] PROPOSED FOLLOW-UP: Existing timing-flake task bob-cli-3w tracks the unrelated stage-ranker 1,000-task 16 ms assertion; this run missed once at 19.98 ms in the full suite, then passed unchanged on immediate full-suite rerun (3,647/3,647).

[2026-10-24T22:21:34Z · bob-cli-bp.5--1] Completed the Live Preview Day strip mount, controls, fence stand-down, docs, and manifest. Verified npm run build, npm test (3,647 passed after the known bob-cli-3w stage-ranker timing assertion missed once then passed unchanged on rerun), npm run validate (7/7 plugins), and npm run docs:check (447 passed, 1 skipped). bob plugins sync deployed successfully; bob stats show -a -f json on apollo returned ok:true. Follow-up and manual Mac-check notes are recorded; epic-symbols is clear.

## Dependencies

- **Depends on:** [bob-cli-bp.4](bob-cli-bp.4.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bp.6](bob-cli-bp.6.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bp.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bp.5.md) | [bob-cli-bp.5](bob-cli-bp.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bp.5--1][1] | Confirm the required follow-up and manual Mac-check notes before closing | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bp.5.md

<!-- sase:referenced-by:end -->
