# Bead: bob-cli-l3.2 — Record route rows accept again (bob-mac-capture)

[Bead Pages](../README.md) / [bob-cli-l3](README.md) / bob-cli-l3.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.dp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.dp.md) · **Assignee:** `bob-cli-l3.2` · **Size:** medium
**Created:** 2026-11-12 16:11:26 EST · **Closed:** 2026-11-12 16:46:27 EST
**Plan:** [202611/record\_capture\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_capture_repairs.md)

## Description

mac-accept: narrow acceptSelectedCompletion's record dispatch to Record Card contexts so route lists accept record rows through the generic replacement path with their next-missing-field continuation, apply the plus_commit_record_rows decision in commitRouteCompletionOnAcceptKey, and add Return/Tab/click and cached-targets regression tests.

## Notes

[2026-11-12T21:46:27Z · bob-cli-l3.2] Narrowed Record Card dispatch and added Bob-served Return/Tab/click, cached-target continuation, ordinary-route, and +/, regression coverage. Verified with Athena just portable-check (2,499 tests), Mac scratch bundle and all test-target type-checks, plus fixture/shell/diff checks; XCTest runtime remains for CI.

## Dependencies

- **Blocks:** [bob-cli-l3.3](bob-cli-l3.3.md) ◐ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-l3.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-l3.2/README.md) | [bob-cli-l3.2](bob-cli-l3.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-l3.2][1] | Confirm whether the required close completed before finalizing this phase | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-l3.2/README.md

<!-- sase:referenced-by:end -->
