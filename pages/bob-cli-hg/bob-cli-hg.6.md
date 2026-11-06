# Bead: bob-cli-hg.6 — bob gmail save and list

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.6` · **Size:** large
**Created:** 2026-11-05 12:37:49 EST · **Closed:** 2026-11-06 06:58:56 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

gmail-save: resolve URL/ID/note inputs to a confirmed thread, fetch it, write or refresh the mail note with inline images under the vault lock, honor headers mode, never_save, and the writer host, commit, journal, and list saved threads offline.

## Notes

[2026-11-06T04:45:57Z · bob-cli-hg.6] Planning audit: no prior phase notes or completed save/list implementation; shell, ids, body renderer, and note engine are landed. Validated four-medium-phase child epic proposal sase_plan_gmail_save_list.md: resolve-policy -> prepare-content -> save-transaction -> list-diagnostics, with its land agent to verify and close only hg.6. Upstream gog v0.44.0 inspection confirms attachment --inline writes a cache; proposal uses its narrowly allowlisted, readonly Discovery attachments.get with --no-cache to preserve the approved no-body-cache and dry-run contracts. No SASE memory edits or implementation changes. epic-symbols currently reports no entries.

[2026-11-06T10:27:25Z · bob-cli-hg.6.1.land] Nested landing audit found four reproducible remaining issues in child hg.6.1: commit-retry image provenance/counts, orphan image writes on unchanged append-only refresh, case-inconsistent account matching, and absent structural preview diff. hg.6.1 records complete child review and all seven follow-up dispositions. A validated medium repair tale will fix these, add transaction acceptance and root-help integration, and then close hg.6.1 and this phase normally in the coding turn. Both remain open; outer hg is not to be closed by the tale.

[2026-11-06T12:00:10Z · bob-cli-hg.6.1.land--1] Save/list phase closeout evidence: bob-cli-hg.6.1, the sole child epic, is closed done, and child phases .6.1.1 through .6.1.4 are all closed. Verified the parent relation and the full phase contract: resolve chosen Gmail URLs/IDs/note inputs to confirmed threads; enforce never_save, headers, and writer policy; prepare MIME and inline image imports without writes; save/refresh append-only mail notes under the vault lock with safe images, scoped commit, and journals; and list saved threads offline with diagnostics. Dependencies bob-cli-hg.4, .2, and .5 are closed. Preserved decisions are full bodies by default, subject-and-who link labels, and no memory edits in this phase. Gmail shell passed 30/30, docs-gen passed, and root-help snapshots match. just check has only the two unchanged clipboard catalog/completion failures (5,371 passed, 2 ignored); docs-check has only the known bob-cli-hs README contract-table digest failure (446 passed, 1 skipped). The child close note records all seven original follow-up dispositions. Outer epic bob-cli-hg remains open.

## Dependencies

- **Blocks:** [bob-cli-hg.12](bob-cli-hg.12.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.14](bob-cli-hg.14.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.2](bob-cli-hg.2.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.4](bob-cli-hg.4.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.5](bob-cli-hg.5.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.7](bob-cli-hg.7.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.9](bob-cli-hg.9.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.md) | [bob-cli-hg.6](bob-cli-hg.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.6.1.land--1][1] | Verify the child and parent closure records and confirm the outer Gmail epic remains open | 3 |
| read-by | [agent:research.5s.mus][2] | gmail user guide research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.mus/README.md

<!-- sase:referenced-by:end -->
