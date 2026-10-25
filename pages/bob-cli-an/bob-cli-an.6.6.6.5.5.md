# Bead: bob-cli-an.6.6.6.5.5 — Make RefsLibraryTests record the ref scan argv again

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5](bob-cli-an.6.6.6.5.md) / bob-cli-an.6.6.6.5.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.5` · **Size:** medium
**Created:** 2026-10-24 07:37:07 EDT · **Closed:** 2026-10-24 08:49:50 EDT
**Plan:** [202610/backlog\_batch5\_highlights\_render\_pomodoro\_name\_duplicate\_link\_mac\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch5_highlights_render_pomodoro_name_duplicate_link_mac_ci.md)

## Description

mac-refs-scan-ci: resolve bob-cli-b7 by restoring a single recorded ref scan in RefsLibraryTests so macOS CI is green aside from other recorded owners.

## Notes

[2026-10-24T12:49:50Z · bob-cli-an.6.6.6.5.5--2] Updated RefsLibraryTests to require the recorded argv  for each scan.  passed 1,555 tests with 0 failures (monitor p8ftwd9qjber; ToolRun 5e67f9c7662d040555ce76d35f3a4206). Mac scratch validation vwjkg8wsqtwh completed successfully: bundle and package checks passed, and every macOS test target type-checked against the documented stub. No --epic-symbol entries for bob-cli-an.6.6.6.5.5. reported no entries.

[2026-10-24T12:50:03Z · bob-cli-an.6.6.6.5.5--2] Evidence correction: RefsLibraryTests now asserts the recorded argv ref scan -a -w -f json. just portable-check passed 1,555 tests with 0 failures (monitor p8ftwd9qjber; ToolRun 5e67f9c7662d040555ce76d35f3a4206). Mac scratch validation vwjkg8wsqtwh completed with exit 0: bundle and package checks passed, and every macOS test target type-checked against the documented stub. epic-symbols reported no entries for this phase.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.5.md) | [bob-cli-an.6.6.6.5.5](bob-cli-an.6.6.6.5.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.5--2][1] | Need the assigned phase scope and current status before recording its completion | 2 |
| read-by | [agent:bob-cli-an.6.6.6.5.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.5.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.land.md

<!-- sase:referenced-by:end -->
