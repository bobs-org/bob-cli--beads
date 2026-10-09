# Bead: bob-cli-5s.8 — Kind-adaptive inspector and actions menu

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.5z` · **Assignee:** `bob-cli-5s.8` · **Size:** medium
**Created:** 2026-10-08 19:32:40 EDT · **Closed:** 2026-10-09 07:05:27 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

## Description

refs-inspector: upgrade the inspector with PDFKit thumbnails or outlines by kind, Bottom-line and abstract excerpts, reading-time estimates, commented highlights from `bob ref show -c`, open history, and a ⌘K actions menu, all lazy, cancellable, and cached.

## Notes

[2026-10-09T11:05:05Z · bob-cli-5s.8] PROPOSED FOLLOW-UP: Write the refs-panel-is-a-thin-client decision strand (Bob Refs ranks bob reference index and never mutates it); auto left refs_decision_memory=no

[2026-10-09T11:05:13Z · bob-cli-5s.8] PROPOSED FOLLOW-UP: Anchor the ⌘K actions menu below the selected row frame instead of the mouse-or-list-center fallback in RefsPanelController.actionsAnchor

[2026-10-09T11:05:27Z · bob-cli-5s.8] refs-inspector done: RefsCore show/summary/reading-time/outline + refs-show lane with tests; PDFKit intrinsics loader (120ms settle, cancel, LRU, disk cache) feeding signals back; full kind-adaptive inspector (thumbnails, Bottom-line/abstract, contents, commented highlights, open tasks); ⌘K menu with copies/toast; README Inspector section. CI green on 2016864 (run 37919892089); inspector chat/paper/encrypted PNGs reviewed in both appearances, quote-bar stretch fixed and re-verified.

## Dependencies

- **Depends on:** [bob-cli-5s.6](bob-cli-5s.6.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.9](bob-cli-5s.9.md) ✓ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.8/README.md) | [bob-cli-5s.8](bob-cli-5s.8.md) | 5 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@64c1333`](https://github.com/bobs-org/bob-mac-capture/commit/64c1333a8092c226d5c7ecf81623f8472024c5e3) | feat(refs): add kind-adaptive inspector and ⌘K actions menu | [bob-cli-5s.8](bob-cli-5s.8.md) | 2026-10-09 06:07:05 EDT |
| bob-mac-capture | [`bob-mac-capture@e4934c9`](https://github.com/bobs-org/bob-mac-capture/commit/e4934c97a705ac669b93227fff2f65f8f8155217) | fix(refs): import CaptureCore in RefsInspector for SchemaVersioned | [bob-cli-5s.8](bob-cli-5s.8.md) | 2026-10-09 06:09:14 EDT |
| bob-mac-capture | [`bob-mac-capture@d1689b3`](https://github.com/bobs-org/bob-mac-capture/commit/d1689b310472ae2c59f3c05e63cecf046af300cb) | fix(refs): resolve loader shadowing and async-let use | [bob-cli-5s.8](bob-cli-5s.8.md) | 2026-10-09 06:21:30 EDT |
| bob-mac-capture | [`bob-mac-capture@f5f6178`](https://github.com/bobs-org/bob-mac-capture/commit/f5f61785edffb9b49df8271688f9d6456b545100) | fix(refs): initialize listing through a local in panel model init | [bob-cli-5s.8](bob-cli-5s.8.md) | 2026-10-09 06:33:36 EDT |
| bob-mac-capture | [`bob-mac-capture@2016864`](https://github.com/bobs-org/bob-mac-capture/commit/2016864dbf518f9f1d048bd16cc8972831bda8ba) | fix(refs): pin the inspector quote bar to the text height | [bob-cli-5s.8](bob-cli-5s.8.md) | 2026-10-09 06:48:48 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.8][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.8/README.md

<!-- sase:referenced-by:end -->
