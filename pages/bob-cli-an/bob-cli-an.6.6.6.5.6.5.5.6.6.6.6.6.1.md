# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1 — Stop vault sync from tracking deployed bob-articles files

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1` · **Size:** medium
**Created:** 2026-10-26 10:47:09 EDT
**Plan:** [202610/backlog\_batch13\_vault\_integrity\_and\_perf\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch13_vault_integrity_and_perf_1.md)

## Description

vault-plugin-ignore: resolve bob-cli-cd by fixing the source-of-truth ignore rule and coordinating untracking/redeployment across hosts; never untrack on one host alone.

## Notes

[2026-10-26T14:59:09Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1] BASELINE: Canonical ignore source is the vault git file ~/bob/.gitignore (tracked in the vault repo). chezmoi does not manage it; bob-plugins is only the deploy source. Custom-plugin block lists block-id-prompt, bob-command-mode, bob-ledger-tools, bob-navigation-hotkeys, bob-project-tasks, bob-vim-surround, task-status-cycler and omits bob-articles. git check-ignore -v .obsidian/plugins/bob-articles/main.js is empty. git ls-files lists main.js, manifest.json, styles.css. Comment still cites ~/projects/github/bbugyi200/bob-plugins. Hosts athena, apollo, and mac are all at vault SHA 4f5ce0ac with those three files tracked and bob-articles 0.2.1 synced/enabled. bob-vault-sync.service is active on athena and apollo. Mac LaunchAgent com.bbugyi.bob-vault-sync is loaded with StartInterval 15s (idle between runs). Live-vault repair will go through a Bryan-approved sase gate so untrack is not done on one host alone. Target task bob-cli-cd stays open for the lander.

[2026-10-26T15:02:18Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1] PROPOSED FOLLOW-UP: Make bob plugins sync maintain the vault custom-plugin gitignore block from the plugin roster — a newly added plugin can be tracked again if only ~/bob/.gitignore is hand-edited.

[2026-10-26T15:03:21Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1] FIX pending Bryan gate: coordinated ignore+untrack+redeploy on athena, apollo, and mac (stop vault-sync first, add .obsidian/plugins/bob-articles/ to ~/bob/.gitignore, git rm --cached the three tracked files, vault-sync commit/push, plugins sync on each host, restart watchers). Never untrack on one host alone.

## Dependencies

- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1.md) | 0 |
