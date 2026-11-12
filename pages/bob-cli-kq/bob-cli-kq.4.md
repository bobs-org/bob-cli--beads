# Bead: bob-cli-kq.4 — Durable and race-free vault writes

[Bead Pages](../README.md) / [bob-cli-kq](README.md) / bob-cli-kq.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bo](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bo.md) · **Assignee:** `bob-cli-kq.4` · **Size:** medium
**Created:** 2026-11-12 05:24:40 EST · **Closed:** 2026-11-12 06:08:43 EST
**Plan:** [202611/security\_audit\_fixes\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes_1.md)

## Description

durable-vault-writes: bind bank ensure's write-guard preimage to its single planning snapshot, install clip attachments via hard_link/create_new, fsync the three non-flushing atomic_write variants and the gkeep token write, and verify ownership of the shared-tmp script-cache fallback.

## Notes

[2026-11-12T11:08:11Z · bob-cli-kq.4] PROPOSED FOLLOW-UP: Track the intermittent full-check failure for native::subprocess_runner::tests::raw_run_bounds_pipe_drain_when_detached_grandchild_holds_output in existing bob-cli-kl; it failed once under parallel load and passed on an unchanged isolated rerun.

[2026-11-12T11:08:43Z · bob-cli-kq.4] Implemented the single-snapshot bank guard, no-clobber clip attachment install, fsyncing atomic writes, atomic 0600 gkeep recovery token replacement, and per-uid checked temp-cache fallback. Regression tests for the changed paths passed; formatting and Clippy passed. Full just check had one intermittent subprocess pipe-drain failure tracked by bob-cli-kl, which passed on an isolated unchanged rerun. No epic symbols remain.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kq.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kq.4/README.md) | [bob-cli-kq.4](bob-cli-kq.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1507772`](https://github.com/bobs-org/bob-cli/commit/15077720eefcc714ecec559c62106149648f9a25) | fix(storage): harden vault and cache writes | [bob-cli-kq.4](bob-cli-kq.4.md) | 2026-11-12 06:10:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kq.4][1] | Confirm the recorded follow-up note before closing this phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kq.4/README.md

<!-- sase:referenced-by:end -->
