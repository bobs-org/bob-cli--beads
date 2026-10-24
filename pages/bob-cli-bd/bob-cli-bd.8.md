# Bead: bob-cli-bd.8 — Section headers in the Bob Mac Capture Refs panel

[Bead Pages](../README.md) / [bob-cli-bd](README.md) / bob-cli-bd.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2d.linker.w0.md) · **Assignee:** `bob-cli-bd.8` · **Size:** large
**Created:** 2026-10-24 07:59:21 EDT · **Closed:** 2026-10-24 09:46:54 EDT
**Plan:** [202610/ref\_note\_annotation\_sections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_note_annotation_sections.md)

## Description

mac: in bob-mac-capture, decode sections, project section headers into the inspector feed without shifting entry indices, draw the header view with tokens and VoiceOver, group the Copy card, and update docs and design renders.

## Notes

[2026-10-24T13:46:54Z · bob-cli-bd.8] Mac Refs inspector and Copy card now present bob ref show sections. Lossy decode of row.sections and annotation.section; feed headers attach without shifting flat indices, paging, or keyboard numbering; inspector draws native section headers and OTHER HIGHLIGHTS; Copy A groups notes under ### Title with description blockquotes; H picker shows non-selectable group rows and shrinks a sectioned window so headers fit the unsectioned card budget. Older unsectioned responses stay unchanged. Verified: athena just portable-check exit 0 (1574 tests); Mac isolated scratch ./Scripts/bundle.sh --identity - and just typecheck-tests exit 0 (stub typecheck); BOB_CLI_DIR docs-check exit 0. macOS XCTest/design PNG execution was not run here (Command Line Tools host has no XCTest); parent land should run macOS CI and inspect section/picker renders. epic-symbols: none.

[2026-10-24T13:47:09Z · bob-cli-bd.8] PROPOSED FOLLOW-UP: epic DECISIONS skipped memory writes (decision_record=no, glossary_term=no). Do not edit decisions:annotation-sections-are-name-keyed-folds. Do not edit glossary:annotation-section. Parent land should record those when the epic lands.

[2026-10-24T13:47:14Z · bob-cli-bd.8] PROPOSED FOLLOW-UP: macOS XCTest and design PNG review remain for parent land / macOS CI. Render tests are defined (refs-inspector-sections-880/1344/880-revealed/880-ax light+dark, refs-copy-highlight-picker-sections). This host ran portable-check on athena (1574 tests, 0 failures) and Mac scratch bundle.sh + just typecheck-tests (stub typecheck, not XCTest). Inspect the CI PNGs for spacing, clipping, contrast, empty headers, and large text.

## Dependencies

- **Depends on:** [bob-cli-bd.5](bob-cli-bd.5.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bd.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bd.8.md) | [bob-cli-bd.8](bob-cli-bd.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@f9cd88a`](https://github.com/bobs-org/bob-mac-capture/commit/f9cd88add5f2b4bdb8ca5a0dffde9b42617b7253) | feat(refs): present annotation sections in the inspector and Copy card | [bob-cli-bd.8](bob-cli-bd.8.md) | 2026-10-24 09:48:43 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.2][1] | Identify the existing owner and task evidence for clean-base just check failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-an.6.6.6.5.6.5.2/README.md

<!-- sase:referenced-by:end -->
