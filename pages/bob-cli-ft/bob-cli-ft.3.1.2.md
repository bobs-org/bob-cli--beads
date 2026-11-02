# Bead: bob-cli-ft.3.1.2 — Live Preview decorations, session toggle, and refresh lifecycle

[Bead Pages](../README.md) / [bob-cli-ft.3.1](bob-cli-ft.3.1.md) / bob-cli-ft.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ft.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.md) · **Assignee:** `bob-cli-ft.3.1.2` · **Size:** medium
**Created:** 2026-11-02 07:34:44 EST · **Closed:** 2026-11-02 08:34:37 EST
**Plan:** [202611/block\_marks\_editor.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/block_marks_editor.md)

## Description

live_preview: render block marks on visible Live Preview task rows; add lazy checkbox tooltips, the session toggle, popout gating, and coalesced invalidation from Tasks, ladder, midnight, and resume. Keep rendering free of disk reads and selection-only rebuilds; prove behavior with focused node tests.

## Notes

[2026-11-02T13:34:15Z · bob-cli-ft.3.1.2--2] PROPOSED FOLLOW-UP: Full-suite comparison for bob-cli-ft.3.1 lander. npm test on the phase tree failed 8 tests; npm test on clean base 89dae58a7d136e4a9a1bb79156212ecd926e706a failed 6, so the full-suite failures are not identical. Five names matched: the reload event fires only when the due key set changes (bob-cli-et); forced check feedback follows the bob refresh result (bob-cli-f7); the startup storm is linear and relationIndex registers after layout-ready and never reads non-markdown during startup replay (bob-cli-eh); future scheduling on Pending marks Blocked but still writes the Work Log (bob-cli-ff). The phase full run also failed three thresholds in unchanged scripts/test-block-id-prompt-task-wikilink-index-performance.cjs: cold build chunk 16.3 ms > 16 ms, warm snapshot plus order 157.3 ms > 50 ms, and keystroke rank 28.4 ms > 12 ms. Isolated node --test scripts/test-block-id-prompt-task-wikilink-index-performance.cjs failed warm snapshot plus order and keystroke rank on both phase (113.4 ms; 14.7 ms) and clean base (70.9 ms; 15.3 ms), matching the tracked bob-cli-f8 issue; cold build passed isolated on both and remains intermittent. The clean-base full run alone failed production CSS reduced-motion; the focused phase CSS test passed 2/2. The new Live Preview editor test passed 9/9. Land agent should evaluate these nonidentical full-suite results with the cited existing tasks, rather than treating all eight phase failures as clean-base matches.

[2026-11-02T13:34:37Z · bob-cli-ft.3.1.2--2] Verified Live Preview editor tests (9/9) and reduced-motion CSS tests (2/2); compared npm test against clean base 89dae58a7d136e4a9a1bb79156212ecd926e706a and recorded nonidentical failures in the proposed follow-up note.

## Dependencies

- **Depends on:** [bob-cli-ft.3.1.1](bob-cli-ft.3.1.1.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-ft.3.1.3](bob-cli-ft.3.1.3.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.1.2.md) | [bob-cli-ft.3.1.2](bob-cli-ft.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@257255e`](https://github.com/bobs-org/bob-plugins/commit/257255e429123f38b478442e10b3ab5cb05d3f73) | feat(plugins): add Live Preview blocked mark lifecycle | [bob-cli-ft.3.1.2](bob-cli-ft.3.1.2.md) | 2026-11-02 08:35:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ft.3.1.2--2][1] | Verify the phase follow-up evidence before closing | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.1.2.md

<!-- sase:referenced-by:end -->
