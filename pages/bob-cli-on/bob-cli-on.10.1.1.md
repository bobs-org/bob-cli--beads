# Bead: bob-cli-on.10.1.1 — Recognizer and layout twins in the cycler

[Bead Pages](../README.md) / [bob-cli-on.10.1](bob-cli-on.10.1.md) / bob-cli-on.10.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.md) · **Assignee:** `bob-cli-on.10.1.1` · **Size:** medium
**Created:** 2026-11-21 14:10:17 EST · **Closed:** 2026-11-21 15:03:24 EST
**Plan:** [202611/obsidian\_req\_gestures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_gestures.md)

## Description

req-read-twin: port bob-cli's task_reqs recognizer (RQ) and task_block_layout zones, slots, violations, note homes, tidy, scoop, and file-into-NOTES (RL) into new plugin-agnostic cycler fragments, copy the RQ/RL fixtures, and pass every RQ and RL vector.

## Notes

[2026-11-21T20:03:01Z · bob-cli-on.10.1.1] PROPOSED FOLLOW-UP: bob-cli ^prj NOTES filing is broken (twin mirrors it, as the plan requires) — for a ^prj project task, file_into_notes → ensure_notes_drawer → capture_drawers::ensure_drawer takes the is_prj_parent path: it appends "## NOTES" at EOF and files notes at first_child_indentation/dominant unit (a tab under an H2 renders as an indented code block); because drawers() only lists bullet drawers, an existing "## NOTES" section is never found, so a second empty "## NOTES" heading is appended while the notes land in the first. bob task tidy refuses these plans via content_preserved ("it would add the line \"## NOTES\""), but the RW writers (toggle note→req first-req scoop, insert_reqs) have no such guard. No RL/RW vector covers ^prj. Decide the intended ^prj behaviour in bob-cli (contract §3), add vectors, and re-copy.

[2026-11-21T20:03:09Z · bob-cli-on.10.1.1] PROPOSED FOLLOW-UP: bob plugins sync cannot deploy task-status-cycler without -F — the vault holds cycler 1.52.0 stamped clean from bob-cli_13 at 726f9a5, which was rebased and landed as 6e0d764 (manifest/main.js/styles.css all byte-identical, reachable from HEAD). deploy.rs only consults find_inclusion_proof for dirty stamps; the clean-stamp branch requires the stamped SHA to be an ancestor, so the documented "Landed" recipe (stash, ff, clean sync) still refuses. The deployment doc says a clean checkout reaching a byte-identical commit syncs without --force. Fix bob-cli to apply the inclusion proof to clean stamps too. This phase did not force (AGENTS.md); cycler 1.53.0 (inert twins) is not deployed, and req-write-twin, which must sync the cycler, will hit the same refusal.

[2026-11-21T20:03:24Z · bob-cli-on.10.1.1] req-read-twin done in bob-plugins (uncommitted at close; committed by this turn's final declaration). New pure, plugin-agnostic cycler fragments: 194-task-reqs-lines-twin.js (line spans, list items, fences, frontmatter, managed-line/log/drawer predicates, note_tasks scan with clean_description; Rust whitespace and UTF-8 indent comparisons), 195-task-reqs-twin.js (RQ: taskReqForest/ForOwner/InfoAtLine/OwnerOfLine/IsReqLine/PathText/RowKey(ownerKey,row,digest8)/Run; rows keep ledger-tools field names, Index fields are 0-based), 196-task-block-layout-twin.js (RL: classify, zones, taskBlockRead/InsertionSlot/DrawerHeaderOffset/Drawers/DrawerInsertion/EnsureNotesDrawer incl. the ^prj H2 path/NoteHome/DesiredOrder/LayoutViolations/FindTask), 197-task-block-tidy-twin.js (edit helpers PhysicalLines/WithEnding/Bare/RestoreFinalNewline/RebaseIndent/InsertLines/PullRanges/Rebased, ScoopLooseNotes, FileIntoNotes, PlanTidy), and 211-task-reqs-exports.js; slot 198 is free for the RW writers and 193 for the guard. Options are {globalFilter, statusTypes}; offsets are UTF-16. Fixtures README/vectors/layout copied byte for byte into plugins/task-status-cycler/scripts/fixtures/task_reqs/. scripts/test-task-status-cycler-task-reqs-vectors.cjs (in test:unit): all 21 RQ cases (every node field, probes, distinct row keys via node crypto, per-owner entry point), all 52 RL slots/violations/tidy (with no-violations-after and idempotence)/note_homes, fixture byte-equality against bob-cli, plus mirrors of bob-cli unit tests: 84/84 pass. Differential fuzz against a fresh bob-cli debug build (bob task tidy -f json dry run, scratch vaults): 4,200 random notes incl. CRLF, no final newline, frontmatter, fences, NBSP, ^prj, 0 mismatches. cycler manifest 1.53.0, docs:gen version cells. Gates: npm run build and build:check clean; docs inventory current; npm test 8384/8390 pass. The 2 failures reproduce identically on clean base: the stale cycler offer_close SV fixture (re-copied by req-write-twin step 3) and the known load flake test-ledger-tools-frees-marks.cjs:481 (passes 3/3 alone). npm run docs:check fails identically on base (word budgets: plugin-apis.md tracked by bob-cli-ob; reference bob-ledger-tools.md and bob-navigation-hotkeys.md). Not synced: see the sync follow-up note.

## Dependencies

- **Blocks:** [bob-cli-on.10.1.2](bob-cli-on.10.1.2.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.10.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.1/README.md) | [bob-cli-on.10.1.1](bob-cli-on.10.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f292fff`](https://github.com/bobs-org/bob-plugins/commit/f292fffaf6f0db2e87d0d9bc9fa63b67d3870997) | feat(task-status-cycler): add task requirement and block layout twins | [bob-cli-on.10.1.1](bob-cli-on.10.1.1.md) | 2026-11-21 15:08:09 EST |
