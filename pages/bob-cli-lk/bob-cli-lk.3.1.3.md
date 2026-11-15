# Bead: bob-cli-lk.3.1.3 — Integrate reply reopening with sync durability and archiving

[Bead Pages](../README.md) / [bob-cli-lk.3.1](bob-cli-lk.3.1.md) / bob-cli-lk.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-lk.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.md) · **Assignee:** `bob-cli-lk.3.1.3` · **Size:** medium
**Created:** 2026-11-14 14:00:56 EST · **Closed:** 2026-11-14 18:47:25 EST
**Plan:** [202611/gmail\_closed\_reply\_reopen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_closed_reply_reopen.md)

## Description

reopen-transaction: wire closed-thread preparation and the local planner into command/file apply, including snapshot revalidation, atomic mail/task/restore edits, marker-last recovery, retry/cursor settlement, and archive suppression with receipt let-go. Exercise the complete live and dry-run path with synthetic fixtures and failure injection. Implement section 3 and its acceptance vectors.

## Notes

[2026-11-14T23:47:25Z · bob-cli-lk.3.1.3--3] Closed by explicit `sase stitch create -B close` after create_commit landed 88fb9cb4 ("fix(gmail): reopen synced messages"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-lk.3.1.3` if more work remains.

## Dependencies

- **Depends on:** [bob-cli-lk.3.1.1](bob-cli-lk.3.1.1.md) ✓ · ⧖ 2026-11-14
- **Depends on:** [bob-cli-lk.3.1.2](bob-cli-lk.3.1.2.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-lk.3.1.4](bob-cli-lk.3.1.4.md) ✓ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lk.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.1.3.md) | [bob-cli-lk.3.1.3](bob-cli-lk.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`88fb9cb`](https://github.com/bobs-org/bob-cli/commit/88fb9cb46f345a6c4a4d1d41a1cbaf6826355742) | fix(gmail): reopen synced messages | [bob-cli-lk.3.1.3](bob-cli-lk.3.1.3.md) | 2026-11-14 18:46:15 EST |
