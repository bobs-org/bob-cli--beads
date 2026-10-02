# Bead: bob-cli-3l.1 — Positional Work Log bullets in bob-cli

[Bead Pages](../README.md) / [bob-cli-3l](README.md) / bob-cli-3l.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.47](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.47.md) · **Assignee:** `bob-cli-3l.1` · **Size:** medium
**Created:** 2026-10-02 15:17:48 EDT · **Closed:** 2026-10-02 15:47:21 EDT
**Plan:** [202610/unnumbered\_close\_log\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/unnumbered_close_log_bullets.md)

## Description

bob-cli: lex unnumbered first-level bullets (all or none), assign them in order to the close's worked tasks (lexically when `<N>`/`*<P>` is typed, against the running session otherwise), make `CloseLogEntry.index` optional with a positional origin, report resolved indices in `bob capture` JSON, add the new diagnostics, and update help, docs, and tests.

## Notes

[2026-10-02T19:43:42Z · bob-cli-3l.1] PROPOSED FOLLOW-UP: just lint fails on tests/cli/capture/pomodoro_name.rs:808 clippy::overly_complex_bool_expr (|| true) — reproduces identically on the clean base tree; see also bead bob-cli-v (Eliminate existing bob-cli clippy warnings)

[2026-10-02T19:47:21Z · bob-cli-3l.1] Closed by explicit `sase stitch create -B close` after create_commit landed 923adb8 ("feat(capture): accept unnumbered =x Work Log bullets resolved positionally"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-3l.1` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-3l.2](bob-cli-3l.2.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3l.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3l.1/README.md) | [bob-cli-3l.1](bob-cli-3l.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`923adb8`](https://github.com/bobs-org/bob-cli/commit/923adb8a7e70a233d2910ef9658405fe5db064d9) | feat(capture): accept unnumbered =x Work Log bullets resolved positionally | [bob-cli-3l.1](bob-cli-3l.1.md) | 2026-10-02 15:46:58 EDT |
