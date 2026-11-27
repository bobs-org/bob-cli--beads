# Bead: bob-cli-re.1 — Make the clipboard SIGINT test independent of inherited signal disposition

[Bead Pages](../README.md) / [bob-cli-re](README.md) / bob-cli-re.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r8.land.md) · **Assignee:** `bob-cli-re.1` · **Size:** small
**Created:** 2026-11-27 15:31:19 EST · **Closed:** 2026-11-27 15:51:33 EST
**Plan:** [202611/task\_bead\_burndown\_3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_3.md)

## Description

clipboard-signal: fix the inherited-SIGINT test failure in chezmoi and close bob-cli-rd.

## Notes

[2026-11-27T20:51:33Z · bob-cli-re.1] Completed clipboard-signal phase: run_doctor now resets inherited ignored SIGINT before execing Bash while preserving the actual doctor execution and signal/restore assertions. Verified the focused SIGINT test normally and with inherited SIG_IGN, full clipboard file (32/32), just test-bash (635/635; 3141 assertions), and git diff --check. Closed scoped task bob-cli-rd; no epic-symbol entries remained.

## Dependencies

- **Blocks:** [bob-cli-re.2](bob-cli-re.2.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-re.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-re.1.md) | [bob-cli-re.1](bob-cli-re.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@378cb6c`](https://github.com/bbugyi200/dotfiles/commit/378cb6c9e56064a53d57a722d68c02a924b3e23b) | fix(tests): reset inherited SIGINT in clipboard test runner | [bob-cli-re.1](bob-cli-re.1.md) | 2026-11-27 15:53:47 EST |
