# Bead: bob-cli-3j.7 — bash adapter and bash lifecycle support

[Bead Pages](../README.md) / [bob-cli-3j](README.md) / bob-cli-3j.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.46](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.46.md) · **Assignee:** `bob-cli-3j.7` · **Size:** medium
**Created:** 2026-10-02 11:06:16 EDT · **Closed:** 2026-10-02 13:50:15 EDT
**Plan:** [202610/bob\_shell\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_shell_completion.md)

## Description

bash: add the values-only bash adapter with COMP_LINE word reassembly and wordbreak-safe replies, wire bash into install/status/uninstall and verification, and cover it with real-bash tests.

## Notes

[2026-10-02T17:50:04Z · bob-cli-3j.7] PROPOSED FOLLOW-UP: Fix pre-existing clippy deny overly_complex_bool_expr in tests/cli/capture/pomodoro_name.rs:808 (|| true makes expression constant; untouched by bash phase, reproduces on clean HEAD)

[2026-10-02T17:50:15Z · bob-cli-3j.7] Bash adapter plus lifecycle wired and verified: real-bash COMPREPLY cases (cap, --format=j, colon-split @dev:, quoted, unicode, TEXT-empty, !dirs), bash install/status/uninstall and SHELL selection, just install-smoke and 81 completion tests pass; pre-existing clippy deny in pomodoro_name.rs recorded as follow-up

## Dependencies

- **Depends on:** [bob-cli-3j.4](bob-cli-3j.4.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3j.6](bob-cli-3j.6.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3j.8](bob-cli-3j.8.md) ◐ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3j.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3j.7/README.md) | [bob-cli-3j.7](bob-cli-3j.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5a60bd8`](https://github.com/bobs-org/bob-cli/commit/5a60bd8f7e91c94838166f8823155b22e8deab27) | feat(completion): add bash adapter and bash lifecycle support | [bob-cli-3j.7](bob-cli-3j.7.md) | 2026-10-02 13:51:29 EDT |
