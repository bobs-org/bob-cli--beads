# Bead: bob-cli-ph.7 — Obsidian drawer rendering, typing, and bold writers

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.7

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.7` · **Size:** large
**Created:** 2026-11-22 17:36:49 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

obsidian-drawers: the drawer glyph and true-case title in Live Preview and reading view, the `*` typing assists and Toggle Drawer, bold plugin writers, and verbatim promotion and reversal.

## Notes

[2026-11-25T13:56:30Z · bob-cli-q4.2] Coordination note from bob-cli-q4.2 (open-lines / upcoming notes-key) for o / O / Ctrl+Shift+O in task-status-cycler:

1. Keep taskBlockEnsureNotesDrawer and the insert planners callable as pure functions that report whether they created the drawer, so Ctrl+Shift+O on a req-owning task can reuse them and auto-prune an empty newly materialized Notes drawer if the user exits insert mode without typing.
2. Make the * assist work on a freshly opened drawer-indent sibling (which o on an existing drawer header will emit).
3. Keep Smart Enter as "child inside the drawer". o opens a sibling after the drawer's subtree; Ctrl+Shift+O / Smart Enter open a child. The three stay orthogonal.
4. notes-key (bob-cli-q4.12, Ctrl+Shift+O) lands after ph.7 so it inherits drawer spelling from the shared helpers rather than hard-coding NOTES or **Notes** bytes.

## Dependencies

- **Depends on:** [bob-cli-ph.4](bob-cli-ph.4.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.9](bob-cli-ph.9.md) ◐ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pq.5](../bob-cli-pq/bob-cli-pq.5.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.7.md) | [bob-cli-ph.7](bob-cli-ph.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |
| read-by | [agent:bob-cli-pq.1][2] | sequencing check for glyph-contract | 2 |
| read-by | [agent:bob-cli-pq.3][3] | Check prerequisite drawer implementation and remaining integration | 1 |
| read-by | [agent:bob-cli-q4.2][4] | Need ph.7 status before leaving the open-lines coordination note | 1 |
| read-by | [agent:g1][5] | Check whether phase is blocked on the release gate | 1 |
| read-by | [agent:research.66.cld][6] | Check overlap of drawer typing/writers with better-o Ctrl+Shift+O design | 2 |
| read-by | [agent:research.66.grk][7] | Need drawer-writer sequencing so better-o can leave the right note on bob-cli-ph | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.1fk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pq.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q4.2/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.66.cld/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.66.grk/README.md

<!-- sase:referenced-by:end -->
