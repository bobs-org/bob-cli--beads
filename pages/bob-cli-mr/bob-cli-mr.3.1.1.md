# Bead: bob-cli-mr.3.1.1 — Share full-scan planning and capture validation inputs

[Bead Pages](../README.md) / [bob-cli-mr.3.1](bob-cli-mr.3.1.md) / bob-cli-mr.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-mr.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.md) · **Assignee:** `bob-cli-mr.3.1.1` · **Size:** medium
**Created:** 2026-11-17 12:14:07 EST · **Closed:** 2026-11-17 12:58:33 EST
**Plan:** [202611/highlights\_scan\_lock\_window.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/highlights_scan_lock_window.md)

## Description

prepared-scan: extract a shared prepared full scan, an exhaustive mutation predicate, and input validation for optimistic planning; retain the existing lock window while establishing tested helpers.

## Notes

[2026-11-17T17:58:21Z · bob-cli-mr.3.1.1] PROPOSED FOLLOW-UP: just docs-check generated drift in docs/develop/decisions.md reproduces identically on clean base (run just docs-gen); not caused by prepared-scan changes

[2026-11-17T17:58:33Z · bob-cli-mr.3.1.1] prepared-scan landed: shared scan_plan module (prepare_from_inputs/prepare_full_scan/with_retry, actual-work predicate, evidence+validate stale/error, reset, unchanged assembly) wired into human+JSON locked lifecycle with canonical finalize-then-reserve order; 7 new unit tests pass; targeted gates pass (116 scan, 20 marker/overwrite/ingest, 1063 lib highlights_ref); fmt+clippy clean; docs-check drift pre-existing on clean base (recorded as follow-up)

## Dependencies

- **Blocks:** [bob-cli-mr.3.1.2](bob-cli-mr.3.1.2.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mr.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mr.3.1.1/README.md) | [bob-cli-mr.3.1.1](bob-cli-mr.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1e8f77a`](https://github.com/bobs-org/bob-cli/commit/1e8f77af0541ab29fdec657e9139a0c95a10f597) | feat(scan): share prepared full-scan planning and validation inputs | [bob-cli-mr.3.1.1](bob-cli-mr.3.1.1.md) | 2026-11-17 12:59:58 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mr.3.1.1][1] | check notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mr.3.1.1/README.md

<!-- sase:referenced-by:end -->
