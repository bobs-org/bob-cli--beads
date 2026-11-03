# Bead: bob-cli-gf.3 — Real-Obsidian e2e and visual review (bob-plugins, bob-cli)

[Bead Pages](../README.md) / [bob-cli-gf](README.md) / bob-cli-gf.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c9.md) · **Assignee:** `bob-cli-gf.3` · **Size:** medium
**Created:** 2026-11-03 09:51:51 EST · **Closed:** 2026-11-03 11:35:52 EST
**Plan:** [202611/off\_clock\_link\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_clock_link_chips.md)

## Description

live_verify: drive the chip in an isolated real-Obsidian scratch vault, compare its computed look with the Event Task chip, record screenshots and timings, and write the contract's Live verification section.

## Notes

[2026-11-03T15:39:29Z · 17b--code] COORDINATION NOTE (from a planning agent; not remaining work and not an earlier attempt at this phase): Read the CROSS-EPIC COORDINATION note on epic bob-cli-gf. Item 4 applies to every `bob plugins sync` in this phase. If gg has landed, a time pill may sit before a chipped Event Task link in the scratch vault; that is intended (item 5), not a regression.

[2026-11-03T16:35:26Z · bob-cli-gf.3] PROPOSED FOLLOW-UP: Reading-view status rings still paint on ledger rows including the unchipped parser — Live Preview stays ring-free; e2e skipped reading no-ring when the unchipped parser also rings. Pre-existing task-link-marks ledger exclusion gap, not caused by the off-clock chip.

[2026-11-03T16:35:32Z · bob-cli-gf.3] PROPOSED FOLLOW-UP: Reading view did not expose .bob-progress-mark on the in-progress lunch-wip row while Live Preview did — e2e skipped reading OP5 progress when the glyph was missing. Pre-existing, not caused by the off-clock chip.

[2026-11-03T16:35:52Z · bob-cli-gf.3] Verified live_verify: isolated Athena xvfb-run e2e 88/88 pass (Obsidian 1.15.0, never live vault); OP6 shared look 14.08px dashed muted timer-off; row height 26.375 on/off; liveness fun 262ms, bob 263ms, local 167ms; toggle, popout, calendar-off, OC10 past daily, OT1 tooltip, OP2 order, OP4 cursor. Offline self-test green. just docs-check passed after Live verification in docs/off-clock-link-chips.md. bob plugins sync --no-pull without -F: 0 copied, ledger-tools up to date. No leftover --epic-symbol entries. Skipped reading no-ring (rings also on unchipped parser) and reading OP5 progress (◐ missing in reading); recorded as PROPOSED FOLLOW-UP. Prose-link chips stay deferred (prose_links=no). gg time pill was not present.

## Dependencies

- **Depends on:** [bob-cli-gf.2](bob-cli-gf.2.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gf.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gf.3/README.md) | [bob-cli-gf.3](bob-cli-gf.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e9deb7f`](https://github.com/bobs-org/bob-cli/commit/e9deb7f8ab5e7cc5ecb7ffe68a025d142454e582) | docs(off-clock-chips): record live verification | [bob-cli-gf.3](bob-cli-gf.3.md) | 2026-11-03 11:37:11 EST |
