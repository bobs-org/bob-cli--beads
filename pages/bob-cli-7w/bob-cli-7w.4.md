# Bead: bob-cli-7w.4 — Template-aware completion and rewrite

[Bead Pages](../README.md) / [bob-cli-7w](README.md) / bob-cli-7w.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1j.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1j.linker.w0.md) · **Assignee:** `bob-cli-7w.4` · **Size:** small
**Created:** 2026-10-15 14:04:18 EDT · **Closed:** 2026-10-15 16:23:41 EDT
**Plan:** [202610/bulk\_capture\_templates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bulk_capture_templates.md)

## Description

complete: gate `capture-complete` and `capture-rewrite` for template drafts, offer the `template:` header candidate, finish the protocol docs, and apply the memory decisions.

## Notes

[2026-10-15T20:09:57Z · bob-cli-7w.4--1] PROPOSED FOLLOW-UP: Add the declined decision record for explicit @template: expansion before parsing — memory_template_decision was set to no in the epic decisions.

[2026-10-15T20:23:41Z · bob-cli-7w.4--2] Template-aware completion and rewrite verified: capture-complete gates template drafts (header/rows/placeholders return empty, body pickers run against masked draft, template: candidate offered first for prefix and last for empty query), capture-rewrite leaves template drafts untouched, protocol docs updated. Fixed dead-code deny: Candidates::is_empty now used by render.rs. just check passes (fmt+clippy+all tests); template-focused tests 27/27 pass; no epic-symbol leftovers; glossary Bulk Capture strand already covers template drafts.

## Dependencies

- **Depends on:** [bob-cli-7w.3](bob-cli-7w.3.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7w.5](bob-cli-7w.5.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7w.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7w.4.md) | [bob-cli-7w.4](bob-cli-7w.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3f2b775`](https://github.com/bobs-org/bob-cli/commit/3f2b775a1d52eba29c2300ea96e6ae2ab9c33db0) | feat(capture-complete): gate template drafts in completion and rewrite | [bob-cli-7w.4](bob-cli-7w.4.md) | 2026-10-15 16:24:58 EDT |
