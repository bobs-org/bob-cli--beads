# Bead: bob-cli-ib.5 — Crontab skill, memory note, README, and alias cleanup

[Bead Pages](../README.md) / [bob-cli-ib](README.md) / bob-cli-ib.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5w.linker.w1.md) · **Assignee:** `bob-cli-ib.5` · **Size:** small
**Created:** 2026-11-07 12:43:37 EST · **Closed:** 2026-11-07 15:30:43 EST
**Plan:** [202611/crontab\_as\_code.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/crontab_as_code.md)

## Description

agent-docs: teach agents the read and write flow through a global /crontab skill and reference memory note, document the human flow, and retire legacy cron aliases.

## Notes

[2026-11-07T20:30:22Z · bob-cli-ib.5] PROPOSED FOLLOW-UP: repair athena's busted/nlua toolchain for the chezmoi repo — `just test-nvim` and `just test-hammerspoon` both die at startup with "module 'busted.runner' not found" (~/.luarocks busted 2.3.0-1 via ~/.luarocks/bin/nlua) before any spec runs; environmental, independent of this phase (no Lua touched); no existing task bead found.

[2026-11-07T20:30:26Z · bob-cli-ib.5] PROPOSED FOLLOW-UP: chezmoi tests/bash/poseidon_chezmoi_isolation_test.sh still fails 2 cases ("Mac ignores poseidon files", "Cargo config renders only on athena") after 9430387a; same failure bob-cli-ib.4 recorded as reproducing on the clean base; all other 432 bashunit tests pass with this phase's changes; no existing task bead found.

[2026-11-07T20:30:38Z · bob-cli-ib.5] Handoff for migrate: the /crontab skill source is home/sase/skills/crontab.md (read it from the chezmoi checkout until deployed); its write flow stages `sase monitor start --reason ... --timeout 15m --start-status 'APPLYING CRONTAB' --stop-status 'APPLIED CRONTAB' --next '<checkout>/home/bin/executable_cronctl status <machines> ...' -- <checkout>/home/bin/executable_cronctl apply <machines>` (flags checked against sase monitor start --help). Remote cronrun dry run: `ssh -o BatchMode=yes <m> "bash -s -- --dry-run <job> '<command>'" < <checkout>/home/bin/executable_cronrun` (verified locally via bash -s). sase skill init is hard-wired to ~/.local/share/chezmoi/home and only deploys committed, landed sources, so the 7 per-provider copies and the 7 .sase-skills-manifest.json entries were produced with the generator's exact transform; a temp-HOME run of the installed sase over a copy of this tree reported all 168 targets current, `skill init --check`/`--diff` clean, and prepare_skill_manifest would write nothing (macro_set_sha256 recomputed by sase itself; the baseline hash reproduced first). Gotcha: a plain YAML description must not contain 'cron: ' (colon-space), or the frontmatter fails to parse and the skill silently stops registering.

[2026-11-07T20:30:43Z · bob-cli-ib.5] Done in the chezmoi linked repo: added the global /crontab skill (home/sase/skills/crontab.md) teaching the read flow (status/list/render/diff/logs), the write flow (sase repo open → edit cron: data → check/diff --source → cronrun --dry-run → staged post-commit cronctl apply monitor → /sase_final), and the rules; generated its 7 per-provider SKILL.md copies plus manifest entries, verified byte-exact by the installed sase in a temp HOME (168/168 targets current, manifest no-op). Created reference memory home/sase/memory/crontab.md (decision crontab_memory_note) and added a one-line [[crontab.md]] link to tailnet.md (decision tailnet_memory_link); both links resolve via sase memory show; home memory README re-rendered with sase's own renderer. Added a ## Crontabs section to README.md. Repointed vcron to 'cronctl edit' and deleted vab/vdb/vwb/vmb (bash -n and zsh -n clean). Verified: just lint passes; just test-bash 432/434 (2 known poseidon failures that reproduce on the clean base, see bob-cli-ib.4 note); just test-python 26/26; test-nvim/test-hammerspoon cannot start locally (busted.runner missing; follow-up noted). Live read-only check with the checkout's cronctl: check ok for 3 machines, status --all = athena in_sync, apollo pending (source behind origin), mac pending (asleep), exit 3.

## Dependencies

- **Depends on:** [bob-cli-ib.4](bob-cli-ib.4.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ib.6](bob-cli-ib.6.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ib.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.5.md) | [bob-cli-ib.5](bob-cli-ib.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@16701bf`](https://github.com/bbugyi200/dotfiles/commit/16701bfa8745723d040a8b8f701c9631b8adea86) | feat(cron): add the /crontab skill, crontab memory note, and Crontabs README section | [bob-cli-ib.5](bob-cli-ib.5.md) | 2026-11-07 15:31:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ib.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.land.md

<!-- sase:referenced-by:end -->
