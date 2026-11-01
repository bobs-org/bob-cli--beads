# Bead: bob-cli-ey.2 — bob-cli task drawers, drawer menu, and capture-drawers

[Bead Pages](../README.md) / [bob-cli-ey](README.md) / bob-cli-ey.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2x.linker.w0.md) · **Assignee:** `bob-cli-ey.2` · **Size:** large
**Created:** 2026-10-31 12:52:03 EDT · **Closed:** 2026-11-01 02:42:28 EST
**Plan:** [202610/capture\_drawers\_and\_directives.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_drawers_and_directives.md)

## Description

cli-drawers: make a `#` glued after `@route+id` always name a task drawer, matched exactly, created on demand, and guarded against reserved names and near-duplicates; allow a separate `#type` to retype the target in the same transaction; retire attached `#type` on `+id` and `^id`; add the cached drawer catalog and the `drawer` completion context; add `-D/--drawer` and `bob capture-drawers` (keeping `capture-task-sections` as a hidden alias); bump to `grammar: 3`; rename "task section" everywhere; write the Task Drawer term, the grammar decision record, and the Annotation Section fix.

## Notes

[2026-11-01T07:42:10Z · bob-cli-ey.2--3] PROPOSED FOLLOW-UP: capture output still carries parent_section (drawer title string) with no per-item drawer {title, key, created} object; plan sec4 calls for drawer object plus legacy first-item mirror. Left as-is to keep just check green and wire compatible with ey.5 Mac pickers; revisit when ey.5 defines the preview contract.

[2026-11-01T07:42:16Z · bob-cli-ey.2--3] PROPOSED FOLLOW-UP: docs/reference/mac-capture/protocol.md and task-pickers.md still name task_section completion; those pages are mounted from bob-mac-capture and owned by ey.5, so not edited here.

[2026-11-01T07:42:28Z · bob-cli-ey.2--3] feat(capture)!: glued #drawer capture with exact matching, on-demand creation, drawer menu, and capture-drawers

Implemented cli-drawers per plan:202610/capture_task_drawers.md: DrawerSelector with slug/literal keys, exact matching, reserved/near-duplicate/ambiguous refusals, catalog-backed creation spelling, single-header batch coalescing, separate #type retype in same transaction, R3 ^id refusal, !-toggle refusal, ^prj refusal, GRAMMAR_REVISION 3 with schema_version 1, drawer completion context/menu, -D/--drawer, canonical capture-drawers with hidden capture-task-sections alias, full test coverage, docs and memory strands (glossary:task-drawer, decisions:capture-sigils-say-where-what-how, annotation-section link).

Verification: cargo fmt clean; just check exit 0 (all suites green, 0 failed incl. 4251 lib tests); just docs-gen + docs-check green; rg audit clean except allowed hidden-alias/negative/unrelated-mounted refs; perf on 400-note/1200-task fixture: cold drawer 19.6ms, drawer warm median 23.7ms p90 34.0ms vs type warm median 34.0ms p90 41.2ms (delta -10.4ms, within 20ms target); sase bead epic-symbols clean.

BREAKING CHANGE: removes attached @route+id#type and @route^id#type forms, -S/--task-section, and the task_section/sub_bullet_section span, need, context, and command names.

## Dependencies

- **Depends on:** [bob-cli-ey.1](bob-cli-ey.1.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.4](bob-cli-ey.4.md) ○ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.5](bob-cli-ey.5.md) ◐ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.6](bob-cli-ey.6.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.2.md) | [bob-cli-ey.2](bob-cli-ey.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e660c8d`](https://github.com/bobs-org/bob-cli/commit/e660c8d8844df3542f701a4b83cd1fc6826bf5f3) | feat(capture)!: glued #drawer capture with exact matching, on-demand creation, drawer menu, and capture-drawers | [bob-cli-ey.2](bob-cli-ey.2.md) | 2026-11-01 02:44:01 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.2--3][1] | final state check before closing drawer phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.2.md

<!-- sase:referenced-by:end -->
