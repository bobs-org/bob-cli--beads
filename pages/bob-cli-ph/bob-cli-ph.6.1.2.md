# Bead: bob-cli-ph.6.1.2 — Admit bold container drafts across all four contexts

[Bead Pages](../README.md) / [bob-cli-ph.6.1](bob-cli-ph.6.1.md) / bob-cli-ph.6.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.6.md) · **Assignee:** `bob-cli-ph.6.1.2` · **Size:** medium
**Created:** 2026-11-25 08:39:52 EST · **Closed:** 2026-11-25 12:12:27 EST
**Plan:** [202611/capture\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_true_case_drawers.md)

## Description

bold-drafts: replace ALL-CAPS authored container detection with whole-bold headers for task drawers, project-note sections, notebook creation seeds, and record groups. Preserve literal titles, add delimiter/title spans and the temporary caps_drawer_retired refusal, keep notebook route-only behavior, and make bullet menu replacements valid bold drafts. Advance grammar 29 to 30.

## Notes

[2026-11-25T17:12:00Z · bob-cli-ph.6.1.2] PROPOSED FOLLOW-UP: Existing docs headroom task bob-cli-ob still covers the fatal docs-check overage: unchanged docs/reference/plugins/bob-navigation-hotkeys.md is 6068/6000 words; docs/develop/plugins/plugin-apis.md is a warning at 9287/8000. The nav-page failure reproduces on clean HEAD as already recorded by bob-cli-ph.5 note #1; this phase changes neither page.

[2026-11-25T17:12:27Z · bob-cli-ph.6.1.2] Implemented grammar 30 whole-bold container drafts for task drawers, project-note sections, notebook creation seeds, and record groups; added spans/refusal behavior and valid completion insertions; updated and regenerated capture docs. Verified: docs-gen passed, cargo fmt and git diff --check passed, and cargo test --test cli capture:: passed (2055 tests). docs-check still fails only on the unchanged bob-navigation-hotkeys reference page over the 6000-word cap; recorded as a proposed follow-up citing bob-cli-ob.

## Dependencies

- **Depends on:** [bob-cli-ph.6.1.1](bob-cli-ph.6.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.6.1.3](bob-cli-ph.6.1.3.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.2/README.md) | [bob-cli-ph.6.1.2](bob-cli-ph.6.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`22fea30`](https://github.com/bobs-org/bob-cli/commit/22fea308101c894185bc29d494c1b5bdca6dff71) | feat(capture): admit whole-bold container drafts | [bob-cli-ph.6.1.2](bob-cli-ph.6.1.2.md) | 2026-11-25 12:14:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.6.1.2][1] | Need the phase scope, notes, design file, and epic decisions before completing assigned work | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.2/README.md

<!-- sase:referenced-by:end -->
