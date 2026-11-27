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

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_card.md

<!-- sase:links:end -->

## Description

Snooze one task safely from Obsidian, retime or remove its row, and wake it through bob, with keyboard and undo behavior verified before closing bob-cli-q5.6.

## Notes

[2026-11-27T11:27:14Z · bob-cli-qi.land] DISCOVERED ISSUE (from the bob-cli-qi land agent): npm test on clean bob-plugins ad38b38a (this epic's bob-cli-q5.6.1.3 Alt+Z Snooze Card commit) fails 2 of 10218 tests, reproduced identically with and without the qi fix. (1) scripts/test-navigation-relation-links-stage.cjs test 8 'links-to row follows blocks with N, first label, cut target, and +K' (line 864): the Task Card row ids now include 'snooze' after 'schedule', which the expected list lacks. (2) scripts/test-prose-field-roles.cjs: plugins/bob-navigation-hotkeys/src/744-snooze-card-modal.js:129 text control needs a bob-text role within the previous 3 lines. Repro: cd bob-plugins && node --test scripts/test-navigation-relation-links-stage.cjs scripts/test-prose-field-roles.cjs. Decide whether the test expectations or the new snooze row/role give.

[2026-11-27T12:02:18Z · bob-cli-q5.6.1.land] LAND TRIAGE (bob-cli-q5.6.1.land): (1) Epic note #1 DISCOVERED ISSUE (two npm failures from ad38b38a) and task bob-cli-qu (same report) — epic-caused, FIXED in this landing: relation-links-stage now expects the planned snooze row; 744 modal time input declares a bob-text literal role. Also fixed a third epic-caused failure the full suite exposed: test-navigation-task-card-view 'q closes from a focused More row' asserted z was inert, which c6a979eb's real dispatch wrapper made false; replaced with an inert key and added a Task Card z dispatch + repeat-guard unit test. bob-cli-qu closed superseded. (2) q5.6.1.2 PROPOSED FOLLOW-UP #1 (ENOSPC e2e self-tests, full /tmp) — duplicate of bob-cli-qt; +1 recorded with new evidence that obsidian-block-marks-e2e-lib scratchRoot hardcodes /tmp/bm-e2e. (3) q5.6.1.2 #2 and q5.6.1.3 #1 (docs/reference/vault-format.md word budget 6030/6000) — DECLINED: already resolved upstream by dc96ef4c; bob-plugins docs:check with BOB_CLI_DIR passes lint ok. (4) q5.6.1.3 #1 second clause (bob-cli just check exceeds 9-min window) — DECLINED: not a defect; the lander ran just check to completion. (5) Newly observed, not epic-caused: frees-marks 25 ms budget under full-suite load -> +1 bob-cli-io; wispr_summary kicker letter-spacing -> +1 bob-cli-q9; live SVG highlights PDF renders 0 of 1 -> +1 bob-cli-kp (related live-diagram zero-render). No new task beads were needed.

[2026-11-27T13:47:34Z · bob-cli-q5.6.1.land--1] Passing Snooze Card acceptance report (56 assertions) and all inspected screenshots: 🔒 snooze-card-e2e.json 🔒 blocked-snoozed-light.png 🔒 forced-colors-snooze-card.png 🔒 invalid-time-light.png 🔒 ordinary-dark.png 🔒 ordinary-light.png 🔒 over-cap-footer-light.png 🔒 snoozed-dark.png 🔒 snoozed-light.png

## Attachments

- 🔒 blocked-snoozed-light.png · image/png · 1440×1000 · 139.617 KiB (private attachment)
- 🔒 forced-colors-snooze-card.png · image/png · 1440×1000 · 151.282 KiB (private attachment)
- 🔒 invalid-time-light.png · image/png · 1440×1000 · 151.268 KiB (private attachment)
- 🔒 ordinary-dark.png · image/png · 1440×1000 · 150.358 KiB (private attachment)
- 🔒 ordinary-light.png · image/png · 1440×1000 · 151.434 KiB (private attachment)
- 🔒 over-cap-footer-light.png · image/png · 1440×1000 · 151.268 KiB (private attachment)
- 🔒 snooze-card-e2e.json · application/json · 29.7646 KiB (private attachment)
- 🔒 snoozed-dark.png · image/png · 1440×1000 · 138.031 KiB (private attachment)
- 🔒 snoozed-light.png · image/png · 1440×1000 · 140.271 KiB (private attachment)

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.6.1.land.md) | [bob-cli-q5.6.1](bob-cli-q5.6.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@56baeb9`](https://github.com/bobs-org/bob-plugins/commit/56baeb9f44ca51df41a8a0fb00889c83d2510e28) | test(snooze): repair Snooze Card unit expectations and add Task Card z dispatch coverage | [bob-cli-q5.6.1](bob-cli-q5.6.1.md) | 2026-11-27 07:06:19 EST |
| bob-cli | [`064fc51`](https://github.com/bobs-org/bob-cli/commit/064fc51ef361bb0628aa2d9f16bb10f9ef74f7d9) | docs(snooze): document Snooze Card gestures and undo | [bob-cli-q5.6.1](bob-cli-q5.6.1.md) | 2026-11-27 08:57:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.6.1.1][1] | Need phase and parent epic plan details, decisions, and notes | 1 |
| read-by | [agent:bob-cli-q5.6.1.3][2] | Need parent epic scope and prior phase interfaces | 1 |
| read-by | [agent:bob-cli-q5.6.1.land][3] | Need the epic scope, children, and linked plan file | 1 |
| read-by | [agent:bob-cli-qi.land][4] | Check whether the two nav-hotkeys npm failures are already recorded on the causing epic | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.6.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.6.1.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qi.land.md

<!-- sase:referenced-by:end -->
