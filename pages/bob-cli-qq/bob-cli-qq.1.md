# Bead: bob-cli-qq.1 — Cabinet gate, model, session state, provider registry, and the view collector

[Bead Pages](../README.md) / [bob-cli-qq](README.md) / bob-cli-qq.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6m.linker.w0.md) · **Assignee:** `bob-cli-qq.1` · **Size:** medium
**Created:** 2026-11-26 16:09:02 EST · **Closed:** 2026-11-26 19:24:02 EST
**Plan:** [202611/property\_card\_cabinets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_cabinets.md)

## Description

kit: add the cabinet-owned `cabinetsPreview` gate. Add the frozen kind table with canonical ranks, roles, and defaults; bottom-up numbering; session state per (path, kind) with rename/delete carry; the content-provider registry; the view-scoped cabinet collector; a role-aware `_` fold facade; and one toggle router. Also add the go-live dependency edges onto the gating sibling go-lives and COORDINATION notes.

## Notes

[2026-11-26T22:24:40Z · bob-cli-qq.1--1] VERIFICATION: monitored npm test passed (10,093 passed, 0 failed, 5 skipped; performance suite 26/26). The full sync deployed bob-ledger-tools 1.170.0 from source 319862a cleanly, and the vault reports it synced. Full sync exited 1 only on bob-articles, bob-command-mode, and bob-navigation-hotkeys, whose vault bundles are stamped to unlanded workspace-10 build 0bae838; fetch showed no upstream changes for those plugins and the workspace-10 agents are done. No -F was used; awaiting direction on whether to replace those unrelated protected bundles or keep them and use the scoped sync result for closeout.

[2026-11-27T00:24:02Z · bob-cli-qq.1--6] VERIFICATION: npm run build passed; npm test passed (10,127 passed, 0 failed, 5 skipped; performance suite 26/26). The three authorized protected-plugin syncs completed, then ordinary full sync succeeded (2 copied, 32 unchanged), deploying bob-ledger-tools 1.170.0. sase bead epic-symbols bob-cli-qq.1 reported no remaining entries.

## Dependencies

- **Blocks:** [bob-cli-qq.4](bob-cli-qq.4.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.1.md) | [bob-cli-qq.1](bob-cli-qq.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@9c1123b`](https://github.com/bobs-org/bob-plugins/commit/9c1123bdf6c224d1e5cefa54ad5e5135070a907e) | feat(cabinets): add gated cabinet kit and view state | [bob-cli-qq.1](bob-cli-qq.1.md) | 2026-11-26 17:08:09 EST |
