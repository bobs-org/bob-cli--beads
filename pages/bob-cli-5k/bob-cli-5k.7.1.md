# Bead: bob-cli-5k.7.1 — Migrate zorg-era reading records into the reference library

[Bead Pages](../README.md) / [bob-cli-5k.7](bob-cli-5k.7.md) / bob-cli-5k.7.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-5k.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.7.md) · **Assignee:** `bob-cli-5k.7.1.land`
**Created:** 2026-10-07 16:17:59 EDT
**Plan:** [202610/zorg\_ref\_migration.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/zorg_ref_migration.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/zorg_ref_migration.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/zorg_ref_migration.md

<!-- sase:links:end -->

## Description

`bob ref migrate-zorg` moves every unindexed zorg-era reading record (424 on 2026-10-07) into legacy reference notes under `ref/zorg/<hub>/`. It runs as a dry-run-first, idempotent vault write: one sync-sandwiched commit that a single `git revert` undoes. Book chapters fold into their book's note. On athena, `bob ref doctor` then reports `coverage: ok`, `bob ref find` / `bob ref list` return the migrated records, the JSON `coverage.scope` caveat no longer claims that zorg history is invisible, and bob-cli-4x is closed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.7.1.land/README.md) | [bob-cli-5k.7.1](bob-cli-5k.7.1.md) | 0 |
