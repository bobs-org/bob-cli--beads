# Bead: bob-cli-kx.2.1.6 — Archive apply, let-go, and crash reconciliation

[Bead Pages](../README.md) / [bob-cli-kx.2.1](bob-cli-kx.2.1.md) / bob-cli-kx.2.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.md) · **Assignee:** `bob-cli-kx.2.1.6` · **Size:** medium
**Created:** 2026-11-12 11:37:45 EST · **Closed:** 2026-11-12 21:17:59 EST
**Plan:** [202611/gmail\_archive\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_core.md)

## Description

apply: Integrate the archive phase after durable filing/watch application, with fresh per-thread metadata, frozen IDs, ownership release, receipt reconciliation, isolated failures, and authentication aborts. Implement section 6 and its tests.

## Notes

[2026-11-13T02:17:59Z · bob-cli-kx.2.1.6] Implemented live archive apply after filing/watch with fresh per-thread metadata, frozen IDs, receipt create/recovery, per-thread let-go, isolated failures and invalid_grant aborts. Verified: 6 new gmail_archive_apply tests pass, gmail_archive_preview (3), gmail_transport (4), gmail_sync (41) pass, cargo fmt clean, just lint clean, no epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-kx.2.1.5](bob-cli-kx.2.1.5.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kx.2.1.7](bob-cli-kx.2.1.7.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.6/README.md) | [bob-cli-kx.2.1.6](bob-cli-kx.2.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`62ad26d`](https://github.com/bobs-org/bob-cli/commit/62ad26d7472c4ee98153a9ac8a86d661faa5b4f4) | feat(gmail)!: add archive apply, let-go and crash reconciliation | [bob-cli-kx.2.1.6](bob-cli-kx.2.1.6.md) | 2026-11-12 21:21:27 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.6/README.md

<!-- sase:referenced-by:end -->
