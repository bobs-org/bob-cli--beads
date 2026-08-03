# Bead: bob-cli-e.3 — Counted-session priority writes

[Bead Pages](../README.md) / [bob-cli-e](README.md) / bob-cli-e.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.s8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.s8/README.md) · **Assignee:** `bob-cli-e.3` · **Size:** medium
**Created:** 2026-08-03 04:08:24 EDT · **Closed:** 2026-08-03 04:35:02 EDT
**Plan:** [202608/priority\_property.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/priority_property.md)

## Description

counted: extend the counted batch planner so N<Ctrl+Shift+P> applies one priority to every counted task while rolling an independent scheduled date per task.

## Notes

[2026-08-03T08:35:02Z · bob-cli-e.3] Verified counted priority selection rolls one scheduled date per target, writes priority before a rightmost inline schedule, routes ^prj schedules to project frontmatter, applies Blocked/recovery decisions per rolled date, preserves label aggregation and stale-session guards, and emits one counted notice. npm test passed 263/263; npm run validate passed 6/6 plugins.

## Dependencies

- **Depends on:** [bob-cli-e.2](bob-cli-e.2.md) ✓
- **Blocks:** [bob-cli-e.5](bob-cli-e.5.md) ✓

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-e.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-e.3/README.md) | [bob-cli-e.3](bob-cli-e.3.md) | 0 |
