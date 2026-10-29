# Bead: bob-cli-e7.1 — Block-ID suggestions skip link URLs

[Bead Pages](../README.md) / [bob-cli-e7](README.md) / bob-cli-e7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b3.md) · **Assignee:** `bob-cli-e7.1` · **Size:** small
**Created:** 2026-10-29 17:02:45 EDT · **Closed:** 2026-10-29 17:17:55 EDT
**Plan:** [202610/wikilink\_task\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/wikilink_task_picker.md)

## Description

id-suggestions: in bob-cli, make the shared block-ID suggestion generator ignore Markdown link destinations and bare URLs, so Keep-captured tasks stop suggesting `https-keep-google-com`; update the pinned tests and the documented algorithm.

## Notes

[2026-10-29T21:17:55Z · bob-cli-e7.1] Shared suggest_ids_with_used now skips Markdown link destinations and bare URLs (scheme:// and www.). Keep-captured 'Try Opus with Blender. [💡](https://keep.google.com/...)' suggests try-opus-blender then opus-blender. Existing pinned suggestion and SB1-SB9 successor mint vectors still pass. docs/capture.md algorithm updated; task-dependencies.md §11.7 has no URL vectors. No --epic-symbol leftovers.

[2026-10-29T21:36:57Z · bob-cli-e7.1--1] PROPOSED FOLLOW-UP: just check `-p bob-obsidian --test cli` fails 7 tests on clean HEAD d0603a5d after e6.1 types wording (meters say "types", tests still expect "themes"; catalog protocol_1 still asserts themes-split path ["themes","split"]). Reproduced without this phase tree. Causal owner bob-cli-e6 / likely e6.16. This phase did not cause it; URL-skip work is complete.

## Dependencies

- **Blocks:** [bob-cli-e7.3](bob-cli-e7.3.md) ◐ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-e7.1.md) | [bob-cli-e7.1](bob-cli-e7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`30e093a`](https://github.com/bobs-org/bob-cli/commit/30e093ac9f8742c39575de476a7a9cf23b927602) | fix(capture): skip URLs in block-ID suggestions | [bob-cli-e7.1](bob-cli-e7.1.md) | 2026-10-29 17:41:28 EDT |
