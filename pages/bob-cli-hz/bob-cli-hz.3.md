# Bead: bob-cli-hz.3 — Mac adopts the = opener and post-token flip

[Bead Pages](../README.md) / [bob-cli-hz](README.md) / bob-cli-hz.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.198](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.198.md) · **Assignee:** `bob-cli-hz.3` · **Size:** medium
**Created:** 2026-11-06 12:50:21 EST · **Closed:** 2026-11-06 18:13:08 EST
**Plan:** [202611/relation\_equals\_alias\_and\_direction\_flips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/relation_equals_alias_and_direction_flips.md)

## Description

mac-equals-opener: the Mac forwards `=` and token-glued `~` to Bob and replaces the dash arm with an equals opener arm that keeps the Space/Escape restores. It applies `toggle_relation_direction` natively without a picker and deletes every relation `-` path.

## Notes

[2026-11-06T22:01:22Z · bob-cli-hz.3--3] PROPOSED FOLLOW-UP: 12 pre-existing macOS CI failures on clean base cbb50dc (word motion, comma x2, backslash/slash aliases, period x2, semicolon, delayed alias, native undo, move undo) reproduce identically without phase changes; master runs 42278025697 and 42268256300 show same 12. Needs triage as CI/task bead.

[2026-11-06T23:13:08Z · bob-cli-hz.3--4] Phase test fixed and verified. Fixed async race in testLabeledRelationTildeFlipsAndEqualsStaysLiteral: the literal '=' path returns changed:false so the text wait succeeded before fake-bob wrote the record file; now waits for both text and record content, matching testOlderBobLeaves pattern. just portable-check passed (2261 tests, 1 skipped). git diff --check clean. Exact-SHA macOS CI run 42308430792 (snapshot dd6afd15): Build ok, all 10 CaptureRelationFlipAliasTests passed including the fixed test; remaining 12 failures reproduce identically on clean base cbb50dc (master runs 42278025697/42268256300) and are recorded as PROPOSED FOLLOW-UP. No epic-symbol entries. Memory equals-alias record belongs to records phase, untouched. Mac was offline for scratch-copy typecheck.

## Dependencies

- **Depends on:** [bob-cli-hz.1](bob-cli-hz.1.md) ✓ · ⧖ 2026-11-06
- **Depends on:** [bob-cli-hz.2](bob-cli-hz.2.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hz.4](bob-cli-hz.4.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hz.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hz.3.md) | [bob-cli-hz.3](bob-cli-hz.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@418604a`](https://github.com/bobs-org/bob-mac-capture/commit/418604a58a502ca6cadd8a7442eca0257901e66d) | feat(mac-capture)!: adopt = opener and post-token relation flips | [bob-cli-hz.3](bob-cli-hz.3.md) | 2026-11-06 17:04:07 EST |
| bob-cli--plans | [`bob-cli--plans@42f38ce`](https://github.com/bobs-org/bob-cli--plans/commit/42f38ce2198df5a0f0af799e04a4940904f8c5a4) | chore(plans): record successor card verdicts plan decisions | [bob-cli-hz.3](bob-cli-hz.3.md) | 2026-11-06 17:46:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hz.3--3][1] | Need phase scope and design for CI failure triage | 2 |
| read-by | [agent:bob-cli-hz.3--5][1] | Need to confirm close policy before submitting keep | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hz.3.md

<!-- sase:referenced-by:end -->
