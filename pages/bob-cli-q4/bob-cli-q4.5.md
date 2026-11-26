# Bead: bob-cli-q4.5 — Plain split and BLOCKS placement match the layout contract

[Bead Pages](../README.md) / [bob-cli-q4](README.md) / bob-cli-q4.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.5` · **Size:** medium
**Created:** 2026-11-25 08:51:35 EST · **Closed:** 2026-11-25 10:17:58 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

## Description

layout-parity: fix bead bob-cli-pn so plain Task Split writes LINKED FROM in the managed-link zone, update the SP vectors, and re-copy them into the nav split twin. Verify and fix the known JS BLOCKS-before-Depends-On insert-order divergence from contract §14.5.

## Notes

[2026-11-25T14:37:37Z · bob-cli-q4.5] PROPOSED FOLLOW-UP: nav split vectors SP34/SP35/SP39 still expect **Notes** (bob-cli bold drawers, ph.4) but the nav tidy twin creates NOTES; needs ph.7.1 true-case drawers before the re-copied vectors.json goes green

[2026-11-25T15:17:47Z · bob-cli-q4.5--1] PROPOSED FOLLOW-UP: just check lib target has 17 xelatex failures (15 meet_route + 2 meetings::profile, Can be used only in preamble at \AtBeginDocument hypersetup l.277) that reproduce identically on the clean base tree with this bead stashed; environment/TeX-preamble issue unrelated to task_split files

[2026-11-25T15:17:58Z · bob-cli-q4.5--1] layout-parity done: plain-split back-link routed through shared insert_managed_back_link (carry.rs) with note indent unit; 10 SP vectors updated; nav twin mirrored (split-apply + BLOCKS-after-Depends-On per contract S14) and vectors re-copied byte-identical. Verified: cargo fmt clean, scoped clippy clean in touched regions, 8/8 task_split lib tests pass, nav 111 split/block + 142/121 dep + 49/52 split-vector suites pass. Full just check: 8086 passed / 17 failed, all 17 xelatex preamble failures reproduce identically on clean base (stashed) so pre-existing/environmental, recorded as PROPOSED FOLLOW-UP. epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-q4.1](bob-cli-q4.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.10](bob-cli-q4.10.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.13](bob-cli-q4.13.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.7](bob-cli-q4.7.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.5.md) | [bob-cli-q4.5](bob-cli-q4.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`814b658`](https://github.com/bobs-org/bob-cli/commit/814b6583e63165a4f2419158af50d4774fc8b034) | fix(task-split): route plain-split back-link through managed-link zone | [bob-cli-q4.5](bob-cli-q4.5.md) | 2026-11-25 10:19:06 EST |
| bob-plugins | [`bob-plugins@eac9d74`](https://github.com/bobs-org/bob-plugins/commit/eac9d7448d056e60af1e0f4224554c6ca1ed28d2) | fix(nav-split): mirror managed back-link and BLOCKS-after-Depends-On order | [bob-cli-q4.5](bob-cli-q4.5.md) | 2026-11-25 10:19:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.5--1][1] | Need the phase scope and design file to finish close-out after verify | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.5.md

<!-- sase:referenced-by:end -->
