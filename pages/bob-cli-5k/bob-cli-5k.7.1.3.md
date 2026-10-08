# Bead: bob-cli-5k.7.1.3 — Reversible --write path, rollback runbook, and scope caveat

[Bead Pages](../README.md) / [bob-cli-5k.7.1](bob-cli-5k.7.1.md) / bob-cli-5k.7.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-5k.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.7.md) · **Assignee:** `bob-cli-5k.7.1.3` · **Size:** medium
**Created:** 2026-10-07 16:18:00 EDT · **Closed:** 2026-10-07 20:08:03 EDT
**Plan:** [202610/zorg\_ref\_migration.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/zorg_ref_migration.md)

## Description

writer: add `-w/--write`. Under bob_sync.lock it pre-syncs, re-plans, and refuses existing targets. It then writes new files only, verifies them through the index and coverage, and deletes its own files on any failure. Then one scoped commit and a post-sync. Test it against temp git vaults, document the rollback, and update the coverage.scope caveat.

## Notes

[2026-10-08T00:07:45Z · bob-cli-5k.7.1.3] Writer quirk for later phases: cargo test --test cli sometimes reports Finished in <1s without rebuilding after src edits (exotic build.build-dir setup); touch the edited files before test runs to force a rebuild. Verified via strings on build/debug/deps/bob-HASH.

[2026-10-08T00:07:50Z · bob-cli-5k.7.1.3] Writer finding: git revert of the migration commit prunes newly-emptied dirs including a pre-existing-but-empty ref/ itself; on athena ref/ holds real notes so it will survive, but any test vault with an otherwise-empty ref/ needs it recreated before re-running doctor/migrate-zorg.

[2026-10-08T00:08:03Z · bob-cli-5k.7.1.3] Writer done: -w/--write applies the dry-run plan under bob_sync.lock (pre-sync, re-plan, refuse existing targets/dirty ref-zorg, create-new writes, index+coverage verify with self-cleanup, one scoped commit, post-sync). Verified: 4 new unit tests (write/verify round-trip, verify-failure rollback incl dir pruning, TOCTOU no-clobber, commit message), 6 new CLI tests in temp git vaults (offline write+scoped commit, idempotent rerun nothing-to-migrate, dirty-zorg refuse, non-git refuse, blocked-dir write failure byte-identical, bare-remote sync sandwich with push, git-revert rollback + doctor ok), help snapshot + Library one-line assert, new scope_text, docs write flow + rollback runbook + vault-git-sync pointer. Full just check gate green: fmt clean, clippy no new warnings, 1945 lib + 1180 cli + all integration suites 0 failures. No epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-5k.7.1.2](bob-cli-5k.7.1.2.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-5k.7.1.4](bob-cli-5k.7.1.4.md) ◐ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.7.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.7.1.3/README.md) | [bob-cli-5k.7.1.3](bob-cli-5k.7.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`74c2afc`](https://github.com/bobs-org/bob-cli/commit/74c2afc82785b10a7a54a58ab36fb53cb128ee44) | feat(ref-library): add reversible bob ref migrate-zorg --write path | [bob-cli-5k.7.1.3](bob-cli-5k.7.1.3.md) | 2026-10-07 20:09:29 EDT |
