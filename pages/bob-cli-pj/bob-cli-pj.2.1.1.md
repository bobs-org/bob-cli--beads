# Bead: bob-cli-pj.2.1.1 — Track PDF dependencies and classify scan changes

[Bead Pages](../README.md) / [bob-cli-pj.2.1](bob-cli-pj.2.1.md) / bob-cli-pj.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-pj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pj.2.md) · **Assignee:** `bob-cli-pj.2.1.1` · **Size:** medium
**Created:** 2026-11-22 18:51:56 EST · **Closed:** 2026-11-22 19:29:37 EST
**Plan:** [202611/refs\_incremental\_coherence.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/refs_incremental_coherence.md)

## Description

dependency_classification: record actual shared reads, retain per-PDF locator inputs, build many-owner evidence, and classify all snapshot differences with fail-closed precedence. Keep existing rebuild behavior until the refresh consumer lands.

## Notes

[2026-11-23T00:29:37Z · bob-cli-pj.2.1.1] Observation flags, many-owner evidence, and typed ScanChange classifier land in model/sync/sidecar_render/scan_plan. Production still translates Refresh/Rebuild to existing stale rebuild. Verified: cargo fmt --check; cargo check --lib (no dead_code); cargo test --lib highlights_ref (1223 ok); cargo test --test cli highlights::scan_interleave (29 ok); epic-symbols empty.

## Dependencies

- **Blocks:** [bob-cli-pj.2.1.2](bob-cli-pj.2.1.2.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pj.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pj.2.1.1/README.md) | [bob-cli-pj.2.1.1](bob-cli-pj.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`063a876`](https://github.com/bobs-org/bob-cli/commit/063a876807b0a008cc6cc0e65d68ddb10c0eea60) | feat(highlights): classify scan changes from per-PDF dependency evidence | [bob-cli-pj.2.1.1](bob-cli-pj.2.1.1.md) | 2026-11-22 19:31:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pj.2.1.1][1] | Need design file path and DECISIONS | 6 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pj.2.1.1/README.md

<!-- sase:referenced-by:end -->
