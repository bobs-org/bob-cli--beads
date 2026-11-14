# Bead: bob-cli-lk.3.1.2 — Plan task reopening, restore, and the exact-message log

[Bead Pages](../README.md) / [bob-cli-lk.3.1](bob-cli-lk.3.1.md) / bob-cli-lk.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-lk.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.md) · **Assignee:** `bob-cli-lk.3.1.2` · **Size:** medium
**Created:** 2026-11-14 14:00:56 EST · **Closed:** 2026-11-14 15:59:33 EST
**Plan:** [202611/gmail\_closed\_reply\_reopen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_closed_reply_reopen.md)

## Description

reopen-plan: implement the pure local reopen planner over staged vault snapshots. Share the task-restore row helper, select the newest effective closed linker, restore done/ tasks through plan_task_move, lift awaiting holds, preserve other blockers, resurface Ready rows, and prepend the REOPEN LOG. Return edits, post-restore task identities, and typed permanent/transient outcomes. Implement section 2 and its acceptance vectors.

## Notes

[2026-11-14T20:59:33Z · bob-cli-lk.3.1.2] Implemented the pure local Gmail reply-reopen planner over staged VaultSnapshot overlays. Shared reopen_task_root_line with restore, factored plan_named_log_entry_insertion, added apply_reopen_lift (no mark_unblocked while blockers remain), and bounced on PreparedReopenCandidate. Verified: cargo test --lib native::gmail::sync::reopen_plan (23), capture_schedule_log::tests (22), restore_reopen (1), native::gmail::sync::hold (31), native::gmail::sync::reopen:: (8); cargo fmt --all -- --check; just lint; sase bead epic-symbols empty. Did not close parent epic bob-cli-lk.3.1.

## Dependencies

- **Depends on:** [bob-cli-lk.3.1.1](bob-cli-lk.3.1.1.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-lk.3.1.3](bob-cli-lk.3.1.3.md) ◐ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lk.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.3.1.2/README.md) | [bob-cli-lk.3.1.2](bob-cli-lk.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`78f9bdc`](https://github.com/bobs-org/bob-cli/commit/78f9bdc9acd852162efb0c52cd5b54a3316fb198) | feat(gmail): plan closed-thread reply reopens over vault snapshots | [bob-cli-lk.3.1.2](bob-cli-lk.3.1.2.md) | 2026-11-14 16:01:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lk.3.1.2][1] | Need notes, remaining work, and whether earlier agents left remainder | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.3.1.2/README.md

<!-- sase:referenced-by:end -->
