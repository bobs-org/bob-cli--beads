# Bead: bob-cli-du.2.1.1 — Parse closing-label policy and expose complete verdicts

[Bead Pages](../README.md) / [bob-cli-du.2.1](bob-cli-du.2.1.md) / bob-cli-du.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-du.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.2.md) · **Assignee:** `bob-cli-du.2.1.1` · **Size:** medium
**Created:** 2026-10-28 15:26:10 EDT · **Closed:** 2026-10-28 15:48:25 EDT
**Plan:** [202610/complete\_label\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/complete_label_capture.md)

## Description

close-policy: share the cancel/complete label parser, drop overlapping keys from both lists, add CloseEffect and complete verdicts, and exercise the existing config, key, and rule vectors without enabling relation-triggered completion.

## Notes

[2026-10-28T19:48:25Z · bob-cli-du.2.1.1] Implemented shared cancel/complete label parsing, overlap filtering and warnings, CloseEffect and inverse lookup, and completion verdict/policy APIs. Verified complete-label config/key/rule/Done vectors, existing task-cancel and config unit suites, formatting, diff hygiene, and cargo check --all-targets.

## Dependencies

- **Blocks:** [bob-cli-du.2.1.2](bob-cli-du.2.1.2.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.1/README.md) | [bob-cli-du.2.1.1](bob-cli-du.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a32a32f`](https://github.com/bobs-org/bob-cli/commit/a32a32fbe081506316174cb45333531055dffc50) | feat(relations): add complete-label policy and verdicts | [bob-cli-du.2.1.1](bob-cli-du.2.1.1.md) | 2026-10-28 15:49:37 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-du.2.1.1][1] | Confirm explicit closure of the assigned phase after checks | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.1/README.md

<!-- sase:referenced-by:end -->
