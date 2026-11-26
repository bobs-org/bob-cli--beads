# Bead: bob-cli-ph.3 — Every host reads bold drawers before any writer flips

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.3` · **Size:** small
**Created:** 2026-11-22 17:36:48 EST · **Closed:** 2026-11-25 06:48:30 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | [bead:bob-cli-qg][1] | Proposing phase; built bob-host-currency probes because --version cannot show master builds |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-qg/README.md

<!-- sase:links:end -->

## Description

reader-rollout: a host-currency script plus a gated check that bob on athena, apollo, and the Mac and the vault's deployed plugins all read bold drawers.

## Notes

[2026-11-23T23:49:39Z · bob-cli-ph.3] Reader-rollout implementation: added executable scripts/dev/bob-host-currency and wired it into just check-scripts. Final just check-scripts passed (exit 0). The gate checked drawer-contract commits 37b2080e and c25d92fd plus bob-task-drawer-dual-read-v1 in task-status-cycler, block-id-prompt, bob-ledger-tools, and bob-navigation-hotkeys. All four markers were present on athena, apollo, and mac; all hosts reported bob 0.6.0, but no v* release tag contains both commits, so the reader gate remains held for the release train.

[2026-11-24T12:03:32Z · bob-cli-ph.3] ROLLOUT RECHECK 2026-11-24: Earlier implementation is landed in fd99ebb85dcf0555cc48570397c419f4dd8f3167; no rewrite needed. Fresh git fetch origin --tags still has v0.6.0 as newest and no release containing both 37b2080e and c25d92fd. Re-ran scripts/dev/bob-host-currency with bob-task-drawer-dual-read-v1 required for task-status-cycler, block-id-prompt, bob-ledger-tools, and bob-navigation-hotkeys: all three hosts reachable; all 12 plugin rows current; athena/apollo/mac each installed 0.6.0 and all three release rows behind (exit 1). epic-symbols reports none. Remaining work is the external rollout gate, small enough for one follow-up: monitor the release train for at most 36h, propose any host updates via sase_gate per plan section 9, rerun and artifact the passing table, then close only this phase. No memory or writer changes authorized here.

[2026-11-24T12:04:33Z · bob-cli-ph.3] PROPOSED FOLLOW-UP: macOS property tests block the reader release train — latest scheduled release run https://github.com/bobs-org/bob-cli/actions/runs/45277877777 at 588c62102181d75920f5826b3c3c25b170e11bf1 failed only ci / test (macos-latest), job 138054384600; release and binaries were skipped. CLI suite: 4069 passed, 4 failed. props::absolute_note_with_relative_bob_dir_stays_confined reports prop_traversal for a /var/folders/.../notes/groceries.md path; props::lock_wait_preserves_formatting_only_frontmatter_edit, props::lock_wait_schema_change_owns_a_previously_loose_field, and props::lock_wait_semantic_edit_is_stale fail at tests/cli/props.rs:767 because the child never opened vault.lock. Linux tests, lint, and package passed on this SHA. Exact-node bead searches and task search for props found no matching report. Land agent should route this to the property-editor epic bob-cli-pf; these are not drawer-rollout implementation failures. No out-of-scope repair or release bypass attempted.

[2026-11-24T12:08:29Z · bob-cli-ph.3] VERIFIED 2026-11-24: Re-ran just check-scripts against unchanged landed source 8d82c621; exit 0. Includes all shell checks, Highlights self-test 13/13, macOS CI helper tests 43/43, and installer UI tests 152/152. The only remaining acceptance item is the release/host currency gate, not implementation or local verification. Staged zero-weight monitor eh82bkngbp55 (36h maximum) polling release tags for ancestry of both 37b2080e and c25d92fd, with an automatic continuation to perform gated host updates if needed, artifact the passing table, check epic-symbols again, and close only bob-cli-ph.3. Phase intentionally remains in_progress until that actual gate passes; no parent or phase status was changed.

[2026-11-24T16:11:37Z · fy--1] RELEASE-UNBLOCK PROGRESS 2026-11-24: The planned props alias-containment fix and portable inode-based lock probe are implemented but intentionally uncommitted pending real macOS verification. The new alias regression fails with prop_traversal against the original resolver; all 20 props tests pass with the fix, and the full standard check passed (ToolRun e195005ce684ec410e416a4184112e05). The precommit helper exited 2 after its filtered gh run list query returned no match, but unfiltered listing and direct run view recovered https://github.com/bobs-org/bob-cli/actions/runs/45432444592 for exact snapshot 452cf2cf60dd1c40dc2f3bb4baaf4e2fa62a956e on ci/precommit/d6cfb3226fae8d6ed3740f4b2a41c708. Current worktree matches that snapshot byte-for-byte; the temporary remote branch was deleted by helper cleanup. Continuing to watch that existing run and apply the original macOS step gate plus explicit CLI zero-failure checks. This snapshot is not a landed fix SHA. No bead status or reader-rollout monitor was changed; a final evidence note will follow only after landed master CI passes.

[2026-11-24T17:55:34Z · bob-cli-ph.3] ROLLOUT RECHECK 2026-11-24 17:55Z: earlier monitor eh82bkngbp55 no longer exists (no monitor for this phase in sase monitor list --all), so re-staged the release watch as monitor yze12k21fh57 (36h max, weight 0, polls v* tags every 10m for ancestry of 37b2080e and c25d92fd; follow-up does gated host updates, artifacts the passing table, rechecks epic-symbols, closes only this phase). Fresh bob-host-currency run: all 12 plugin rows current on athena/apollo/mac; all three release rows behind at installed 0.6.0 because v0.6.0 is still the newest tag. The props macOS fix that failed the train landed as fb946f9c; master CI for b832e58d was queued. epic-symbols: none. No source changes this turn.

[2026-11-24T20:47:19Z · fy--7] PROPS RELEASE BLOCKER RESOLVED — verified 2026-11-24 20:46 UTC.

ORIGINAL_FIX_SHA=fb946f9c5bd4d195a1221a17f1e97fe09f8ac1d3
LANDED_CORRECTIVE_SHA=3deee354ad8cf4a7cfd600a12af0501e8de5153f
MASTER_CI_URL=https://github.com/bobs-org/bob-cli/actions/runs/45464312427
MASTER_CI_ATTEMPT=4
MACOS_JOB_ID=138738982663

The alias-containment fix and portable inode-based lock probe are landed. The corrective commit (fix(props): satisfy settings contract lint gates) removes inherited deterministic lint failures without behavior changes. Monitor s46r0h44daas exited 0 at 2026-11-24T20:44:19Z after recovering newer-push cancellations of this same run. It verified exact ci.yml/master/push identity, original-fix and origin/master ancestry, the corrective subject and two changed paths, corrective-patch application to the landed parent reproducing the landed tree, and the full original patch reverse/apply round-trip. This is the actual landed corrective SHA, not a scratch snapshot or unrelated newer master run.

Fresh GitHub metadata confirms workflow success on attempt 4; lint (138738985383), package (138738987482), Ubuntu (138739053628), and macOS (138738982663) all succeeded. Every macOS step passed except the expected skipped Linux-only Install full-test tools. Inspected the complete successful macOS job log: tests/cli/main.rs reports 4081 passed; 0 failed; 0 ignored. All 27 props tests passed, including props::absolute_note_with_relative_bob_dir_stays_confined, props::absolute_note_and_vault_accept_symlink_aliases_but_stay_confined, props::lock_wait_preserves_formatting_only_frontmatter_edit, props::lock_wait_schema_change_owns_a_previously_loose_field, and props::lock_wait_semantic_edit_is_stale. The path-traversal and symlink-escape refusal tests also passed. Original master run 45452592310 at fb946f9c failed inherited lints and is not claimed green.

The props release blocker is resolved; the scheduled train publishes after its own exact-SHA release gate. Reader rollout remains pending the existing qualifying-release/host-currency gate. No bead status changed or closed; neither reader monitor eh82bkngbp55 nor replacement yze12k21fh57 was touched or re-armed. No version/changelog edit, manual release dispatch, or override was used.

Timing checked at 2026-11-24 20:46 UTC: tomorrow's 08:17 and 10:47 UTC scheduled slots and the plan's observed 16:00–22:15 UTC delayed starts fit before the original 2026-11-26 00:05 UTC expiry. Note #6 additionally records the reader agent's replacement watch staged at 2026-11-24 17:55 UTC with a 36h cap (approximately 2026-11-26 05:55 UTC). No re-arm is indicated by this timing check.

The broader PROPOSED FOLLOW-UP/land-agent deadlock and permanent CI run-discovery helper repair remain out of scope.

[2026-11-25T11:14:06Z · bob-cli-ph.3] ROLLOUT RECHECK 2026-11-25 11:10Z: Implementation remains landed (scripts/dev/bob-host-currency wired into just check-scripts; bash -n clean). Fresh git fetch origin --tags: newest tag still v0.6.0; neither 37b2080e nor c25d92fd is in any v* tag. Re-ran bob-host-currency with bob-task-drawer-dual-read-v1 on task-status-cycler, block-id-prompt, bob-ledger-tools, and bob-navigation-hotkeys: athena, apollo, and mac all reachable; all 12 plugin rows current; all three release rows behind at installed 0.6.0 (exit 1). Latest Release run https://github.com/bobs-org/bob-cli/actions/runs/45485415920 at 2b3817fee2c1cb43f02600ece3f52ba9147c6eaa failed after release-plz computed v0.7.0 because git push HEAD:master was rejected non-fast-forward. Today's 08:17 and 10:47 UTC scheduled slots had not appeared by this check. epic-symbols: none. No source changes. Restaging the 36h release watch (replaces gone monitors eh82bkngbp55 and yze12k21fh57).

[2026-11-25T11:14:15Z · bob-cli-ph.3] PROPOSED FOLLOW-UP: HEAD meet_route tests block the reader release train — master CI https://github.com/bobs-org/bob-cli/actions/runs/45570644593 at bcf0566ba90212b9198d38c69da96a00cba9ce78 failed test (ubuntu-latest) 139056143256 and test (macos-latest) 139056143403; lint and package passed. lib tests: 15 failed, all native::highlights_ref::create::meet_route (panic at meet_route.rs:632 file meeting, and overwrite_without_existing_files_as_new at :643 write meeting). CLI suite on the same jobs was green. Last green master CI https://github.com/bobs-org/bob-cli/actions/runs/45499067959 at 15fd03b24c40308ed63bceeff26d4f65e2313c28. These are bob-cli-pw meeting-notes filing tests, not drawer-rollout implementation failures. Closed phases bob-cli-pw.5.1.2–.5.1.4 own meet_route.rs; open epic bob-cli-pw.8 is Mac meeting-notes, not this panic. No out-of-scope repair or release bypass attempted.

[2026-11-25T11:47:59Z · bob-cli-ph.3] READER GATE PASSED 2026-11-25T11:37Z without a release, per the launch prompt ("you should NOT need to wait for a rele

… and 3300 more characters

## Dependencies

- **Depends on:** [bob-cli-ph.1](bob-cli-ph.1.md) ✓ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.2](bob-cli-ph.2.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.4](bob-cli-ph.4.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.3/README.md) | [bob-cli-ph.3](bob-cli-ph.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fd99ebb`](https://github.com/bobs-org/bob-cli/commit/fd99ebb85dcf0555cc48570397c419f4dd8f3167) | chore: add Bob host reader currency gate | [bob-cli-ph.3](bob-cli-ph.3.md) | 2026-11-23 18:51:04 EST |
| bob-cli | [`5ab392a`](https://github.com/bobs-org/bob-cli/commit/5ab392a1ba087c6f87d8685035979498082079ed) | chore(dev): let bob-host-currency gate on a bold-drawer read probe | [bob-cli-ph.3](bob-cli-ph.3.md) | 2026-11-25 06:49:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.3][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-ph.land][2] | Need the child scope and notes | 1 |
| read-by | [agent:fy--5][3] | Inspect existing rollout evidence before final props unblock note | 1 |
| read-by | [agent:g1][4] | Understand the release gate blocking the epic | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.fy.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md

<!-- sase:referenced-by:end -->
