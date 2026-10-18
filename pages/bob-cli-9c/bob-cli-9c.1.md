# Bead: bob-cli-9c.1 — Writing scans hold the vault-maintenance lock

[Bead Pages](../README.md) / [bob-cli-9c](README.md) / bob-cli-9c.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4s.linker.w0.md) · **Assignee:** `bob-cli-9c.1` · **Size:** small
**Created:** 2026-10-18 14:40:03 EDT · **Closed:** 2026-10-18 14:50:02 EDT
**Plan:** [202610/ref\_ingest\_at\_birth.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_ingest_at_birth.md)

## Description

scan-sync-lock: make every writing `bob ref scan` (human and JSON) take bob_sync.lock before scan.lock and hold both through intake and note writes. This closes the window where vault-sync pushes a library PDF without its ref note. Add the `lock_busy` error and document the lock order.

## Notes

[2026-10-18T18:50:02Z · bob-cli-9c.1] Writing bob ref scan (human and JSON) takes bob_sync.lock before scan.lock and holds both through intake and note writes. lock_busy names the maintenance lock path; dry runs take neither lock. Verified with highlights::scan lock tests (held lock, dry-run, free lock, existing scan_busy). Docs state lock order bob_sync.lock → scan.lock. epic-symbols: none leftover.

## Dependencies

- **Blocks:** [bob-cli-9c.4](bob-cli-9c.4.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9c.6](bob-cli-9c.6.md) ◐ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9c.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9c.1.md) | [bob-cli-9c.1](bob-cli-9c.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`85eac25`](https://github.com/bobs-org/bob-cli/commit/85eac25aa112e0888ec09955ef0bc587e3c514ea) | feat(ref): hold vault-maintenance lock during writing scans | [bob-cli-9c.1](bob-cli-9c.1.md) | 2026-10-18 14:58:58 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9c.1--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9c.1.md

<!-- sase:referenced-by:end -->
