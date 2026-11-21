# Bead: bob-cli-on.5 — The bob task rename-drawer command

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.5` · **Size:** medium
**Created:** 2026-11-21 11:13:26 EST · **Closed:** 2026-11-21 15:31:55 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

drawer-rename: add `bob task rename-drawer OLD NEW`, a previewed, idempotent, one-commit rename and merge of task drawers and ^prj H2 drawer sections across the vault, with heading-link repair and an inventory report.

## Notes

[2026-11-21T20:31:36Z · bob-cli-on.5] PROPOSED FOLLOW-UP: just docs-check fails at lint on the clean base — mounted bob-plugins reference pages docs/reference/plugins/bob-ledger-tools.md (6042 words) and bob-navigation-hotkeys.md (6307 words) exceed the 6000-word reference/ budget (reproduced identically on a clean HEAD worktree; no task bead found tracking it). Trim those plugin reference pages in bob-plugins so the docs gate is green again.

[2026-11-21T20:31:55Z · bob-cli-on.5] Shipped bob task rename-drawer OLD NEW (src/native/task_drawer_rename: pure per-note pass, heading-link repair, CLI shell). Dry run by default; -a/-b/-f/-h; OLD by drawer key, NEW as ALL-CAPS drawer / Title Case ## section. Scope: every #task drawer (open, closed, done/ archive) plus project-note ## drawer sections; merges keep one container at the earliest position labelled NEW with bodies in original order; [[note#Old]], ![[note#Old]], and note.md#Old links repaired, block links untouched; ambiguous-heading notes refused with reason; excluded lookalikes, unresolved links, and _templates hits reported only. -a: shared lock, pre-sync, preimage-guarded writes, verify (no replan, no remaining link repair), one commit 'bob task rename-drawer: OLD → NEW (N notes)', post-sync, drawer catalog invalidated; rerun reports nothing. Refusals (reserved_drawer, invalid_drawer_title, same_drawer) exit 2. Verified: 31 unit + 5 CLI tests; just lint and cargo fmt clean; full cargo test --workspace green (7627 lib, 3917 cli, all other binaries); docs-gen run, docs build --strict and fragment link check OK; docs-check lint fails only on pre-existing bob-plugins page budgets (reproduced on clean HEAD; PROPOSED FOLLOW-UP recorded). Help: bob task group about now 'Task maintenance: archive, merge, move, reconcile, reroll, split, tidy, and more' and reconcile row 'Reconcile statuses from the Pomodoro ledger and dependencies' to keep bob task --help within 80 columns. Evidence for vault-migration: read-only dry run of REQUIREMENTS → NOTES on ~/bob = 3 drawers (1 open in sase_art_links.md, 2 archived in done/bob_done.md and done/sase_done.md) + 51 project sections in 53 notes; 0 merges, links, refusals, exclusions, template hits; vault untouched. The plan's '6 drawers' includes 3 under hidden .bob/ref-sources/, which are out of scope (dot directories).

## Dependencies

- **Blocks:** [bob-cli-on.16](bob-cli-on.16.md) ◐ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-on.4](bob-cli-on.4.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.5/README.md) | [bob-cli-on.5](bob-cli-on.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d8fae3e`](https://github.com/bobs-org/bob-cli/commit/d8fae3e5c734404864da0376818953733743ce56) | feat(task): add bob task rename-drawer to rename and merge drawers vault-wide | [bob-cli-on.5](bob-cli-on.5.md) | 2026-11-21 15:33:08 EST |
