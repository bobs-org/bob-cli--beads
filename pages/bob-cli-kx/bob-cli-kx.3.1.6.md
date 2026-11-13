# Bead: bob-cli-kx.3.1.6 — Show closed-task chips and the morning archive notice

[Bead Pages](../README.md) / [bob-cli-kx.3.1](bob-cli-kx.3.1.md) / bob-cli-kx.3.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.md) · **Assignee:** `bob-cli-kx.3.1.6` · **Size:** medium
**Created:** 2026-11-13 08:02:47 EST · **Closed:** 2026-11-13 13:55:30 EST
**Plan:** [202611/gmail\_archive\_receipts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_receipts.md)

## Description

ledger_receipts: add display-only archive chips in Live Preview and Reading view and one morning recent_archive notice through Ledger Tools, with cached CLI data and plugin deployment.

## Notes

[2026-11-13T17:56:46Z · bob-cli-kx.3.1.6] PROPOSED FOLLOW-UP: Clear the remaining docs-budget and timing-flake failures — clean-base docs:check flags bob-ledger-tools at 6,136/6,000 (tracked by bob-cli-il) and navigation-hotkeys at 6,055/6,000 (prior cleanup bob-cli-jz); unrelated full-suite timing assertions pass alone and are tracked by bob-cli-io, bob-cli-km, and bob-cli-ej.

[2026-11-13T18:55:30Z · bob-cli-kx.3.1.6--3] Deployed the landed Ledger Tools build from a clean upstream tree, restored and rebuilt the archive-receipt phase, synced bob-ledger-tools without force, and verified all 11 plugins report synced; epic-symbol check returned no entries.

## Dependencies

- **Depends on:** [bob-cli-kx.3.1.5](bob-cli-kx.3.1.5.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.3.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.1.6.md) | [bob-cli-kx.3.1.6](bob-cli-kx.3.1.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`01ab076`](https://github.com/bobs-org/bob-cli/commit/01ab0767f85ab3fa3ef2467b505e2ce4f676234b) | docs(gmail): document archive receipt UI | [bob-cli-kx.3.1.6](bob-cli-kx.3.1.6.md) | 2026-11-13 13:58:36 EST |
| bob-plugins | [`bob-plugins@e102fe2`](https://github.com/bobs-org/bob-plugins/commit/e102fe2dba808bdcf5c8ba307eee8d94204e1ace) | feat(plugins): render Gmail archive receipts | [bob-cli-kx.3.1.6](bob-cli-kx.3.1.6.md) | 2026-11-13 13:59:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.3.1.6--3][1] | Verify that only the assigned phase closed after deployment | 2 |
| read-by | [agent:bob-cli-kx.3.1.land][2] | Need the child scope and notes | 1 |
| read-by | [agent:bob-cli-kx.3.1.land--5][2] | Verify the receipt phase, child epic, and all six closed implementation phases before final integration close | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.1.6.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.1.land.md

<!-- sase:referenced-by:end -->
