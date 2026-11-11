# Bead: bob-cli-k3.5.1.2 — Rebuild the index inside record transactions

[Bead Pages](../README.md) / [bob-cli-k3.5.1](bob-cli-k3.5.1.md) / bob-cli-k3.5.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-k3.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.5.md) · **Assignee:** `bob-cli-k3.5.1.2` · **Size:** medium
**Created:** 2026-11-11 13:48:49 EST · **Closed:** 2026-11-11 16:12:15 EST
**Plan:** [202611/album\_records\_index.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_records_index.md)

## Description

record-writes: overlay staged record frontmatter on the cached album folder, stage one final album edit with capture and records new/update, preserve preimage guards and preview parity, and keep ordinary tasks lazy.

## Notes

[2026-11-11T21:11:51Z · bob-cli-k3.5.1.2] PROPOSED FOLLOW-UP: 7 vault_sync CLI tests fail identically on the clean base tree (vault_sync_dry_run_reports_task_loss_without_writes, counts_resolved_same_note_and_path_alias_links, detects_whole_note_deletion_from_remaining_links, ignores_task_moves_archives_and_rewritten_hand_renames, drops_pending_loss_when_task_reappears, legacy_same_id_danglers_are_unlinked_not_linked, reports_confirmed_linked_task_loss_once_after_settle_window); environment/git-dependent, unrelated to record-writes

[2026-11-11T21:11:58Z · bob-cli-k3.5.1.2] PROPOSED FOLLOW-UP: just lint fails on clean base with clippy::items_after_test_module in src/native/vault_git.rs:65 (pre-existing, unrelated to record-writes)

[2026-11-11T21:12:02Z · bob-cli-k3.5.1.2] PROPOSED FOLLOW-UP: just docs-check word-budget lint fails on clean base for 8 reference pages including docs/reference/json-outputs.md (6015 words base vs 6000 cap; record-writes adds ~20 contract words); needs a budget or page-split decision by docs owners

[2026-11-11T21:12:15Z · bob-cli-k3.5.1.2] record-writes done: album-write overlay planner (albums/write.rs) renders the index from cached folder + staged postimages; capture stages one final album edit per album with preimage/schema binding and read guards; records new/update plan the album write set before dry-run/mkdir/write with guarded two-file install and album_index JSON; capture JSON/human show album_files. Verified: 29 new tests (7 capture unit incl. laziness counters + stale refusal + rollback hook, 6 write.rs unit incl. two-file drift refusal, 8 records CLI, 8 capture CLI incl. CRLF/parity/batches), full workspace suite green except 7 pre-existing vault_sync failures reproduced identically on clean base (noted as follow-ups); just lint and docs-check budget failures also pre-existing on base (noted). No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-k3.5.1.1](bob-cli-k3.5.1.1.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-k3.5.1.3](bob-cli-k3.5.1.3.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.2/README.md) | [bob-cli-k3.5.1.2](bob-cli-k3.5.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b79ea37`](https://github.com/bobs-org/bob-cli/commit/b79ea376ff57017d460c83b5f08e7f8153860be7) | feat(albums): rebuild the records index inside record transactions | [bob-cli-k3.5.1.2](bob-cli-k3.5.1.2.md) | 2026-11-11 16:13:47 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k3.5.1.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.2/README.md

<!-- sase:referenced-by:end -->
