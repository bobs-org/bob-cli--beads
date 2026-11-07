# Bead: bob-cli-ib.3 — Local reconciler, hook, and offline cronctl commands

[Bead Pages](../README.md) / [bob-cli-ib](README.md) / bob-cli-ib.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5w.linker.w1.md) · **Assignee:** `bob-cli-ib.3` · **Size:** medium
**Created:** 2026-11-07 12:43:37 EST · **Closed:** 2026-11-07 14:00:34 EST
**Plan:** [202611/crontab\_as\_code.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/crontab_as_code.md)

## Description

sync: create cronctl with list, render, and check plus the marked-block sync reconciler, and the run_onchange hook that runs it when this machine's block changes.

## Notes

[2026-11-07T19:00:30Z · bob-cli-ib.3] Handoff for remote/agent-docs/migrate: home/bin/executable_cronctl is all functions with `main "$@"` last; every child reads </dev/null or a file. crontab ALWAYS gets its file on stdin (`crontab - <file`, also `crontab -n -`): Debian cron 3.0pl1 silently truncates crontab file arguments to 99 bytes (verified on athena: a long agent TMPDIR path made `crontab -n` open a truncated path), so a file argument could name a different file -- keep this in remote code. Reusable internals: cronctl_template <tmpl> <out> (returns 2 on a template fail = validation, 1 on chezmoi error), cronctl_resolve_local (sets cronctl_hostname/cronctl_machine; CRONCTL_HOSTNAME test hook), cronctl_find_chezmoi (CRONCTL_CHEZMOI, CHEZMOI_EXECUTABLE, PATH, then ~/.nix-profile/bin /opt/homebrew/bin /usr/local/bin ~/bin ~/go/bin ~/.local/bin), cronctl_read_crontab, cronctl_read_block, cronctl_build_candidate, cronctl_probe_native_check (Debian -n / cronie -T found by parsing `crontab -h`). Added a dry-run-only `sync --retire FILE` next to `--block FILE`, so `diff --source` can preview a checkout block AND its retire lines on a target. sync state: installed.block, backups/crontab.<UTC stamp> (20 kept), sync.lock (flock fd 8) or sync.lock.d/pid (CRONCTL_LOCK_IMPL, CRONCTL_LOCK_TIMEOUT default 60s); sync runs under umask 077. Offline tests are tests/bash/cronctl_offline_test.sh, so tests/bash/cronctl_test.sh stays free for remote. Mac facts (2026-11-07): its chezmoi source is at ec5ff17d with no cron partials yet, so `cronctl sync` there cannot resolve until apply pulls; Homebrew flock exists at /opt/homebrew/bin but is off the non-interactive PATH.

[2026-11-07T19:00:34Z · bob-cli-ib.3] sync phase done in the chezmoi repo: home/bin/executable_cronctl (list [--json] [--source], render <m> [--source], check [--source], sync [--dry-run [--block F] [--retire F]], help; --help on every command; exit 0/1/2) and .chezmoiscripts/run_onchange_after_sync_crontab.sh.tmpl (enrolled host: inert heredoc with its block + retire lines, cronctl sha256, then exec "$HOME/bin/cronctl" sync; unknown host: renders empty). sync follows plan steps 1-9: resolve via cron-machine (unknown host or missing managed.crontab warns, exits 0), lock (flock or mkdir with stale-pid break), read (no crontab = empty; any other -l failure exits 1), markers (0 pairs insert on top, 1 pair replace in place, else refuse), retire exact matches outside the block only, hand-edit warning vs installed.block, dry-run diff, backup (keep 20) + native syntax check (probed), re-read/rebuild once, install, read back, restore backup on mismatch, record installed.block + one-line summary. Tests: tests/bash/cron_sync_test.sh (34: every plan case incl. watchdog-line preservation, byte-identical no-op with no installer call, verify-failure restore, mkdir and flock lock paths, hook empty/enrolled/changes, mid-sync change rebuild, plus an end-to-end chezmoi apply -> hook -> sync test) and tests/bash/cronctl_offline_test.sh (16: list text/JSON, render, check incl. native check, help/usage, bash -s streaming with no stdin reads). Verified: all 109 cron tests pass on chezmoi v2.13.1 and v2.74.0 (athena, bash 5) and on the Mac under /bin/bash 3.2.57 with chezmoi v2.52.1; shellcheck + shfmt clean; just lint green; just test green (test-nvim/test-hammerspoon need `eval "$(luarocks path --bin)"` in non-interactive shells, as bob-cli-ib.2 noted). Rollout preview on athena (read-only): `render athena --source <checkout>` + `sync --dry-run --block`, and the default managed.crontab dry run, both only add the 3-line block (markers + MAILTO) above the existing lines and remove nothing; `check` on the real data is ok on all 3 machines with Debian `crontab -n`. A post-commit `chezmoi update -a --force` monitor is staged to perform and verify the first real install on athena.

## Dependencies

- **Depends on:** [bob-cli-ib.1](bob-cli-ib.1.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ib.4](bob-cli-ib.4.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ib.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.3.md) | [bob-cli-ib.3](bob-cli-ib.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@0b8e738`](https://github.com/bbugyi200/dotfiles/commit/0b8e73884bdf1cc28d753e37fb74c3d04b26d389) | feat(cron): add cronctl list/render/check/sync and the crontab sync hook | [bob-cli-ib.3](bob-cli-ib.3.md) | 2026-11-07 14:01:55 EST |
