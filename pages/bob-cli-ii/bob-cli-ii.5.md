# Bead: bob-cli-ii.5 — Route repair, alert-once problems, staleness, and doctor sync

[Bead Pages](../README.md) / [bob-cli-ii](README.md) / bob-cli-ii.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19q.md) · **Assignee:** `bob-cli-ii.5` · **Size:** medium
**Created:** 2026-11-07 17:21:22 EST · **Closed:** 2026-11-08 18:26:21 EST
**Plan:** [202611/gmail\_sync\_reply\_watch.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_reply_watch.md)

## Description

health: refile a gmail_inbox.md row once its routing label resolves, report persisting route problems without failing again, raise a staleness alarm when syncs keep skipping, and add a doctor sync row.

## Notes

[2026-11-08T23:26:08Z · bob-cli-ii.5] PROPOSED FOLLOW-UP: docs-check word budgets for three mac-capture reference pages — capture-panel.md (6088), keyboard.md (6060), and protocol.md (6014) exceed the 6000-word reference/ cap on this tree and on unchanged HEAD copies; json-outputs.md was trimmed in this phase.

[2026-11-08T23:26:21Z · bob-cli-ii.5] Verified: later syncs refile a resolved inbox row through plan_task_move (refiled/would_refile, gmail.refiled, no freshness stamp), persist the same route problem with first_seen false and exit 0, clear leftover unrouted GMAIL ROUTE warnings, and report outside-inbox dest mismatches once as gmail.route_conflict without moving the row. Live runs write XDG_STATE_HOME/bob/gmail/sync-state.json; dry-run writes none; a quiet busy-skip with last_success_at older than 2h exits 1. labels list runs including -l 0. doctor sync is local-only (host, writer pin, last success, open route problems, watching/awaiting) and Warns when last success is stale. cargo fmt --check, just lint, gmail_sync (35) and gmail_shell (62) passed. just docs-check still fails three unchanged mac-capture reference pages over the 6000-word cap (recorded as PROPOSED FOLLOW-UP).

## Dependencies

- **Depends on:** [bob-cli-ii.4](bob-cli-ii.4.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ii.8](bob-cli-ii.8.md) ◐ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.5.md) | [bob-cli-ii.5](bob-cli-ii.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8427bd9`](https://github.com/bobs-org/bob-cli/commit/8427bd96dbab8470c2e4228d8f199265b690ab50) | feat(gmail): refile resolved inbox routes and alarm stale skips | [bob-cli-ii.5](bob-cli-ii.5.md) | 2026-11-08 18:47:14 EST |
