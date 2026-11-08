# Bead: bob-cli-iq.3 — Resolver, exact-path launch, and page request

[Bead Pages](../README.md) / [bob-cli-iq](README.md) / bob-cli-iq.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3o.linker.w0.md) · **Assignee:** `bob-cli-iq.3` · **Size:** medium
**Created:** 2026-11-08 10:40:42 EST · **Closed:** 2026-11-08 11:26:20 EST
**Plan:** [202611/highlights\_annotation\_page\_jump.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/highlights_annotation_page_jump.md)

## Description

open_at_page: extend the ⌘↵ command so that one resolver handles reading tasks, 🔖 lines, Task Links, and managed blocks. It follows hops, stubs, and the unique-ID fallback, and opens ref_history archives through their annotated_pdf. It opens the exact path, then sends the Hammerspoon page request. Adds a dry mode, an announce seam with plain notices, a re-entry lock, and the additive api page option.

## Notes

[2026-11-08T16:26:20Z · bob-cli-iq.3] open_at_page ships: 677b resolver (frozen target, bookmark/task-link/embed/in-note order, 3-hop stub cycle check, unique-ID fallback, ref_history annotated_pdf, dry/live parity, railLines), 677 launch (exact-path open, encoded Hammerspoon page URL, announce seam with plain notices, re-entry lock 400ms, api page passthrough), command renamed, docs/highlights.md updated. Verified: npm run build ok, npm test 5723 pass/0 fail/1 skipped, npm run validate ok, npm run docs:check ok, bob plugins sync ok.

## Dependencies

- **Depends on:** [bob-cli-iq.1](bob-cli-iq.1.md) ✓ · ⧖ 2026-11-08
- **Depends on:** [bob-cli-iq.2](bob-cli-iq.2.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-iq.4](bob-cli-iq.4.md) ◐ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-iq.6](bob-cli-iq.6.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-iq.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-iq.3/README.md) | [bob-cli-iq.3](bob-cli-iq.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e16f794`](https://github.com/bobs-org/bob-plugins/commit/e16f7944494aea3a900785c81ff62f1846603a39) | feat(navigation): resolve highlight targets and open exact PDF at page | [bob-cli-iq.3](bob-cli-iq.3.md) | 2026-11-08 11:27:39 EST |
