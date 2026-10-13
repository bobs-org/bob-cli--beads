# Bead: bob-cli-78.5 — Navigation sub-project discovery, tag proxy, and subtree planner

[Bead Pages](../README.md) / [bob-cli-78](README.md) / bob-cli-78.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.71](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.71.md) · **Assignee:** `bob-cli-78.5` · **Size:** medium
**Created:** 2026-10-13 03:14:28 EDT · **Closed:** 2026-10-13 03:57:10 EDT
**Plan:** [202610/subproject\_cascade.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/subproject_cascade.md)

## Description

nav-model: add bob-navigation-hotkeys sub-project discovery and a pure top-down subtree planner, make existing project-blocking helpers treat a tagged ^prj as still blocked, and refuse descendant targets in the Depends on stage.

## Notes

[2026-10-13T07:56:49Z · bob-cli-78.5] PROPOSED FOLLOW-UP: Update glossary:project-task to say sub-projects inherit ancestor blocking — skipped here because epic DECISION memory_glossary=no; rollout (bob-cli-78.8) owns memory notes.

[2026-10-13T07:56:53Z · bob-cli-78.5] PROPOSED FOLLOW-UP: bob-plugins npm test still fails the known clean-base cases bob-cli-6v (4 unblocked-glyph), bob-cli-6w (Keep counts once), and bob-cli-3w (stage-ranker 16ms flake under parallel load); reproduced on HEAD, isolation 16ms test passes 12–14ms.

[2026-10-13T07:57:10Z · bob-cli-78.5] nav-model shipped in bob-plugins: 217-project-subprojects.js (parent scalar wikilink, NoteIndex-style resolve, descendants BFS depth 16, planProjectSubtreePass), tag proxy on tagged ^prj (getProjectBlockState project_parent, shouldRecoverProjectResidents false, 265 due/delete keep [?] + tag, planDependencyEdit no recover), PDG13 descendant refuse (failProjectPrjInternalAdd + stage disable), reversal strips #prj_is_blocked. Stage builder collects descendants via file-level helper so proto.call stubs do not throw. Manifest 2.30.0. Verified: 19/19 test-navigation-project-subprojects.cjs (PDS6/PDS15, PDG8–11, tag proxy, PDG13, reversal); 133/133 related blocking/stage/schedule/reversal/performance/ranker tests; npm run validate 6/6; bob plugins sync -n -p bob-navigation-hotkeys. npm test 2610/2616, remaining 6 are clean-base bob-cli-6v x4, bob-cli-6w x1, bob-cli-3w flake. Fragments <=1000 (590=997). No epic-symbols leftover. Did not edit memory notes.

## Dependencies

- **Depends on:** [bob-cli-78.1](bob-cli-78.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-78.6](bob-cli-78.6.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-78.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-78.5/README.md) | [bob-cli-78.5](bob-cli-78.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5d6392e`](https://github.com/bobs-org/bob-plugins/commit/5d6392e9b9d70e22bd42f084baca4873718cf5bc) | feat(nav): cascade project blocking through sub-projects | [bob-cli-78.5](bob-cli-78.5.md) | 2026-10-13 03:58:34 EDT |
