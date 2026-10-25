# Bead: bob-cli-bj.12.1 — Bound the relation-label catalog cache and isolate its tests

[Bead Pages](../README.md) / [bob-cli-bj.12](bob-cli-bj.12.md) / bob-cli-bj.12.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-bj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bj.land.md) · **Assignee:** `bob-cli-bj.12.1` · **Size:** small
**Created:** 2026-10-24 20:05:46 EDT · **Closed:** 2026-10-24 20:20:43 EDT
**Plan:** [202610/relation\_label\_vocabulary\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary_landing_repairs.md)

## Description

relation-cache-bound: prune relation catalog cache files whose vault no longer exists, plus stale-version and stale temp files, the way bc.land bounded the theme cache in 09b26957. Isolate XDG_CACHE_HOME in every lib test that loads the relation catalog, so `cargo test` stops writing into the real ~/.cache/bob-cli/relations.

## Notes

[2026-10-25T00:20:43Z · bob-cli-bj.12.1] Bounded the relation catalog cache and isolated its tests. just check green (fmt, clippy, 18 test binaries ok). New unit test catalog_scan_prunes_vanished_vaults_and_sweeps_orphan_files passes. Acceptance: cargo test --lib relation + capture_complete added 0 files to ~/.cache/bob-cli/relations (151 before/after); read-only bob relations list -b ~/bob swept the real cache 151->7 files, all 7 for vaults that still exist. docs-check passed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.12.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.12.1/README.md) | [bob-cli-bj.12.1](bob-cli-bj.12.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d8a8f1f`](https://github.com/bobs-org/bob-cli/commit/d8a8f1f8a4ba10c80583c9f638fdf7355678137f) | fix(relations): bound catalog cache and isolate its tests | [bob-cli-bj.12.1](bob-cli-bj.12.1.md) | 2026-10-24 20:21:41 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bj.12.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.12.1/README.md

<!-- sase:referenced-by:end -->
