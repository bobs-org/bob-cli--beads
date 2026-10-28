# Bead: bob-cli-dm.3 — Theme rename covers note defaults and task fields

[Bead Pages](../README.md) / [bob-cli-dm](README.md) / bob-cli-dm.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2s.linker.w0.md) · **Assignee:** `bob-cli-dm.3` · **Size:** medium
**Created:** 2026-10-28 08:45:53 EDT · **Closed:** 2026-10-28 18:21:37 EDT
**Plan:** [202610/task\_theme\_suggestions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_suggestions.md)

## Description

rename-coverage: `bob themes rename` also rewrites `theme:` frontmatter and `[theme::]` fields in one previewed, verified commit with separate counts; `config_reference` guards `plan.reading_theme`; `bob themes split` leaves them alone and warns.

## Notes

[2026-10-28T22:21:37Z · bob-cli-dm.3] Verified rename-coverage: bob themes rename rewrites area/project theme: defaults and [theme::]/(theme::) task fields (including done/) in the same PT10 vault-rewrite txn as session tails; preview/JSON counts sessions, defaults, and task_themes separately (entries stays session count); verifier proves non-daily changed lines differ only in the theme value span; config_reference refuses when OLD equals plan.reading_theme; split leaves defaults/fields and warns split_leaves_task_themes. Tests: themes_rename_rewrites_defaults_and_task_fields, themes_rename_merge_rewrites_task_fields_to_new, themes_rename_refuses_reading_theme, themes_split_warns_and_leaves_defaults_and_task_fields, verify_rejects_non_daily_collateral_bytes. just all and just docs-check passed. No leftover --epic-symbol entries. No memory notes edited.

## Dependencies

- **Depends on:** [bob-cli-dm.1](bob-cli-dm.1.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dm.4](bob-cli-dm.4.md) ◐ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dm.6](bob-cli-dm.6.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.3/README.md) | [bob-cli-dm.3](bob-cli-dm.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`13b2430`](https://github.com/bobs-org/bob-cli/commit/13b243032a212a5671d569d438b7f5d2f880b80c) | feat(themes): rewrite note defaults and task fields on rename | [bob-cli-dm.3](bob-cli-dm.3.md) | 2026-10-28 18:23:08 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.3][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.3/README.md

<!-- sase:referenced-by:end -->
