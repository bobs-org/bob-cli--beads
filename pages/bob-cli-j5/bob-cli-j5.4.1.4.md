# Bead: bob-cli-j5.4.1.4 — Use resolved pairs in archiving and report archive health

[Bead Pages](../README.md) / [bob-cli-j5.4.1](bob-cli-j5.4.1.md) / bob-cli-j5.4.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-j5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.4.md) · **Assignee:** `bob-cli-j5.4.1.4` · **Size:** medium
**Created:** 2026-11-09 16:44:34 EST · **Closed:** 2026-11-09 18:59:20 EST
**Plan:** [202611/archive\_pairing\_and\_rename.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/archive_pairing_and_rename.md)

## Description

archive-health: resolve archive destinations and historical link repair from captured inputs; report binding conflicts and all five required health findings in human and JSON output, including preview and refused plans, without silently repairing findings.

## Notes

[2026-11-09T23:59:20Z · bob-cli-j5.4.1.4] archive-health: pair index from CapturedInputs drives destination and historical link repair; bound noncanonical archives stay the one destination; diagnostics (6 codes) on every captured run including preview/noop/refused; binding conflicts skip affected writes with exit 1; schema_version stays 1. Verified cargo fmt --all, collect_done 155 tests, CLI stayed-pathless-link test, just check, just docs-check. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-j5.4.1.1](bob-cli-j5.4.1.1.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j5.4.1.5](bob-cli-j5.4.1.5.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j5.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.4.1.4/README.md) | [bob-cli-j5.4.1.4](bob-cli-j5.4.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2327590`](https://github.com/bobs-org/bob-cli/commit/2327590f2caabced31e6320a232d57355dfe2007) | feat(archive): report health findings and use bound pair destinations | [bob-cli-j5.4.1.4](bob-cli-j5.4.1.4.md) | 2026-11-09 19:00:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j5.4.1.4][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-j5.4.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.4.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-j5.4.1.land.md

<!-- sase:referenced-by:end -->
