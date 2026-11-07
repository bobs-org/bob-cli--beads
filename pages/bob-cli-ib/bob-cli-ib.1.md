# Bead: bob-cli-ib.1 — Cron data schema, partials, and per-machine rendering

[Bead Pages](../README.md) / [bob-cli-ib](README.md) / bob-cli-ib.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5w.linker.w1.md) · **Assignee:** `bob-cli-ib.1` · **Size:** medium
**Created:** 2026-11-07 12:43:37 EST · **Closed:** 2026-11-07 13:03:44 EST
**Plan:** [202611/crontab\_as\_code.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/crontab_as_code.md)

## Description

render: add the cron: schema, validating chezmoi partials, the per-machine managed.crontab and retire.crontab targets, and render tests on chezmoi v2.13.1 and the latest release.

## Notes

[2026-11-07T18:03:30Z · bob-cli-ib.1] PROPOSED FOLLOW-UP: chezmoi repo `just test-nvim` / `just test-hammerspoon` fail on athena before running any spec — `~/.luarocks/bin/nlua` busted 2.3.0 cannot load module busted.runner (package.path lacks the luarocks tree); reproduces identically on the clean base tree (f1da6b64), so `just test` is red locally while CI is unaffected.

[2026-11-07T18:03:34Z · bob-cli-ib.1] Handoff for sync/remote: partials are cron-validate (cron), cron-machine (hostname, cron), cron-block (machine, cron), cron-retire (machine, cron), plus cron-host (output=block|retire, hostname, cron) which the run_onchange hook can call twice for this host. Every partial validates first, even for unknown hosts. Gotcha: chezmoi v2.74.0 drops the middle segment of fail messages shaped "a: <word>: c" (prints "a: c"), so keep fail text to one "path: message" prefix. Renders are byte-identical on v2.13.1 and v2.74.0.

[2026-11-07T18:03:44Z · bob-cli-ib.1] render phase done in chezmoi repo: home/.chezmoidata.yaml cron: schema (version 1; athena/apollo/mac enrolled; MAILTO env; jobs []; retire {}), .chezmoitemplates cron-validate/cron-machine/cron-block/cron-retire/cron-host, dot_config/cron/managed.crontab.tmpl + retire.crontab.tmpl (one-liners), tests/bash/cron_render_test.sh (41 tests: real data for every machine+hostname, golden fixture, quoting round-trip through /bin/sh incl. ' % $(date +%F) pipe $HOME, disabled/[all]/sorted env, unknown host renders 0 bytes, zero-jobs markers-only, one fail test per validation rule). Verified: 41/41 pass on chezmoi v2.13.1 (athena nix) and v2.74.0 (latest release, checksum-verified); renders byte-identical across both; chezmoi apply into a temp dest creates only managed.crontab on enrolled hosts and nothing on unknown hosts on both versions; full-source chezmoi cat/diff on athena OK. just lint green; just test-bash 343/343, test-python 26/26; test-nvim/test-hammerspoon fail identically on clean base (busted.runner missing; follow-up noted).

## Dependencies

- **Blocks:** [bob-cli-ib.3](bob-cli-ib.3.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ib.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ib.1/README.md) | [bob-cli-ib.1](bob-cli-ib.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@d15ace3`](https://github.com/bbugyi200/dotfiles/commit/d15ace344c84b4d9c9bb8ab39a85305caf75f446) | feat(cron): add cron: data schema, validating partials, and per-machine crontab targets | [bob-cli-ib.1](bob-cli-ib.1.md) | 2026-11-07 13:04:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ib.1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-ib.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ib.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.land.md

<!-- sase:referenced-by:end -->
