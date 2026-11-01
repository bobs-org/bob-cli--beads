# Bead: bob-cli-f9.1 — Bob Mac Capture stops showing the type cap

[Bead Pages](../README.md) / [bob-cli-f9](README.md) / bob-cli-f9.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.by](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.by.md) · **Assignee:** `bob-cli-f9.1` · **Size:** small
**Created:** 2026-11-01 12:12:35 EST · **Closed:** 2026-11-01 12:32:11 EST
**Plan:** [202611/retire\_type\_cap\_today\_roots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/retire_type_cap_today_roots.md)

## Description

mac-drop-type-meter: in bob-mac-capture, drop the Types capsule, the +N type delta chip, and the red after/cap completion badge, decode old and new bob budget JSON, update tests and docs, and compile per AGENTS.md.

## Notes

[2026-11-01T17:32:11Z · bob-cli-f9.1] Mac Capture no longer shows the type cap: removed the Types capsule, +N type delta chip, after/cap completion badge (plan_themes_after/cap), and the plan_theme_cap_exceeded hint; CapturePlanBudget now decodes only links + added_theme_refs, ignoring old themes/added_themes and dropping old theme-cap warnings. Tests/docs updated. Verified: swift build + swift test on athena (1895 pass), bundle.sh + just typecheck-tests on mac pass, just docs-check passes. Lint not clean-checked (swift-format on Linux reports pre-existing warnings repo-wide).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f9.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f9.1/README.md) | [bob-cli-f9.1](bob-cli-f9.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@f4face9`](https://github.com/bobs-org/bob-mac-capture/commit/f4face9fe8ea965cfa12bb4b3a88dad1c5403b29) | feat(capture)!: stop showing the daily type cap | [bob-cli-f9.1](bob-cli-f9.1.md) | 2026-11-01 12:32:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f9.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f9.1/README.md

<!-- sase:referenced-by:end -->
