# Bead: bob-cli-3n.12.9.6.5 — Reinstall bob and resync the plugins with the remaining fixes

[Bead Pages](../README.md) / [bob-cli-3n.12.9.6](bob-cli-3n.12.9.6.md) / bob-cli-3n.12.9.6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.12.9.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.9.land.md) · **Assignee:** `bob-cli-3n.12.9.6.5` · **Size:** small
**Created:** 2026-10-03 02:54:24 EDT · **Closed:** 2026-10-03 03:50:46 EDT
**Plan:** [202610/task\_dep\_links\_landing\_remaining.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_landing_remaining.md)

## Description

rollout: reinstall bob and sync the plugins on athena and apollo, update the MacBook best effort, dry-run the hooks against the real vault and explain every dependency count, and record versions and what is left for Bryan.

## Notes

[2026-10-03T07:50:40Z · bob-cli-3n.12.9.6.5] Rollout results (2026-10-03 ~04:00 EDT). athena: bob rebuilt from 50350db via cargo install --path . --locked --force; plugins synced from bob-plugins 6648a2c — nav 1.63.0, ledger-tools 1.22.0, cycler 1.23.0, block-id-prompt 1.21.0; bob plugins list: 6 synced, 0 drift. apollo: pulled bob-cli 72964be..50350db and bob-plugins 2bd875d..6648a2c, cargo installed, plugins synced — 6 synced, 0 drift (apollo runs no hooks). MacBook: UNREACHABLE — tailscale offline, 3x ssh timeout over ~10min; left for Bryan below. Real-vault dry run: REFUSED as anticipated — 2026/20261003.md does not exist yet (retried twice); no live pass run. Vault read-only census: 16 notes carry DEPENDS ON lines (33 lines), 0 label-only lines (R9 fix changes no live data), 49 dependsOn fields, 4 notes with blockquoted #task (unsupported, untouched). Deployed-binary proof (scratch vaults, both machines): Pomodoro-linked dep task projects to Next; label-only line yields line_removed + dependsOn removed + dependency_field_ids_dropped (R9 fix live in both binaries). LEFT FOR BRYAN: (1) MacBook — when reachable: check ~/.cargo/.crates2.json install kind, git pull + cargo install --path . --locked --force (or reinstall from git+ source), pull + sync bob-plugins, verify with ssh mac ~/.cargo/bin/bob task-status-hooks --dry-run -f json | jq has(dependency_projection_updates); (2) reload the four plugins in each running Obsidian (athena + apollo vaults); (3) create today daily note, then run real-vault dry run and review counts; (4) pilot checklist: prerequisites from two projects, remove a completed one, follow a chip in Live Preview + Reading view (incl. two tasks sharing one prerequisite), edit with another note unsaved, optionally bind Edit task dependencies chord.

[2026-10-03T07:50:46Z · bob-cli-3n.12.9.6.5] Rollout done except known-unreachable MacBook. athena: bob@50350db installed, 4 plugins synced (nav 1.63.0, ledger-tools 1.22.0, cycler 1.23.0, block-id-prompt 1.21.0), 0 drift. apollo: pulled to same commits, installed, 0 drift. Both binaries proven on scratch vaults (Next projection; R9 line_removed path). Real-vault dry run refused — 20261003.md not yet created (retried); vault census (16 notes/33 lines, 0 label-only) recorded in phase notes. No epic-symbol leftovers. MacBook offline + pilot checklist left for Bryan per phase notes.

## Dependencies

- **Depends on:** [bob-cli-3n.12.9.6.1](bob-cli-3n.12.9.6.1.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3n.12.9.6.2](bob-cli-3n.12.9.6.2.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3n.12.9.6.3](bob-cli-3n.12.9.6.3.md) ✓ · ⧖ 2026-10-03
- **Depends on:** [bob-cli-3n.12.9.6.4](bob-cli-3n.12.9.6.4.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.9.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.9.6.5/README.md) | [bob-cli-3n.12.9.6.5](bob-cli-3n.12.9.6.5.md) | 0 |
