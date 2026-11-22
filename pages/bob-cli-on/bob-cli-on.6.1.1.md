# Bead: bob-cli-on.6.1.1 — Numeric authored depth with today's behavior kept

[Bead Pages](../README.md) / [bob-cli-on.6.1](bob-cli-on.6.1.md) / bob-cli-on.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.md) · **Assignee:** `bob-cli-on.6.1.1` · **Size:** medium
**Created:** 2026-11-21 13:50:29 EST · **Closed:** 2026-11-21 15:11:23 EST
**Plan:** [202611/capture\_req\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_req_bullets.md)

## Description

depth-model: turn AuthoredDepth into a numeric level, teach the authored-line classifier any even-space level with a capped form, move every consumer and the grouping helpers onto it, and make the sub-bullet renderers depth-preserving, all without changing any capture, parse, or rewrite output.

## Notes

[2026-11-21T20:11:09Z · bob-cli-on.6.1.1] HANDOFF for req-positions: AuthoredDepth is a Copy newtype (FIRST/NESTED, from_level, level, indent_units, is_first, is_nested, shallower, MAX_LEVEL=64). classify_authored_line reads any even-space level; classify_authored_line_capped(line, TWO_LEVEL_CAP) is the old two-level classifier byte for byte; strip_authored_bullet(line, max) is the shared stripper. Deeper marker-only rows (`    - `) stay Invalid. The four task-host parser loops (item.rs parse_capture_item main loop and parse_list_bullet_item; editor_parse.rs parse_editor_item_inner and parse_editor_list_item) classify uncapped and route `depth.level() > TWO_LEVEL_CAP` into the existing invalid_child_line branch: replace that guard with the resolver. DEVIATION from plan step 3: uncapping tokens.rs selectors, type_marker/directive authored_body, item.rs target-run child loops, completion child-line contexts, and dependencies.rs changed outputs on level-3 drafts (`Task\n- note\n    - deep +abc` dropped invalid_child_line for an interactive placeholder and bob capture reported a task-selection error; a level-3 `#fix` became a task_type span; capture-parse gained `targets`; capture-rewrite returned a sigil_alias_tip). So those helpers, all rewrite.rs sites, and the editor drawer-grouping scan stay capped at TWO_LEVEL_CAP; grep TWO_LEVEL_CAP to lift each cap where the resolver admits the line. Grouping (first_level_groups via new authored_level_groups, editor drawer grouping) uses is_nested(); renders are depth-preserving (render_authored_sub_bullets, new render_nested_sub_bullets in plan_multi_note_sub_bullet_item incl. drawer-entry subtrees, capture_project_note nested_line for rows and section entries).

[2026-11-21T20:11:23Z · bob-cli-on.6.1.1] depth-model done (refactor(capture), no output change). AuthoredDepth is a numeric newtype; classify_authored_line reads any even-space level up to 64 with classify_authored_line_capped(…, TWO_LEVEL_CAP) as the exact old classifier; all ~65 callers audited (Ineligible hosts, first-level rules, rewrite.rs, and the lexical helpers capped; task-host parsers uncapped with an explicit level>2 → invalid_child_line guard); first_level_groups generalized via authored_level_groups; new-task, multi-note @route+id (plain, glued drawer, drawer entries), and project-note row/section renders are depth-preserving. Verified: just check green (fmt, clippy, 43 test binaries, 0 failures; existing tests changed only by the mechanical First/Nested → FIRST/NESTED rename); new unit tests for the classifier (levels 1–4, odd/tab/mixed prefixes, capped form, 64-level bound and u8 overflow), AuthoredDepth predicates, parser refusals of level 3 with code and range, level groups, and level-3 renders; baseline-vs-new binary diff of capture --dry-run, capture-parse, and capture-rewrite + capture-complete at every cursor over 51 drafts with level-3+ lines: byte-identical apart from the temp vault path. Deviation from plan step 3 (lexical helpers kept capped to honor no-output-change) recorded in the HANDOFF note. No docs or grammar change; no epic symbols.

## Dependencies

- **Blocks:** [bob-cli-on.6.1.2](bob-cli-on.6.1.2.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.1/README.md) | [bob-cli-on.6.1.1](bob-cli-on.6.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1d89d95`](https://github.com/bobs-org/bob-cli/commit/1d89d95f3b2288601111965abad896eff5fd0195) | refactor(capture): make authored bullet depth a numeric level | [bob-cli-on.6.1.1](bob-cli-on.6.1.1.md) | 2026-11-21 15:12:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.6.1.1][1] | Check for prior notes before closing | 2 |
| read-by | [agent:bob-cli-on.6.1.2][2] | check depth-model notes | 2 |
| read-by | [agent:bob-cli-on.6.1.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.1.land.md

<!-- sase:referenced-by:end -->
