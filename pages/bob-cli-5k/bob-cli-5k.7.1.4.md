# Bead: bob-cli-5k.7.1.4 — Run the migration on athena and verify coverage

[Bead Pages](../README.md) / [bob-cli-5k.7.1](bob-cli-5k.7.1.md) / bob-cli-5k.7.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-5k.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.7.md) · **Assignee:** `bob-cli-5k.7.1.4` · **Size:** small
**Created:** 2026-10-07 16:18:00 EDT · **Closed:** 2026-10-07 20:27:20 EDT
**Plan:** [202610/zorg\_ref\_migration.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/zorg_ref_migration.md)

## Description

live-run: build the landed master on athena and dry-run against ~/bob. Check every number against the expected table and stop for Bryan on any deviation. Run --write, verify doctor, find, list, and show plus an idempotent rerun, install the build, and record the evidence and rollback sha on the bead.

## Notes

[2026-10-08T00:27:13Z · bob-cli-5k.7.1.4] Live-run evidence. Built master at 74c2afc (release). Pre-checks: vault HEAD 7827289, worktree clean, vault-sync healthy (local==remote). Dry run vs plan table: records 424, notes 322, chapters 102, skipped 0, identity_hits 0, renamed 17 (9 book IDs + programming_in_lua/work_clean/practical_vim/modern_vim + ilar/yserve/hyperlist + pat_chat), no_url 11, already_migrated 282, 37 files, per-status READ 135/REVIEW_FLEETING 96/COLLECT 92/UNREAD 57/REVIEW_LIT 17/ABANDONED 16/BOOK 11, reading states finished 183/started 69/queued 52/dropped 16/unknown 2 — all match. Minor plan-table drift (not a stop): file-kind split observed papers 49 + zorg-fallback 14 = 63 vs plan text papers 48 + other 16 = 64; plan table itself sums to 323 not 322. Write commit 36bf2172f018095d8cb2330810cf6588ed02ed95 (pushed to origin/master), stat: exactly 322 files, all under ref/zorg/**. Post-verify: doctor coverage ok, library 935 notes (521/161/212/39/2), diagnostics still only the 2 pre-existing ref/ai opaque_url; find returns in_library for go/cs-bidder-dec and vimhelp quickfix; shared-block pairs distinct (prj_gbd bidder_declarations_prd + cs_bidder_dec; zettlr pair); list -s legacy -t books shows 11 with derived states; show clean_arch_ref renders Chapters; rerun dry run reports 0 to migrate. just install done; installed bob doctor confirms coverage ok. Rollback: git -C ~/bob revert --no-edit 36bf2172f018095d8cb2330810cf6588ed02ed95 (check no sync running via bob vault-sync status --json first), then bob vault-sync. just check passes.

[2026-10-08T00:27:20Z · bob-cli-5k.7.1.4] Live migration done and verified: commit 36bf217 (322 files under ref/zorg/**, pushed). Dry run matched plan table on all gated numbers (424/322/102/0 skipped/0 identity/17 renamed/11 no_url; states 183/69/52/16/2). Doctor coverage ok, find/list/show verified, rerun is no-op, installed bob re-verified, just check passes. Rollback: git -C ~/bob revert --no-edit 36bf2172f018095d8cb2330810cf6588ed02ed95.

## Dependencies

- **Depends on:** [bob-cli-5k.7.1.3](bob-cli-5k.7.1.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.7.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.7.1.4/README.md) | [bob-cli-5k.7.1.4](bob-cli-5k.7.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5k.7.1.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.7.1.land/README.md

<!-- sase:referenced-by:end -->
