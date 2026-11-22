# Bead: bob-cli-oj.5 — The group row at the bottom of property cards

[Bead Pages](../README.md) / [bob-cli-oj](README.md) / bob-cli-oj.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.5` · **Size:** large
**Created:** 2026-11-21 07:41:35 EST · **Closed:** 2026-11-21 17:09:11 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

## Description

group-rail: add the kit group-row builder and the shared missing-target look (dashed `+` creatable, dotted ghost), adopt it on day, week, and quarter cards and the record walk rail, give legacy dailies a derived step row, add the album card's "walks by" pill, and prove the look in the preview matrix.

## Notes

[2026-11-21T17:17:57Z · bob-cli-oj.5] PROPOSED FOLLOW-UP: skipped decisions:group-stops-are-derived — memory_decision_group_stops=no forbids editing the decisions web; the epic land agent should decide whether to record that group stops are derived on Bob notes and authored only as «/» links on link-only nav lines (same follow-up already recorded on bob-cli-oj.1, oj.2, oj.4).

[2026-11-21T22:09:39Z · bob-cli-oj.5.1.land] PHASE CLOSEOUT (bob-cli-oj.5.1.land). The delegated close of child epic bob-cli-oj.5.1 auto-closed this phase. Every deliverable was re-verified on bob-plugins origin/master ae305a3 plus the landing stitch (Ledger Tools 1.157.0, deployed and synced):
- Kit group row and shared missing-target look: propertyCardBuildGroupRow (240l), plus dashed `+` creatable and dotted `· not in vault` ghost on rail items, chips, and arms. After Bryan's bob-cli-oj note #2, arms are decluttered: skip mark plus group name, track-only centre, underline states. Footer done too.
- Adopted on day, week, and quarter cards (296ca) and the grouped record walk rail (242va). Years, all_time, ungrouped, and single-group albums keep today's rail (preview year-no-row and record-single-group).
- Legacy derived step row: preview legacy-daily-derived; intention e2e display-legacy-daily passes in real Obsidian.
- Album `walks by Section` pill: preview album-walks-by; album-header 42/42.
- Preview matrix: scripts/preview-group-rail.cjs, 16 fixtures, 128 renders, 0 failing.

EVIDENCE:
- rail-proof preview archive file:explicit:1ea931c37a15f083506627fd, inspection note file:explicit:6855882619ca7a9c4a4522f2
- rail-proof e2e: intention-card file:explicit:003cd62b2c9be7f840066a24, record-card file:explicit:0c04b6ecc8cc4b01ac582292, record-walk file:explicit:cff4d9180b258b4d19a9ed3a, title-block file:explicit:cb0873051c5cd643efb970d7, screenshots file:explicit:0a9da40ecafc983951e90d99, contrast file:explicit:1ec8bb4c28bdb584c4e81e31
- landing tale: declutter preview archive file:explicit:9cf5815b4f609e0391edbda8, inspection note file:explicit:0810648fd519b42127cbe1ed, contrast file:explicit:2d421ffa815baa593e33d56d
- landing e2e: intention-card file:explicit:6d9a9dfc810fb1ef3a31ed2c (81/82, yaml-done-returns = bob-cli-ot), record-card file:explicit:52e2fe78b6593e1d06652c85 (180/180), record-walk file:explicit:608eb22989c8cad86c532146 (passed), walker-footer file:explicit:43eb9c4ca9480d51ed367145 (groups and marks pass; geometryStable base failure = bob-cli-oj.6 note #3)

FOLLOW-UP OUTCOMES:
- corroborated: bob-cli-io, bob-cli-km, bob-cli-m1, bob-cli-nw, bob-cli-ob
- new tasks: bob-cli-ot, bob-cli-ou, bob-cli-ov
- declined: the command-mode sheet timeout and the gcal minute rollover
- epic-caused: the 296d comment, fixed in the landing tale
- left to the outer bob-cli-oj lander: the decisions-web follow-up (this phase's note #1) and the walker-footer geometryStable follow-up (bob-cli-oj.6 note #3, corroborated on clean base)

## Dependencies

- **Depends on:** [bob-cli-oj.1](bob-cli-oj.1.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-oj.2](bob-cli-oj.2.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-oj.4](bob-cli-oj.4.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.7](bob-cli-oj.7.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.md) | [bob-cli-oj.5](bob-cli-oj.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.5.1.2][1] | Need outer DECISIONS for the group-rail phase | 1 |
| read-by | [agent:bob-cli-oj.5.1.3][2] | Need outer DECISIONS | 1 |
| read-by | [agent:bob-cli-oj.6][3] | Need sibling phase statuses so I do not redo landed work or collide with group-rail | 2 |
| read-by | [agent:bob-cli-oj.7][4] | Need landed phase notes, versions, and follow-ups before adoption and e2e proof | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md

<!-- sase:referenced-by:end -->
