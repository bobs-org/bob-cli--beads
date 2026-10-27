# Bead: bob-cli-an.6.6.6.5.6.5.5.6 — Backlog batch 9: quiet EPIPE exits, explicit listen publish manifest state, and three recurring test flakes

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5](bob-cli-an.6.6.6.5.6.5.5.md) / bob-cli-an.6.6.6.5.6.5.5.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.land`
**Created:** 2026-10-25 08:44:09 EDT · **Closed:** 2026-10-25 09:57:47 EDT
**Plan:** [202610/backlog\_batch9\_epipe\_listen\_publish\_refresh\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md

<!-- sase:links:end -->

## Description

Close five existing task beads by making bob exit quietly when its stdout reader closes early, marking explicitly published listen episodes in their source library, and removing the Mac hidden-refresh flake, the capture-related debug perf-gate flake, and the migrate-tasks snapshot race. Continue the bounded backlog campaign until all project task beads are resolved.

## Notes

[2026-10-25T13:30:15Z · bob-cli-an.6.6.6.5.6.5.5.6.land] LANDER VERIFY + TRIAGE (bob-cli-an.6.6.6.5.6.5.5.6.land), part 1.
VERIFIED AND CLOSED: c1 (sase-listen 9d69f50, 129 focused tests rerun), c0 (bob-mac-capture 461f46c; macOS CI 40195734261: 3087/0, target test passed), bo (0e75ca56; 3 loaded --test-threads=64 cli runs 2053/2053 at load avg 7-22), c2 (f255819a; 4x ref_library at 64 threads 132/132). bob-cli CI 40196386071 on 6292c35b passed.
REMAINING EPIC WORK (caused by this epic, bl left open): run_bob's panic hook in src/runner.rs (6292c35b) is silent for EVERY panic. Its non-EPIPE branch is empty, and std::panic::resume_unwind never invokes the restored hook, so an unrelated panic now exits 101 with NO message. Panics in other threads during run_bob_inner are also silenced. Reproduced with a standalone probe of the same take_hook/set_hook/catch_unwind/resume_unwind shape: BOOM panic gives exit 101 and empty stderr. This violates the phase acceptance 'Unrelated panics still print and exit 101'. Phase note #1's claim 'message + 101 preserved' is wrong. The EPIPE path itself is verified: the fixture stats|head -c 10 under pipefail exits 0 with empty stderr, and bogus subcommands still exit 2. The fix goes to a lander-authored tale.
FOLLOW-UP TRIAGE: no phase recorded a PROPOSED FOLLOW-UP. From post-start drift commit 1194779f (docs-only, chop.refresh_docs.bob-cli.2; no integration needed with this epic), two unfixed source follow-ups were routed via /sase_new_task. Neither had a duplicate or a causal active epic: created bob-cli-c3 (bug, small: dedupe_key_for/display_url drop explicit non-default ports, reproduced with the url crate) and bob-cli-c4 (bug, xsmall: capture TEXT help overstates the unknown-flag guard). Not filed: phase .2's local auto-publish mark-failure warning wording. It is an accepted limitation, visible and repairable, and it replaced a pre-epic crash. epic-symbols: none.

[2026-10-25T13:33:24Z · bob-cli-an.6.6.6.5.6.5.5.6.land] LANDER HANDOFF (bob-cli-an.6.6.6.5.6.5.5.6.land), part 2. A second epic-caused defect from 6292c35b: route_help and run_bob_with_args return 0 on a BrokenPipe while printing a clap error, so usage errors exit 0 when the reader is gone. Reproduced: '( sleep 0.3; bob bogus-subcommand 2>&1 ) | true' and 'bob stats --bogus-flag' both gave 0 (normally 2). The remaining work is proposed as tale sase_plan_backlog_batch9_land_epipe_hook_and_closeout.md (size medium). It fixes the hook delegation (defect A) and the usage-error exit code (defect B) with re-exec unit tests and a CLI regression, runs just check, closes bob-cli-bl, closes this epic normally, and checks symvision. It also marks the plan status: done, confirms parent bob-cli-an.6.6.6.5.6.5.5 is already closed, commits via /sase_git_commit, and then carries out the mandatory continuation contract (batch 10 with parent_bead this epic). Unresolved count after the lander's closures: 127 (123 ready, 4 snoozed), 126 once bl closes. Also verified: bob-cli-4k's Mac test passed on 461f46c (fourth consecutive pass).

[2026-10-25T13:57:47Z · bob-cli-an.6.6.6.5.6.5.5.6.land] Lander verified and closed c1 (sase-listen 9d69f50, 129 tests), c0 (bob-mac-capture 461f46c, macOS CI 3087/0), bo (0e75ca56, 3x loaded cli 2053/2053), c2 (f255819a, 4x ref_library 132/132); bob-cli CI 40196386071 on 6292c35b passed. Triage created c3 (port-dedupe) and c4 (capture TEXT help) via /sase_new_task; declined phase-2 auto-publish warning wording as accepted limitation; epic-symbols none. This tale fixed the two epic-caused defects from 6292c35b in src/runner.rs (delegating run_with_quiet_epipe hook; BrokenPipe usage errors keep clap exit_code in route_help, run_bob_with_args, and all native print_clap_error including stats) with 3 re-exec guard unit tests + 2 closed-pipe CLI regressions; lib runner 10/10, epipe CLI 3/3, just check green. Hand checks: stats|head 0 empty stderr, --help|head 0 empty stderr, bogus-subcommand closed pipe 2, stats --bogus-flag closed pipe 2. No symvision recipe (just --list has none), epic-symbols clean.

[2026-10-25T14:03:00Z · bob-cli-an.6.6.6.5.6.5.5.6.land] CONTINUATION: batch 10 epic scratch sase_plan_backlog_batch10_port_help_doctor_mermaid_startpending.md proposes c3 (port-dedupe), c4 (capture help), b8 (ref doctor implement/decline), 9i (pdftotext Mermaid), 4k (StartPending recheck for closeable non-reproduction). Parent_bead bob-cli-an.6.6.6.5.6.5.5.6. Fresh unresolved count 126 (122 ready + 4 snoozed 3o/6q/aa/ah; 126 once bl closed, now closed). Ownership to batch-10 lander on propose.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land.md) | [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f1ab0df`](https://github.com/bobs-org/bob-cli/commit/f1ab0df9d37759b330f628aee343024577b99140) | fix(cli): quiet EPIPE guard keeps usage-error exit 2 and panic output | [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) | 2026-10-25 09:58:47 EDT |
| bob-cli--plans | [`bob-cli--plans@af3b30c`](https://github.com/bobs-org/bob-cli--plans/commit/af3b30c5c2d6b941b95a4f684e4420d2c813db23) | chore(plans): mark batch 9 plan done after EPIPE hook closeout | [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) | 2026-10-25 09:59:38 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.2][1] | parent epic | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land][2] | Landing: check plan-ancestor closure status | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.land][3] | Need the parent link and landing notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land.md

<!-- sase:referenced-by:end -->
