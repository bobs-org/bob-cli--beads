# Bead: bob-cli-ex.1 — Seal the caret project-note form with @ in bob

[Bead Pages](../README.md) / [bob-cli-ex](README.md) / bob-cli-ex.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bp.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bp.f0.md) · **Assignee:** `bob-cli-ex.1` · **Size:** medium
**Created:** 2026-10-31 12:01:12 EDT · **Closed:** 2026-10-31 13:46:21 EDT
**Plan:** [202610/project\_note\_seals.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_seals.md)

## Description

seal_grammar: bob-cli switches `@route^id+` to `@route^id@` in the execution grammar, editor spans, completion, type markers, and `@@` handling. The old `+` forms are retired with teaching diagnostics. `capture-parse` emits a separator span and the `project_note: "create"` span modifier. `+` after `@route^id` now toggles to `@route+id`. CLI help, docs, and tests are migrated.

## Notes

[2026-10-31T17:46:06Z · bob-cli-ex.1] PROPOSED FOLLOW-UP: articles adopt completion tests (adopt_note_completion_is_a_vault_note, article_note_completion_shows_section_count) flaked once under full just test (passed alone and on retry); watch for order-dependent shell-completion interference

[2026-10-31T17:46:21Z · bob-cli-ex.1] seal_grammar done: @route^id@ with separator span and project_note:create modifier; retired + forms teach seal; + after ^ toggles to plus; verified just fmt, just lint, cargo test --test cli capture (1179 passed), cargo test --lib capture_language (440 passed), just docs-gen, just docs-check (all gates passed); full just test 2566 passed except 2 flaky articles tests that pass on retry (noted separately)

## Dependencies

- **Blocks:** [bob-cli-ex.2](bob-cli-ex.2.md) ◐ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ex.3](bob-cli-ex.3.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ex.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.1/README.md) | [bob-cli-ex.1](bob-cli-ex.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`76f2347`](https://github.com/bobs-org/bob-cli/commit/76f234719fd756a2808434a65dcd0268468d3285) | feat(capture)!: seal project notes with @ instead of + | [bob-cli-ex.1](bob-cli-ex.1.md) | 2026-10-31 13:48:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ex.1][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-ex.3][2] | See what ex.1 landed | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.3/README.md

<!-- sase:referenced-by:end -->
