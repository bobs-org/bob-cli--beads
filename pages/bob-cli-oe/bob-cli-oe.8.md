# Bead: bob-cli-oe.8 — Jump pin landing repairs

[Bead Pages](../README.md) / [bob-cli-oe](README.md) / bob-cli-oe.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-oe.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oe.land.md) · **Assignee:** `bob-cli-oe.8.land`
**Created:** 2026-11-20 21:39:28 EST · **Closed:** 2026-11-21 09:53:28 EST
**Plan:** [202611/successor\_jump\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/successor_jump_repairs.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:73581b2443f045fcd5a90e60 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_repairs.md

<!-- sase:links:end -->

## Description

Every Ctrl+J jump pin lands exactly once, on the right task, after every write of the gesture has landed, on all three surfaces. Bob never lands on an unrelated twin, never reports a findable task as lost, never lands before a Task Link strike or an inbox-route move, and never drops the pin on the Mac inbox-route path. A pinned close from a `]s` landing still records its review answer. The card capsule looks the way the design specifies.

## Notes

[2026-11-21T13:03:47Z · bob-cli-oj.2] DISCOVERED ISSUE: on bob-plugins origin/master 9c4b401, scripts/test-navigation-checklist-ctrl-enter.cjs "cycler v6 checklist jump parks the walk then lands on the pin" fails: after a pinned checklist complete, reviewLanding stays the PRE row instead of null. Isolated reproduction on clean HEAD, independent of bob-cli-oj.2 calendar-groups. Assertion at line 952. Phase oe.8.3 is still in_progress.

[2026-11-21T13:34:22Z · bob-cli-oe.8.land] LAND FOLLOW-UP TRIAGE: oe.8.1 #1 and oe.8.2 #2 (vault-format.md 6016/6000) are duplicate bob-cli-oc; +1 recorded. oe.8.2 #1 event-link-times and frees-marks timing failures (also reported in oe.8.3 close note) are duplicates bob-cli-km and bob-cli-io; +1 recorded on each. oe.8.4 #1 macos-ci-check GateTests deadline flakes are new task bob-cli-ok (small, flake), covering the shared subprocess-harness deadline cause across the three named tests; full Python module independently passed 43/43 at 109c30db, files unchanged since before the epic. Searches across all task statuses, the last-week sweep, and all active epic scopes found no duplicate or causal active epic for that harness issue. No proposals declined; no duplicate tasks created. These are outside epic scope. Remaining jump identity/receipt defects found in source/repros are epic work, not follow-up tasks.

[2026-11-21T13:36:35Z · bob-cli-oe.8.land] LAND AUDIT: Reviewed every child scope/note, the repair plan and parent shared semantics/DECISIONS, bob-cli d27041cd, bob-plugins 9c4b401e/767a5970/6debb63b, and Mac 109c30db. Epic note #1 checklist regression is fixed by 767a5970; focused checklist passes. Fifteen focused plugin test files and build:check pass; Mac script tests 43/43 and exact-SHA push CI 44859450606 green. No new Swift or full just check run in this audit. Post-start album grouping e11f2a0c, ledger calendar navGroups 168b665d, and title rendering 1a95b292 do not duplicate/use successor jump landing; no integration changes needed. DECISIONS honored (walk park recorded; no jump glossary strand; repair commits make no memory edits). No epic-symbol entries for oe.8 or oe; no symvision recipe presently available. Remaining epic work confirmed: (1) CLI settling uses stale row.line in final text: after !sase:bar followed by @deps+above with one child note, pinned key deps.md@70339031~2 lands on first Beta at line 3 instead of second at line 4. Installed-binary repro plus exact source inspection; add checkout-built regression. (2) Deferred non-walk Task Link and parked-offer paths use successorJumpTarget=return, suppressing the jump receipt although no follow toast replaces it; direct current-source notice harness confirms. (3) Mac chooseNoPullInOffers and footer retain unpinned-only note-pull guards even with jumpKey set, violating Shift-Return pin commit and pinned footer copy. A single medium tale will repair these and perform this epic and parent-plan closeout normally; do not close yet.

[2026-11-21T14:53:28Z · bob-cli-oe.8.land] Landing repairs for remaining jump-pin gaps, then closeout of this child epic.

Fixes:
1. bob-cli ID-less identity is now captured per planned item (`settle_latest_idless_offer_ordinals` after each planner push) and ordinary ID-less `successor_task_lookup` uses settled ordinals, so a later insertion cannot certify another twin. JS16 covers `-p none -j KEY` of the second Beta (lands line 4) and `-p 1 -j KEY` of the second after the first twin mints an ID (jump left on remaining ID-less Beta at line 4). Fail-closed null landing is unchanged when identity cannot be established.
2. bob-plugins separates deferred `successorJumpTarget: "return"` from receipt ownership. `presentSuccessorModel` strips ↗ only when `successorNoticeTarget === "return"` or `successorJumpReceipt === "follow"`. Task Link closes keep the receipt; walk parked unlinks pass follow without notice-return. Manifests: cycler 1.52.2, block-id-prompt 1.39.2. Deployed via `bob plugins sync --repo` after fast-forwarding to origin/master 38605130; no -F.
3. Mac note-pull-only Shift-Return honors a staged pin: `chooseNoPullInOffers` early-returns only when unpinned; pinned footer copy/a11y take precedence. Unpinned guard preserved.

Verification:
- bob-cli: `cargo test --test cli capture::successor_jump` JS1–JS16 green; `just check` exit 0.
- bob-plugins: `build:check` green; focused successor/unlink/parked/wiring suites 114/114; `docs:inventory:check` green. Full `npm test` failed only the known ledger-tools 25ms budgets (`perf — one build over a 200-link ledger` 38.3ms; `200-link / 2000-task` 218ms), provenance of bob-cli-km / bob-cli-io. `docs:check`/`just docs-check` still only over-budget `plugin-apis.md` 8165/8000 and `vault-format.md` 6016/6000 (bob-cli-oc); task-dependencies.md was not in the lint error.
- Mac: athena `just portable-check` 2633/0 earlier this landing; scratch Mac `bundle.sh` + `just typecheck-tests` PASS on BobMacCaptureTests/InstallHelper/CaptureCore/RefsCore; `Scripts/macos-ci-check` green at https://github.com/bobs-org/bob-mac-capture/actions/runs/44914092810 (snapshot db8d4c59).

Integration drift: post-audit bob-cli still at e11f2a0c (album walk_by) plus uncommitted identity repair; plugins origin gained 38605130 title-block e2e tests (no cycler/block-id overlap); Mac HEAD still 109c30db plus this pin repair. None consume successor jump landing.

Follow-ups: epic note #1 checklist park is already fixed by 767a5970. oc/km/io corroborated earlier; ok remains the macos-ci-check harness flake. oh/oi stay out of scope. No epic-symbols. No nested tale bead. Plan 202611/successor_jump_repairs.md status:done.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oe.8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oe.8.land.md) | [bob-cli-oe.8](bob-cli-oe.8.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`05c1679`](https://github.com/bobs-org/bob-cli/commit/05c1679a0c2377822b27d6915273acd26fa70d0f) | fix(capture): preserve ID-less jump identity across later insertions | [bob-cli-oe.8](bob-cli-oe.8.md) | 2026-11-21 09:55:39 EST |
| bob-mac-capture | [`bob-mac-capture@f112622`](https://github.com/bobs-org/bob-mac-capture/commit/f11262242cd253bf32f07a5a2fa25c94efb0f1fc) | fix(capture): honor pinned Shift-Return on note-pull-only Pull-In | [bob-cli-oe.8](bob-cli-oe.8.md) | 2026-11-21 09:56:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oe.8.2][1] | Check repair epic decisions and prior work notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oe.8.2.md

<!-- sase:referenced-by:end -->
