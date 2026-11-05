# Bead: bob-cli-hc.1 — bob-cli resolver, lints, shared vectors, and contract docs

[Bead Pages](../README.md) / [bob-cli-hc](README.md) / bob-cli-hc.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3c.linker.w0.md) · **Assignee:** `bob-cli-hc.1` · **Size:** medium
**Created:** 2026-11-05 10:03:53 EST · **Closed:** 2026-11-05 11:09:34 EST
**Plan:** [202611/offclock\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/offclock_types.md)

## Description

clock-type-filter: parse the `offclock_types` key, extract a catalog-free effective-type helper shared with type suggestions, give HomeResolver type rules, apply the nearest-declaration rule in the clock walk, add the shadowed lint and key-naming messages, extend the shared clock vectors with a `config` member and the new cases, and update every bob-cli doc that states the clock rule.

## Notes

[2026-11-05T16:08:36Z · bob-cli-hc.1] PROPOSED FOLLOW-UP: docs first-day tutorial replays `=#focus` which current capture rejects as retired (TUTORIAL_FENCE 12 docs/start/first-bob-day.md:117); reproduces identically on clean base, unrelated to offclock_types

[2026-11-05T16:09:34Z · bob-cli-hc.1] clock-type-filter done: offclock_types reader/facts, catalog-free effective-type core shared by suggest+clock, TypeRules lazy PlanConfig load, nearest-declaration walk with shadowed lint and key-naming notices, 13 unit/parser tests, 20 shared vector cases (43 total) green in capture+dry-run, suggest/theme/capture suites unchanged green, full workspace 5038 lib + 3157 cli tests green, just lint/fmt green, docs lint/build/lychee/links/search green; docs tutorial fence-12 failure is base-identical pre-existing (recorded as follow-up)

## Dependencies

- **Blocks:** [bob-cli-hc.2](bob-cli-hc.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hc.3](bob-cli-hc.3.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hc.4](bob-cli-hc.4.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hc.5](bob-cli-hc.5.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hc.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hc.1/README.md) | [bob-cli-hc.1](bob-cli-hc.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ecc3d32`](https://github.com/bobs-org/bob-cli/commit/ecc3d32d27d199f962d37d89bf954e6b7efa8168) | feat(clock): add clock-type filter with strict offclock\_types reader | [bob-cli-hc.1](bob-cli-hc.1.md) | 2026-11-05 11:22:27 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hc.1][1] | Need full bead details and notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hc.1/README.md

<!-- sase:referenced-by:end -->
