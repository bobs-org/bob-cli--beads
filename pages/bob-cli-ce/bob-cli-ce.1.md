# Bead: bob-cli-ce.1 — Make the colon key safe and keep the new plugin out of vault git

[Bead Pages](../README.md) / [bob-cli-ce](README.md) / bob-cli-ce.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5c.linker.w0.md) · **Assignee:** `bob-cli-ce.1` · **Size:** small
**Created:** 2026-10-26 10:35:52 EDT · **Closed:** 2026-10-26 10:44:00 EDT
**Plan:** [202610/bob\_colon\_command\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_colon_command_mode.md)

## Description

vault-prep: turn all 16 recursive `nmap … :bob_*<CR>` lines in the vault vimrc into `nnoremap`, add `nnoremap g: :`, and gitignore `.obsidian/plugins/bob-command-mode/` in the vault, without binding `:` yet.

## Notes

[2026-10-26T14:44:00Z · bob-cli-ce.1] vault-prep done: 16 nmap->nnoremap in ~/bob/obsidian_vimrc.md plus header comment and nnoremap g: :; no ':' binding. .gitignore gains .obsidian/plugins/bob-command-mode/ (check-ignore verified); bob-articles omission left for bob-cli-cd. Landed via vault sync as 402d1f7b, pushed (local==origin/master). Verified loadVimCommands passes lines unchanged to CodeMirror handleEx; nnoremap is CodeMirror-builtin (plugin only tracks map/nmap/noremap for chords). Smoke list for Bryan after vimrc reload: -, ]s, [s, [S, ]S, Z, !, \\ behave as before and g: opens the ex line. Agents cannot drive the Obsidian UI; no UI pass claimed.

## Dependencies

- **Blocks:** [bob-cli-ce.9](bob-cli-ce.9.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ce.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.1/README.md) | [bob-cli-ce.1](bob-cli-ce.1.md) | 0 |
