# Bead: bob-cli-7x.5 — Guard Obsidian rename-current-file for managed ref notes

[Bead Pages](../README.md) / [bob-cli-7x](README.md) / bob-cli-7x.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1k.linker.w0.md) · **Assignee:** `bob-cli-7x.5` · **Size:** small
**Created:** 2026-10-15 15:25:59 EDT · **Closed:** 2026-10-15 17:29:09 EDT
**Plan:** [202610/bob\_ref\_rename.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_rename.md)

## Description

obsidian-guard: in bob-plugins bob-navigation-hotkeys, refuse rename-current-file (modal open and submit) when the active file is a managed ref note under ref/ with source_pdf frontmatter, with a Notice pointing at `bob ref rename`; first tests for the rename path; build, test, and bob plugins sync.

## Notes

[2026-10-15T21:29:09Z · bob-cli-7x.5] Added managed ref note detection and guarded both modal open and submit; legacy and non-ref rename paths remain allowed. Verified: node --test scripts/test-navigation-hotkeys-rename.cjs (3 pass), npm run build, npm test build-check. Full npm test reports six failures in unrelated unblocked-glyph, review-card keep notice, and project-reversal tests. bob plugins sync --repo <linked bob-plugins checkout> completed. epic-symbols was empty.

## Dependencies

- **Depends on:** [bob-cli-7x.4](bob-cli-7x.4.md) ✓ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7x.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7x.5/README.md) | [bob-cli-7x.5](bob-cli-7x.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@13dbb3d`](https://github.com/bobs-org/bob-plugins/commit/13dbb3d7c5f5e014d9e8286ab12cce767ff79b2b) | feat(bob-navigation-hotkeys): guard managed reference renames | [bob-cli-7x.5](bob-cli-7x.5.md) | 2026-10-15 17:29:43 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7x.5][1] | Check prior phase notes before planning implementation | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7x.5/README.md

<!-- sase:referenced-by:end -->
