# Bead: bob-cli-ab.1 — Matching engine and the --query harness

[Bead Pages](../README.md) / [bob-cli-ab](README.md) / bob-cli-ab.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.27.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.27.linker.w0.md) · **Assignee:** `bob-cli-ab.1` · **Size:** medium
**Created:** 2026-10-20 17:44:13 EDT · **Closed:** 2026-10-20 18:50:59 EDT
**Plan:** [202610/capture\_similar\_tasks\_band.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_similar_tasks_band.md)

## Description

engine: add bob capture-related with the Bob-aware tokenizer, the per-call TF-IDF scorer, candidate discovery (open tasks in routable notes plus a closed window), bands, and --query human/JSON output, with table tests and a synthetic-vault perf test.

## Notes

[2026-10-20T22:50:59Z · bob-cli-ab.1] Shipped bob capture-related --query (Bob-aware tokenizer, per-call TF-IDF, capture_targets+note_tasks discovery, bands, human/JSON schema_version 1). just check and just docs-check passed. Apollo vault read-only 30-run --query 'Install UPS battery' -f json: median 96.0ms, p95 168.7ms (min 85.4, max 178.5). No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-ab.2](bob-cli-ab.2.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ab.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ab.1/README.md) | [bob-cli-ab.1](bob-cli-ab.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`787d62c`](https://github.com/bobs-org/bob-cli/commit/787d62cbad07597023f0f005ad9285ec3cc84529) | feat(capture-related): add matching engine and --query harness | [bob-cli-ab.1](bob-cli-ab.1.md) | 2026-10-20 18:52:23 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ab.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ab.1/README.md

<!-- sase:referenced-by:end -->
