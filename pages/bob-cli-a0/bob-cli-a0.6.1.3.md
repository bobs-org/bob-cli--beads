# Bead: bob-cli-a0.6.1.3 — Deterministic CLI media and Learn visual verification

[Bead Pages](../README.md) / [bob-cli-a0.6.1](bob-cli-a0.6.1.md) / bob-cli-a0.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.6.md) · **Assignee:** `bob-cli-a0.6.1.3` · **Size:** medium
**Created:** 2026-10-19 23:17:16 EDT · **Closed:** 2026-10-20 00:56:19 EDT
**Plan:** [202610/learn\_path.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/learn_path.md)

## Description

cli-media: reuse the isolated tutorial environment for real PTY captures, render deterministic Rich SVGs, add media drift checking, replace the homepage terminal illustration, and verify the completed Learn pages in both builders.

## Notes

[2026-10-20T04:56:04Z · bob-cli-a0.6.1.3] PROPOSED FOLLOW-UP: Clean-machine tutorial walkthrough — Bryan should follow /start/ from a fresh install, open the demo in Obsidian, and try the Mac continuation; automated Linux checks cannot verify those GUI interactions.

[2026-10-20T04:56:10Z · bob-cli-a0.6.1.3] PROPOSED FOLLOW-UP: Docs a11y axe serious findings are theme-wide (Zensical aria-prohibited-attr on header nav/search labels; Material aria-dialog-name on .md-search; pygments color-contrast on capture/first-bob-day; scrollable-region-focusable on capture/today-marks) plus 200% zoom page scroll from unwrapped code fences and task cards. Learn copy buttons, 360 overflow, footer links, keyboard focus, and compatibility wrap passed on both builders; CLI SVG is not the overflow source. just docs-a11y is dev-only and not in docs-check.

[2026-10-20T04:56:19Z · bob-cli-a0.6.1.3] Verified: just docs-tutorial, bob-docs media -c (byte-stable WOFF2 SVGs), just docs-check, 339 docs pytest, just docs-build-material. Homepage uses real capture.svg with copyable command. Inspected Zensical and Material Learn screenshots at 360/768/1280 light/dark (CLI SVG readable both themes; mermaid diagram present; compatibility wraps). Recorded clean-machine walkthrough and theme-wide a11y follow-ups. No --epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-a0.6.1.2](bob-cli-a0.6.1.2.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.6.1.3/README.md) | [bob-cli-a0.6.1.3](bob-cli-a0.6.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`50d0e99`](https://github.com/bobs-org/bob-cli/commit/50d0e990138287513304fbde2487cf54defbb86c) | feat(docs): capture deterministic CLI SVGs for the Learn path | [bob-cli-a0.6.1.3](bob-cli-a0.6.1.3.md) | 2026-10-20 01:09:15 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.6.1.3][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.6.1.3/README.md

<!-- sase:referenced-by:end -->
