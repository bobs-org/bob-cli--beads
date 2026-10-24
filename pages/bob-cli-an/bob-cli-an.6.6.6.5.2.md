# Bead: bob-cli-an.6.6.6.5.2 — Stop rendering the page-1 marker mirror as an annotation

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5](bob-cli-an.6.6.6.5.md) / bob-cli-an.6.6.6.5.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.2` · **Size:** large
**Created:** 2026-10-24 07:37:07 EDT · **Closed:** 2026-10-24 08:40:00 EDT
**Plan:** [202610/backlog\_batch5\_highlights\_render\_pomodoro\_name\_duplicate\_link\_mac\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch5_highlights_render_pomodoro_name_duplicate_link_mac_ci.md)

## Description

highlight-marker-mirror: resolve bob-cli-4r by skipping the real page-1 marker mirror even when a setext title preamble consumes the current one-shot skip.

## Notes

[2026-10-24T12:39:32Z · bob-cli-an.6.6.6.5.2] Color-grouped marker-mirror fix implemented.

Baseline: source adb9c324 + prerequisite 215d93c7. Color-grouped sidecars with no page headings retained the setext title+underline in the first chunk; parse_sidecar_chunk strips color/date headings but keeps the prefix; strict parse_marker rejected the title so the marker rendered as a note with an h- ID, and beautify joined title+underline onto one line so region reads also missed it. Preserved highlight_id_on_quote_fix=remint and existing page-grouped tests.

Fix: extended the shared classifier in src/native/highlights_ref/region.rs. is_marker_mirror_text still tries strict whole-text parse first, then strips a leading nonempty setext title plus === underline (raw two-line or rendered single-line title ===... form, blank lines allowed) and validates the entire remainder with parse_marker + status/parent rules. Title with extra prose, malformed items, or missing keys stays visible. Updated is_sidecar_marker_mirror comment in sidecar_render.rs. No page labels manufactured; PDF marker parsing untouched. Docs updated in docs/highlights-ref-sync.md.

Tests: new fixture tests/fixtures/highlights_ref/color_grouped_sidecar.md; unit color_grouped_title_prefixed_marker_is_excluded (sidecar.rs); region tests title_prefixed_marker_text_is_a_mirror, region_parses_rendered_title_prefixed_mirror, color_grouped_rerender_drops_phantom_without_tombstone, color_grouped_genuine_loss_still_tombstones, color_grouped_plain_prose_and_titled_notes_survive, color_grouped_mirror_with_task_text_yields_no_task; CLI highlights_ref_sync_drops_color_grouped_mirror_without_tombstone (dry-run update without write, phantom removed without tombstone, genuine highlight+note survive, second sync stable); CLI show_excludes_color_grouped_mirror_with_counts (unsynced leaked callout excluded, counts exclude it).

Gates: cargo test --lib native::highlights_ref 637/637; cargo test --test cli highlights:: 378/378; cargo test --test cli ref_library:: 130/130; just docs-check pass (447 passed); just check pass (fmt+clippy+full tests).

Live read-only (fresh binary built 08:39 EDT 2026-10-24 from adb9c324+tree, queries 08:39 EDT): ref/chat/remote_sase_agents_consolidated.md library-API annotation_count 1, comment_count 1, excluded.marker_mirrors 1, phantom h-0803707b4f20 excluded, genuine h-e2d9e4fa6422 survives; stored highlights_count still 2. ref/chat/apollo_remote_agents_workspace_topology.md annotation_count 0, comment_count 0, excluded 1, phantom h-d003d0a4b3ab excluded; stored highlights_count still 1. Census bob ref list -R all -n 10000: 1,122 listed references (library notes 1122, coverage notes 1124), 86 with positive stored highlights; show of all 86: total excluded.marker_mirrors 2, zero unexcluded mirror-like annotations. No live vault writes, no scan/sync, no install. Live recovery path is the next normal scan/sync.

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.1](bob-cli-an.6.6.6.5.1.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.2.md) | [bob-cli-an.6.6.6.5.2](bob-cli-an.6.6.6.5.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bff7bc7`](https://github.com/bobs-org/bob-cli/commit/bff7bc724b5ac854c554ed916a13f5802dede634) | fix(highlights): exclude color-grouped setext title-prefixed marker mirrors | [bob-cli-an.6.6.6.5.2](bob-cli-an.6.6.6.5.2.md) | 2026-10-24 08:41:38 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.land.md

<!-- sase:referenced-by:end -->
