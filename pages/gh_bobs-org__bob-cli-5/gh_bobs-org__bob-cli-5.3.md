# Bead: gh\_bobs-org\_\_bob-cli-5.3 — Counted-session priority writes

[Bead Pages](../README.md) / [gh\_bobs-org\_\_bob-cli-5](README.md) / gh\_bobs-org\_\_bob-cli-5.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.s8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.s8/README.md) · **Assignee:** `gh_bobs-org__bob-cli-5.3` · **Size:** medium
**Created:** 2026-08-03 08:08:24 UTC · **Closed:** 2026-08-03 08:35:02 UTC
**Plan:** [202608/priority\_property.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/priority_property.md)

## Description

counted: extend the counted batch planner so N<Ctrl+Shift+P> applies one priority to every counted task while rolling an independent scheduled date per task.

## Notes

[2026-08-03T08:35:02Z · gh_bobs-org__bob-cli-5.3] Verified counted priority selection rolls one scheduled date per target, writes priority before a rightmost inline schedule, routes ^prj schedules to project frontmatter, applies Blocked/recovery decisions per rolled date, preserves label aggregation and stale-session guards, and emits one counted notice. npm test passed 263/263; npm run validate passed 6/6 plugins.

## Dependencies

- **Depends on:** [gh\_bobs-org\_\_bob-cli-5.2](gh_bobs-org__bob-cli-5.2.md) ✓
- **Blocks:** [gh\_bobs-org\_\_bob-cli-5.5](gh_bobs-org__bob-cli-5.5.md) ◐

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.gh\_bobs-org\_\_bob-cli-5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.gh_bobs-org__bob-cli-5.3/README.md) | [gh\_bobs-org\_\_bob-cli-5.3](gh_bobs-org__bob-cli-5.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed (UTC) |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@11ccbd5`](https://github.com/bobs-org/bob-plugins/commit/11ccbd520fb0eb6e3ae507f4be3a2dfa97f8818e) | feat(navigation): roll schedules for counted priority writes | [gh\_bobs-org\_\_bob-cli-5.3](gh_bobs-org__bob-cli-5.3.md) | 2026-08-03 08:36:12 |
