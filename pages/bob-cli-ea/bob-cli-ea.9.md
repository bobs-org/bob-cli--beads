# Bead: bob-cli-ea.9 — Mac rollout, config, and handoff

[Bead Pages](../README.md) / [bob-cli-ea](README.md) / bob-cli-ea.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2w.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2w.linker.w0.md) · **Assignee:** `bob-cli-ea.9` · **Size:** small
**Created:** 2026-10-29 19:40:04 EDT · **Closed:** 2026-10-30 03:49:49 EDT
**Plan:** [202610/bob\_gcal\_daily\_events.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_gcal_daily_events.md)

## Description

rollout: add the gcal config block and (when chosen) the Mac LaunchAgent in chezmoi, reword the gtd_daily calendar checklist row, update and check the Mac best-effort, and hand Bryan the short login checklist.

## Notes

[2026-10-30T07:49:30Z · bob-cli-ea.9] Rollout handoff — Bryan's login checklist (Mac was unreachable over ssh, so on-Mac steps are still yours):

1. In Cloud Console, enable the Calendar API and confirm the consent screen is External and In production.
2. On the Mac, run `bob gcal login`, or `bob gcal login -c <client json>`. Approve the Keychain prompt the first time the LaunchAgent runs. (Needs: bob at a master build including gcal sync, and the chezmoi change below deployed via `chezmoi update`.)
3. Run `bob gcal sync -d`, then `bob gcal sync`.
4. Run `bob gcal doctor` on apollo, which reports the Mac as writer. (apollo config still needs the gcal block uncommented for this check to be meaningful.)
5. Colour privacy: recolour one invitation and ask its organizer whether their copy changed. If it did, keep `gcal.colors` empty.
6. Close `bob.md ^sync-gcal-meets` when happy.

Landed this phase: commented `gcal:` block in chezmoi home/dot_config/bob/config.yml (account, writer kellys-macbook-pro, root meet, calendars [primary], colors {}, tentative context) plus new home/Library/LaunchAgents/com.bbugyi.bob-gcal-sync.plist (bob gcal sync -q, StartInterval 300, RunAtLoad, same HOME/PATH as vault-sync agent, logs to /var/tmp/com.bbugyi.bob-gcal-sync.{out,err}). Chezmoi changes left UNCOMMITTED in the linked clone for the land agent to review; live chezmoi source (~/.local/share/chezmoi) untouched. Vault: reworded the open gtd_daily #pre row to drop the @EVENT half, committed under the sync lock as 7cb7ab69. Mac best-effort NOT done: ssh mac timed out twice; still needs bob update, chezmoi update, `bob gcal doctor`, and `launchctl bootstrap gui/$(id -u) ~/Library/LaunchAgents/com.bbugyi.bob-gcal-sync.plist`. Note: PATH reused from vault-sync agent covers /Users/bbugyi/bin, /opt/homebrew/bin etc.; if doctor reports gog missing on the Mac, prepend gog's dir to the plist PATH. Glossary + all three gcal decision records already written by earlier phases; no memory edits made.

[2026-10-30T07:49:49Z · bob-cli-ea.9] Rollout phase done and verified: commented gcal config block + com.bbugyi.bob-gcal-sync LaunchAgent added in chezmoi (uncommitted, for land-agent review); gtd_daily #pre row reworded and committed under the sync lock (7cb7ab69); plist is well-formed XML differing from vault-sync agent in exactly the 4 intended fields; config.yml still parses with gcal absent; no epic-symbol leftovers; glossary + 3 gcal decision records already present from earlier phases. Mac best-effort not done (ssh mac timed out twice) — on-Mac steps recorded in bead notes handoff.

## Dependencies

- **Depends on:** [bob-cli-ea.1](bob-cli-ea.1.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-ea.3](bob-cli-ea.3.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-ea.7](bob-cli-ea.7.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-ea.8](bob-cli-ea.8.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ea.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ea.9/README.md) | [bob-cli-ea.9](bob-cli-ea.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@1374445`](https://github.com/bbugyi200/dotfiles/commit/13744456df8e16ada7c30b7166dd3a6d72c4cce0) | feat(gcal): add chezmoi gcal config block and Mac sync LaunchAgent | [bob-cli-ea.9](bob-cli-ea.9.md) | 2026-10-30 03:51:09 EDT |
