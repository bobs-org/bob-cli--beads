# Bead: bob-cli-e6.11 — Link to today retypes and Alt+Enter keeps the type

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.11` · **Size:** medium
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-29 22:36:50 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

link-picker-retype: replace the block-id-prompt theme write guards with the retype rule, turn link once into the keep-type merge, and update footers, toasts, and docs.

## Notes

[2026-10-30T02:36:50Z · bob-cli-e6.11] Link-to-today write path uses planRetype: Enter retypes (set/clear/consistent/container), Alt+Enter keep-type merges destination names, Tab cycles composite tabPick, shown revalidation remains, dropped shown/caps guards retype from live suggestFor. Verified node tests for theme-write, picker-view (D10 footers, PLAN/LATER/Tab), picker/link runtime notices, link-picker-api tabPick, plugin-build, docs:inventory:check, and docs:check. Deployed block-id-prompt via bob plugins sync --repo this checkout -p block-id-prompt -F. Fragments 077/078/085/120 stay ≤1000. epic-symbols: none leftover.

## Dependencies

- **Blocks:** [bob-cli-e6.16](bob-cli-e6.16.md) ◐ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.8](bob-cli-e6.8.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.11/README.md) | [bob-cli-e6.11](bob-cli-e6.11.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.11][1] | Need the phase scope, notes, and design file after compaction | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.11/README.md

<!-- sase:referenced-by:end -->
