# Bead: bob-cli-mx.4 — CaptureCore walks models, client, tones, and presentation

[Bead Pages](../README.md) / [bob-cli-mx](README.md) / bob-cli-mx.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.es.md) · **Assignee:** `bob-cli-mx.4` · **Size:** medium
**Created:** 2026-11-17 17:59:53 EST · **Closed:** 2026-11-17 21:12:55 EST
**Plan:** [202611/mac\_walk\_attention\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_walk_attention_marks.md)

## Description

mac-walks-core: decode `bob walks --format json` on its own process lane, add the tier hue table, title-row walk marks in the agenda presentation, the pure refresh policy, fake-bob support, protocol docs, and green macOS CI.

## Notes

[2026-11-18T01:45:45Z · bob-cli-mx.4] PROPOSED FOLLOW-UP: bob-cli just docs-check reports generated drift (docs/reference/glossary.md out of date, run just docs-gen) on the clean base tree with no mac-repo changes involved; mac protocol.md lint itself passes

[2026-11-18T02:12:42Z · bob-cli-mx.4--1] PROPOSED FOLLOW-UP: macOS CI red on BobMacCaptureTests.CaptureDotRouteAliasTests testLaterItemStartDotAliasAppliesAndOpensRouteList (line 938, Condition not met before timeout; completion=nil). Identical failure on parent 394b3442 master run 44201825837, on fee9ffab master run 44218174307, and on snapshot run 44218451932 (same argv incl. cursor-2 xx entry) — so not caused by the walks changes in fee9ffab, which are purely additive (new walks lane, new presentation fields with defaults). Related-but-distinct flake bead: bob-cli-ko (same file, different test).

[2026-11-18T02:12:55Z · bob-cli-mx.4--1] walks core landed as bob-mac-capture fee9ffab (pushed, HEAD==origin/master): WalkAttention models/client/tones/presentation + refresh policy + fake-bob + protocol docs. Verified: portable-check 2583 tests 0 failures and docs lint pass (per bead session); macOS CI red is pre-existing — testLaterItemStartDotAliasAppliesAndOpensRouteList fails identically on parent 394b3442 run 44201825837 and fee9ffab runs 44218174307/44218451932, recorded as PROPOSED FOLLOW-UP (related: bob-cli-ko).

## Dependencies

- **Depends on:** [bob-cli-mx.2](bob-cli-mx.2.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-mx.5](bob-cli-mx.5.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mx.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mx.4.md) | [bob-cli-mx.4](bob-cli-mx.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@fee9ffa`](https://github.com/bobs-org/bob-mac-capture/commit/fee9ffabfd34dadfeb67b281daa26655d18ab4c5) | feat(walks): capture-core models, client, tones, and presentation | [bob-cli-mx.4](bob-cli-mx.4.md) | 2026-11-17 20:45:01 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mx.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mx.4.md

<!-- sase:referenced-by:end -->
