# Bead: bob-cli-do.3 — Vault-sync clobber detection and quarantine

[Bead Pages](../README.md) / [bob-cli-do](README.md) / bob-cli-do.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.157.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.157.f0.md) · **Assignee:** `bob-cli-do.3` · **Size:** medium
**Created:** 2026-10-28 10:46:06 EDT · **Closed:** 2026-10-28 11:30:36 EDT
**Plan:** [202610/clobbered\_note\_repair\_and\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/clobbered_note_repair_and_guards.md)

## Description

sync-clobber-guard: detect displaced-plus-foreign-identity rewrites of tracked notes before staging, quarantine or warn per the decision, record in status, alert, document, test.

## Notes

[2026-10-28T15:16:49Z · bob-cli-do.3] Implemented quarantine-on-clobber: vault_clobber.rs signature detector, cycle restore+conflict copy+log, clobbers/recent_clobbers status, desktop notify, docs, unit and temp-repo cycle tests. clobber_response=quarantine.

[2026-10-28T15:30:36Z · bob-cli-do.3--1] Verified quarantine-on-clobber: vault_clobber detector, cycle restore+conflict copy+log, clobbers/recent_clobbers status, desktop notify, docs, unit and temp-repo cycle tests. just check passed (exit 0). No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-do.4](bob-cli-do.4.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-do.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-do.3.md) | [bob-cli-do.3](bob-cli-do.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`16f3da4`](https://github.com/bobs-org/bob-cli/commit/16f3da48ac167002d29c7b0e1119fc4b0a97a125) | feat(vault-sync): quarantine displaced-plus-foreign-identity note clobbers | [bob-cli-do.3](bob-cli-do.3.md) | 2026-10-28 11:38:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-do.3--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-do.3.md

<!-- sase:referenced-by:end -->
