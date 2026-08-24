# Bead: bob-cli-13.2 — bob capture-rewrite and the bare @@ absorption rule

[Bead Pages](../README.md) / [bob-cli-13](README.md) / bob-cli-13.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0cv](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0cv.md) · **Assignee:** `bob-cli-13.2` · **Size:** medium
**Created:** 2026-08-24 15:01:18 EDT · **Closed:** 2026-08-24 15:49:11 EDT
**Plan:** [202608/capture\_global\_destination\_anywhere.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/capture_global_destination_anywhere.md)

## Description

rewrite: add the `bob capture-rewrite` subcommand that turns a bare `@@` into `@@<payload>` by absorbing the item's local destination marker (or the draft's other declaration), deleting the source token and returning edits, cursor, and a human summary.

## Notes

[2026-08-24T19:48:59Z · bob-cli-13.2] PROPOSED FOLLOW-UP: capture_global_destination_anywhere.md Vocabulary section for "Local destination marker" omits the three-component sub-bullet-with-section form (@route+block-id#section) — I treated it as non-absorbable (same "cannot take a section" A5-style notice family as @route#Section) since Rule A1 only names @<route> and @<route>+<block-id> as absorbable, but the design doc never explicitly classifies this form either way.

[2026-08-24T19:49:11Z · bob-cli-13.2] Implemented bob capture-rewrite (Rules A1-A6): rewrite_draft + DraftRewrite/TextEdit/RewriteRule/LocalDestinationMarker in capture_language.rs, new src/native/capture_rewrite.rs subcommand (human+JSON schema_version 1, purely lexical, no --bob-dir), wired into native.rs/runner.rs alphabetically between capture-parse and capture-sections, justfile install-smoke, docs/capture.md new section + Contents entry, README.md command table + capture-command mention. Added 12 rewrite_draft unit tests (local/sub-bullet/leading/child-line absorption, declaration-only-line absorption, all 4 Rule A5 notice forms, Rule A6 two-marker no-op, no-bare-@@ no-op, cursor first/last selection, idempotence, no-double-space + clean re-parse, multi-byte char-boundary safety), 10 capture_rewrite.rs CLI/JSON unit tests, and 9 tests/cli.rs integration tests plus updates to the two all-subcommands help-listing tests. Verified: cargo fmt --check, cargo clippy --all-targets --all-features (no new warnings), cargo test (full workspace: 667 lib + 387 cli + others, 0 failures).

## Dependencies

- **Depends on:** [bob-cli-13.1](bob-cli-13.1.md) ✓ · ⧖ 2026-08-24
- **Blocks:** [bob-cli-13.3](bob-cli-13.3.md) ◐ · ⧖ 2026-08-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-13.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-13.2/README.md) | [bob-cli-13.2](bob-cli-13.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`025dc06`](https://github.com/bobs-org/bob-cli/commit/025dc0610d2cb6cd7123165fe2db8a3a988bf3c7) | feat(capture): add capture-rewrite and the bare @@ absorption rule | [bob-cli-13.2](bob-cli-13.2.md) | 2026-08-24 15:49:41 EDT |
