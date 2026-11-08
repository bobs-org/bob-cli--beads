# Bead: bob-cli-iq.4 — The Highlights toast card

[Bead Pages](../README.md) / [bob-cli-iq](README.md) / bob-cli-iq.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3o.linker.w0.md) · **Assignee:** `bob-cli-iq.4` · **Size:** small
**Created:** 2026-11-08 10:40:42 EST · **Closed:** 2026-11-08 11:44:18 EST
**Plan:** [202611/highlights\_annotation\_page\_jump.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/highlights_annotation_page_jump.md)

## Description

toast: replace the plain announce notices with one rich .bob-nh-notice Highlights card in highlighter ink. It shows a page receipt, the title, and a quote snippet, appears before dispatch, and updates in place on failure.

## Notes

[2026-11-08T16:44:18Z · bob-cli-iq.4] Implemented the rich Highlights notice card with opening, unavailable, failure, removed, missing-highlight, archive, and no-DOM fallback states; added styling, documentation, and focused tests. Verified with npm test (5725 passed, 1 skipped), npm run validate, npm run docs:check (all implemented gates passed), and bob plugins sync --repo for the linked checkout. epic-symbols reports none.

## Dependencies

- **Depends on:** [bob-cli-iq.3](bob-cli-iq.3.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-iq.5](bob-cli-iq.5.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-iq.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-iq.4/README.md) | [bob-cli-iq.4](bob-cli-iq.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6390587`](https://github.com/bobs-org/bob-plugins/commit/6390587b15a771ecd7b188e01bb93d9bbee170f5) | feat(navigation): add Highlights toast card | [bob-cli-iq.4](bob-cli-iq.4.md) | 2026-11-08 11:45:15 EST |
