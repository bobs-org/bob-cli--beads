# Bead: bob-cli-nu.8 — GTD rows, guide, glossary, and coordination

[Bead Pages](../README.md) / [bob-cli-nu](README.md) / bob-cli-nu.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.8` · **Size:** medium
**Created:** 2026-11-20 05:59:33 EST · **Closed:** 2026-11-20 13:35:18 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

## Description

adopt: convert the open gtd_daily.md rows that hold bob commands (the Bank row only once the Mac's bob has -D), add the vimrc comment and the bob-cli guide section, apply the accepted memory decisions, and leave coordination notes on bob-cli-nc and bob-cli-nn.

## Notes

[2026-11-20T18:34:27Z · bob-cli-nu.8] PROPOSED FOLLOW-UP: Convert the gtd_daily.md Bank row once the Mac's bob has -D — the gate could not be checked: on 2026-11-20 ssh mac timed out and Tailscale showed kellys-macbook-pro offline (apollo's bob already lists -D, --delete). When `ssh mac 'bob bank import --help'` lists `-D, --delete`, edit only the open **Bank** row (never Done & Canceled), replacing `` `bob bank import ~/Downloads/*.qfx && rm ~/Downloads/*.qfx` `` with `` `run[Import bank files]: bob bank import -D ~/Downloads/*.qfx` `` and nothing else. That exact chip already parses with bob-chips 0.14.0 and resolves ready against apollo's bob __catalog (one step, entry bank-import, argv [bank, import, -D, ~/Downloads/*.qfx]); -D's digest-gated delete replaces the rm, which chips never run. Then ask Bryan to sync bob on the Mac (chezmoi update / bob plugins sync) if it is behind.

[2026-11-20T18:34:34Z · bob-cli-nu.8] PROPOSED FOLLOW-UP: Catalog TTY metadata so interactive commands refuse up front in Command Mode and command chips — bob __catalog's gcal-ack entry (effect writes, policy preview-first, hosts [], no TTY marker) lets Command Mode resolve `run: bob gcal ack -n 7` as ready (verified 2026-11-20 with bob-command-mode 0.4.0's resolver on bob 0.5.0's catalog), so a chip or the sheet's Ctrl+Enter would start the explicit ack walk with no terminal. Add a catalog field such as tty: required for the interactive walk (non --dry-run gcal ack), and have Command Mode's resolve refuse those steps with a reason like "needs a terminal" (chip shows ⊘; the sheet refuses or offers Copy). Until then the gtd_daily Ack row stays a copy chip (`copy: bob gcal ack -n 7` in a terminal).

[2026-11-20T18:34:41Z · bob-cli-nu.8] PROPOSED FOLLOW-UP: just docs-check fails on the clean base (master bb91c370): lint reports docs/reference/vault-format.md over budget at 6016 words (cap 6000 for reference/), so docs-check stops before the build/link gates. The overflow came in with bb91c370 (bob-cli-o6.3, album title key and bob albums tidy); no bead tracks it. Fix: trim at least 16 words from vault-format.md, or move the albums section to its own reference page under an approved plan with URLs preserved. nu.8 ran bob-docs build, links (offline, fragments), and urls separately; all passed with its guide and glossary changes.

[2026-11-20T18:34:48Z · bob-cli-nu.8] PROPOSED FOLLOW-UP: obsidian_vimrc.md comment "Mod+Shift+Y makes or edits a copy chip in any mode." has been stale since the author phase (bob-cli-nu.7): Make or edit chip now makes, converts, and edits both kinds. The adopt phase was limited to adding exactly one comment line, so it left this line alone; reword it to "Mod+Shift+Y makes or edits a copy or command chip in any mode." (vault-only edit; commit just obsidian_vimrc.md).

[2026-11-20T18:35:18Z · bob-cli-nu.8] Adopt done. Preflight: bob plugins list on apollo shows bob-chips 0.14.0 (keymap+author) and bob-command-mode 0.4.0 (engine) synced+enabled. Census (plan rg) found exactly the planned rows, plus the copy-chip period prompts, which stay as they are. Vault gtd_daily.md open rows only (Done & Canceled untouched): #sync -> `run[Sync calendar and inboxes]: bob gcal sync -n 2 && bob gkeep pull && bob gmail sync`; #init -> `run: bob task reconcile`; Ack (gtd_ack_copy_chip=yes) -> run `copy: bob gcal ack -n 7` in a terminal. Bank left unchanged: Mac offline (ssh timeout, Tailscale offline), follow-up with exact replacement recorded. obsidian_vimrc.md gains the one ⌘↵ comment line under the gy comments. vault-sync auto-committed just those two files (4b3169fd0, ca5b89793; both on origin/master). Verify: a Node script loading bob-plugins bob-chips helpers (runChipScanLine/copyChipScanLine) and bob-command-mode cmCreateApi.resolve over live `bob __catalog --protocol 1` (bob 0.5.0) parsed the edited rows: both run chips resolve ready with payloads equal to the intended lines (gcal-sync, gkeep-pull, gmail-sync; task-reconcile), Ack is a copy chip with payload `bob gcal ack -n 7`; the Bank -D chip also resolves ready. `bob task reconcile --dry-run -f json` touches no gtd_daily row. bob-cli: docs/guides/run-bob-from-obsidian.md gains "Run a command from a note" (run:/labels, click, Shift+Click, ⌘↵ + keycap, && and bob-run sequences, confirm floor, attack-surface bounds, copy-only notes, never completes the task) + Bob Chips links; no other guide step was wrong. Memory (accepted only): new glossary:command-chip strand; glossary:copy-chip closing sentence names [[command-chip]]; decisions record not written (reviewer said no). sase memory init + just docs-gen regenerated AGENTS/CLAUDE/README/glossary.md/docs/reference/glossary.md. just docs-check fails only on pre-existing vault-format.md 6016/6000 (same on clean base; follow-up recorded); bob-docs lint (no guide warning), strict build, offline links with fragments, and urls all pass. Coordination notes left on bob-cli-nc and bob-cli-nn. Follow-ups: Bank row, catalog TTY metadata, vault-format budget, stale vimrc Mod+Shift+Y comment. Report: Bryan should reload Obsidian; other desktop hosts need chezmoi update + bob plugins sync before chips run there.

## Dependencies

- **Depends on:** [bob-cli-nu.6](bob-cli-nu.6.md) ✓ · ⧖ 2026-11-20
- **Depends on:** [bob-cli-nu.7](bob-cli-nu.7.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.8/README.md) | [bob-cli-nu.8](bob-cli-nu.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2443e0a`](https://github.com/bobs-org/bob-cli/commit/2443e0a4e1580f1ce956ef8a576caa1ba2d8ac66) | docs(chips): add the command-chip guide section and glossary term | [bob-cli-nu.8](bob-cli-nu.8.md) | 2026-11-20 13:36:33 EST |
