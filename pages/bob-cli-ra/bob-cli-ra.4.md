# Bead: bob-cli-ra.4 — The rail on every tree card and the card-floor invariant

[Bead Pages](../README.md) / [bob-cli-ra](README.md) / bob-cli-ra.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6o.linker.w0.md) · **Assignee:** `bob-cli-ra.4` · **Size:** medium
**Created:** 2026-11-27 15:01:37 EST · **Closed:** 2026-11-27 18:08:55 EST
**Plan:** [202611/tree\_note\_link\_walks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/tree_note_link_walks.md)

## Description

cards: after bob-cli-qq.10.5 closes, mount the rail on area, project, notebook, and prose cards in both views, make the foot and cabinet stack insert above the floor, move the day/period and record rails to the floor, and prove that any rail is the card's last child on every species.

## Notes

[2026-11-27T23:08:30Z · bob-cli-ra.4] PROPOSED FOLLOW-UP: test-snooze-model-vectors "snooze-add-resnooze-replaces-history daily postimage" still fails identically on this tree (10438 pass / 1 fail / 5 skipped) — same pre-existing vector already tracked by epic bob-cli-q5; does not belong to the card-floor work.

[2026-11-27T23:08:55Z · bob-cli-ra.4] Mounted the tree walk rail as the card floor on area/project (249d), notebook (249i), and prose (249n) in both views; foot and cabinet appends go through propertyCardFloorAppend (240r/240wl/242kc); day/period and record rails dock via propertyCardFloorDock (296b/242k/242v). New test-ledger-tools-card-floor-invariant.cjs plus updated home/notebook/prose/intention/foot/passive suites prove the rail is last through cabinet open/close, lazy body, repaint, and in-place swap. Shipped bob-ledger-tools 1.174.0 (npm run build, build:check, docs:inventory:check, focused suites, npm test 10438 pass / 1 pre-existing snooze fail / 5 skipped; bob plugins sync copied ledger-tools without -F).

## Dependencies

- **Depends on:** [bob-cli-qq.10.5](../bob-cli-qq/bob-cli-qq.10.5.md) ✓ · ⧖ 2026-11-27
- **Depends on:** [bob-cli-ra.2](bob-cli-ra.2.md) ✓ · ⧖ 2026-11-27
- **Depends on:** [bob-cli-ra.3](bob-cli-ra.3.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-ra.5](bob-cli-ra.5.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ra.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ra.4/README.md) | [bob-cli-ra.4](bob-cli-ra.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@28b13c4`](https://github.com/bobs-org/bob-plugins/commit/28b13c4e17c4cc5668dd65ce82919ef979c86b82) | feat(ledger-tools): dock the link-walk rail as every property card's floor | [bob-cli-ra.4](bob-cli-ra.4.md) | 2026-11-27 18:10:58 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ra.1][1] | find cards bead for gate edge | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ra.1/README.md

<!-- sase:referenced-by:end -->
