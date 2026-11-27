# Bead: bob-cli-qq.10.3 — Footer overlay narrow clipping, Areas title row, and runner console errors

[Bead Pages](../README.md) / [bob-cli-qq.10](bob-cli-qq.10.md) / bob-cli-qq.10.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.g7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.g7.md) · **Assignee:** `bob-cli-qq.10.3` · **Size:** small
**Created:** 2026-11-27 09:12:20 EST · **Closed:** 2026-11-27 09:42:35 EST
**Plan:** [202611/finish\_property\_card\_cabinets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_property_card_cabinets.md)

## Description

polish: make the armed footer overlay shed `esc` and truncate nouns at 420 px without clipping either end. Drop the duplicated callout title row in the Areas cabinet body. Make the cabinets runner fail on console.error, including during Live Preview cursor motions.

## Notes

[2026-11-27T14:38:26Z · bob-cli-qq.10.3--1] PROPOSED FOLLOW-UP: Refresh the generated docs inventory for docs/bob-ledger-tools.md and docs/index.md — npm test reaches docs:inventory:check and fails because these regions are stale on the clean repo; bob-cli-qq.10.6 already owns the docs overhaul and regeneration.

[2026-11-27T14:42:27Z · bob-cli-qq.10.3--1] PROPOSED FOLLOW-UP: Investigate navigation snooze-add-resnooze mutation vector — test:unit fails reproducibly in isolation because snooze-add-resnooze-replaces-history retains an extra woken row in the daily postimage; this is unrelated to the cabinets polish changes.

[2026-11-27T14:42:35Z · bob-cli-qq.10.3--1] Verified focused suites (63/63), build check, and standalone test:perf (26/26); npm test is blocked by the known stale docs inventory (recorded for bob-cli-qq.10.6) and test:unit has a reproducible out-of-scope snooze vector failure (recorded as follow-up). bob plugins sync succeeded with 0 copied and all plugins up to date. epic-symbols reports no leftovers.

## Dependencies

- **Blocks:** [bob-cli-qq.10.4](bob-cli-qq.10.4.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.10.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.10.3.md) | [bob-cli-qq.10.3](bob-cli-qq.10.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b6ae31d`](https://github.com/bobs-org/bob-plugins/commit/b6ae31d8f5b89bc7898cefc79a0f21000c25dd87) | fix(cabinets): polish footer overlay and acceptance checks | [bob-cli-qq.10.3](bob-cli-qq.10.3.md) | 2026-11-27 09:28:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qq.10.4][1] | Acceptance phase needs the landed repair commits and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.4/README.md

<!-- sase:referenced-by:end -->
