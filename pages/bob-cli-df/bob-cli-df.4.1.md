# Bead: bob-cli-df.4.1 — Preserve full worktrees across failed-close relaunches

[Bead Pages](../README.md) / [bob-cli-df.4](bob-cli-df.4.md) / bob-cli-df.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.md) · **Assignee:** `bob-cli-df.4.1.land`
**Created:** 2026-10-27 21:39:18 EDT · **Closed:** 2026-10-28 00:36:08 EDT
**Plan:** [202610/preserve\_failed\_close\_worktrees.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/preserve_failed_close_worktrees.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/preserve_failed_close_worktrees.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:40409c9e03e43f92b43cbaf8 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/preserve_failed_close_worktrees.md

<!-- sase:links:end -->

## Description

Failed finalization and subsequent workspace preparation retain recoverable tracked, staged, and untracked work before destructive Git operations, with durable recovery locations in failure evidence.

## Notes

[2026-10-28T03:53:09Z · bob-cli-df.4.1.land] LAND AUDIT / FOLLOW-UP TRIAGE (before remaining-work tale): reviewed all notes on this epic and phases .1-.4, both linked plans, actual source/tests, and commits 42512dc116 (snapshot), 55ebb614f2 (relaunch), 2bb3e813d3 (reset replay), dcb7d2a6e7 (failed-close evidence). Clean external SASE checkout fast-forwarded from daf54c5b2d to origin/master dcb7d2a6e7. The sole non-epic commit since the first epic commit is 067eeeb17b (Footprint facades, core pin, docs, whitelist); no new recovery caller/conflict, but it re-keys Overlay/load_overlay to open sase-1p1.8. No discretionary DECISIONS or memory edits were authorized. FOLLOW-UP DISPOSITIONS: .1 #2/.2 #1/.3 #1/.4 #1 Symvision reports consolidated into a DISCOVERED ISSUE note on active causal epic sase-1p1 and supplementary impact on existing sase-o7; no new task. Overlay/load_overlay part declined as already re-keyed to audited open .8; other_id/custom_id now have production callers but remain exempted, for Footprint to resolve. .1 #3/.3 #2/.4 #1 missing plans sidecar independently reproduced by sase validate on clean dcb7d2a6e7 (only failed stage plan links validate, invalid-root); new large ready bug bob-cli-dg after duplicate and active-epic triage. .4 #1 close_provenance API-change proposal declined as stale-environment evidence: current installed sase-core-rs 0.43.0 bead_close has the tenth close_provenance parameter; the original 0.42.7 failure is not evidence to alter the facade. The tale must provision its isolated test environment and actually execute the previously blocked end-to-end tests. REMAINING EPIC WORK reproduced: delete/modify DU conflict (stages 1 and 3, no stage 2) snapshot succeeds but restore omits unique edited conflict.txt; and a clean parent ignoring sase/repos permits recreate_managed_workspace to delete a dirty linked child after rescue_git_repo returns None. These violate the approved conflict and nested-repository guarantees, so epic and parent df.4 stay open. epic-symbols bob-cli-df.4.1 currently empty. No source changes, full gate, or successful landing claimed.

[2026-10-28T03:57:20Z · bob-cli-df.4.1.land] Remaining-work evidence is file:explicit:40409c9e03e43f92b43cbaf8. Authored one medium tale, Finish failed-close preservation and land bob-cli-df.4.1, for conflict-stage worktree coverage and strict nested-repository preservation before relaunch/reclone/clear removal. Validation with --explain identified missing required title/goal and an inert tale parent_bead field; corrected them and revalidated successfully with zero warnings. The tale explicitly owns this epic close, post-close Symvision, original plan status done, and normal close of parent phase bob-cli-df.4; it must not close df or cv, and must not wait on its own future commit. No source changes or full test pass claimed; submitting through sase plan propose.

[2026-10-28T04:36:08Z · bob-cli-df.4.1.land] Landed the remaining preservation holes on SASE HEAD dcb7d2a6e7 (no later commits; 067eeeb17b remains the sole non-epic commit and does not touch recovery). All four child phases were already closed.

Repairs: `_worktree_entries` now captures live bytes for every index stage (DU stages 1+3, UD, AA). Nested git checkouts under `sase/repos` (and `clear_paths`) are snapshotted before recreate/launch/corrupt-remove/reset-clear; `rescue_git_repo` returning None is not proof. Parent fingerprint skips managed sidecar paths so nested git dirs are not hashed as blobs.

Verification: isolated `.venv` via `just install-venv`, then `just rust-install` from opened `gh:sase-org/sase-core` 0.43.0 (`bead_close` accepts `close_provenance`; `assess_repository_landing_proof` present). Focused suites 84 passed (snapshot, reset_replay, nested_preservation, repo_rescue, reclone). Combined recovery including rescue/, self-heal, plan-archive, and all `test_finalizers_failed_close_recovery*` files: snapshot tests 4/4 passed after adding a dummy origin and typed deferral (action=defer is no longer legal). Relaunch cleanup restores tracked/untracked/staged/binary bytes from the evidence locator; snapshot failure still reopens and refuses cleanup; deferred follow-up does not snapshot or reopen.

`sase tool run check` ba742b7008803cf3b427577388663bd0: fmt/ruff/mypy and other lint stages passed. lint(symvision) 7 KNOWN sase-1p1 / stale sase-1p1.8 whitelist rows (already routed; Overlay/load_overlay re-keyed to closed .8). SASE validation UNKNOWN `plan links validate` invalid-root for missing external `sase/repos/plans`, owned by ready bug bob-cli-dg. No epic-symbol entries for bob-cli-df.4.1. close_provenance facade change remains declined.

[2026-10-28T04:38:17Z · bob-cli-df.4.1.land] Post-close just symvision in the SASE checkout: no unused symbols from this epic. Failures are the already-routed Footprint whitelist rows (sase-1p1 other_id/custom_id already used; sase-1p1.8 Overlay/load_overlay/footprint_* stale because .8 is closed). Owner remains sase-1p1 / sase-o7.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.1.land.md) | [bob-cli-df.4.1](bob-cli-df.4.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.4.1.1--1][1] | Need DECISIONS from parent epic | 1 |
| read-by | [agent:bob-cli-df.4.1.3][2] | Need epic DECISIONS and plan context for phase 4.1.3 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.4.1.3/README.md

<!-- sase:referenced-by:end -->
