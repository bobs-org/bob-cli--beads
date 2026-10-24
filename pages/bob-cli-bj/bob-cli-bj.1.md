# Bead: bob-cli-bj.1 — Mac relation card as a navigate-then-accept chooser

[Bead Pages](../README.md) / [bob-cli-bj](README.md) / bob-cli-bj.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2e.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2e.linker.w0.md) · **Assignee:** `bob-cli-bj.1` · **Size:** medium
**Created:** 2026-10-24 13:34:45 EDT · **Closed:** 2026-10-24 14:24:21 EDT
**Plan:** [202610/relation\_label\_vocabulary.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md)

## Description

mac-chooser: fix the Tab collapse by separating query from selection (selection by key), add Ctrl+N/P and arrow navigation with wrap, Tab accepts or completes the top match, AppKit field with focus repair, local filtering of a once-fetched catalog, the redesigned vertical card, a collapsing fake-client regression test, and keyboard docs. No bob change.

## Notes

[2026-10-24T18:17:06Z · bob-cli-bj.1] PROPOSED FOLLOW-UP: Add relation-label hide, one-off, and rename guidance to glossary:task-relation — skipped by the epic decision memory_glossary=no.

[2026-10-24T18:24:05Z · bob-cli-bj.1--1] PROPOSED FOLLOW-UP: Arrange a reachable macOS host/toolchain for Swift format and macOS-target verification. Athena is Debian Linux with Swift 6.0.3 but no swift-format or xcode-select; original format-lint monitor s6sb97b08hrf and clean-base c5d560c format-lint both exited 69 with the same missing Apple developer tools directory error. The phase scratch portable-check passed all 1,587 tests on Athena; the Mac SSH attempt timed out.

[2026-10-24T18:24:21Z · bob-cli-bj.1--1] Verified: Athena just portable-check passed all 1,587 tests; just docs-check passed (447 tests, 1 optional asset test skipped); shell syntax and fake-Bob JSON smoke checks passed. Athena format-lint could not select Apple developer tools, and the same exit 69 occurred on clean base c5d560c; proposed follow-up recorded. Mac targets remain unverified because Mac SSH timed out.

## Dependencies

- **Blocks:** [bob-cli-bj.7](bob-cli-bj.7.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bj.1.md) | [bob-cli-bj.1](bob-cli-bj.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bj.1--1][1] | Review the assigned relation chooser phase, verification evidence, and close criteria | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bj.1.md

<!-- sase:referenced-by:end -->
