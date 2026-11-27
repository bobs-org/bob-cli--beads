# Bead: bob-cli-q5.6.1 — Complete Alt+Z Snooze Card and Task Card z

[Bead Pages](../README.md) / [bob-cli-q5.6](bob-cli-q5.6.md) / bob-cli-q5.6.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.6.md) · **Assignee:** `bob-cli-q5.6.1.land`
**Created:** 2026-11-27 01:34:15 EST
**Plan:** [202611/snooze\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_card.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/snooze_card.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_card.md

<!-- sase:links:end -->

## Description

Snooze one task safely from Obsidian, retime or remove its row, and wake it through bob, with keyboard and undo behavior verified before closing bob-cli-q5.6.

## Notes

[2026-11-27T11:27:14Z · bob-cli-qi.land] DISCOVERED ISSUE (from the bob-cli-qi land agent): npm test on clean bob-plugins ad38b38a (this epic's bob-cli-q5.6.1.3 Alt+Z Snooze Card commit) fails 2 of 10218 tests, reproduced identically with and without the qi fix. (1) scripts/test-navigation-relation-links-stage.cjs test 8 'links-to row follows blocks with N, first label, cut target, and +K' (line 864): the Task Card row ids now include 'snooze' after 'schedule', which the expected list lacks. (2) scripts/test-prose-field-roles.cjs: plugins/bob-navigation-hotkeys/src/744-snooze-card-modal.js:129 text control needs a bob-text role within the previous 3 lines. Repro: cd bob-plugins && node --test scripts/test-navigation-relation-links-stage.cjs scripts/test-prose-field-roles.cjs. Decide whether the test expectations or the new snooze row/role give.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.6.1.land/README.md) | [bob-cli-q5.6.1](bob-cli-q5.6.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.6.1.1][1] | Need phase and parent epic plan details, decisions, and notes | 1 |
| read-by | [agent:bob-cli-q5.6.1.3][2] | Need parent epic scope and prior phase interfaces | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.6.1.3/README.md

<!-- sase:referenced-by:end -->
