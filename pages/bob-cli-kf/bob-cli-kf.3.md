# Bead: bob-cli-kf.3 — Vault sync and rewrite write durability

[Bead Pages](../README.md) / [bob-cli-kf](README.md) / bob-cli-kf.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bj.md) · **Assignee:** `bob-cli-kf.3` · **Size:** medium
**Created:** 2026-11-11 13:33:44 EST · **Closed:** 2026-11-11 13:53:07 EST
**Plan:** [202611/security\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes.md)

## Description

vault-sync-durability: literal git pathspecs, a pre-restore byte recheck in clobber quarantine, conflict copies before merge aborts, fsync before rename in the atomic-write helpers, and per-file stale rechecks in the rewrite transaction.

## Notes

[2026-11-11T18:53:07Z · bob-cli-kf.3] All 5 durability fixes landed with 4 new regression tests. Verified: 15 targeted lib tests pass (ob, vault_sync, archive), 10 vault_rewrite tests pass, just lint exit 0, cargo fmt clean. Fixes: (1) --literal-pathspecs in ob::git_command + vault_rewrite status; (2) clobber quarantine re-reads live bytes and skips on change; (3) _conflicts/ worktree copies before merge/rebase/cherry-pick aborts; (4) sync_all before rename in atomic_write, restore_head_bytes, write_status_record, plus temp+rename for write_union_merge; (5) per-file stale recheck before each rewrite write.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kf.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kf.3/README.md) | [bob-cli-kf.3](bob-cli-kf.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1f691b1`](https://github.com/bobs-org/bob-cli/commit/1f691b197bb53446bc2c40f30dfaebde7e66aeb9) | fix(sync): harden vault sync and rewrite write durability | [bob-cli-kf.3](bob-cli-kf.3.md) | 2026-11-11 13:54:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kf.3][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-kf.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kf.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kf.land.md

<!-- sase:referenced-by:end -->
