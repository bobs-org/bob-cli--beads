# Bead: bob-cli-ka.4 — Notebook-aware slash alias in capture-rewrite

[Bead Pages](../README.md) / [bob-cli-ka](README.md) / bob-cli-ka.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1b9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1b9.md) · **Assignee:** `bob-cli-ka.4` · **Size:** small
**Created:** 2026-11-11 09:22:46 EST · **Closed:** 2026-11-11 14:14:24 EST
**Plan:** [202611/notebook\_section\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/notebook_section_bullets.md)

## Description

alias: let `capture-rewrite` read notebook route frontmatter only when a typed `/` sits at a first-level bullet start, so `- /` becomes `- #` exactly where the section menu opens and stops firing on notebook note detail; update the help contract and alias tips.

## Notes

[2026-11-11T19:14:06Z · bob-cli-ka.4] PROPOSED FOLLOW-UP: docs-check lint fails on word budgets (6000 cap) for docs/reference/mac-capture/{capture-panel,capture-previews,keyboard,protocol}.md and docs/reference/plugins/bob-navigation-hotkeys.md; reproduces identically on the clean base tree, unrelated to this phase

[2026-11-11T19:14:24Z · bob-cli-ka.4] Notebook-aware / alias: rewrite_draft_with/sigil_alias_tip_with thread an optional notebook policy; adapter builds it only when bullet_sigil_may_need_notebook_policy holds (- / or - # at a first-level bullet start). Verified: @nb list and %n - / become - #; @area list, Text @nb, @nb+id, @nb#Section header, nested detail, and unrouted+missing-vault stay literal; tip teaches / for typed - #; parse (section Git/existing) and dry-run agree. Tests: 5 new CLI rewrite tests, preflight unit test, help_options pin updated, goldens regen; fmt/clippy/CLI+lib suites green. docs-check lint word-budget failures are pre-existing on clean tree (recorded as PROPOSED FOLLOW-UP).

## Dependencies

- **Depends on:** [bob-cli-ka.3](bob-cli-ka.3.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-ka.5](bob-cli-ka.5.md) ◐ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-ka.6](bob-cli-ka.6.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ka.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ka.4/README.md) | [bob-cli-ka.4](bob-cli-ka.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f709200`](https://github.com/bobs-org/bob-cli/commit/f7092004f02f210eaaef0599f46f4fc4568c8a65) | feat(capture): add notebook-aware slash alias in capture-rewrite | [bob-cli-ka.4](bob-cli-ka.4.md) | 2026-11-11 14:18:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ka.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ka.4/README.md

<!-- sase:referenced-by:end -->
