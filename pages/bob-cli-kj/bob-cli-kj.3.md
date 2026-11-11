# Bead: bob-cli-kj.3 — Stats RefCell double-borrow panic

[Bead Pages](../README.md) / [bob-cli-kj](README.md) / bob-cli-kj.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.3` · **Size:** small
**Created:** 2026-11-11 17:20:03 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

## Description

stats-borrow: restructure HomesEngine::finish so remember/ensure_root never re-borrow the resolver, add a regression test for single-metric ranges covering today, and record bob-cli-hp close evidence from just check (beads bob-cli-jr, bob-cli-hp).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kj.3/README.md) | [bob-cli-kj.3](bob-cli-kj.3.md) | 0 |
