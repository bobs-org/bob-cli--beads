# Bead: bob-cli-an.6.6.5 — Map relative PDF paths to their real reference notes

[Bead Pages](../README.md) / [bob-cli-an.6.6](bob-cli-an.6.6.md) / bob-cli-an.6.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.land.md) · **Assignee:** `bob-cli-an.6.6.5` · **Size:** small
**Created:** 2026-10-23 17:27:15 EDT · **Closed:** 2026-10-23 17:48:21 EDT
**Plan:** [202610/backlog\_batch3\_rfserver\_backups\_day\_zone\_webclip\_fonts\_ref\_paths.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch3_rfserver_backups_day_zone_webclip_fonts_ref_paths.md)

## Description

ref-relative-paths: resolve bob-cli-9a by absolutizing and normalizing PDF arguments before library mapping in bob ref sync and marker.

## Notes

[2026-10-23T21:48:21Z · bob-cli-an.6.6.5] Resolved cwd-relative PDF paths with the existing absolute lexical normalizer in ref sync and marker. Focused regression passed for a nested lib/ path containing ..; just fmt and just check passed (3,205 unit tests, one ignored, and all integration suites). Epic symbols: none.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.5/README.md) | [bob-cli-an.6.6.5](bob-cli-an.6.6.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fb535ef`](https://github.com/bobs-org/bob-cli/commit/fb535ef66d679830e70c5791483248f53760ad20) | fix(ref): resolve relative PDF paths before mapping | [bob-cli-an.6.6.5](bob-cli-an.6.6.5.md) | 2026-10-23 17:48:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.5][1] | Need phase notes and originating task acceptance details | 3 |
| read-by | [agent:bob-cli-an.6.6.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.land.md

<!-- sase:referenced-by:end -->
