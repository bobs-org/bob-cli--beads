# Bead: bob-cli-an.6.6.6 — Backlog batch 4: green bob-cli CI, capture flag guard, bob-plugins red tests, and relation-label race

[Bead Pages](../README.md) / [bob-cli-an.6.6](bob-cli-an.6.6.md) / bob-cli-an.6.6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.land`
**Created:** 2026-10-24 05:39:21 EDT · **Closed:** 2026-10-24 07:28:26 EDT
**Plan:** [202610/backlog\_batch4\_ci\_identity\_capture\_flags\_plugin\_tests\_relation\_race.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch4_ci_identity_capture_flags_plugin_tests_relation_race.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch4_ci_identity_capture_flags_plugin_tests_relation_race.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch4_ci_identity_capture_flags_plugin_tests_relation_race.md

<!-- sase:links:end -->

## Description

Close five prioritized task beads. Restore bob-cli master CI so the release train can ship and regressions stop hiding, stop bob capture from silently filing unknown flags as task text, fix bob-plugins' two deterministic test failures including the dangling BLOCKS link they expose, and stop Bob Mac Capture committing a stale relation label. The lander continues the backlog through further epics of at most five phases and five task beads until every project task bead is closed.

## Notes

[2026-10-24T10:43:09Z · bob-cli-an.6.6.6.land] LAND AUDIT / FOLLOW-UP TRIAGE (2026-10-24): Read epic plan and all notes on .1, .2, .3, .4; there are ZERO PROPOSED FOLLOW-UP entries. Reviewed actual commits and source: bob-cli 30f10f15/0afeb2f3, bob-mac-capture 22598dc/8400bd3, bob-plugins e6b2ec2. Fetched every origin/master: no non-epic commit since this epic began, so no unrelated drift requires integration. b5, 6v, 7i independently verified and closed with evidence. Plugin focused suites pass 29/29; full-suite monitor yac9rg630jn6 passed 3529/3529 and phase sync record confirms all 7 plugins, navigation-hotkeys 2.56.1, zero drift. bob-cli CI 40084439229 fully green at 30f10f15; 40085996699 lint/package/Ubuntu pass at 0afeb2f3. Mac 40084777082 runs 2931 tests with only three b7 failures; relation race tests execute and pass, resolving the phase's XCTest availability caveat.

EPIC-CAUSED REMAINDER, keep 8a/al and this epic open: (1) Current capture_flag_guard.rs only understands pure switch clusters or a value-taking first short flag. Compiling this exact source module in a rustc harness confirms -nf json --bogus -- hi returns no GuardHit while -f json --bogus is rejected. The initial executable reproduction used stale target/debug/bob and is NOT current-tree integration evidence; the coder must build via Cargo's actual target_directory and reproduce safely. (2) 22598dc adds Swift relationLabelAuthoredReplacement, violating decisions:mac-capture-is-a-thin-client. Exact production submit+helper extracted into a Swift harness inserts |"see (old)" both while suggestions are pending AND with a fresh typed disabled candidate whose replacement is empty; the nonempty replacement check skips Bob's disabled reason. Real Rust normalization rejects parentheses and >40 characters; current tests incorrectly supply a nonempty replacement on the disabled candidate. Remove local grammar, preserve current-request freshness, and queue a submit until Bob supplies its authoritative replacement or refusal. (3) Mac integrated CI 40086037387 at 8400bd3 has 24 assertions failing: 21 new capture argv assertions across CapturePanelModelTests, CapturePullInChoiceModelTests, CaptureTemplateShelfModelTests still require the guard without positive capability; the other three are b7. Update the integrated tests/fixtures while preserving the positive-capability gate and meaningful negative submission assertions.

External triage via sase_new_task: corroborated existing bob-cli-b7 (+1) with both Mac runs; no new task and no causal active epic (scan receipt work belongs to closed bob-cli-at). A separate observation in bob-cli run 40085996699 is capture::related::draft_related_stays_under_the_debug_perf_gate, 1.712423541s versus 500ms, macOS only. Search all task types + weekly sweep found no owner. DECLINED immediate task creation: this single observation has neither a confirmed reproducible CI failure nor same-tree fail/pass flake evidence, so no supported task type yet; no capture-related runtime/test path changed in this epic. Do not misclassify it as a proved flake or add it to the repair scope without further evidence. Any new reproducible failure in verification must be triaged then.

Audit incident: one diagnostic accidentally used the stale binary without BOB_DIR and inserted the exact inbox task '- [ ] #task --bogus [created::2026-10-24]'. Removed that unique exact line immediately, preserved every other byte, and verified absence. No product source files were changed by the audit. epic-symbols reports no entries; bob-cli has no symvision recipe. Parent bob-cli-an.6.6 is a CLOSED plan, with prior landing notes and a mandatory continuing-backlog contract; closure must recheck parents per the user prompt. Remaining bounded repair will be proposed as a medium tale whose coder performs this epic's closeout and continuation, with no dependency on that coder's own eventual commit/SHA/CI.

[2026-10-24T10:46:03Z · bob-cli-an.6.6.6.land] REPAIR HANDOFF: sase_plan_finish_batch4_capture_guard_and_relation_labels.md is a medium tale, validated with --explain, corrected, and revalidated successfully with zero warnings. It owns only this epic remainder: short-cluster flag-guard scanning, Bob-authoritative relation submission including disabled/normalized responses, and the Mac model test integration for positive capability. Its final step closes 8a/al, retires epic symbols, closes bob-cli-an.6.6.6 normally, runs symvision if available, marks the linked plan done, rechecks concrete parent plans an.6.6 -> an.6 -> an, and preserves the original bounded-backlog continuation. Follow-up triage was completed in the preceding landing note before proposal. No implementation or plan-status edits need committing in this planner turn; the proposal consumes the scratch tale. Do not wait for the tale coder own eventual commit or CI before same-turn closeout.

[2026-10-24T11:28:26Z · bob-cli-an.6.6.6.land] Landing closeout (bob-cli-an.6.6.6.land / finish_batch4 tale, 2026-10-24). All four original phases remain closed with no PROPOSED FOLLOW-UP. b5, 6v, and 7i stay closed from the prior land audit. This tale finished the three audit remainders: (1) capture_flag_guard now walks mixed short clusters through their value-taking option, then rejects unknown alphabetic longs; clap-declaration consistency test added; capture::flag_guard 9/9; isolated vault/inbox/template shelf unchanged; capture_flag_guard=refuse honored. (2) relationLabelAuthoredReplacement removed; pending Return waits for a fresh bob capture-complete typed row (generation + exact authoredLabel); disabledReason consulted even on empty replacement; no Swift quoting. CaptureRelationPanelTests cover delayed/out-of-order/immediate Return/edit-after-Return/dismiss-reopen/repeated Return plus realistic refusals. Thin-client decision honored. (3) Mac model tests omit --require-pull-in-choice without positive pull_in.supported; guard-refusal obtains a capability-bearing no-offer preview then a write-only refusal via FAKE_BOB_CAPTURE_WRITE_STDOUT. Verification: just check green on bob-cli; just portable-check 1555/0 in bob-mac-capture; AppKit scratch typecheck on mac (rsync without .build/.git, bundle.sh --identity '-', just typecheck-tests) PASS BobMacCaptureTests. Known b7 RefsLibraryTests remain preexisting. Follow-up dispositions unchanged: b7 +1 already recorded; capture::related debug-perf overrun in CI 40085996699 still a single observation, not filed. epic-symbols empty; justfile has no symvision recipe. 8a and al closed with the notes above. Post-start integration: this tale's uncommitted source is the remainder; no later unrelated master commits were integrated. Parent bob-cli-an.6.6 is already closed; rechecked and noted. Backlog campaign continues: 132 unresolved at start of this closeout (128 ready, 4 snoozed).

[2026-10-24T11:35:33Z · bob-cli-an.6.6.6.land] CONTINUATION (2026-10-24): fresh enumeration after 8a/al close is 130 unresolved (126 ready, 4 snoozed: 3o, 6q, aa, ah). Successor epic scratch sase_plan_backlog_batch5_highlights_render_pomodoro_name_duplicate_link_mac_ci.md validated with 0 warnings. Owns ba (highlight-quote-heading), 4r (highlight-marker-mirror, after ba), bb (pomodoro-name-reuse), 2l (completed-link-dedupe), b7 (mac-refs-scan-ci). One decision highlight_id_on_quote_fix default remint. Commits: bob-cli 3d62fb54, bob-mac-capture 54131b1, plans status done. Proposing next.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.land.md) | [bob-cli-an.6.6.6](bob-cli-an.6.6.6.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3d62fb5`](https://github.com/bobs-org/bob-cli/commit/3d62fb548fde190cddad0e8d5b2b80a23bde1e0c) | fix(capture): walk mixed short clusters before unknown-flag refusal | [bob-cli-an.6.6.6](bob-cli-an.6.6.6.md) | 2026-10-24 07:33:27 EDT |
| bob-mac-capture | [`bob-mac-capture@54131b1`](https://github.com/bobs-org/bob-mac-capture/commit/54131b189da279d6e5b5b2c21b5b4f0e76400848) | fix(capture): take relation labels from bob and omit ungated pull-in | [bob-cli-an.6.6.6](bob-cli-an.6.6.6.md) | 2026-10-24 07:34:13 EDT |
| bob-cli--plans | [`bob-cli--plans@0a8ca46`](https://github.com/bobs-org/bob-cli--plans/commit/0a8ca4610cc97eacdda6b71b01867d9c78035aca) | chore(plans): mark backlog batch 4 epic plan done | [bob-cli-an.6.6.6](bob-cli-an.6.6.6.md) | 2026-10-24 07:34:52 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.4][1] | epic context | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.4/README.md

<!-- sase:referenced-by:end -->
