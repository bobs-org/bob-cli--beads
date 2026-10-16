# Bead: bob-cli-8g.3 — Number-aware capture section selectors in articles

[Bead Pages](../README.md) / [bob-cli-8g](README.md) / bob-cli-8g.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1o.linker.w0.md) · **Assignee:** `bob-cli-8g.3` · **Size:** small
**Created:** 2026-10-16 10:53:03 EDT · **Closed:** 2026-10-16 12:24:02 EDT
**Plan:** [202610/article\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/article_notes.md)

## Description

capture: in article notes, `@route#prefix` and `--section` match headings by de-numbered identity as well as raw title, so captures keep finding renumbered sections.

## Notes

[2026-10-16T16:24:02Z · bob-cli-8g.3] Article notes match @route#prefix and --section on de-numbered heading identity as well as raw title. Unit and CLI tests cover #agent → 1.3 Agent CLIs, #1.3 preferring 1.3 over 1.3.1 in document order, exact Agent CLIs and stale 1.4 Agent CLIs, and non-article numbered headings keeping raw matching. capture-sections output unchanged. cargo fmt --check and the project clippy unused gate passed. sase bead epic-symbols reported no leftovers.

[2026-10-16T16:42:16Z · bob-cli-8g.3--1] PROPOSED FOLLOW-UP: just check lib failures reproduce on clean HEAD — every_value_arg_has_a_decision missing capture-templates delete:template, save:template-origin, show:template; every_native_command_is_on_exactly_one_canonical_path 36 vs 31 (bob-cli-8b, also 8g.1#1); renders_contract_with_clean_text_layer_and_metadata titlesec.sty missing and pandoc_maps_every_contract_construct_to_tex lifted link (bob-cli-87, 8g.1#2).

[2026-10-16T16:42:37Z · bob-cli-8g.3--1] Verified article @route#prefix and --section identity matching: 50 placement unit tests and 18 capture sections CLI tests passed, including de-numbered prefix, #1.3 preferring 1.3 over 1.3.1, exact and stale numbers, plain identity, and non-article raw matching. capture-sections JSON tests still pass. just check lib 4 failures reproduce on clean HEAD (capture-templates kinds/NativeCommand on bob-cli-8b; titlesec.sty and lifted-link snapshot on bob-cli-87 / 8g.1). No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-8g.1](bob-cli-8g.1.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8g.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8g.3.md) | [bob-cli-8g.3](bob-cli-8g.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a3e45a3`](https://github.com/bobs-org/bob-cli/commit/a3e45a3b530163829087975f234d1f08d004dee5) | feat(capture): match article section selectors on de-numbered identity | [bob-cli-8g.3](bob-cli-8g.3.md) | 2026-10-16 12:43:32 EDT |
