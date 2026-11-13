# Bead: bob-cli-kx.4 — Close-time notice polish

[Bead Pages](../README.md) / [bob-cli-kx](README.md) / bob-cli-kx.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bt](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bt.md) · **Assignee:** `bob-cli-kx.4` · **Size:** small
**Created:** 2026-11-12 11:11:53 EST · **Closed:** 2026-11-13 16:55:16 EST
**Plan:** [202611/gmail\_archive\_on\_task\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_on_task_close.md)

## Description

polish: In bob-plugins, show the no-network close-time notice when a managed Done lands on a row watching an enrolled mail note while archive is enabled, and optionally a back-in-inbox chip on let-go rows. Pure rendering of what bob reports; no network calls, no vault writes.

## Notes

[2026-11-13T21:55:16Z · bob-cli-kx.4--1] Implemented and built the close-time notice; npm run build and npm run build:check passed. Retried bob plugins sync after the deployment owner finished; sync succeeded (0 copied, 31 unchanged), and epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-kx.3](bob-cli-kx.3.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kx.5](bob-cli-kx.5.md) ◐ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.4.md) | [bob-cli-kx.4](bob-cli-kx.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@4e197dd`](https://github.com/bobs-org/bob-plugins/commit/4e197dd99285c42f6faf9a0514529493d924524f) | feat(gmail-archive): add managed close notice | [bob-cli-kx.4](bob-cli-kx.4.md) | 2026-11-13 16:56:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.3.1.land--5][1] | Verify that only the requested receipt phase closed and protected ancestor/sibling statuses remain unchanged | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.1.land.md

<!-- sase:referenced-by:end -->
