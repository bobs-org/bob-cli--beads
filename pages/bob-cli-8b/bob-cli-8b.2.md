# Bead: bob-cli-8b.2 — bob capture-templates protocol command

[Bead Pages](../README.md) / [bob-cli-8b](README.md) / bob-cli-8b.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1n.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1n.linker.w0.md) · **Assignee:** `bob-cli-8b.2` · **Size:** medium
**Created:** 2026-10-16 08:18:36 EDT · **Closed:** 2026-10-16 09:15:34 EDT
**Plan:** [202610/saved\_capture\_templates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/saved_capture_templates.md)

## Description

protocol: add the `bob capture-templates` group (list default, show, save, delete, clear) with ready-to-insert drafts, cursors, and capture-parse spans in JSON, colored human output, definition-only validation for save, help, completion, and docs.

## Notes

[2026-10-16T13:15:14Z · bob-cli-8b.2] PROPOSED FOLLOW-UP: Add an accepted decisions record that saved capture templates are bob-owned and checked out, not popped — the epic decision sheet skipped memory_saved_templates_decision.

[2026-10-16T13:15:23Z · bob-cli-8b.2] PROPOSED FOLLOW-UP: Add a glossary strand for Saved Template (alias template shelf) — the epic decision sheet skipped memory_saved_template_glossary.

[2026-10-16T13:15:34Z · bob-cli-8b.2] Implemented the capture-templates list/show/save/delete/clear protocol with parser-derived drafts and spans, help, completion, and docs. Verified cargo check; 2 protocol CLI tests; 17 shelf unit tests; the definition-validation unit test; 30 help tests; 109 completion tests; cargo fmt and git diff checks. epic-symbols reported none.

## Dependencies

- **Depends on:** [bob-cli-8b.1](bob-cli-8b.1.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8b.3](bob-cli-8b.3.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8b.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8b.2/README.md) | [bob-cli-8b.2](bob-cli-8b.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`31528a1`](https://github.com/bobs-org/bob-cli/commit/31528a11bc3162e80f4e40011af4de4cad64c995) | feat(capture-templates): add saved template protocol | [bob-cli-8b.2](bob-cli-8b.2.md) | 2026-10-16 09:16:36 EDT |
