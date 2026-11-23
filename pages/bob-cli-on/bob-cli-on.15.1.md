# Bead: bob-cli-on.15.1 — Requirements on the Mac Pull-In card

[Bead Pages](../README.md) / [bob-cli-on.15](bob-cli-on.15.md) / bob-cli-on.15.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.md) · **Assignee:** `bob-cli-on.15.1.land`
**Created:** 2026-11-22 14:56:48 EST · **Closed:** 2026-11-22 21:38:26 EST
**Plan:** [202611/mac\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_requirement_close_card.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/mac_requirement_close_card.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_requirement_close_card.md

<!-- sase:links:end -->

## Description

Complete bob-cli-on.15 so the Mac Pull-In card presents nested requirement groups, stages their verdicts safely, and submits them through the existing capability-gated bob contract with compiled and tested native UI.

## Notes

[2026-11-23T02:08:48Z · bob-cli-pj.2.1.land] DISCOVERED ISSUE: pj.2.1 lander triaged bob-cli-pj.2.1.3 PROPOSED FOLLOW-UP #1 and independently reproduced just docs-check on bob-cli 29d7fec7 / Mac 33649498. All three fatal budget errors are introduced by this epic phase .5 commit d76a4849: capture-previews 5998→6082, keyboard 5974→6036, protocol 5999→6107 (cap 6000, canonical bob_docs.markdown.count_words). They are not inherited base failures for .5. Trim the additions within this epic while preserving contract facts. Evidence file:explicit:f0ee94709e52d2aa9074a8ad. Existing trackers bob-cli-jz and bob-cli-h9 also received corroboration; no new task.

[2026-11-23T02:38:26Z · bob-cli-on.15.1.land] Land verification: all 5 phases (.1 protocol, .2 outcomes, .3 pipeline, .4 card_ui, .5 integration) closed with notes addressed; no PROPOSED FOLLOW-UP entries on any child. Read Mac commits bf4b55ed..c0959905 and spot-checked source: BobProcessClient gates --req-choice on a per-executable positive capability proof, encodes Met/--complete-offer, Drop/--cancel-offer key[=reason], Carry/--carry, Carry-and-pull/--pull-in only (never both), refuses staged req choices without support; CaptureRequirementBranch.isStrictAncestor compares path components; Ctrl+Shift+T routes to stageRequirementCarry and no-ops on ordinary rows; requirement rows stay out of allUnblockedRows (tests). RV vectors.json cmp-identical to bob-cli tests/fixtures/req_close. Epic note #1 (docs budget regression from d76a4849) was resolved by Mac c0959905: Mac Scripts/docs-check.sh against bob-cli 29d7fec7 passes, count_words capture-previews 5976 / keyboard 5995 / protocol 6000 (cap 6000); corroboration noted on existing trackers bob-cli-jz and bob-cli-h9, no new task. Mac master c0959905 exact-SHA macOS CI green (run 45098831346: lint/build/test/bundle/plist/launch smoke/install). Integration: reviewed bob-cli commits since epic start (c72c941d..29d7fec7); only 513ec478 (picker v6 consumer wording) touched this contract, so updated docs/task-dependencies.md section 12.5 row note and section 12.25 to name the Bob Mac Capture Pull-In card as a consumer alongside picker v6; bob-cli just docs-check passes. Other drift (props, highlights, tick, gmail, Pomodoro-close mentions) does not touch the Pull-In requirement contract. epic-symbols: none.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.15.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.land/README.md) | [bob-cli-on.15.1](bob-cli-on.15.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@d2f879c`](https://github.com/bobs-org/bob-cli--plans/commit/d2f879cd52ce4fad42f08f522d496c97a5cad6c7) | chore(plans): mark mac\_requirement\_close\_card done | [bob-cli-on.15.1](bob-cli-on.15.1.md) | 2026-11-22 21:40:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.15.1.1][1] | Need exact epic decisions, phase notes, and plan metadata | 2 |
| read-by | [agent:bob-cli-on.15.1.5--3][2] | Check parent epic scope and land requirements for phase completion | 1 |
| read-by | [agent:bob-cli-on.15.1.land][3] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.5.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.land/README.md

<!-- sase:referenced-by:end -->
