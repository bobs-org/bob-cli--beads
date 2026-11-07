# Bead: bob-cli-ib.2 — Machine-agnostic job runner

[Bead Pages](../README.md) / [bob-cli-ib](README.md) / bob-cli-ib.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5w.linker.w1.md) · **Assignee:** `bob-cli-ib.2` · **Size:** small
**Created:** 2026-11-07 12:43:37 EST · **Closed:** 2026-11-07 13:06:40 EST
**Plan:** [202611/crontab\_as\_code.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/crontab_as_code.md)

## Description

cronrun: add ~/bin/cronrun, which derives the job environment at run time, guards overlaps, logs, records status, mails only failures, and offers a side-effect-free --dry-run.

## Notes

[2026-11-07T18:06:26Z · bob-cli-ib.2] NOTE for remote/sync phases: cronrun state lives in ~/.local/state/cron/ — <job>.log (+ .log.1, rotated past 1 MiB), <job>.status (job host pid start end exit; end/exit empty while running), <job>.lock (flock) and <job>.lock.d/pid (mkdir fallback, used on the Mac, which has no flock). Lock impl override: CRONRUN_LOCK_IMPL=flock|mkdir. `cronrun --dry-run <job> <cmd>` writes nothing and exits 1 when the first word does not resolve; usage errors exit 2. host= is `hostname -s` (Mac reports Kellys-MacBook-Pro, not the alias mac).

[2026-11-07T18:06:30Z · bob-cli-ib.2] PROPOSED FOLLOW-UP: chezmoi `just test` fails in non-interactive shells on athena because test-nvim cannot find busted.runner — busted is only on LUA_PATH after `eval "$(luarocks path --bin)"`; with that loaded every test recipe passes. The test-nvim recipe (or CI-parity docs) could load luarocks paths itself. Not caused by this phase; reproduces with no changes.

[2026-11-07T18:06:40Z · bob-cli-ib.2] Added chezmoi home/bin/executable_cronrun (cronrun [--dry-run] <job> <command>; bash 3.2-compatible, no jq/python) and tests/bash/cronrun_test.sh (18 tests): silent success writes log+status; failure prints summary + last 40 lines of this run and propagates the exit code; overlap skipped under flock and the mkdir fallback (stale and recycled pids broken); log rotates past the size cap; --dry-run never executes or writes state; runtime env set only when unset and only on Linux; profile sourcing and its failure logged; stdin is /dev/null; the lock fd is not inherited by children. Verified: 18/18 on athena (bash 5); 17 passed and 1 skipped (flock-only test) on the Mac under /bin/bash 3.2.57; real-HOME cron-like (env -i) dry-runs resolve pass_git_sync, bob, and the nvm-prefixed bob nightly command on athena (derived XDG_RUNTIME_DIR/DBUS/DISPLAY match the legacy hard-coded lines), and maybe_bob_highlights_sync and bob on the Mac, writing no state. shellcheck clean; just lint passes; test-nvim, test-hammerspoon, test-bash (319/319), and test-python all pass with luarocks paths loaded (see PROPOSED FOLLOW-UP).

## Dependencies

- **Blocks:** [bob-cli-ib.4](bob-cli-ib.4.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ib.6](bob-cli-ib.6.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ib.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ib.2/README.md) | [bob-cli-ib.2](bob-cli-ib.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@a2c680b`](https://github.com/bbugyi200/dotfiles/commit/a2c680bce7eb4b912d8d58453fee858672df0310) | feat(cron): add cronrun, the machine-agnostic cron job runner | [bob-cli-ib.2](bob-cli-ib.2.md) | 2026-11-07 13:07:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ib.2][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-ib.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ib.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.land.md

<!-- sase:referenced-by:end -->
