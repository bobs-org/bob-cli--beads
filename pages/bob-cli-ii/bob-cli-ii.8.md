# Bead: bob-cli-ii.8 — Chezmoi gmail config and the bob-gmail-sync cron job

[Bead Pages](../README.md) / [bob-cli-ii](README.md) / bob-cli-ii.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19q.md) · **Assignee:** `bob-cli-ii.8` · **Size:** small
**Created:** 2026-11-07 17:21:22 EST · **Closed:** 2026-11-08 18:54:05 EST
**Plan:** [202611/gmail\_sync\_reply\_watch.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_reply_watch.md)

## Description

cron: add Bryan's gmail block (route prefixes # and +, three reply-wait days) to the chezmoi bob config and a Mac bob-gmail-sync job at 7,22,37,52 to the cron data, then document the slot in bob-cli.

## Notes

[2026-11-08T23:53:40Z · bob-cli-ii.8] PROPOSED FOLLOW-UP: just docs-check lint fails on clean tree — docs/reference/mac-capture/{capture-panel,keyboard,protocol}.md exceed the 6000-word reference budget (6088/6060/6014 words); unrelated to this phase, which only touched docs/vault-git-sync.md

[2026-11-08T23:54:05Z · bob-cli-ii.8] cron phase done: gmail block (route_prefixes #/+, reply_wait_days 3, writer left commented) in chezmoi bob config; Mac bob-gmail-sync job at 7,22,37,52 with enabled:false (cron_enabled=no) in cron data; slot documented in docs/vault-git-sync.md. Verified: cronctl check ok, diff mac renders the disabled job, config YAML parses and matches bob gmail.sync schema with pull fallbacks. docs-check lint failure is pre-existing on the clean tree (recorded as PROPOSED FOLLOW-UP). Mac convergence staged via monitor py38ce; TCC failure expected until bob-cli-if resolves.

## Dependencies

- **Depends on:** [bob-cli-ii.4](bob-cli-ii.4.md) ✓ · ⧖ 2026-11-07
- **Depends on:** [bob-cli-ii.5](bob-cli-ii.5.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.8.md) | [bob-cli-ii.8](bob-cli-ii.8.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ad2298d`](https://github.com/bobs-org/bob-cli/commit/ad2298d44d9810beb721db6085a1a92dfa361795) | docs(vault-sync): document mac bob-gmail-sync maintenance slot | [bob-cli-ii.8](bob-cli-ii.8.md) | 2026-11-08 18:59:07 EST |
| chezmoi | [`chezmoi@d227de1`](https://github.com/bbugyi200/dotfiles/commit/d227de13589dfeb6696846dd9541917cfff6f49e) | feat(gmail): add disabled mac bob-gmail-sync cron slot and config | [bob-cli-ii.8](bob-cli-ii.8.md) | 2026-11-08 18:59:39 EST |
