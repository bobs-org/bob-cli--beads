# Bead: bob-cli-du.2.1 — Complete relation sources through the shared capture Done path

[Bead Pages](../README.md) / [bob-cli-du.2](bob-cli-du.2.md) / bob-cli-du.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-du.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.2.md) · **Assignee:** `bob-cli-du.2.1.land`
**Created:** 2026-10-28 15:26:10 EDT · **Closed:** 2026-10-28 19:32:45 EDT
**Plan:** [202610/complete\_label\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/complete_label_capture.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/complete_label_capture.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/complete_label_capture.md

<!-- sase:links:end -->

## Description

Finish bob-cli-du.2 by composing complete-label relation commits with existing task completion, atomic capture writes, successor choice, and additive output.

## Notes

[2026-10-28T22:14:19Z · bob-cli-du.2.1.land] LANDING AUDIT / FOLLOW-UP TRIAGE: Read this epic and all four child beads and every note. No separate DECISIONS on the child epic; inherited bob-cli-du.2 decisions remain offer_successors=yes, glossary-only memory authorization reserved for outer rollout, and no decision-record edit. Reviewed implementation commits a32a32fb, 4c55a595, 4be02241, 87b6e608 and production config/verdict, shared Done, close coordinator, relation writer, output/offer traversal, inbox routing, and commit code. The shared Done extraction and additive schema-v1 output are present; closure cannot proceed because capture-acceptance omitted explicitly required cases. All three PROPOSED FOLLOW-UP entries on bob-cli-du.2.1.4 are declined as independent tasks and retained as epic work: #1 recovered inbox-candidate routing and tracking; #2 complete-batch stale-preimage/partial-apply rollback and one-off journal safety; #3 archived/Cancelled targets, ||, same-note composition, and #ref sources. They will be consolidated in one medium corrective tale, not filed as unrelated tasks. Additional static findings to reproduce/fix there: relations_close::source_identity groups by (path, block_id, line), although relation mirror staging can move a stable block between updates; this splits one source and loses grouped labels/effects. relations_complete::complete_target_for_label looks up the first label across all updates, so mixed To/From edges with the same label can report another source target. The acceptance suite also lacks one-item multiple-source numeric probe selection, mixed x! offers, and later-item net-filter assertions explicitly requested by the plan. No new test run has been claimed in this landing audit.

[2026-10-28T22:14:29Z · bob-cli-du.2.1.land] INTEGRATION AUDIT at 1e8e0ecce3201cfc6efa1614c62a289832617661: master and origin/master match. Non-epic commits since a32a32fb (also all commits since epic creation) are 3281de1f capture-related perf ceiling; 9409bfa5 task-theme suggestions/cache and shared task-toggle lookup; e998ee4e project cancellation docs; c6243477 PT13 task-theme preservation contract/tests; fc594281 theme scalar/placement repairs and shared complete/cancel field-preservation regressions; 1e8e0ecc Task Link relation keymap docs. No replacement completion writer or conflicting feature landed. Shared Done already inherits the authored-theme preservation behavior; add a composed relation-completion assertion with an authored theme field in the remaining acceptance work. Keep the keymap additions and outer-epic planned markers. No --epic-symbol entries currently remain for bob-cli-du.2.1, and this checkout has no just symvision recipe. Parent is phase bob-cli-du.2: after successful corrective tale verification, close child epic normally, mark plan:202610/complete_label_capture.md done, then verify/close only bob-cli-du.2. Leave containing epic bob-cli-du to its waiting land agent. All follow-up proposals are accounted for above; no unrelated proposal needs sase_new_task.

[2026-10-28T23:32:45Z · bob-cli-du.2.1.land] Landing tale complete. Prior commits a32a32fb (shared closing-label parser, overlap exclusion, verdicts, production vectors), 4c55a595 (complete_existing_task extraction, additive summaries, shared successor traversal), 4be02241 (staged complete composition, opposite-effect refusal, initial CLI acceptance), 87b6e608 (further acceptance + capture/json-outputs markers) all retained and reused; no second Done writer. Tale fixes: (1) relations_close::source_identity now groups by resolved note path + block ID (line only for idless sources) so same-note mirror staging no longer splits one source; (2) complete/cancel warnings resolve each triggering label within its own source group via group_target_for_label, fixing mixed-direction same-label attribution for both effects with no duplicated lookup. Verification: relations_complete 29/29 pass (20 prior + 9 new: same-note shift grouping, mixed-direction warnings + human dry/real, ref/archived/Cancelled/same-note orders, one-off hide/date/recurrence/new-target/grammar, offer probe-rerun/stable-key/netfilter, inbox routed recovery + keep + guard, bang parity tree/ledger/recovery/offers + exact CRLF + NY-midnight, authored-theme preservation, mixed bang/pomodoro-close/relation offers); relations_cancel green (shared grouping, no cancel regression); capture commit unit tests 7/7 incl. 2 new complete-label batch tests (stale preimage keeps external edit; injected post-replace failure rolls back source/mirror/dependent/day bytes via the commit failure path with clean temp files; failed one-off batch writes no hide journal). Dry-run proof strengthened into capture_json_with (every dry asserts zero creates/writes). Baseline byte-compat vs pre-epic a32a32fb^ (detached worktree, separate build, removed after): no-config and cancel-only human/JSON outputs identical. Drift review: no commits after 1e8e0ecc (HEAD == origin/master at audit); shared Done inherits PT13 authored-theme behavior, asserted for composed closes. All three bob-cli-du.2.1.4 PROPOSED FOLLOW-UPs completed as original-scope work, not separate tasks: (1) inbox routing for complete-label-recovered candidates, (2) stale-preimage/partial-apply rollback + one-off journal safety, (3) archived/Cancelled targets, || labels, same-note composition, #ref sources. just check green (fmt/clippy/full workspace: lib 3855, cli 2403), just docs-check green (447 passed). epic-symbols empty for bob-cli-du.2.1; no symvision recipe in this repo. No memory edits; no CLI/version/CHANGELOG changes.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.2.1.land.md) | [bob-cli-du.2.1](bob-cli-du.2.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d1f445c`](https://github.com/bobs-org/bob-cli/commit/d1f445cafc5b95a1181cf38f5ab7254ed49af872) | feat(capture): land complete-label closeout with edge grouping, scoped warnings, and acceptance | [bob-cli-du.2.1](bob-cli-du.2.1.md) | 2026-10-28 19:35:21 EDT |
| bob-cli--plans | [`bob-cli--plans@042236a`](https://github.com/bobs-org/bob-cli--plans/commit/042236a754219e29c8240ceedba27d3f949ca9e6) | docs(plans): mark complete\_label\_capture\_landing done | [bob-cli-du.2.1](bob-cli-du.2.1.md) | 2026-10-28 19:36:26 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-du.2.1.1][1] | Read parent epic decisions governing this phase | 1 |
| read-by | [agent:bob-cli-du.2.1.2][2] | Need epic DECISIONS | 1 |
| read-by | [agent:bob-cli-du.2.1.4][3] | Need child epic status for acceptance phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.4/README.md

<!-- sase:referenced-by:end -->
