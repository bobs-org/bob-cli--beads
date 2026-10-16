# Bead: bob-cli-8b.4 — Bob Mac Capture Control-T template shelf

[Bead Pages](../README.md) / [bob-cli-8b](README.md) / bob-cli-8b.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1n.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1n.linker.w0.md) · **Assignee:** `bob-cli-8b.4` · **Size:** medium
**Created:** 2026-10-16 08:18:36 EDT · **Closed:** 2026-10-16 11:00:06 EDT
**Plan:** [202610/saved\_capture\_templates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/saved_capture_templates.md)

## Description

mac-shelf: the Control-T shelf itself: cache, opening rules, keys, syntax-colored rows with slot dots, one-undo-step insert (empty and rows-first drafts), two-press delete, Control-T/Control-S switching, and the Templates footer button.

## Notes

[2026-10-16T15:00:06Z · bob-cli-8b.4] Control-T shelf: cache, opening rules, keys, syntax-colored rows with slot dots, one-undo NSTextView insert (empty and rows-first), two-press delete with failure restore, Control-T/Control-S switching, Templates footer. Verified: athena just portable-check (1254 tests, 0 failures); Mac scratch bundle.sh and just typecheck-tests (BobMacCaptureTests PASS). pop_visible_in_count and Command-S save left to bob-cli-8b.5.

## Dependencies

- **Depends on:** [bob-cli-8b.3](bob-cli-8b.3.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8b.5](bob-cli-8b.5.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8b.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8b.4/README.md) | [bob-cli-8b.4](bob-cli-8b.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@ee08ca7`](https://github.com/bobs-org/bob-mac-capture/commit/ee08ca7a4f8d7fc88fcd21067b2deab9f97b8b46) | feat(mac-capture): add Control-T saved-template shelf | [bob-cli-8b.4](bob-cli-8b.4.md) | 2026-10-16 11:01:15 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8b.4][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8b.4/README.md

<!-- sase:referenced-by:end -->
