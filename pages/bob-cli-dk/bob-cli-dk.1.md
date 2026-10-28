# Bead: bob-cli-dk.1 — bob-cli themes config, hue rule, and catalog reports

[Bead Pages](../README.md) / [bob-cli-dk](README.md) / bob-cli-dk.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.151](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.151.md) · **Assignee:** `bob-cli-dk.1` · **Size:** medium
**Created:** 2026-10-28 07:47:10 EDT · **Closed:** 2026-10-28 08:17:24 EDT
**Plan:** [202610/configured\_pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/configured_pomodoro_themes.md)

## Description

config: parse and validate the `themes:` block, put config colors first in the hue rule, add `configured` to every ThemeRef, make `bob themes list` and `bob themes color` config-aware, extend the hue vectors, and document PT12.

## Notes

[2026-10-28T12:17:09Z · bob-cli-dk.1] PROPOSED FOLLOW-UP: memory_vocabulary_record (decisions:configured-themes-are-a-soft-vocabulary strand) was decided no for this plan; a later epic can propose it

[2026-10-28T12:17:24Z · bob-cli-dk.1] config phase done and verified: themes: parser with strict validation (tests in config/themes.rs), one-read ThemeSources loader, config-first hue rule with config/unconfigured HueSources and per-ThemeRef configured flag, themes list with never-used configured rows + counts.configured + configured_themes JSON, config_color refusal on themes color, 8 new hue vector cases, PT12 + PT5/PT6/JSON/CLI docs + configuration.md + generated CLI reference, docs-gen/docs-check green, memory glossary + new config-first hue decision (old superseded) + memory init. just all green; fixture-vault checks: 6 configured rows/header/never rows/unconfigured ◌, refusal exit 1 with journal untouched, invalid block degrades with warning, no-config JSON and human output byte-identical to installed release binary.

## Dependencies

- **Blocks:** [bob-cli-dk.2](bob-cli-dk.2.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dk.3](bob-cli-dk.3.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dk.4](bob-cli-dk.4.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dk.5](bob-cli-dk.5.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dk.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dk.1/README.md) | [bob-cli-dk.1](bob-cli-dk.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ec018a5`](https://github.com/bobs-org/bob-cli/commit/ec018a5bcf5f7f9e48a52f81a40de7050145be70) | feat(themes): configured themes vocabulary, config-first hue rule, and catalog reports | [bob-cli-dk.1](bob-cli-dk.1.md) | 2026-10-28 08:19:13 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dk.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dk.1/README.md

<!-- sase:referenced-by:end -->
