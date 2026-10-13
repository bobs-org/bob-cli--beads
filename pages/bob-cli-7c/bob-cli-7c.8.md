# Bead: bob-cli-7c.8 — Decision record, supersession marks, and epic acceptance

[Bead Pages](../README.md) / [bob-cli-7c](README.md) / bob-cli-7c.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.11.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.11.linker.w0.md) · **Assignee:** `bob-cli-7c.8` · **Size:** small
**Created:** 2026-10-13 09:48:13 EDT · **Closed:** 2026-10-13 17:10:20 EDT
**Plan:** [202610/successor\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_offers.md)

## Description

decision_record: record the accepted Successor Offers decision, mark the records it partly supersedes, optionally add the glossary term, re-run the cross-repo acceptance checks, and record the deferred follow-ups.

## Notes

[2026-10-13T21:02:36Z · bob-cli-7c.8] PROPOSED FOLLOW-UP: Add an Obsidian rescue command for held successor offers — the accepted epic plan explicitly defers a revalidated “Pull in unblocked tasks…” command. PROPOSED FOLLOW-UP: Consider per-row destination overrides in Bob Mac Capture and a destination grammar for --pull-in — the plan defers both while JSON already carries destination. PROPOSED FOLLOW-UP: Consider an interactive TTY picker for bob capture — the plan explicitly defers this. PROPOSED FOLLOW-UP: Investigate macOS 26 CI failures in RefsInspectorScrollTests on run 38464978866 (commit 6c4209b); the four failures were hosted-notes/short-content scroll expectations, while the successor-offer tests passed.

[2026-10-13T21:10:06Z · bob-cli-7c.8--1] PROPOSED FOLLOW-UP: Bob plugins npm test on clean bob-plugins 8406ebb reports 7 failures (2747/2754 pass): four ledger-tools unblocked-glyph cases (tracked by bob-cli-6v); navigation Keep counts once and saturates at 999 (tracked by bob-cli-6w); task-status-cycler Pomodoro-line close appends successor (already surfaced in parent epic DISCOVERED ISSUE and reproduced by bob-cli-7e.3/.4); and navigation-hotkeys forward conversion carries a Depends-On line and reverse restores it, whose old assertion conflicts with the new BLOCKS mirror (no existing tracking bead found).

[2026-10-13T21:10:20Z · bob-cli-7c.8--1] Decision record and authorized supersession/glossary updates are complete. cargo test passed. Bob plugins npm test completed with 2747/2754 passing and 7 clean-tree failures recorded as proposed follow-ups (four tracked by bob-cli-6v, one by bob-cli-6w, the successor-wiring failure already surfaced on the parent epic, and one BLOCKS-conversion assertion with no tracking bead). bob plugins sync --dry-run passed (9 to copy, 7 unchanged). Latest Bob Mac Capture CI remains failed at run 38464978866 (commit 6c4209b); the phase record identifies four RefsInspectorScrollTests hosted-notes/short-content scroll expectation failures, while successor-offer tests passed. macOS CI remains the platform verification limitation. Epic-symbol check found no leftovers.

## Dependencies

- **Depends on:** [bob-cli-7c.3](bob-cli-7c.3.md) ✓ · ⧖ 2026-10-13
- **Depends on:** [bob-cli-7c.4](bob-cli-7c.4.md) ✓ · ⧖ 2026-10-13
- **Depends on:** [bob-cli-7c.5](bob-cli-7c.5.md) ✓ · ⧖ 2026-10-13
- **Depends on:** [bob-cli-7c.6](bob-cli-7c.6.md) ✓ · ⧖ 2026-10-13
- **Depends on:** [bob-cli-7c.7](bob-cli-7c.7.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7c.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.8.md) | [bob-cli-7c.8](bob-cli-7c.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`19075ee`](https://github.com/bobs-org/bob-cli/commit/19075ee673e0dd8a187676204575dced50d2f3dd) | feat(memory): record successor offers decision | [bob-cli-7c.8](bob-cli-7c.8.md) | 2026-10-13 17:11:07 EDT |
