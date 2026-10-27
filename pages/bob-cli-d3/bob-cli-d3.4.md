# Bead: bob-cli-d3.4 — Web overwrites repoint instead of clearing

[Bead Pages](../README.md) / [bob-cli-d3](README.md) / bob-cli-d3.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ao](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ao.md) · **Assignee:** `bob-cli-d3.4` · **Size:** medium
**Created:** 2026-10-27 11:21:28 EDT · **Closed:** 2026-10-27 13:36:57 EDT
**Plan:** [202610/web\_ref\_saved\_sources.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/web_ref_saved_sources.md)

## Description

web-overwrite-store: stage the new web store inside the overwrite transaction after capture instead of clearing source_markdown, keeping Clear for PDF URL and arXiv and as the fallback.

## Notes

[2026-10-27T17:36:57Z · bob-cli-d3.4] Web -f overwrite now stages the converted source view into the overwrite transaction (web_article / web_collection) after capture, repoints source_markdown, keeps the old store as history, and reuses unchanged bytes. Missing source views keep Clear with a warning; PDF URL and arXiv still Clear. Verified: overwrite_web store tests (repoint/reuse, clear fallback, frozen pointer, rollback, PDF URL clear, collection), markdown/local PDF store tests, web_source_store create tests, collection listen overwrite, execute store unit tests, just docs-check, cargo fmt, and clippy with the project deny set. Reviewer decision_record=no: no memory decision written. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-d3.3](bob-cli-d3.3.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-d3.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-d3.4/README.md) | [bob-cli-d3.4](bob-cli-d3.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bab568f`](https://github.com/bobs-org/bob-cli/commit/bab568fc200aec3785acab3021f55942dcb8d1f5) | feat(ref): stage web overwrite sources instead of clearing | [bob-cli-d3.4](bob-cli-d3.4.md) | 2026-10-27 13:39:03 EDT |
