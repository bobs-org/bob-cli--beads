# Bead: bob-cli-hg.1 — Shared Google and gog plumbing extracted from gcal

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.1` · **Size:** medium
**Created:** 2026-11-05 12:37:49 EST · **Closed:** 2026-11-05 17:50:14 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Previously Closed

> ↺ Closed 2026-11-05T19:16:49Z · done
>
> (none)
>
> Reopened 2026-11-05T22:22:38Z by `sase bead open`

## Description

google-plumbing: move gcal's service-agnostic gog transport, sign-in, client discovery, account choice, and failure classification into src/native/google/ behind a service profile, with gcal behavior byte-identical.

## Notes

[2026-11-05T19:16:20Z · bob-cli-hg.1--3] PROPOSED FOLLOW-UP: Fix the pre-existing strict Clippy collapsible_if in the task-status config snapshot — Reproduces unchanged on the formatted clean base at src/native/task_status_hooks/sync.rs:1620; clean-base ToolRun 024baa723eafe9a02fae569539c906ee / monitor 72tjp5fbvej7, also present in original full-check ToolRun b7c0a716db1a7c367226928f47d897d5 / monitor 5qdsn0qv0wme. This is outside the Google refactor scope.

[2026-11-05T19:16:49Z · bob-cli-hg.1--3] Extracted shared Google transport, OAuth/client discovery, account selection, sign-in, error classification, and doctor primitives behind service profiles; Calendar wording and behavior remained compatible. All six Calendar integration targets passed (168 tests) and 28 shared Google unit tests passed. Full just check is blocked by the same pre-existing clippy::collapsible_if at src/native/task_status_hooks/sync.rs:1620 on clean base (ToolRun 024baa723eafe9a02fae569539c906ee / monitor 72tjp5fbvej7; original ToolRun b7c0a716db1a7c367226928f47d897d5 / monitor 5qdsn0qv0wme), recorded as a PROPOSED FOLLOW-UP. Temporary clean-base worktree removed; epic-symbol check found no entries.

[2026-11-05T22:18:37Z · bob-cli-hg.1] CLOSED-BEAD LAUNCH: agent bob-cli-hg.1 launched against this closed bead; status left closed.
Launch submitted 2026-11-05T22:17:40.257396Z; run 20261105171743.
Prior close: 2026-11-05T19:16:49Z · done.

[2026-11-05T22:22:47Z · bob-cli-hg.1] Recovery: the prior implementation commit 20c60d18 exists in the earlier checkout reflog, but its publication rebase failed and origin/master has no src/native/google. Reopened to recover that completed implementation onto current master, resolve conflicts, and verify it before finalization.

[2026-11-05T22:30:43Z · bob-cli-hg.1] Recovered the source changes from unlanded commit 20c60d18 onto master 6e816775, retaining the newer gmail module declaration and omitting old unrelated formatting churn. Review found and corrected a compatibility regression: logout must pass explicit account identifiers through to gog without adding login email validation; added two isolated fake-gog regression tests without changing existing expectations. Formatting passes. Initial full check ToolRun 4d6f263ab3a80fbbf771aaec535b776f fails at pre-existing src/native/gmail/body/mime.rs:27 clippy::derivable_impls. Remaining work fits one verification follow-up: run the final gate, Google/Calendar unit tests and all Calendar integration targets, confirm the same gate error on pinned clean base 6e816775, then record follow-up evidence and close this reopened phase manually. No epic symbols remain.

[2026-11-05T22:30:59Z · bob-cli-hg.1] PROPOSED FOLLOW-UP: Fix the Gmail MIME inventory strict Clippy failure already recorded on bob-cli-hg.3.1 — Initial recovered-tree just check (ToolRun 4d6f263ab3a80fbbf771aaec535b776f) fails at src/native/gmail/body/mime.rs:27 with clippy::derivable_impls. This file is unchanged by the Google plumbing phase; bob-cli-hg.3.1 note 1 identifies its introduction in df9178df. The verification monitor will add clean-base reproduction evidence.

[2026-11-05T22:49:58Z · bob-cli-hg.1--1] PROPOSED FOLLOW-UP: Confirmed the Gmail MIME strict Clippy failure already recorded on bob-cli-hg.3.1 — Recovery monitor 9ny17wp86z9t (ToolRun a50cad16af98007c60567ccbdcccdd21) ran just check on the recovered tree and on detached clean base 6e816775f0252b6bd68af2900699e6bd537168fb; both exited 101 with the same sole strict diagnostic: src/native/gmail/body/mime.rs:27:1, clippy::derivable_impls for impl Default for MimeInventory. Formatting passed in both runs. Exact local evidence: .git/google-recovery-verification/current-check.log:4071 and base-check.log:4085; results.json records same_errors_on_clean_base=true. The Gmail file is unchanged by this phase; no new bead is needed. The temporary base worktree was removed. Full-gate failure is pre-existing and does not block closing this phase.

[2026-11-05T22:50:14Z · bob-cli-hg.1--1] Recovered the unlanded shared Google plumbing from 20c60d18 onto base 6e816775, preserved the newer Gmail module, and restored legacy logout account passthrough with two new fake-gog regressions. Monitor 9ny17wp86z9t / ToolRun a50cad16af98007c60567ccbdcccdd21 passed all 28 shared Google unit tests, 193 Calendar unit tests, and 170 integration tests across gcal_auth, gcal_cli, gcal_diagnostics, gcal_lifecycle, gcal_list, and gcal_sync (391 total). Existing Calendar expectations are unchanged, including output/JSON/exit-code compatibility; service-profile failure tests pass. Formatting and git diff --check pass. Full just check fails only for the identical pre-existing Gmail MIME clippy::derivable_impls on clean base 6e816775f0252b6bd68af2900699e6bd537168fb, with exact evidence in the preceding PROPOSED FOLLOW-UP note. Temporary base worktree removed. sase bead epic-symbols bob-cli-hg.1 reported no entries. No memory, docs, CLI, parent, or ancestor changes.

## Dependencies

- **Blocks:** [bob-cli-hg.4](bob-cli-hg.4.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.1.md) | [bob-cli-hg.1](bob-cli-hg.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fe120a1`](https://github.com/bobs-org/bob-cli/commit/fe120a1edc7fc023e6572c46247a647324cb7887) | feat(gmail): extract shared Google plumbing for bob-cli-hg.1 | [bob-cli-hg.1](bob-cli-hg.1.md) | 2026-11-05 17:51:22 EST |
