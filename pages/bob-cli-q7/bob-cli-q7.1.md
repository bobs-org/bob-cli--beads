# Bead: bob-cli-q7.1 — bob-cli: claim, resolve, and refuse the bare caret address

[Bead Pages](../README.md) / [bob-cli-q7](README.md) / bob-cli-q7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g6.md) · **Assignee:** `bob-cli-q7.1` · **Size:** medium
**Created:** 2026-11-25 15:25:24 EST · **Closed:** 2026-11-25 17:11:12 EST
**Plan:** [202611/caret\_address\_goto\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/caret_address_goto_capture.md)

## Description

cli-goto: add the shared whole-draft caret-address claim, the read-only resolver (exact hit, duplicates, archive hop, did-you-mean), the capture-parse task_goto mode and goto payload, the bob capture refusal, grammar +1, docs, and tests.

## Notes

[2026-11-25T21:29:54Z · bob-cli-q7.1] Timing on athena vs ~/bob (debug bob, median of 7 after 2 warmup): found @bob^intention-rollovers 30.4ms landing bob.md:78; worst-case miss @bob^zzzz-not-a-real-id-xyz 43.8ms; archive found @bob^use-list-for-reflections 65.2ms at done/bob_done.md:2165; missing note 20.9ms. Vault git status porcelain empty before and after.

[2026-11-25T21:29:59Z · bob-cli-q7.1] PROPOSED FOLLOW-UP: docs word-budget lint already over on master for capture-syntax.md and json-outputs.md (also plugin-apis.md, bob-ledger-tools.md, bob-navigation-hotkeys.md). This phase added a compact Go To subsection; just docs-check still fails those pre-existing over-budget files.

[2026-11-25T22:09:33Z · bob-cli-q7.1--1] PROPOSED FOLLOW-UP: just check is red on clean master (reproduced at e6eb52a1; origin d67a5b7b/68dee6e1/dfc7facb do not touch these tests): lib three_component_marker_keeps_route_and_task_contexts (#"REQUIREMENTS" vs #requirements after 8a1d16a6 catalog spellings), task_drawers_and_project_h2_drawers_resolve_for_merge (create path missing **REQUIREMENTS**), wispr_summary_renders_one_or_two_pages_with_stable_words (pdftotext kicker letter-spaced); CLI drawers_complete_after_id_hash, inbox_route open.block_id null, note_pull/project_note_offer/task_theme_writes/task_status_hooks fixture drift from Tasks-section chips. Same failures on this phase tree — close anyway.

[2026-11-25T22:11:12Z · bob-cli-q7.1--1] Closed by explicit `sase stitch create -B close` after create_commit landed 4d930129 ("feat(capture): treat whole-draft @route^id as read-only Go To"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-q7.1` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-q7.2](bob-cli-q7.2.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q7.4](bob-cli-q7.4.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q7.1.md) | [bob-cli-q7.1](bob-cli-q7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4d93012`](https://github.com/bobs-org/bob-cli/commit/4d93012907c8d8048e2a6498450f4a803763c66a) | feat(capture): treat whole-draft @route^id as read-only Go To | [bob-cli-q7.1](bob-cli-q7.1.md) | 2026-11-25 17:10:47 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q7.1--1][1] | Need the phase scope, design file, and notes after just check failed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q7.1.md

<!-- sase:referenced-by:end -->
