# Bead: bob-cli-pl.6.1.2 — Extend the Property Editor with contract groups and stable virtual rows

[Bead Pages](../README.md) / [bob-cli-pl.6.1](bob-cli-pl.6.1.md) / bob-cli-pl.6.1.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.md) · **Assignee:** `bob-cli-pl.6.1.2` · **Size:** medium
**Created:** 2026-11-24 15:49:21 EST
**Plan:** [202611/area\_project\_settings.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_settings.md)

## Description

settings-rows: add a per-kind row provider, render stable settings and project virtual rows, preserve selection and clipboard behavior, gate unsupported actions, and implement capability fallback.

## Notes

[2026-11-24T22:48:22Z · bob-cli-pl.6.1.2--2] PROPOSED FOLLOW-UP: docs-check baseline exceeds word budgets — verification on the phase tree fetched bob-cli master 15fd03b2 and reported plugin-apis.md at 9,287/8,000 words and json-outputs.md at 6,005/6,000, plus bob-navigation-hotkeys.md at 6,029/6,000. The phase commit changes only ledger-tools source/build output and its focused test, so these documentation inputs are unchanged from the clean base.

## Dependencies

- **Depends on:** [bob-cli-pl.6.1.1](bob-cli-pl.6.1.1.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-pl.6.1.3](bob-cli-pl.6.1.3.md) ◐ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.1.2.md) | [bob-cli-pl.6.1.2](bob-cli-pl.6.1.2.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d55a175`](https://github.com/bobs-org/bob-plugins/commit/d55a17599e017f309880b4a3f520e495cfcd131c) | feat(props): add contract-backed settings rows | [bob-cli-pl.6.1.2](bob-cli-pl.6.1.2.md) | 2026-11-24 17:28:59 EST |
| bob-plugins | [`bob-plugins@7649f6f`](https://github.com/bobs-org/bob-plugins/commit/7649f6fe4f45394d517c4b57e864f717c3bad64b) | fix(property-editor): correct settings row grouping and navigation | [bob-cli-pl.6.1.2](bob-cli-pl.6.1.2.md) | 2026-11-24 17:40:26 EST |
| bob-plugins | [`bob-plugins@a22851f`](https://github.com/bobs-org/bob-plugins/commit/a22851fd13501bf0169ee690e07c60f573f9e5f6) | fix(props): preserve source row identity in settings fallback | [bob-cli-pl.6.1.2](bob-cli-pl.6.1.2.md) | 2026-11-24 18:05:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.6.1.2--1][1] | Need the assigned phase scope, decisions, and current notes before fixing the failed verification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.1.2.md

<!-- sase:referenced-by:end -->
