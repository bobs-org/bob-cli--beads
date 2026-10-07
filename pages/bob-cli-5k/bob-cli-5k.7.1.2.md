# Bead: bob-cli-5k.7.1.2 — bob ref migrate-zorg dry-run planner and report

[Bead Pages](../README.md) / [bob-cli-5k.7.1](bob-cli-5k.7.1.md) / bob-cli-5k.7.1.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-5k.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.7.md) · **Assignee:** `bob-cli-5k.7.1.2` · **Size:** medium
**Created:** 2026-10-07 16:17:59 EDT
**Plan:** [202610/zorg\_ref\_migration.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/zorg_ref_migration.md)

## Description

planner: add `bob ref migrate-zorg` (dry run by default). It plans one legacy note per record, with books folding their chapters. It picks collision-free stems, ref_type, title, URLs, and tags, renders the notes exactly, and prints a human or JSON report: counts by file and status, renamed targets, records without a URL, identity hits, already migrated, and skipped. Add CLI tests, help and completion updates, and docs.

## Dependencies

- **Depends on:** [bob-cli-5k.7.1.1](bob-cli-5k.7.1.1.md) ◐ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-5k.7.1.3](bob-cli-5k.7.1.3.md) ◐ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.7.1.2/README.md) | [bob-cli-5k.7.1.2](bob-cli-5k.7.1.2.md) | 0 |
