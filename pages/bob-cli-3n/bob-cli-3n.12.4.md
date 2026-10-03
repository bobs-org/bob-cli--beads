# Bead: bob-cli-3n.12.4 — Fix the navigation-hotkeys dependency writer across notes

[Bead Pages](../README.md) / [bob-cli-3n.12](bob-cli-3n.12.md) / bob-cli-3n.12.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.land.md) · **Assignee:** `bob-cli-3n.12.4` · **Size:** medium
**Created:** 2026-10-02 23:24:08 EDT · **Closed:** 2026-10-02 23:45:28 EDT
**Plan:** [202610/task\_dep\_links\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_fixes.md)

## Description

nav-writer-fix: await cross-note preparation, load or tolerate every linked note, check link uniqueness vault-wide, fix the same-note +id batch, ADJ-8 recovery, counted line shifts, undo grouping, and stale checks, and add async plugin-level tests.

## Notes

[2026-10-03T03:45:28Z · bob-cli-3n.12.4] nav-writer-fix done: async txn awaited (abort-before-commit), existing-link notes loaded/tolerated (deleted-target removal works), vault-wide link form via vaultFiles+linkpath resolver, same-note batch +id stamped in working copy, ADJ-8 recovery over vault snapshot incl. daily note, counted vault writes bottom-up, single+batch id writes folded to one undo group, counted CURRENT removal, stale-editor + not-on-line refusals. Verified: new test-navigation-dependencies-writer.cjs 12/12, npm test 1303/1303, validate 6/6, bob-cli just all green, manifest 1.56.0 deployed to vault.

## Dependencies

- **Blocks:** [bob-cli-3n.12.5](bob-cli-3n.12.5.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.4/README.md) | [bob-cli-3n.12.4](bob-cli-3n.12.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b61727a`](https://github.com/bobs-org/bob-cli/commit/b61727abf00e5d64f9a4008cc779aa55b429dc5a) | docs(deps): pin removeDependency not-on-line refusal in contract S9 | [bob-cli-3n.12.4](bob-cli-3n.12.4.md) | 2026-10-02 23:46:50 EDT |
