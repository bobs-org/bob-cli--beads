# Bead: bob-cli-go.10.1.1 — Shared transfer lexer and shell redirect guard

[Bead Pages](../README.md) / [bob-cli-go.10.1](bob-cli-go.10.1.md) / bob-cli-go.10.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-go.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.10.md) · **Assignee:** `bob-cli-go.10.1.1` · **Size:** medium
**Created:** 2026-11-04 01:50:44 EST · **Closed:** 2026-11-04 02:37:32 EST
**Plan:** [202611/capture\_transfer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_transfer.md)

## Description

transfer-lexer: implement the pure span-aware transfer recognizer and its complete grammar vectors, plus the stdout regular-file shell guard. Keep the recognizer test-gated until the next phase wires both consumers; do not bump grammar yet.

## Notes

[2026-11-04T07:37:20Z · bob-cli-go.10.1.1] PROPOSED FOLLOW-UP: clean base 3741ce2e fails cargo check with missing successor_labels in MergeContext initializers (relations_merge.rs:143, task_merge/command.rs:420); just check blocked identically on clean tree, no tracking task bead found

[2026-11-04T07:37:32Z · bob-cli-go.10.1.1] transfer-lexer done: pure span-aware recognizer in capture_language/transfer.rs (test-gated) with 17 table tests covering 4 destinations, partial needs, arrow spacing, extra text, children, suffix/marker, destination marker, duplicates, destination-is-source, escaping, UTF-8/CRLF, quotes, code/prose/blockquote; shell guard in capture/shell_guard.rs wired before planning with 3 unit + 2 CLI tests (refuses @c redirect before mutation, normal files/pipes pass); fmt and clippy gates pass; just check blocked by pre-existing clean-base MergeContext successor_labels breakage recorded as follow-up; no grammar bump, no CaptureKind change

## Dependencies

- **Blocks:** [bob-cli-go.10.1.2](bob-cli-go.10.1.2.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.10.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.10.1.1/README.md) | [bob-cli-go.10.1.1](bob-cli-go.10.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e00f907`](https://github.com/bobs-org/bob-cli/commit/e00f90748429329d00b3bed3a7c0513c39e3b06d) | feat(capture): add transfer lexer and shell redirect guard | [bob-cli-go.10.1.1](bob-cli-go.10.1.1.md) | 2026-11-04 02:39:07 EST |
