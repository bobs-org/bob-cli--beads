# Bead: bob-cli-bj.12.1 — Bound the relation-label catalog cache and isolate its tests

[Bead Pages](../README.md) / [bob-cli-bj.12](bob-cli-bj.12.md) / bob-cli-bj.12.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-bj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bj.land.md) · **Assignee:** `bob-cli-bj.12.1` · **Size:** small
**Created:** 2026-10-24 20:05:46 EDT
**Plan:** [202610/relation\_label\_vocabulary\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary_landing_repairs.md)

## Description

relation-cache-bound: prune relation catalog cache files whose vault no longer exists, plus stale-version and stale temp files, the way bc.land bounded the theme cache in 09b26957. Isolate XDG_CACHE_HOME in every lib test that loads the relation catalog, so `cargo test` stops writing into the real ~/.cache/bob-cli/relations.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.12.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.12.1/README.md) | [bob-cli-bj.12.1](bob-cli-bj.12.1.md) | 0 |
