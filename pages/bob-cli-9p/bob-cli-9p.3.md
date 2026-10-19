# Bead: bob-cli-9p.3 — Plural page labels in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-9p](README.md) / bob-cli-9p.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4u.linker.w0.md) · **Assignee:** `bob-cli-9p.3` · **Size:** xsmall
**Created:** 2026-10-19 07:59:12 EDT · **Closed:** 2026-10-19 08:06:08 EDT
**Plan:** [202610/highlight\_continuations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlight_continuations.md)

## Description

mac-pp-label: in the linked bob-mac-capture repo, make `RefsCopyFormat.shortPageLabel` render `Pages 11–12` as `pp. 11–12`, matching `Page 11` → `p. 11`, with tests.

## Notes

[2026-10-19T12:06:08Z · bob-cli-9p.3] Plural page labels: RefsCopyFormat.shortPageLabel maps Pages 11–12 to pp. 11–12 (case-insensitive, remainder preserved), matching Page 11 to p. 11. Verified with just portable-check on Linux: format lint clean, build ok, all 1389 tests pass including RefsCopyTests.testNoteFormatHandlesBlankQuoteLinesAndMissingProvenance with the new plural assertions. Changes left uncommitted in linked bob-mac-capture checkout (Sources/RefsCore/RefsCopy.swift, Tests/RefsCoreTests/RefsCopyTests.swift) for the land agent.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9p.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9p.3/README.md) | [bob-cli-9p.3](bob-cli-9p.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1968cc3`](https://github.com/bobs-org/bob-mac-capture/commit/1968cc36aa244455e2fadecb208966ee31fd91ab) | feat(refs): shorten plural page labels to pp. form | [bob-cli-9p.3](bob-cli-9p.3.md) | 2026-10-19 08:06:43 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9p.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9p.3/README.md

<!-- sase:referenced-by:end -->
