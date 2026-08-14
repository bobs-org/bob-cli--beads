# Bead: bob-cli-n.2 — Caret-correct link intelligence in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-n](README.md) / bob-cli-n.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.00w.f0.f0.w0.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.00w.f0.f0.w0.w0.md) · **Assignee:** `bob-cli-n.2` · **Size:** medium
**Created:** 2026-08-14 11:05:27 EDT · **Closed:** 2026-08-14 11:52:16 EDT
**Plan:** [202608/obsidian\_link\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/obsidian_link_completion.md)

## Description

caret_integration: update the linked bob-mac-capture app to decode the additive contract, drive completion from the real AttributedTextSelection insertion point, preserve selection and IME state while applying highlights, accept server-provided replacements with a restored caret, and harden cancellation, stale-response, Unicode, and failure behavior with fixture-backed Swift tests.

## Notes

[2026-08-14T15:52:06Z · bob-cli-n.2] PROPOSED FOLLOW-UP: Mac validation gate — run bob-mac-capture just format-lint/build/test on a host with Swift/Xcode; this runner lacks swift so those commands fail with exit 127 before compiling.

[2026-08-14T15:52:16Z · bob-cli-n.2] Implemented bob-mac-capture caret integration for additive wikilink metadata, warnings, cursor_after acceptance, real AttributedTextSelection caret scheduling, selection-preserving highlighting, stale cursor/range rejection, range-selection completion suppression, independent preview, and fixture-backed Swift tests. Verified bash -n Tests/Fixtures/fake-bob and git diff --check in linked repo. Attempted just format-lint, just build, and just test; all fail before validation because swift is not installed on this runner (exit 127).

[2026-08-14T15:53:35Z · bob-cli-n.2] Verified bash -n Tests/Fixtures/fake-bob and git diff --check passed; just format-lint/build/test were attempted but blocked because swift is unavailable on this runner.

## Dependencies

- **Depends on:** [bob-cli-n.1](bob-cli-n.1.md) ✓ · ⧖ 2026-08-14
- **Blocks:** [bob-cli-n.3](bob-cli-n.3.md) ◐ · ⧖ 2026-08-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-n.2/README.md) | [bob-cli-n.2](bob-cli-n.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@3f9b70c`](https://github.com/bobs-org/bob-mac-capture/commit/3f9b70c7c9d8fa6d51a38bd309eab1ad9b23d8c5) | feat: support caret-aware wikilink completions | [bob-cli-n.2](bob-cli-n.2.md) | 2026-08-14 12:00:40 EDT |
