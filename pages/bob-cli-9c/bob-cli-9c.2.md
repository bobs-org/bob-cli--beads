# Bead: bob-cli-9c.2 — Shared intake session and create wiring

[Bead Pages](../README.md) / [bob-cli-9c](README.md) / bob-cli-9c.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4s.linker.w0.md) · **Assignee:** `bob-cli-9c.2` · **Size:** medium
**Created:** 2026-10-18 14:40:03 EDT · **Closed:** 2026-10-18 15:07:11 EDT
**Plan:** [202610/ref\_ingest\_at\_birth.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_ingest_at_birth.md)

## Description

create-ingest: build the shared locked intake session in a new highlights_ref intake module. It takes the locks, pre-syncs, re-checks, moves, plans with rollback, writes, makes one scoped commit, and post-syncs. Wire it into every `bob ref create` route in place of `next: bob ref scan`. Add `-k/--keep-intake`, the `highlights.ingest_on_create` switch, and `BOB_HIGHLIGHTS_INGEST_ON_CREATE`, with scratch-vault integration tests.

## Notes

[2026-10-18T19:07:11Z · bob-cli-9c.2] Implemented locked create-time intake, keep/config/env controls, all create-route wiring, rollback, scoped sync, tests, and docs. Verified: just check passed (formatting, clippy, and all test binaries); the focused intake tests passed 5/5 and create tests passed 102/102. epic-symbols was empty.

## Dependencies

- **Blocks:** [bob-cli-9c.3](bob-cli-9c.3.md) ◐ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9c.4](bob-cli-9c.4.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9c.6](bob-cli-9c.6.md) ◐ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9c.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9c.2/README.md) | [bob-cli-9c.2](bob-cli-9c.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c4ac06f`](https://github.com/bobs-org/bob-cli/commit/c4ac06fb47633fcf1b26e592031a6c32c0087a8e) | feat(highlights): ingest references during create | [bob-cli-9c.2](bob-cli-9c.2.md) | 2026-10-18 15:15:47 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9c.2][1] | Confirm phase scope and remaining notes before closure | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9c.2/README.md

<!-- sase:referenced-by:end -->
