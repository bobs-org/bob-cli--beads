# Bead: bob-cli-6u.18.7.5 — Install the fixed bob and plugins on this host and the MacBook

[Bead Pages](../README.md) / [bob-cli-6u.18.7](bob-cli-6u.18.7.md) / bob-cli-6u.18.7.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.land.md) · **Assignee:** `bob-cli-6u.18.7.5` · **Size:** small
**Created:** 2026-10-12 20:32:25 EDT · **Closed:** 2026-10-12 21:47:24 EDT
**Plan:** [202610/prj\_line\_blocking\_land\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_land_audit_fixes.md)

## Description

rollout: bob then plugins on this host, then best-effort on the MacBook with a detached install; dry-run verification only; record versions and what Bryan still has to do.

## Notes

[2026-10-13T01:47:13Z · bob-cli-6u.18.7.5] Rollout record — HOST DONE: bob installed from master 12abfd7 via just install (exit 0). Reconcile dry-run with BOB_NOW=2026-10-12: exit 0, ok:true, empty plan (no prj_is_blocked adds/strips, no unblocked writes); without BOB_NOW it exits 1 only because UTC Oct-13 daily note does not exist yet (vault today is Oct-12 EDT) — environmental. Projects sync dry-run: exit 0, 85 projects, 0 updated, 0 warnings. Plugins from bob-plugins origin/master d34e078: sync exit 0 (0 copied, 16 unchanged), list shows 6 synced 0 drift (block-id-prompt 1.29.0, ledger-tools 1.49.0, nav-hotkeys 2.26.0, project-tasks 1.0.0, vim-surround 1.5.2, cycler 1.33.0). MACBOOK UNVERIFIED: link dropped repeatedly as warned; prior 6u.18 log showed INSTALL_EXIT=0 at b09612e; launched detached new-master install logging to /tmp/bob-rollout-install.log but link died before INSTALL_EXIT confirmed, so Mac plugins NOT synced. LEFT FOR BRYAN/LAND: on Mac check INSTALL_EXIT in that log, run both dry-runs, then bob plugins sync + list, reload plugins (or restart Obsidian), then pilot: Ctrl+Shift+P b on ^prj add/remove; schedule on ^prj and Ctrl+D; link gesture on resident of unblocked future-dated project; Alt+] on date-only [?] ^prj. No vault edits; no live reconcile/sync run.

[2026-10-13T01:47:24Z · bob-cli-6u.18.7.5] Host rollout verified: bob 12abfd7 installed, reconcile dry-run exit 0 empty plan (BOB_NOW=2026-10-12), sync dry-run exit 0 with 0 changes, 6 plugins synced 0 drift. MacBook detached install launched but link dropped before INSTALL_EXIT confirmed; Mac plugins not synced; remainder recorded in bead note.

## Dependencies

- **Depends on:** [bob-cli-6u.18.7.1](bob-cli-6u.18.7.1.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.18.7.2](bob-cli-6u.18.7.2.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.18.7.3](bob-cli-6u.18.7.3.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.18.7.4](bob-cli-6u.18.7.4.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.5/README.md) | [bob-cli-6u.18.7.5](bob-cli-6u.18.7.5.md) | 0 |
