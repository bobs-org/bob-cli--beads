# Bead: bob-cli-ap.3 — Render group pieces in the Bob Mac Capture Refs inspector

[Bead Pages](../README.md) / [bob-cli-ap](README.md) / bob-cli-ap.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12y.md) · **Assignee:** `bob-cli-ap.3` · **Size:** medium
**Created:** 2026-10-23 05:11:20 EDT · **Closed:** 2026-10-23 06:36:11 EDT
**Plan:** [202610/tucked\_continuation\_groups.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/tucked_continuation_groups.md)

## Description

mac-inspector-pieces: in bob-mac-capture, decode the optional `pieces` array and render a group as one HIGHLIGHTS entry whose pieces each carry their own quote rule and note card, separated by a captioned dashed seam; update Copy payloads, VoiceOver labels, fixtures, tests, and docs/refs-inspector.md.

## Notes

[2026-10-23T10:36:11Z · bob-cli-ap.3] Implemented group pieces in Bob Mac Capture Refs inspector: RefsShowPiece decoding + group-aware feed counts, Copy payloads, and per-piece inspector rendering with dashed seam. Verified: swift build ok, swift test 1531/1531 pass (incl. 5 new group tests), Mac bundle.sh ok, just typecheck-tests 4xPASS, just docs-check passed.

## Dependencies

- **Depends on:** [bob-cli-ap.2](bob-cli-ap.2.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ap.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ap.3/README.md) | [bob-cli-ap.3](bob-cli-ap.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@da5faa8`](https://github.com/bobs-org/bob-mac-capture/commit/da5faa8c54daa19444577564f36f068a1690e01b) | feat(refs): render tucked group pieces in the Refs inspector | [bob-cli-ap.3](bob-cli-ap.3.md) | 2026-10-23 06:37:17 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ap.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ap.3/README.md

<!-- sase:referenced-by:end -->
