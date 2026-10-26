# Bead: bob-cli-cc.1 — Keep bob's note walkers out of .bob

[Bead Pages](../README.md) / [bob-cli-cc](README.md) / bob-cli-cc.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.1` · **Size:** small
**Created:** 2026-10-26 09:00:55 EDT · **Closed:** 2026-10-26 09:15:06 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

## Description

walkers: add .bob to the always-excluded note directories so task archive, link repair, project scans, and gkeep/articles walkers can never read or edit a saved source, with regression tests.

## Notes

[2026-10-26T13:15:06Z · bob-cli-cc.1] Added .bob to ALWAYS_EXCLUDED_NOTE_DIRECTORY_NAMES so task archive, link repair, project/ready scans, task-status hooks, bob query, and the gkeep ledger skip saved sources. Regression: fixture .bob/ref-sources/chat/x--0123456789ab/source.md stays byte-identical through archive and task move, is omitted from projects/ready/query, and does not create a gkeep ledger duplicate. Unit tests cover collect_done, gkeep ledger, and articles path exclusion. docs/reference/vault-format.md states .bob/ is machine data never scanned as notes. sase bead epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-cc.3](bob-cli-cc.3.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.1/README.md) | [bob-cli-cc.1](bob-cli-cc.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`01f7ec9`](https://github.com/bobs-org/bob-cli/commit/01f7ec972ccbe499ca46dc1e377023c0c32bdf92) | fix(vault): keep note walkers out of .bob | [bob-cli-cc.1](bob-cli-cc.1.md) | 2026-10-26 09:20:31 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-cc.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.1/README.md

<!-- sase:referenced-by:end -->
