# Bead: bob-cli-r7.4 — Editing headroom on the near-cap bob-plugins reference pages

[Bead Pages](../README.md) / [bob-cli-r7](README.md) / bob-cli-r7.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1h4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1h4.md) · **Assignee:** `bob-cli-r7.4` · **Size:** medium
**Created:** 2026-11-27 10:16:12 EST · **Closed:** 2026-11-27 12:22:36 EST
**Plan:** [202611/task\_bead\_burndown\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_1.md)

## Description

plugin-docs-headroom: per docs_headroom, condense the bob-navigation-hotkeys and bob-ledger-tools reference pages to at least 300 words under the cap, or cancel both beads, then close bob-cli-ob and bob-cli-il.

## Notes

[2026-11-27T17:22:36Z · bob-cli-r7.4--1] Verified scoped docs gates and counts: bob-navigation-hotkeys.md 5638/6000; bob-ledger-tools.md 5688/6000; plugin-apis.md 7524/8000 (upstream 4dd95d52 added 14 words vs the earlier count, still under cap). Both requested gates passed: BOB_CLI_DIR=/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16 npm --prefix /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins run docs:check; BOB_DOCS_BOB_PLUGINS_DIR=/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/linked/bob-plugins just docs-check. epic-symbols reported no entries.\n\nDeployment closeout: fetched and fast-forwarded bob-plugins to 4dd95d52, then the documented clean sync refused the Ledger Tools overwrite. The vault has version 1.172.8 stamped from a dirty workspace-17 build at 17a64fa; current committed 1.172.8 bundle differs (deployed editor route uses ==, current source uses bare = with a habit guard). No overwrite or force flag was used; Bryan approval is being requested separately.

## Dependencies

- **Depends on:** [bob-cli-r7.3](bob-cli-r7.3.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-r7.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r7.4.md) | [bob-cli-r7.4](bob-cli-r7.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7de181e`](https://github.com/bobs-org/bob-plugins/commit/7de181e4211c2255a3de9efcbe6bc8c5b76f259e) | docs: restore headroom in plugin references | [bob-cli-r7.4](bob-cli-r7.4.md) | 2026-11-27 12:00:12 EST |
