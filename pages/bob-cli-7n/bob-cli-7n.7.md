# Bead: bob-cli-7n.7 — Bob Mac Capture direction-aware picker and blocks preview

[Bead Pages](../README.md) / [bob-cli-7n](README.md) / bob-cli-7n.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4g.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4g.linker.w1.md) · **Assignee:** `bob-cli-7n.7` · **Size:** medium
**Created:** 2026-10-14 11:27:20 EDT · **Closed:** 2026-10-14 14:36:20 EDT
**Plan:** [202610/capture\_star\_blocks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_star_blocks.md)

## Description

mac: parameterize the dependency picker by direction for `*`, add span kinds, Backspace and Add-ID support, and render dependency_updates[], consumed_links[], and deleted sessions from real-bob fixtures.

## Notes

[2026-10-14T18:36:11Z · bob-cli-7n.7] PROPOSED FOLLOW-UP: Add the explicit macOS SDK path to Scripts/typecheck-tests.sh. On the unchanged base script, just typecheck-tests fails in its XCTest fallback because direct swiftc cannot load the macOS standard library after SDKROOT is unset; adding -sdk from xcrun in the isolated scratch checker lets all four targets typecheck.

[2026-10-14T18:36:20Z · bob-cli-7n.7] Implemented the direction-aware * blocks picker and Bob contract decoding/preview; added real Bob fixtures, fake-bob coverage, UI presentation, and README docs. Verified just portable-check (1,164 tests passed), Mac bundle build, and all four Mac test targets typechecked in the scratch copy with the explicit SDK path. git diff --check passes; epic-symbols reports none. Recorded the unchanged checker SDK-path issue as a proposed follow-up. Interactive GUI smoke check remains for Bryan.

[2026-10-14T18:42:54Z · bob-cli-7n.7] Verified the preserved Blocks picker and preview implementation; just portable-check passes (1,164 tests), and prior phase verification recorded Mac bundle build plus all four Mac targets typechecked in the scratch copy. epic-symbols is empty.

## Dependencies

- **Depends on:** [bob-cli-7n.5](bob-cli-7n.5.md) ✓ · ⧖ 2026-10-14
- **Depends on:** [bob-cli-7n.6](bob-cli-7n.6.md) ✓ · ⧖ 2026-10-14
- **Blocks:** [bob-cli-7n.8](bob-cli-7n.8.md) ✓ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7n.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7n.7/README.md) | [bob-cli-7n.7](bob-cli-7n.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@f2a5cb5`](https://github.com/bobs-org/bob-mac-capture/commit/f2a5cb59782f13e5ac3c6deed6bf3bba4e19058d) | feat(capture): add direction-aware Blocks picker to Mac Capture | [bob-cli-7n.7](bob-cli-7n.7.md) | 2026-10-14 14:43:40 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7n.7][1] | Need the phase scope and design file | 4 |
| read-by | [agent:bob-cli-7n.8][2] | Need the completed Mac phase commit evidence for the decision record | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7n.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7n.8/README.md

<!-- sase:referenced-by:end -->
