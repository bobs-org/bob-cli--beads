# Bead: bob-cli-c9.4.1.9 — Finish unannotated overwrite - contract fixes and transaction hardening

[Bead Pages](../README.md) / [bob-cli-c9.4.1](bob-cli-c9.4.1.md) / bob-cli-c9.4.1.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.1.land.md) · **Assignee:** `bob-cli-c9.4.1.9.land`
**Created:** 2026-10-26 03:39:12 EDT · **Closed:** 2026-10-26 07:24:39 EDT
**Plan:** [202610/overwrite\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/overwrite_landing_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/overwrite_landing_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/overwrite_landing_fixes.md

<!-- sase:links:end -->

## Description

Close the contract gaps and transaction-safety gaps the bob-cli-c9.4.1 land review found in `bob ref create -f overwrite`, with behavior tests for each, so the interrupted landing of bob-cli-c9.4.1 can resume and close.

## Notes

[2026-10-26T10:39:16Z · bob-cli-c9.4.1.9.land] FOLLOW-UP TRIAGE: Reviewed all three child beads and every note. (1) bob-cli-c9.4.1.9.2 #1, title-route -N report__v2 with a same-stem/missing-Info local PDF, is accepted as remaining epic contract work, not a separate task: pdf_target::plan_local_pdf currently derives the fallback identity title from the -N target stem. The repair tale will fix and regress it. (2) bob-cli-c9.4.1.9.2 #2 and bob-cli-c9.4.1.9.3 #1 are the same unrelated capture_related synthetic-vault timing flake; /sase_new_task search, recent-flake sweep, bob-cli-ca read, and active-epic sweep completed. Added one corroborating +1 to existing ready small flake bob-cli-ca with both proposing bead IDs and the 855 ms observation. No duplicate task created; bob-cli-bo remains closed because it fixed the distinct CLI timing gate. No other PROPOSED FOLLOW-UP notes were present; no proposals discarded without disposition.

[2026-10-26T10:42:28Z · bob-cli-c9.4.1.9.land] LAND REVIEW at 66f9d67f: Audited all 3 phases and every note, linked plan and binding ancestor contracts, and commits 3e9da7cc/43f8aff5/66f9d67f. Reviewed live selection/preflight, output/user-field/audio plumbing, executor, recovery, shared git helpers, vault-sync and rename integrations plus tests. keep_user_fields=keep is implemented in prepare/stamping/article paths; keep_created and legacy_force inherited choices remain unchanged. Fetched origin/master: no base-branch drift. The sole outside commit since the first epic commit is 17f3881c (root:true project grouping), reviewed in pomodoro_homes/facts.rs, resolve.rs and stats/homes.rs; it does not consume or duplicate overwrite and needs no integration change. Current epic-symbols is empty; justfile has no symvision recipe. 61 existing CLI overwrite_ tests pass. A temporary filename-only probe of overwrite_title_change_keeps_old_version_suffix failed with nothing to overwrite for report.pdf plus -N report__v2; source restored after probe. Remaining work prevents closing: (a) source PDF identity incorrectly depends on -N when Info title is absent/rejected; (b) collection final recheck and marker extraction occur after narration but before the post_listen_error guard, so those failures discard completed audio; analogous marker extraction is unguarded in local/article finish paths; (c) dead selector wrappers select_url_member/select_stem_member survive under new allow(dead_code) annotations, contrary to selection-phase delete-or-wire requirement; (d) failpoint fixture has no authored prose, sidecar, replacement audio, title/status/task change, so several apply checkpoints test a no-op and do not prove rollback of those actual mutations. A medium tale will repair only these gaps and perform nested closeout in the same turn as the final code, without waiting for its own commit or CI.

[2026-10-26T10:46:28Z · bob-cli-c9.4.1.9.land] ADDITIONAL REPRO: A temporary probe of tests/cli/highlights/create.rs::highlights_create_collection_overwrites_exact_set_with_listen made the fake listener write the MP3 successfully, log its path, and remove the selected root note using FAKE_LISTEN_REMOVE. The post-listen recheck exited 2 (-N tokio_internals is not a reading ...); stdout had no kept: line and the produced audio no longer existed. The assertion of preserved audio failed. This confirms the collection preservation gap, not just a code-inspection concern. The diagnostic source was restored. The medium repair tale has concrete regressions, actual-write failpoint proof, and complete same-turn closeout through bob-cli-c9.4.1.9 -> bob-cli-c9.4.1 -> phase bob-cli-c9.4, stopping before outer epic bob-cli-c9.

[2026-10-26T11:24:39Z · bob-cli-c9.4.1.9.land] Repair tale complete at 66f9d67f plus working tree: pdf_target file-stem identity with same-stem regression, collection/create/clip post-listen preservation with recheck and marker regressions, dead selector removal with live preflight migration, stronger failpoint fixture with prose/textbundle/audio-swap/title-status-child and unrelated preservation. Decisions unchanged: keep_user_fields=keep, keep_created=yes, legacy_force=no. Gates: fmt clean, clippy clean, docs-gen and docs-check pass, lib 3547 pass with only known bob-cli-ca timing flake synthetic_vault_query_is_under_250ms (fails parallel, passes isolated), cli 2194 pass including 3 new regressions and updated title-suffix test. Drift: origin/master has no new commits beyond 17f3881c already reviewed. Follow-ups: phase .2 note1 fixed here; phase .2 note2 and phase .3 note1 remain tracked by bob-cli-ca, bob-cli-bo stays closed. Epic-symbols empty, symvision recipe absent.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.4.1.9.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.1.9.land.md) | [bob-cli-c9.4.1.9](bob-cli-c9.4.1.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4ee76d1`](https://github.com/bobs-org/bob-cli/commit/4ee76d114ab76a912350cf62bbe2acea29d87fd7) | fix(highlights): repair overwrite identity, narration, selection, and rollback proof | [bob-cli-c9.4.1.9](bob-cli-c9.4.1.9.md) | 2026-10-26 07:27:34 EDT |
