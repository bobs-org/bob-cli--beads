# Bead: bob-cli-ib.4 — Fleet commands for status, diff, apply, logs, run, and edit

[Bead Pages](../README.md) / [bob-cli-ib](README.md) / bob-cli-ib.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5w.linker.w1.md) · **Assignee:** `bob-cli-ib.4` · **Size:** medium
**Created:** 2026-11-07 12:43:37 EST · **Closed:** 2026-11-07 15:06:35 EST
**Plan:** [202611/crontab\_as\_code.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/crontab_as_code.md)

## Description

remote: add SSH-streamed fleet commands so any machine can read live state and converge any machine to a pushed revision without a bootstrap step.

## Notes

[2026-11-07T20:06:11Z · bob-cli-ib.4] Handoff for agent-docs/migrate: cronctl now has status [--all|<m>...] [--json] [--all-schedulers], diff <m> [--source DIR], apply (--all|<m>...) [--rev REV], logs <job> [--machine M] [-n N], run <job> [--machine M], and edit (help on each; exit 0/1/2/3 per the contract). Remote targets get `ssh -o BatchMode=yes -o ConnectTimeout=8 <alias> bash -s -- __state|__apply|__logs|__run ...` with the caller script on stdin (run passes the job command and cron.env as quoted shell assignments ahead of the script, never on the ssh command line); the local machine runs the same routine in a subshell, no SSH. Routines answer key=value lines, ">section" + "|"-prefixed lines, and end=1; the caller classifies. status states: pending = unreachable, source behind/diverged from origin, or ~/.config/cron not matching the target source (not applied); unmanaged = applied but no block; drifted = cronctl sync would change the table; identity_mismatch; failed; in_sync. "cron.retire can be deleted" prints only when every machine with retire lines was read in that run and none remain (otherwise "cron.retire is still needed: <why>"), so run it with --all. run takes the command from the caller local source data and refuses disabled jobs or machines the job does not target. The script now ends in `{ main "$@"; exit; }` because chezmoi rewrites ~/bin/cronctl in place when its temp dir is on another device. Live fleet 2026-11-07 (read-only): apollo in_sync; athena pending only because ~/.local/share/chezmoi is behind origin (block already live; diff athena = no changes); mac pending (source current, never applied: no managed.crontab, 3 legacy */15 lines outside). All origins are git@github.com and apollo/mac can ls-remote over non-interactive SSH, so apply pull works there.

[2026-11-07T20:06:16Z · bob-cli-ib.4] PROPOSED FOLLOW-UP: fix chezmoi tests/bash/poseidon_chezmoi_isolation_test.sh (2 failures on the clean base) — "Mac ignores poseidon files" expects .cargo/config.toml in the Mac ignore list and "Cargo config renders only on athena" expects an empty Mac render, but commit 9430387a (feat(cargo): lean dev debug info on the MacBook) now renders a Mac cargo config; reproduced identically on a clean worktree of 0b8e7388, unrelated to cronctl; no existing task bead found.

[2026-11-07T20:06:35Z · bob-cli-ib.4] Verified: chezmoi repo home/bin/executable_cronctl gains status/diff/apply/logs/run/edit with SSH-streamed internal routines (script on stdin, children </dev/null, local machine via subshell, exit 255 = pending) and new tests/bash/cronctl_test.sh (23 tests: apply with no prior ~/bin/cronctl, unreachable -> pending + exit 3, unpushed --rev refused, identity_mismatch, local target uses no SSH, status states incl. retire lines still present and cron.retire can be deleted, --json via python3 -m json.tool, diff output, logs tail across rotation, run via cronrun with cron env, edit, stdin-leak guard plus a negative proof). All 132 cron tests pass on chezmoi v2.13.1 and v2.74.0 (athena), and the 73 cronctl/sync tests pass on the Mac (/bin/bash 3.2.57, chezmoi v2.52.1, mkdir lock). shellcheck + shfmt -i 2 clean; just lint green; just test green except 2 poseidon_chezmoi_isolation_test failures that reproduce identically on the clean base (recorded as PROPOSED FOLLOW-UP). Real fleet read-only: cronctl status --all = apollo in_sync, athena pending (source behind origin; block live), mac pending (never applied); cronctl diff athena = block: no changes.

## Dependencies

- **Depends on:** [bob-cli-ib.2](bob-cli-ib.2.md) ✓ · ⧖ 2026-11-07
- **Depends on:** [bob-cli-ib.3](bob-cli-ib.3.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ib.5](bob-cli-ib.5.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ib.6](bob-cli-ib.6.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ib.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.4.md) | [bob-cli-ib.4](bob-cli-ib.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@102e823`](https://github.com/bbugyi200/dotfiles/commit/102e8238aa24840afa0783d5d497e1bbbde4f66e) | feat(cron): add cronctl fleet commands status, diff, apply, logs, run, and edit | [bob-cli-ib.4](bob-cli-ib.4.md) | 2026-11-07 15:07:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ib.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.land.md

<!-- sase:referenced-by:end -->
