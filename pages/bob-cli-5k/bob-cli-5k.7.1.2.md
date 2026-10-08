# Bead: bob-cli-5k.7.1.2 — bob ref migrate-zorg dry-run planner and report

[Bead Pages](../README.md) / [bob-cli-5k.7.1](bob-cli-5k.7.1.md) / bob-cli-5k.7.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-5k.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5k.7.md) · **Assignee:** `bob-cli-5k.7.1.2` · **Size:** medium
**Created:** 2026-10-07 16:17:59 EDT · **Closed:** 2026-10-07 18:45:16 EDT
**Plan:** [202610/zorg\_ref\_migration.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/zorg_ref_migration.md)

## Description

planner: add `bob ref migrate-zorg` (dry run by default). It plans one legacy note per record, with books folding their chapters. It picks collision-free stems, ref_type, title, URLs, and tags, renders the notes exactly, and prints a human or JSON report: counts by file and status, renamed targets, records without a URL, identity hits, already migrated, and skipped. Add CLI tests, help and completion updates, and docs.

## Notes

[2026-10-07T22:44:59Z · bob-cli-5k.7.1.2] PROPOSED FOLLOW-UP: planner classifies prj_yserve yserve as papers (nested file:: items are the first file:: value) while the plan section-2 table counts 48 papers; live-run should expect papers 49 / fallback 14

[2026-10-07T22:45:06Z · bob-cli-5k.7.1.2] PROPOSED FOLLOW-UP: Library help abouts shortened to fit the 64-col group budget (migrate-zorg about no longer the plan 3.9 verbatim); writer phase must keep every Library about on one line

[2026-10-07T22:45:16Z · bob-cli-5k.7.1.2] Planner done: just check fully green (lib 1934, cli 1173 incl 7 new migrate-zorg CLI tests + 10 render unit tests with byte-for-byte goldens). Live dry-run vs plan sec-2: records 424, notes 322, chapters 102, renamed 17, no_url 11, identity 0, already_migrated 282, skipped 0; reading states finished 183/started 69/queued 52/dropped 16/unknown 2 all match. One deviation noted on bead (yserve papers-49 vs table papers-48). No epic-symbols. Vault untouched by dry run.

## Dependencies

- **Depends on:** [bob-cli-5k.7.1.1](bob-cli-5k.7.1.1.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-5k.7.1.3](bob-cli-5k.7.1.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.7.1.2/README.md) | [bob-cli-5k.7.1.2](bob-cli-5k.7.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`937722b`](https://github.com/bobs-org/bob-cli/commit/937722b5506b4095737fa90b67ffbde04edf0178) | feat(ref-library): add bob ref migrate-zorg dry-run planner | [bob-cli-5k.7.1.2](bob-cli-5k.7.1.2.md) | 2026-10-07 18:47:04 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5k.7.1.2][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-5k.7.1.3][2] | Need planner phase evidence to build writer on | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.7.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.7.1.3/README.md

<!-- sase:referenced-by:end -->
