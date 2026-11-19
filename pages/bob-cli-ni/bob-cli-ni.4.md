# Bead: bob-cli-ni.4 — Copy card C row

[Bead Pages](../README.md) / [bob-cli-ni](README.md) / bob-cli-ni.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5g.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5g.linker.w0.md) · **Assignee:** `bob-cli-ni.4` · **Size:** medium
**Created:** 2026-11-19 10:05:34 EST · **Closed:** 2026-11-19 12:33:04 EST
**Plan:** [202611/copy\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/copy_chips.md)

## Description

copycard: add a C row to the Mod+Y Copy card in Bob Navigation Hotkeys that copies the chip at the cursor through api.copyChips.

## Notes

[2026-11-19T17:33:04Z · bob-cli-ni.4] Added the Mod+Y C row backed by api.copyChips, with clear disabled states when the plugin or a resolvable chip is unavailable. Verified npm run build, npm run build:check, npm run docs:check (447 passed, 1 skipped), git diff --check, and deployed the workspace plugin build with bob plugins sync --repo.

## Dependencies

- **Depends on:** [bob-cli-ni.2](bob-cli-ni.2.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-ni.6](bob-cli-ni.6.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ni.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ni.4/README.md) | [bob-cli-ni.4](bob-cli-ni.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@0a4a91f`](https://github.com/bobs-org/bob-plugins/commit/0a4a91f81227999524e6bcb4760d30f47eaa94a6) | feat(navigation): add copy-chip row to Copy card | [bob-cli-ni.4](bob-cli-ni.4.md) | 2026-11-19 12:34:54 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ni.4][1] | Need the phase scope, recorded notes, epic decisions, and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ni.4/README.md

<!-- sase:referenced-by:end -->
