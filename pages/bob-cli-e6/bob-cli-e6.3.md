# Bead: bob-cli-e6.3 — bob types migrate

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.3` · **Size:** small
**Created:** 2026-10-29 16:16:33 EDT · **Closed:** 2026-10-29 19:07:28 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

migrate: add a previewed, single-commit vault rewrite that moves open-task [theme::] fields and area/project theme: defaults to the canonical type spellings.

## Notes

[2026-10-29T22:26:51Z · bob-cli-e6.3] Verified: cargo test --lib pomodoro_themes::migrate (8), CLI themes_migrate + catalog/help/completion, clippy project gates, just docs-gen. epic-symbols none. Prepared just check for host close.

[2026-10-29T23:07:28Z · bob-cli-e6.3--1] Verified: cargo test --lib pomodoro_themes::migrate (8) and CLI themes_migrate (dry-run, apply/commit/revert, idempotence, refusals, lock, alias). Updated 11 leftover vocab/storage CLI assertions from theme to type wording so bob-obsidian --test cli matches landed writers. just fmt --check; epic-symbols none.

## Dependencies

- **Blocks:** [bob-cli-e6.16](bob-cli-e6.16.md) ◐ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.2](bob-cli-e6.2.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-e6.3.md) | [bob-cli-e6.3](bob-cli-e6.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c0f9439`](https://github.com/bobs-org/bob-cli/commit/c0f94390168e23f37da4a186f0b160ec591358b5) | feat(types): add bob types migrate for legacy theme spellings | [bob-cli-e6.3](bob-cli-e6.3.md) | 2026-10-29 19:48:39 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.3--2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-e6.3.md

<!-- sase:referenced-by:end -->
