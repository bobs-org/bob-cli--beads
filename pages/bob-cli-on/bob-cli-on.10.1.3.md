# Bead: bob-cli-on.10.1.3 — Cycler requirement guards, Alt+\[ drop, and Alt+\] restore

[Bead Pages](../README.md) / [bob-cli-on.10.1](bob-cli-on.10.1.md) / bob-cli-on.10.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.md) · **Assignee:** `bob-cli-on.10.1.3` · **Size:** medium
**Created:** 2026-11-21 14:10:17 EST · **Closed:** 2026-11-21 19:41:28 EST
**Plan:** [202611/obsidian\_req\_gestures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_gestures.md)

## Description

cycler-guards-and-drop: add the req-line guard beside the bank-row guard and consult it at every cycler task gesture, link-target, transclusion, and status-writer site with the contract copy, then implement Alt+[ drop (reason prompt plus nav Log Recall) and Alt+] restore through the RW twin as one undo step each.

## Notes

[2026-11-22T00:41:08Z · bob-cli-on.10.1.3] PROPOSED FOLLOW-UP: docs:check has 3 pre-existing failures on clean base (test_current_registry_and_generated_nav_are_complete_and_unique, test_llmstxt_contracts_section_lists_exactly_registry_stems, test_readme_table_matches_original_contract_index_snapshot) — same 3 fail on clean worktree at 235c7db

[2026-11-22T00:41:15Z · bob-cli-on.10.1.3] PROPOSED FOLLOW-UP: test-ledger-tools-frees-marks perf budget (25ms, took 71ms under full test:unit load) is flaky — passes in isolation; unrelated to cycler req guards

[2026-11-22T00:41:20Z · bob-cli-on.10.1.3] PROPOSED FOLLOW-UP: bob plugins sync -p task-status-cycler refused by workspace-13 deploy (726f9a5 still running) — do not force; land agent should sync after sibling lands

[2026-11-22T00:41:28Z · bob-cli-on.10.1.3] Implemented 193 req-line guard + drop/restore (Alt+[ modal with Log Recall, Alt+] restore) and wired all cycler sites net-zero (160 stays 989, 180 stays 999). Verified: npm run build passes, build:check passes, docs inventory up to date, 19 new req-guard/drop tests pass, existing bank-guard/req-vectors/twin-copies/pomodoro-reopen/prose-roles pass. docs:check 3 failures pre-existing on clean base; 1 perf flake passes in isolation; sync blocked by running workspace-13 agent (no -F).

## Dependencies

- **Depends on:** [bob-cli-on.10.1.2](bob-cli-on.10.1.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.10.1.4](bob-cli-on.10.1.4.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.10.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.3/README.md) | [bob-cli-on.10.1.3](bob-cli-on.10.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@28d76fd`](https://github.com/bobs-org/bob-plugins/commit/28d76fdad7cb1a71eb6fde7a1ebcee9b8555ab0f) | feat(task-status-cycler): guard requirement lines, add Alt+\[ drop and Alt+\] restore | [bob-cli-on.10.1.3](bob-cli-on.10.1.3.md) | 2026-11-21 19:44:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.10.1.3][1] | Need to confirm close readiness and remaining notes | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.3/README.md

<!-- sase:referenced-by:end -->
