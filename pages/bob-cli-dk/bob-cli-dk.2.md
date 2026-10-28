# Bead: bob-cli-dk.2 — bob-cli suggestions and warnings for unconfigured themes

[Bead Pages](../README.md) / [bob-cli-dk](README.md) / bob-cli-dk.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.151](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.151.md) · **Assignee:** `bob-cli-dk.2` · **Size:** medium
**Created:** 2026-10-28 07:47:10 EDT · **Closed:** 2026-10-28 09:38:31 EDT
**Plan:** [202610/configured\_pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/configured_pomodoro_themes.md)

## Description

warnings: limit Recent suggestions to configured themes and emit `theme_not_configured` from capture, Name-it, bob plan, rename/split, and themes-list hints, plus menu vectors and docs.

## Notes

[2026-10-28T13:38:31Z · bob-cli-dk.2--2] Verified phase warnings: Recent menus are scoped to the configured vocabulary (never-used names, 12-row empty-query cap, similar_to over visible configured keys); theme_not_configured lands on capture, capture-pomodoro-name, bob plan, rename/split, and themes-list hints; just check (fmt, clippy, tests) and just docs-check passed; epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-dk.1](bob-cli-dk.1.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dk.3](bob-cli-dk.3.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dk.4](bob-cli-dk.4.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dk.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dk.2.md) | [bob-cli-dk.2](bob-cli-dk.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`084a285`](https://github.com/bobs-org/bob-cli/commit/084a2852b121a153852a5c045b3b5ac5385ea89c) | feat(themes): scope Recent to configured themes and warn on unconfigured names | [bob-cli-dk.2](bob-cli-dk.2.md) | 2026-10-28 09:49:09 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dk.2--2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dk.2.md

<!-- sase:referenced-by:end -->
