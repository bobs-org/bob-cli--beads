# Bead: bob-cli-h4.2 — bob enriches merge and move records, serializes merge offers, and fixes their copy

[Bead Pages](../README.md) / [bob-cli-h4](README.md) / bob-cli-h4.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.188](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.188.md) · **Assignee:** `bob-cli-h4.2` · **Size:** medium
**Created:** 2026-11-04 14:57:18 EST · **Closed:** 2026-11-04 15:48:44 EST
**Plan:** [202611/transfer\_previews.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/transfer_previews.md)

## Description

bob-transfer-records: add status names, target status, container-created flags, and Bob-authored `consequences[]` sentences (titles, not keys) to MergeRecord; add landing line, section, and status to move records; serialize merge hand-off offers as item `merge_offers`; give merge-only offers their own Pull-In copy; and print titles in the CLI's dependent rows.

## Notes

[2026-11-04T20:48:28Z · bob-cli-h4.2] PROPOSED FOLLOW-UP: just fmt fails on clean tree in src/native/capture/task_theme.rs:1009 (multi-line call formatting) — re-run just fmt on base to confirm

[2026-11-04T20:48:32Z · bob-cli-h4.2] PROPOSED FOLLOW-UP: just lint denies 10 pre-existing clippy errors in untouched files (capture_language/editor_pomodoro.rs, capture_language/past.rs, articles/inbound.rs) — none in h4.2 files

[2026-11-04T20:48:36Z · bob-cli-h4.2] PROPOSED FOLLOW-UP: just docs-check strict build fails on missing anchor in docs/reference/mac-capture/keyboard.md:104 (untouched by h4.2) — docs lint itself passes

[2026-11-04T20:48:44Z · bob-cli-h4.2] MergeRecord gains previous_status_name/status_symbol/status_name, target line/created/status, titled consequences[]; moves gain destination_line/section/status; merge_offers serialized; merge-only Pull-In copy; CLI prints titles; docs updated; verified lib 4995 pass, 61 CLI transfer/merge/move pass incl 3 new tests, scratch dry-run shows titled consequences/merge_offers/top copy

## Dependencies

- **Blocks:** [bob-cli-h4.4](bob-cli-h4.4.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h4.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h4.2/README.md) | [bob-cli-h4.2](bob-cli-h4.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`029b426`](https://github.com/bobs-org/bob-cli/commit/029b426601d6ef840e33cc24e1472b3a985ef7fe) | feat(capture): enrich merge and move records, serialize merge offers, fix copy | [bob-cli-h4.2](bob-cli-h4.2.md) | 2026-11-04 16:07:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h4.2][1] | Need phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h4.2/README.md

<!-- sase:referenced-by:end -->
