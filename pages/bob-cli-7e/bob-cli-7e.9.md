# Bead: bob-cli-7e.9 — Install, verify, reach the MacBook, record

[Bead Pages](../README.md) / [bob-cli-7e](README.md) / bob-cli-7e.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4d.linker.w0.md) · **Assignee:** `bob-cli-7e.9` · **Size:** small
**Created:** 2026-10-13 11:09:49 EDT · **Closed:** 2026-10-13 15:15:31 EDT
**Plan:** [202610/prerequisite\_blocks\_lines.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prerequisite_blocks_lines.md)

## Description

rollout: install bob on this host, review the live dry-run, verify the pilot script on a vault copy, sync plugins, update the MacBook on a best-effort basis, apply the accepted memory decisions, and record follow-ups.

## Notes

[2026-10-13T19:15:19Z · bob-cli-7e.9] Rollout completed 2026-10-13. Host: installed bob-cli bfdff70; opened/pulled bob-plugins 8406ebb, ran `bob plugins sync -n -r <opened checkout>` and `bob plugins list`: six plugins synced, 0 drift. Live reconcile dry-run scanned 5,123 files in 7s with zero BLOCKS updates, mints, or dependency warnings; the vault already has the 15 generated rows across 8 notes (explains why the research estimate of 15 inserts and 6 mints did not appear in the dry-run). `bob projects sync --dry-run`: 87 projects, 0 changes/warnings. Pilot copy: first and second reconcile had zero changes; after deleting the BLOCKS rows, reconcile inserted 15 rows with no mints/warnings and restored all 8 affected notes to match the host; `blocks_lines: false` removed 15 rows and `true` rebuilt them. Capture `&` inserted a dependency target BLOCKS row; dropping the prerequisite removed the entry and empty line. Pilot copy deleted. Read-only Mac Capture inspection confirmed additive JSON is tolerated and task-block cards render target lines/roles; no Swift changes. MacBook: fast-forwarded and installed bob-cli bfdff70 (`INSTALL_EXIT=0`), dry-run scanned 5,123 files with zero BLOCKS updates/mints/warnings, projects dry-run was 87/0, and `bob plugins sync`/`list` showed all six plugins synced at the same versions: block-id-prompt 1.32.0, bob-ledger-tools 1.50.0, bob-navigation-hotkeys 2.37.0, bob-project-tasks 1.0.0, bob-vim-surround 1.5.2, task-status-cycler 1.40.0. `just check` passed: cargo fmt, Clippy, 2,555 unit tests, 1,519 CLI tests, and all remaining suites (including BR26). Glossary sentence was already present; reviewer declined the decision record. Remaining for Bryan: reload nav, ledger-tools, cycler, and block-id-prompt on Mac, then manually pilot same-note and cross-note Ctrl+Shift+P add/undo, chip ×, close, and a hand edit of a BLOCKS line.

PROPOSED FOLLOW-UP: bob-cli-3p — Add dependent-side BLOCKS editing: write Depends-On from BLOCKS, chip ＋ / write-through ×, Task Card Blocks row, and Ctrl+Shift+P on BLOCKS; reuse the planner seam and ledger reverse index.
PROPOSED FOLLOW-UP: bob-cli-3q — Reuse the reverse index for the task-line ⛓ badge.
PROPOSED FOLLOW-UP: bob-cli-3o — Retire R8 legacy dependency readers so legacy edges leave BLOCKS membership automatically.

[2026-10-13T19:15:31Z · bob-cli-7e.9] Verified host install, zero-change live dry-run, 15-row rebuild and kill-switch/capture pilot on a disposable vault copy, plugin syncs on host and MacBook, Mac dry-run, and passing just check; recorded remaining manual Mac UI pilot and proposed follow-ups on this bead.

## Dependencies

- **Depends on:** [bob-cli-7e.6](bob-cli-7e.6.md) ✓ · ⧖ 2026-10-13
- **Depends on:** [bob-cli-7e.8](bob-cli-7e.8.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7e.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7e.9/README.md) | [bob-cli-7e.9](bob-cli-7e.9.md) | 0 |
