# Bead: bob-cli-b.1 — Shared note-task scanner

[Bead Pages](../README.md) / [bob-cli-b](README.md) / bob-cli-b.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bryanbugyi34@gmail.com` · **Assignee:** `bob-cli-b.1` · **Size:** medium
**Created:** 2026-07-31 07:55:37 EDT · **Closed:** 2026-07-31 08:03:58 EDT
**Plan:** [202607/capture\_sub\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202607/capture_sub_bullets.md)

## Description

scan: add src/native/note_tasks.rs, a pure scanner that turns one note's Markdown into task records (line, indentation, status, description, block ID, section, child span, stale-safe ref digest), plus the small markdown.rs ATX-heading extraction it depends on.

## Notes

[2026-07-31T12:03:58Z · bob-cli-b.1] Implemented the shared note-task scanner and ATX-heading refactor. Verified cargo fmt --check, git diff --check, cargo clippy --all-targets --all-features, focused note_tasks tests (7 passed), and the full cargo test suite (all passed).

[2026-07-31T12:04:43Z · bob-cli-b.1] Finalizer verified the bead is closed with resolution done; formatting, diff checks, Clippy, focused scanner tests, and the full Rust test suite previously passed.

## Dependencies

- **Blocks:** [bob-cli-b.2](bob-cli-b.2.md) ✓
