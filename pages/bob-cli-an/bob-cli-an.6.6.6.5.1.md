# Bead: bob-cli-an.6.6.6.5.1 — Keep hard-wrapped '# ' quote lines inside the highlight

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5](bob-cli-an.6.6.6.5.md) / bob-cli-an.6.6.6.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.1` · **Size:** medium
**Created:** 2026-10-24 07:37:07 EDT · **Closed:** 2026-10-24 08:03:54 EDT
**Plan:** [202610/backlog\_batch5\_highlights\_render\_pomodoro\_name\_duplicate\_link\_mac\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch5_highlights_render_pomodoro_name_duplicate_link_mac_ci.md)

## Description

highlight-quote-heading: resolve bob-cli-ba by treating a heading-shaped sidecar line that immediately follows a quote line as quote continuation, applying highlight_id_on_quote_fix for the two notes whose quote text changes.

## Notes

[2026-10-24T12:03:39Z · bob-cli-an.6.6.6.5.1] Baseline: is_quote_continuation_line rejected every is_markdown_heading line, so a hard-wrapped `# ` sidecar line ended the quote; parse_sidecar_chunk then dropped that line and sent the rest to Comment. Live read-only repros: gastown_readme p.8 missing "Set default agent"; sase_listen_antennapod_setup p.4 missing "# should start with <?xml".

Fix: in linked style, heading-shaped wrap immediately after a quote line is quote continuation unless it is a page heading or an annotation-date header (`##### YYYY-MM-DD:`). Comments still start after a blank line, Comment:/Note: labels, or marker-list fields. highlight_id_on_quote_fix=remint: quote text is identity, so the two notes remint and tombstone on the next highlights sync (not edited in the live vault).

Validation: fixture tests/fixtures/highlights_ref/quote_heading_sidecar.md; parser/render/remint unit tests; live sidecar parse on this host (both quotes keep the `# ` line, comment=None); just docs-check; just check green (fmt, clippy, cargo test --no-fail-fast).

Remaining: bob-cli-ba left open for the lander. Recovery is the next bob ref scan/sync. No --epic-symbol leftovers.

[2026-10-24T12:03:54Z · bob-cli-an.6.6.6.5.1] Linked-style heading-shaped wrap after a quote line is now quote continuation (except page headings and annotation-date headers). Live gastown_readme p.8 and sase_listen_antennapod_setup p.4 sidecars keep the `# ` line inside the quote with comment=None. Remint+tombstone locked by unit test (highlight_id_on_quote_fix=remint). Fixture quote_heading_sidecar.md covers wrap vs blank-line comment vs page heading vs date header. just docs-check and just check green. Live vault not edited; next highlights sync recovers the two notes. No --epic-symbol leftovers. Task bob-cli-ba left open for the lander.

## Dependencies

- **Blocks:** [bob-cli-an.6.6.6.5.2](bob-cli-an.6.6.6.5.2.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.1/README.md) | [bob-cli-an.6.6.6.5.1](bob-cli-an.6.6.6.5.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`215d93c`](https://github.com/bobs-org/bob-cli/commit/215d93c7eb806e033b084951eea38db3dd8906c0) | fix(highlights-ref): keep heading-shaped wrap lines inside quotes | [bob-cli-an.6.6.6.5.1](bob-cli-an.6.6.6.5.1.md) | 2026-10-24 08:05:05 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.land.md

<!-- sase:referenced-by:end -->
