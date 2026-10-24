# Bead: bob-cli-bc.11 — Obsidian Pomodoro themes manager

[Bead Pages](../README.md) / [bob-cli-bc](README.md) / bob-cli-bc.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2c.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2c.linker.w1.md) · **Assignee:** `bob-cli-bc.11` · **Size:** medium
**Created:** 2026-10-24 07:52:22 EDT · **Closed:** 2026-10-24 14:24:34 EDT
**Plan:** [202610/pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_themes.md)

## Description

obsidian-manager: add the Bob Pomodoro themes command to browse, hide, pin, inspect, and rename themes with a previewed rename.

## Notes

[2026-10-24T18:24:34Z · bob-cli-bc.11] Obsidian Pomodoro themes manager landed in bob-plugins nav: FilteredPickerModal manager (Active/Hidden/Possible duplicates/All on Tab, collision hints on top, today/hidden/pinned/exempt/hue/reappeared badges), Ctrl+D hide, Enter actions (rename/color/hide/occurrences with r/c/h/o jump keys when filter empty), previewed one-commit rename (saves touched notes, refuses on failed save, --merge support), 8-hue+Auto color (1-8/a), vault occurrence scan opening the daily note at the entry, mobile Notice. Verified: new test file 13/13 pass; full npm test 3578/3579 (sole failure a 16ms-budget timing assertion in dependencies-stage entry-and-view that passes 23/23 on rerun — environmental flake, unrelated file); build, docs inventory, docs-check green; rename dry-run JSON shape confirmed against real bob on a scratch vault; deployed via bob plugins sync -p bob-navigation-hotkeys.

## Dependencies

- **Depends on:** [bob-cli-bc.10](bob-cli-bc.10.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bc.13](bob-cli-bc.13.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bc.6](bob-cli-bc.6.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bc.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.11/README.md) | [bob-cli-bc.11](bob-cli-bc.11.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1202c6a`](https://github.com/bobs-org/bob-plugins/commit/1202c6a0b1b47cdd973eb5d97d19ff3407bfb596) | feat(navigation): add Obsidian Pomodoro themes manager | [bob-cli-bc.11](bob-cli-bc.11.md) | 2026-10-24 14:26:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.2][1] | Identify the existing owner and task evidence for clean-base just check failures | 1 |
| read-by | [agent:bob-cli-bc.11][2] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-an.6.6.6.5.6.5.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.11/README.md

<!-- sase:referenced-by:end -->
