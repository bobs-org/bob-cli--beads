# Bead: bob-cli-j.1 — Authoritative capture parser endpoint

[Bead Pages](../README.md) / [bob-cli-j](README.md) / bob-cli-j.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.005](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.005.md) · **Assignee:** `bob-cli-j.1` · **Size:** medium
**Created:** 2026-08-13 20:32:34 EDT · **Closed:** 2026-08-13 21:16:09 EDT
**Plan:** [202608/bob\_mac\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/bob_mac_capture.md)

## Description

grammar: refactor bob-cli's existing capture parser into a span-aware reusable model and add the read-only bob capture-parse command with stable JSON, diagnostics, CLI/docs wiring, and Rust plus ported Hammerspoon grammar coverage.

## Notes

[2026-08-14T01:15:54Z · bob-cli-j.1] PROPOSED FOLLOW-UP: parse_pomodoro_route_token's block-ID error message claims '_' is accepted, but is_block_id (collect_done::is_block_id_byte) only allows A-Z, a-z, 0-9, '-' — so '@dev:foo_bar' is rejected with a message saying '_' is legal. Preserved byte-for-byte in the grammar refactor (src/native/capture_language.rs); decide whether the message or the character-class check is the bug and fix the one that's wrong.

[2026-08-14T01:16:09Z · bob-cli-j.1] Refactored bob-cli's capture grammar into src/native/capture_language.rs (span-aware, shared by both bob capture and the new command; extract_terminal_markers genericized over a ParseToken trait so execution and editor parsing share one implementation). Added read-only 'bob capture-parse [-f|--format human|json] [--] [TEXT]...' returning schema_version 1 JSON (ok, input, body, mode, route, section, block_id, needs, spans, diagnostics) plus styled human output; never touches BOB_DIR/clipboard/filesystem (verified with a nonexistent BOB_DIR + '%' marker). Wired into native.rs/runner.rs (alphabetically sorted SUBCOMMANDS, top-level help examples), justfile install-smoke, and README (command table + full contract docs). Added unit tests in capture_language.rs (Unicode/CRLF byte offsets, every span/mode/needs combination, parse/execution equivalence) including ported behavioral fixtures from chezmoi's tests/hammerspoon/task_capture_spec.lua (picker state-machine tests intentionally excluded — not grammar), plus CLI integration tests in tests/cli.rs (help surfaces, JSON/human output, usage errors, UTF-8 byte-offset assertions). Independently verified: cargo fmt --check, cargo clippy --all-targets --all-features (0 new warnings; 3 pre-existing warnings in untouched files), cargo test (464 lib + 271 CLI integration + 27/31/1 other, all passing), just install-smoke, and git diff --check all pass. Manually spot-checked capture-parse output against the plan's worked JSON example (byte-for-byte match) and confirmed bob capture's execution error text/exit codes are unchanged for the same invalid-marker inputs that capture-parse now reports as non-blocking diagnostics. Filed one PROPOSED FOLLOW-UP note on this bead: a pre-existing message/validation mismatch in the Pomodoro block-ID error text (claims '_' is accepted; the character class doesn't allow it), preserved byte-for-byte since fixing it is out of this phase's scope.

[2026-08-14T01:16:38Z · bob-cli-j.1] Refactored capture grammar into new shared, span-aware src/native/capture_language.rs module (generic extract_terminal_markers shared by executor and new editor path). Added read-only 'bob capture-parse' command reporting mode/route/section/block_id/needs/spans/diagnostics as versioned JSON. Verified independently: cargo fmt --check, cargo clippy --all-targets --all-features (0 errors, only 3 pre-existing warnings in untouched files), cargo test (464 lib + 271 CLI integration tests passing), just install-smoke, git diff --check all clean. Manually confirmed capture-parse output matches plan's worked JSON example byte-for-byte and bob capture execution behavior is unchanged.

## Dependencies

- **Blocks:** [bob-cli-j.2](bob-cli-j.2.md) ◐ · ⧖ 2026-08-13
- **Blocks:** [bob-cli-j.3](bob-cli-j.3.md) ◐ · ⧖ 2026-08-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j.1/README.md) | [bob-cli-j.1](bob-cli-j.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8b04200`](https://github.com/bobs-org/bob-cli/commit/8b0420004ca5ac0a57617c1d131ac04777c5c511) | feat(capture): add capture-parse command and shared capture grammar module | [bob-cli-j.1](bob-cli-j.1.md) | 2026-08-13 21:17:22 EDT |
