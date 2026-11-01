# Bead: bob-cli-f5.3 — Reading view, embeds, hover popovers, and query rows

[Bead Pages](../README.md) / [bob-cli-f5](README.md) / bob-cli-f5.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16q.md) · **Size:** medium
**Created:** 2026-11-01 09:24:21 EST · **Closed:** 2026-11-01 10:41:49 EST
**Plan:** [202611/task\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_link_marks.md)

## Description

reading: add the post-processor for Reading view, embeds, hover popovers, and Tasks/Dataview rows, apply the DOM exclusion rules, and add a stamp-and-sweep refresh that updates rings in place across every window.

## Notes

[2026-11-01T15:38:29Z · bob-cli-f5.3--2] PROPOSED FOLLOW-UP: Repair seven bob-plugins tests that fail identically on the clean base and this phase tree: warm snapshot/order <=50 ms; 5,000-row keystroke ranking <=12 ms; reload event only when due keys change; today-note create listener once after layout readiness; forced-check feedback after Bob refresh; linear startup storm; relationIndex layout-ready registration without non-Markdown reads during startup replay. Clean-base comparison: monitor aa9qnd3nw9cw, CLEAN_BASE_MATCH.

[2026-11-01T15:41:49Z · bob-cli-f5.3--2] Reading view, embeds, hover popovers, and query-row rings implemented; npm test ran with 7 failures reproduced identically on clean base (monitor aa9qnd3nw9cw, CLEAN_BASE_MATCH) and recorded as PROPOSED FOLLOW-UP; npm run docs:check passed (447 passed, 1 skipped); bob-ledger-tools synced successfully from this checkout; epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-f5.2](bob-cli-f5.2.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f5.4](bob-cli-f5.4.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-f5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-f5.3.md) | [bob-cli-f5.3](bob-cli-f5.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@bedc7e2`](https://github.com/bobs-org/bob-plugins/commit/bedc7e2a7cb16257b48bc3b26241d663a2f161db) | feat(bob-ledger-tools): mark task links in reading views | [bob-cli-f5.3](bob-cli-f5.3.md) | 2026-11-01 10:42:18 EST |
