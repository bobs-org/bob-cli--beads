# Bead: bob-cli-fb.2.1.3 — Complete batch semantics, human output, and verification

[Bead Pages](../README.md) / [bob-cli-fb.2.1](bob-cli-fb.2.1.md) / bob-cli-fb.2.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fb.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.2.md) · **Assignee:** `bob-cli-fb.2.1.3` · **Size:** medium
**Created:** 2026-11-01 13:00:27 EST · **Closed:** 2026-11-01 17:35:04 EST
**Plan:** [202611/leaf\_keep\_moving\_rust.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/leaf_keep_moving_rust.md)

## Description

finish: implement KM21 with later-item provenance, render the approved human copy, complete cross-surface regression coverage, and verify repository gates and the release-mode performance target.

## Notes

[2026-11-01T22:34:46Z · bob-cli-fb.2.1.3] PROPOSED FOLLOW-UP: keep-moving triggering close misses the <=70 ms target — on apollo (release ab32d58a+finish tree, 6826-note copy of ~/bob, loaded 16-core host, 50 reps, dry-run json !sase_badges:draft-spec) triggering p50 272/314 ms vs nontriggering control p50 174/254 ms; the pre-keep-moving base 83e11967 is itself p50 203/220 ms on the same fixture and host, so the 70 ms target is not met even without keep-moving; keep-moving adds ~45-55 ms (min-to-min), mostly a second pomodoro_themes::scan_root_areas_matching pass over ~650 root notes in D7 routing — share or cache that scan

[2026-11-01T22:34:52Z · bob-cli-fb.2.1.3] PROPOSED FOLLOW-UP: docs/task-dependencies.md §12.15 CLI mock omits the existing (next up) destination capsule that picked rows print — either show it in the mock or drop it for keep-moving rows

[2026-11-01T22:35:04Z · bob-cli-fb.2.1.3] Finish phase verified. KM21: new capture/keep_moving_net.rs tracks per-item day text so a later item's link of any non-pick open N resident or close/re-block of ^prj drops N's whole group while the originating close's picks (several per group) never invalidate their own group; per-row drops (complete, reblock, link, drop) and fold pruning handled; reporting-only, files untouched. Human copy per §12.15: header/offer rows/'not offered' fold/'· keeps N moving' suffix/'· not pulled in', direct, Pomodoro, nested relation and refusal paths, never 'unblocked' or the unlock glyph. KM32/G3: snapshot now built only when a candidate or ^prj carries [dependsOn::], and both kill switches gate the trigger. Tests: 35 CLI keep_moving tests (KM21/22/24/30/31/32, human copy, mixed hand_off refusal, nested labels), engine + net unit tests, KM24 stale-preimage commit test; fixed capture-phase lint and pomodoro_close golden (additive keep_moving). sase tool run check passed; just docs-check passed. Performance: 70 ms target NOT met (triggering p50 272/314 ms vs base 83e11967 p50 203/220 ms on same host/fixture; hello p50 36.5 ms meets 40 ms); recorded as PROPOSED FOLLOW-UP. Epic symbols: none.

## Dependencies

- **Depends on:** [bob-cli-fb.2.1.2](bob-cli-fb.2.1.2.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fb.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.2.1.3/README.md) | [bob-cli-fb.2.1.3](bob-cli-fb.2.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8347a46`](https://github.com/bobs-org/bob-cli/commit/8347a46d949c31078dbea284c0ed1d869e3bb952) | feat(capture): net keep-moving batches, render human copy, and gate snapshot work | [bob-cli-fb.2.1.3](bob-cli-fb.2.1.3.md) | 2026-11-01 18:23:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fb.2.1.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fb.2.1.3/README.md

<!-- sase:referenced-by:end -->
