# Bead: gh\_bobs-org\_\_bob-cli-2.1 — Shared note-task scanner

[Bead Pages](../README.md) / [gh\_bobs-org\_\_bob-cli-2](README.md) / gh\_bobs-org\_\_bob-cli-2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Assignee:** `gh_bobs-org__bob-cli-2.1` · **Size:** medium
**Created:** 2026-07-31 11:55:37 UTC · **Closed:** 2026-07-31 12:03:58 UTC
**Plan:** [202607/capture\_sub\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202607/capture_sub_bullets.md)

## Description

scan: add src/native/note_tasks.rs, a pure scanner that turns one note's Markdown into task records (line, indentation, status, description, block ID, section, child span, stale-safe ref digest), plus the small markdown.rs ATX-heading extraction it depends on.

## Notes

[2026-07-31T12:03:58Z · gh_bobs-org__bob-cli-2.1] Implemented the shared note-task scanner and ATX-heading refactor. Verified cargo fmt --check, git diff --check, cargo clippy --all-targets --all-features, focused note_tasks tests (7 passed), and the full cargo test suite (all passed).

[2026-07-31T12:04:43Z · gh_bobs-org__bob-cli-2.1] Finalizer verified the bead is closed with resolution done; formatting, diff checks, Clippy, focused scanner tests, and the full Rust test suite previously passed.

## Dependencies

- **Blocks:** [gh\_bobs-org\_\_bob-cli-2.2](gh_bobs-org__bob-cli-2.2.md) ◐

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.gh\_bobs-org\_\_bob-cli-2.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.gh_bobs-org__bob-cli-2.1/README.md) | [gh\_bobs-org\_\_bob-cli-2.1](gh_bobs-org__bob-cli-2.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed (UTC) |
|---|---|---|---|---|
| bob-cli | [`31a10c5`](https://github.com/bobs-org/bob-cli/commit/31a10c59c5c34dd0c8bd17377d7816ab1563db07) | feat(native): add shared note task scanner | [gh\_bobs-org\_\_bob-cli-2.1](gh_bobs-org__bob-cli-2.1.md) | 2026-07-31 12:04:56 |
