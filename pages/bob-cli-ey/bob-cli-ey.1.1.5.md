# Bead: bob-cli-ey.1.1.5 — %t frames templates; delete @@template:, @@@, and the @@ template candidate

[Bead Pages](../README.md) / [bob-cli-ey.1.1](bob-cli-ey.1.1.md) / bob-cli-ey.1.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.md) · **Assignee:** `bob-cli-ey.1.1.5` · **Size:** medium
**Created:** 2026-10-31 12:58:15 EDT · **Closed:** 2026-10-31 20:59:12 EDT
**Plan:** [202610/cli\_directives\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/cli_directives_split.md)

## Description

percent-t-templates: add `%t` to the directive lexer and frame the draft's first item as the template (parent plan §1.4) with offset-preserving masking; `template_directive_misplaced`; refuse row values that inject `%c`/`%t`; render shelf `show`/`draft` with ` %t` and keep shelf IDs unchanged; delete the `@@template:` header, the `template_header` span, `@@@`/`start_template` rewrite, and the `@@` template completion candidate; update help, docs, the calibrate script, the runner example, the Bulk Capture glossary strand, and note open shelf beads. Commit as `feat(capture)!:`.

## Notes

[2026-11-01T00:59:12Z · bob-cli-ey.1.1.5] Added %t to the directive lexer (DirectiveKind::Template, Directives.template) and reframed capture_language/template.rs so the draft's first item is the definition when %t sits at either edge of any of its lines; the %t token plus one adjacent separator space is cut from the definition handed to expansion and masked offset-preserving in the editor view. Later-item %t -> template_directive_misplaced; repeated %t -> duplicate_capture_marker; row values injecting %t -> template_directive_misplaced, injecting %c -> template_clipboard; headerless hint renamed template_directive_missing. Deleted @template: HEADER, the template_header span, RewriteRule::StartTemplate/start_template (@@), RouteCandidateKind::Template + template_completion_gate partial-header branch + shell.rs template branch. Shelf: canonical text excludes %t so ids are unchanged (pinned test: '{0} @x %t' -> sha of '{0} @x' = 0fc73235db73); show/draft render ' %t' on the first line then a blank line; save refuses non-template drafts with copy teaching %t. Updated help (capture, capture-rewrite, capture-templates, runner example), docs/capture.md, docs/reference/{capture-syntax,configuration}.md, search_smoke.yml (+%t queries), the capture_related_calibrate script, and glossary:bulk-capture via /sase_memory_write; ran sase memory init and just docs-gen. Added %t-replaced-it notes to bob-cli-82/83/8h/8i/8b. Verified: just check exit 0, just docs-check exit 0, clippy clean for touched code, scratch-vault smoke of -E (trailing/leading/child), misplaced, injected %t/%c, shelf save/show/list, capture-parse directive span. epic-symbols: none. Retirement grep for this phase's forms (@template, @@, start_template, template_header, TemplateHeader) leaves only narrow negative tests; note for land agent: tests/cli/ref_library/today.rs:914 has an unrelated literal '-p @@' argument that still matches the done-when grep.

## Dependencies

- **Depends on:** [bob-cli-ey.1.1.3](bob-cli-ey.1.1.3.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.1.1.6](bob-cli-ey.1.1.6.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.1.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.1.1.5/README.md) | [bob-cli-ey.1.1.5](bob-cli-ey.1.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9527893`](https://github.com/bobs-org/bob-cli/commit/952789343172946aebc67a03c724f9e6c767ae46) | feat(capture)!: frame %t templates, retire @@template:, @@@, and the @@ template candidate | [bob-cli-ey.1.1.5](bob-cli-ey.1.1.5.md) | 2026-10-31 21:00:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.1.1.5][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.1.1.5/README.md

<!-- sase:referenced-by:end -->
