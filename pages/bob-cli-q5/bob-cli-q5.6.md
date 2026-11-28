# Bead: bob-cli-q5.6 — Alt+Z Snooze Card and Task Card z

[Bead Pages](../README.md) / [bob-cli-q5](README.md) / bob-cli-q5.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fx](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fx.md) · **Assignee:** `bob-cli-q5.6` · **Size:** large
**Created:** 2026-11-25 10:22:53 EST · **Closed:** 2026-11-27 09:16:00 EST
**Plan:** [202611/snoozed\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md)

## Description

snooze-card: the Alt+Z command and Task Card z opening a Snooze Card with ranked time suggestions, a consequence footer, retime/Wake now/Unsnooze on snoozed tasks, teaching refusals for Event and Blocked tasks, and a pure JS planner pinned to the shared vectors.

## Notes

[2026-11-27T13:54:37Z · bob-cli-q5.6.1.land--1] CLOSEOUT STATUS (2026-11-27): implementation source bases: bob-cli eef6cc07 (docs/snooze.md modified) and bob-plugins 56baeb9 (Snooze changes in working tree), with upstream at 852b1c69. Verification: plugin build:check and docs:inventory:check pass; docs:check passes (447 tests, 1 expected skip). Earlier Snooze checks: 43 focused tests, 26 performance checks, and live Obsidian E2E 56 assertions pass; report and all 8 inspected screenshots are attached to bob-cli-q5.6.1 note #3. Broad npm test remains red from existing /tmp ENOSPC self-test fixtures and two timing-sensitive thresholds. This turn just check exits 101 on the known unrelated native::meetings::profile::tests::wispr_summary_renders_one_or_two_pages_with_stable_words kicker-width assertion (bob-cli-q9 triage). symvision is not listed as a Just recipe. Deployment: prior bob-navigation-hotkeys copy is preserved; full dry-run reports 0 copies, 31 unchanged, 1 refusal. bob-ledger-tools 1.172.5 remains protected from workspace 11 at 56baeb9; fetched upstream has no commit with the exact deployed bundle bytes. No force was used. Earlier land triage is recorded and resolved in bob-cli-q5.6.1 note #2. Closeout is pending a decision on the unlanded protected ledger build.

[2026-11-27T14:16:49Z · bob-cli-q5.6.1.land--3] Snooze Card phase closeout record. Source references requested for this work: bob-cli eef6cc07 and bob-plugins 99458bd9. The fresh checks ran in bob-cli checkout 064fc51e and bob-plugins checkout 99458bd9.

Fresh monitored gates: bob-plugins npm run build:check passed (exit 0); npm run docs:inventory:check passed (exit 0); npm run docs:check failed (exit 1), with docs/reference/plugins/bob-ledger-tools.md at 6049 words against the 6000-word cap; bob-cli just check failed (exit 101) because clippy::question_mark is denied at src/native/prose/section_model.rs:922. just --list has no symvision recipe. epic-symbols is empty for both bob-cli-q5.6.1 and bob-cli-q5.6.

Earlier Snooze Card verification remains: 43 focused tests passed, 26 performance checks passed, and live Obsidian acceptance passed all 56 assertions. bob-cli-q5.6.1 note #3 contains the E2E JSON and all eight inspected screenshots (9 attachments total). The broad npm test had known /tmp ENOSPC self-test fixture failures and two timing-sensitive performance-threshold failures.

Deployment: the gate-authorized bob plugins sync -p bob-ledger-tools -F replaced the protected bundle; the subsequent full plugin sync and dry-run reported 0 copies and 34 unchanged managed files. The existing bob-navigation-hotkeys deployment remains current. The earlier land triage is preserved in bob-cli-q5.6.1 note #2 and the preceding phase closeout note is superseded by these fresh results.

[2026-11-27T15:10:11Z · 1h1--3] Task Link Task Card z follow-up (2026-11-27). Implementation remains bob-plugins 07715461 (fix(snooze): open the Snooze Card from a Task Link's Task Card). No bob-cli-q5* bead status was changed.

Real Obsidian E2E: PASS. Monitor h591pne5ng44 exited 0 after 1m8s. Report pass=true with counts.pass=60 and 0 failures. Executable /snap/obsidian/current/app/obsidian. Window 2026-11-27T15:04:57.988Z to 2026-11-27T15:05:42.891Z. BOB_BIN provenance: bob 0.6.0 at workspace target/debug/bob, sha256 17fe1be11960839bb39bd46a6db5e06680a60ff97b57acafbdcb76c182e8fe56, sourceSha 4f55514f, sourcePatch null.

Named assertions: task-card-z-from-live-link-moves-subtree=pass (opened ⏰ Snooze "Task Card live-link task", snoozedRows=["- **1024** [[jobs#^task-card-link]]"]); task-card-z-from-live-link-undo=pass (oneUndoRestoredExactPreimage=true). Full report: /tmp/snooze-from-task-link-e2e-final-20261127/snooze-card-e2e.json 🔒 snooze-card-e2e.json

Earlier gates: focused snooze tests 39/39; npm run build:check and validate passed. npm test left unchanged: (1) canonical vector snooze-add-resnooze-replaces-history still expects struck history deleted while planner/E2E keep it (pre-existing on 99458bd9; 07715461 did not touch the planner); (2) api.taskLinks keystroke-to-rows p95 12.81 ms vs 12 ms, documented bob-cli-io timing noise.

Deploy: bob plugins sync --repo <bob-plugins checkout> --no-pull (no -F). 4 copied, 0 skipped, 30 unchanged, backups in /home/bryan/.local/state/bob-cli/plugin-backups/20261127-100937. Copied bob-navigation-hotkeys/main.js (07715461 Task Link z) plus bob-ledger-tools manifest.json/main.js/styles.css already on HEAD. No overwrite refusals.

## Attachments

- 🔒 snooze-card-e2e.json · application/json · 32.9834 KiB (private attachment)

## Dependencies

- **Depends on:** [bob-cli-q5.5](bob-cli-q5.5.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.9](bob-cli-q5.9.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.6.md) | [bob-cli-q5.6](bob-cli-q5.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.6.1.land][1] | Need the parent phase scope for the landing tale closeout | 1 |
| read-by | [agent:bob-cli-q5.6.1.land--1][1] | Verify the newly attached acceptance evidence and closeout state | 2 |
| read-by | [agent:bob-cli-q5.6.1.land--3][1] | Final status: verify phase is closed with complete fresh results and source/deployment record | 3 |
| read-by | [agent:bob-cli-r7.land][2] | Check notes for resnooze vector failure | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.6.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r7.land.md

<!-- sase:referenced-by:end -->
