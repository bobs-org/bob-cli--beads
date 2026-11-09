# Bead: bob-cli-j0 — Restore today's lost task links and guard the vault against silent task loss

[Bead Pages](../README.md) / bob-cli-j0

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.d4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.d4.md) · **Assignee:** `bob-cli-j0.land`
**Created:** 2026-11-09 07:43:10 EST · **Closed:** 2026-11-09 10:00:21 EST
**Plan:** [202611/lost\_task\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/lost_task_guards.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/lost_task_guards.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/lost_task_guards.md

<!-- sase:links:end -->

## Description

The task links lost on 2026-11-09 resolve again. A block-ID rename becomes one unit: a single undo either reverts it in every note or leaves no link dangling. Keep-linked tasks stop getting URL-derived IDs like ^https-keep-google-com. And any future change that removes a linked task, or quietly drops an open one, is named by bob vault-sync within a minute, with the commit to restore it from, instead of being discovered by accident days later.

## Notes

[2026-11-09T14:02:45Z · bob-cli-j0.land] FOLLOW-UP TRIAGE: Reviewed every child note (j0.1: 2, j0.2: 5, j0.3: 1, j0.4: 2). j0.2 note #3 accepted as new medium bug bob-cli-j1, now ready: generic multi-edit applyTargetTaskPlan still makes two replaceRange calls and zero transactions; one undo leaves mixed spans. Blame predates this epic (03f0c17/b1b1144), no duplicate found in searches or one-week all-status sweep, no causal active-epic owner (5w.8 is task-status-cycler close wiring); linked adjacent bob-cli-hk. j0.4 note #1 corroborated existing bob-cli-it (+1) with a fresh production validate_mount_targets reproduction using an ignored/untracked/unmanifested index; no new duplicate. No proposals declined without disposition. Newly reproduced rename-follow race and tripwire link-identity bug are caused by this epic and remain required epic work, not follow-up tasks.

[2026-11-09T14:03:33Z · bob-cli-j0.land] LAND AUDIT: Read the approved plan and all 10 child notes; the epic had no prior notes or parent. Verified vault restoration deead93b5, bob-plugins 94c6df5/5e5e33b, and bob-cli 7fe12b33 against source and tests. Reran 34 rename/navigation tests (all pass); both Keep task prose cases, including quoted link titles, mint prose IDs. Origin snapshot 9c4d2b1a7 retains ^auto-label-kelly-emails and three inbound paths (daily, bob.md, done/bob_done.md). Reviewed post-restore task-note diffs: additions, status/lane changes, and calendar spans; no further loss there. Live Mac Dataview confirms blockId auto-label-kelly-emails; sync is healthy; Mac plugin list reports clean/synced block-id-prompt 1.38.0 from 5e5e33b. Apollo navigation was still missing the Keep fix (77c34f1); deployed it with scoped bob plugins sync from clean 5e5e33b and refreshed the rename bundle stamp to clean. Haircut is absent in the reviewed daily note and remains bob-cli-iz work. Scratch loss-B replay through installed bob produced one pending candidate, one settled linked report and log line, then zero new reports on a third cycle.

INTEGRATION: Used epic creation time because the first main-repo epic commit was the final phase. Reviewed concurrent 44427b30 (similar records), 135793bf (sized close), 262f3cfc (records init), 5f361c5a (sized-close docs), a449193b (gcal skips/tombstones), plus the nearby Templater plugin change 77c34f1. These retain IDs/add records or keep gcal ownership separate; no duplicate loss guard or further source integration identified. Fetched origin: bob-cli HEAD remains 7fe12b33; bob-plugins has only this epic commits after 77c34f1. No epic-symbol entries and no symvision recipe currently.

REMAINING EPIC WORK (do not close yet): (1) vault_task_loss::task_links discards note identity. Repro: tasks.md has open ^shared-id; unrelated legacy.md already has dangling [[#^shared-id]]. Delete the task, sync, age scratch first_seen, sync: it confirms a linked loss with legacy.md inbound, though expected unlinked/no desktop notice (closed task should produce none). (2) renameFollowBusy drops real editor events during awaited writes and followBlockRename clears pending. Existing threeNotes harness: rename old->new; undo bob editor; beforeProcess hook redoes bob and calls noteBlockRenameUpdate while undo follow is running; await deliverUpdate. Bob ends new, daily/done end old, pending empty, sole Notice says Undid block ID rename in 2 notes. Both are caused by this epic. A medium repair tale will fix these and finish this epic closeout in its coding turn. No full Rust check rerun in this planning turn; final just check belongs after the repairs. No check-full run.

[2026-11-09T15:00:21Z · bob-cli-j0.land] CLOSEOUT: both landing defects repaired and verified; original four phases remain closed.

Defect 1 (vault_task_loss inbound identity): inbound links are keyed by (block ID, resolved note path) via vault_links::NoteIndex. git ls-files plus candidate paths keep deleted notes resolvable. Same-note [[#^id]] in another file, [[other#^id]], and ambiguous basenames do not mint a linked loss. Genuine [[note#^id]], [[note.md#^id|alias]], same-note [[#^id]] in the removed note, and whole-note deletion still count as linked. Unlinked losses still do not notify. Tests: cargo test --lib vault_task_loss (9); cargo test --test cli vault_sync_ (37, including legacy dangler unlinked, closed+legacy none, resolved same-note/path/alias linked, whole-note deletion linked).

Defect 2 (rename-follow race): genuine editor events queue during awaited closed writes; plugin-own transactions are ignored via renameFollowApplying; follow revalidates the trigger and drains pending with an 8-cycle cap. Redo-during-undo, undo-during-redo, and unrelated second-editor edits converge or keep the typed buffer with an honest sticky notice. 15/15 test-block-id-prompt-rename-atomic.cjs pass.

Checks: just check green (fmt, clippy, workspace tests). bob-plugins npm run validate green; npm test 5780 pass / 1 skip (command-mode Chromium DOM test without CI). Isolated real-Obsidian e2e on athena (xvfb-run, /snap/obsidian/72/app/obsidian, Node 24) pass=true for vim-undo, api-undo-open-split, and ambiguous-undo. npm run docs:check still fails docs/reference/json-outputs.md 6020/6000 — existing bob-cli-it, not absorbed.

Deploy: bob plugins sync --no-pull -p block-id-prompt from the dirty working tree. Apollo and Mac vault main.js sha256 a923a1157a0e7b5bb26d707e9c738d7c1aedb104fdf10eac79f68109eb56656b matches the build; list reports synced 1.38.0 uncommitted from 5e5e33b.

Vault: origin/master 657b5033f still has ^auto-label-kelly-emails on bob.md with inbound 2026/20261109.md, bob.md BLOCKS, and done/bob_done.md. Live apollo vault and Mac `bob query` TASK WHERE blockId = auto-label-kelly-emails both return the restored row. Haircut Event Task ^haircut-wolves-den is still absent from 2026/20261109.md (only a struck research tomato); left to bob-cli-iz.

Scratch loss-B through the working-tree bob 0.5.0 debug binary: cycle1 one pending linked; cycle2 one confirmed linked report and one sync_conflicts log line (3 inbound); cycle3 zero new reports. Legacy same-ID dangler replay: pending/confirmed unlinked with empty inbound.

Drift: bob-cli origin/master still 7fe12b33; bob-plugins origin/master still 5e5e33b. Integrated the stale root --help snapshot for capture-related's record-notes wording from concurrent 44427b30 so just check matches. No new origin commits on either repo.

Follow-up dispositions (already completed by the lander): j0.2 note #3 is ready medium bug bob-cli-j1; j0.4 note #1 corroborated bob-cli-it (+1). Neither is caused by this epic. No epic-symbol entries. justfile has no symvision recipe.

Children j0.1–j0.4 closed. No parent.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-j0.1](bob-cli-j0.1.md) | Restore the 2026-11-09 losses and re-audit the vault | ✓ closed | small | 2026-11-09 | 1 | 0 |
| [bob-cli-j0.2](bob-cli-j0.2.md) | Make block-ID renames one undo step and undo-coherent across notes | ✓ closed | medium | 2026-11-09 | 1 | 1 |
| [bob-cli-j0.3](bob-cli-j0.3.md) | Stop Keep links from seeding block IDs | ✓ closed | small | 2026-11-09 | 1 | 1 |
| [bob-cli-j0.4](bob-cli-j0.4.md) | vault-sync task-loss tripwire | ✓ closed | medium | 2026-11-09 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-j0: Restore today's lost task links and guard the vault against silent task loss [closed]"]
    n1["bob-cli-j0.1: Restore the 2026-11-09 losses and re-audit the vault [closed]"]
    n2["bob-cli-j0.2: Make block-ID renames one undo step and undo-coherent across notes [closed]"]
    n3["bob-cli-j0.3: Stop Keep links from seeding block IDs [closed]"]
    n4["bob-cli-j0.4: vault-sync task-loss tripwire [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j0.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j0.1/README.md) | [bob-cli-j0.1](bob-cli-j0.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-j0.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j0.2/README.md) | [bob-cli-j0.2](bob-cli-j0.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-j0.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j0.3/README.md) | [bob-cli-j0.3](bob-cli-j0.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-j0.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j0.4/README.md) | [bob-cli-j0.4](bob-cli-j0.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-j0.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j0.land.md) | [bob-cli-j0](README.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@94c6df5`](https://github.com/bobs-org/bob-plugins/commit/94c6df5be8172c017a7855510c2fa2679858b735) | fix(navigation): derive dependency IDs from task prose | [bob-cli-j0.3](bob-cli-j0.3.md) | 2026-11-09 07:52:18 EST |
| bob-plugins | [`bob-plugins@5e5e33b`](https://github.com/bobs-org/bob-plugins/commit/5e5e33b60f008c95fcd14b2ecbc2d71a9c30dfcd) | feat(block-id-prompt): make block-ID renames one undo step across notes | [bob-cli-j0.2](bob-cli-j0.2.md) | 2026-11-09 08:15:12 EST |
| bob-cli | [`7fe12b3`](https://github.com/bobs-org/bob-cli/commit/7fe12b33e46db7429e5d7e95d91afe57103e13f0) | feat(vault-sync): detect linked task losses | [bob-cli-j0.4](bob-cli-j0.4.md) | 2026-11-09 08:45:02 EST |
| bob-cli | [`cb27f8b`](https://github.com/bobs-org/bob-cli/commit/cb27f8bca373ef30d4f734221addd2d2b8a1e005) | fix(vault-sync): key inbound task-loss links by resolved note | [bob-cli-j0](README.md) | 2026-11-09 10:01:59 EST |
| bob-plugins | [`bob-plugins@a2045cc`](https://github.com/bobs-org/bob-plugins/commit/a2045cc9c1c4f4206b425df6985fca91a81928cb) | fix(block-id-prompt): queue editor events during closed rename follow | [bob-cli-j0](README.md) | 2026-11-09 10:02:42 EST |
| bob-cli--plans | [`bob-cli--plans@4ed7cbb`](https://github.com/bobs-org/bob-cli--plans/commit/4ed7cbb025bea9c4ff91c35b1524f1e41548aa89) | chore(plans): mark lost\_task\_guards done after j0 closeout | [bob-cli-j0](README.md) | 2026-11-09 10:03:17 EST |
