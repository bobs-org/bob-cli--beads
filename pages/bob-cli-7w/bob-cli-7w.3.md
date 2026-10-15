# Bead: bob-cli-7w.3 — Template-aware capture-parse

[Bead Pages](../README.md) / [bob-cli-7w](README.md) / bob-cli-7w.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1j.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1j.linker.w0.md) · **Assignee:** `bob-cli-7w.3` · **Size:** medium
**Created:** 2026-10-15 14:04:18 EDT · **Closed:** 2026-10-15 15:56:23 EDT
**Plan:** [202610/bulk\_capture\_templates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bulk_capture_templates.md)

## Description

parse: teach `capture-parse` template drafts through the masked copy, with placeholder and field spans, row items, mapped diagnostics, needs rules, the template object, and the header-less hint.

## Notes

[2026-10-15T19:47:24Z · bob-cli-7w.3] PROPOSED FOLLOW-UP: Record the bulk template expansion decision — the epic declined memory_template_decision; consider documenting capture(D) ≡ capture(expand(D)) from docs/capture.md § Bulk templates if the land agent wants a durable decision.

[2026-10-15T19:56:23Z · bob-cli-7w.3] Implemented template-aware capture-parse with masked parsing, template/row spans and items, mapped and deduplicated diagnostics, needs/refusal handling, header-less hint, docs, tests, and authorized glossary update. Verified with focused template parser/masking tests and full just check (fmt, clippy, all tests passed).

## Dependencies

- **Depends on:** [bob-cli-7w.2](bob-cli-7w.2.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7w.4](bob-cli-7w.4.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7w.5](bob-cli-7w.5.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7w.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7w.3/README.md) | [bob-cli-7w.3](bob-cli-7w.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8408562`](https://github.com/bobs-org/bob-cli/commit/840856213a7eca8b6e64443eabf8159cc22d0899) | feat(capture-parse): support template drafts | [bob-cli-7w.3](bob-cli-7w.3.md) | 2026-10-15 15:57:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7w.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7w.3/README.md

<!-- sase:referenced-by:end -->
