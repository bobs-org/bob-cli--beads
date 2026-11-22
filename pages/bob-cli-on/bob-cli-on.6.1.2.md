# Bead: bob-cli-on.6.1.2 — Shared requirement position resolver, refusals, req\_marker span, grammar 29

[Bead Pages](../README.md) / [bob-cli-on.6.1](bob-cli-on.6.1.md) / bob-cli-on.6.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.md) · **Assignee:** `bob-cli-on.6.1.2` · **Size:** medium
**Created:** 2026-11-21 13:50:29 EST · **Closed:** 2026-11-21 19:05:12 EST
**Plan:** [202611/capture\_req\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_req_bullets.md)

## Description

req-positions: add the pure req-position resolver shared by bob capture and capture-parse, admit nested req chains past level 2, refuse req_in_drawer, req_parent, req_state, and req_depth, emit req_marker spans with depth, and bump the grammar to revision 29.

## Notes

[2026-11-22T00:04:45Z · bob-cli-on.6.1.2] PROPOSED FOLLOW-UP: Update the Mac protocol docs for deeper sub_bullet_depths — docs/reference/mac-capture/protocol.md and capture-previews.md are mounted from bob-mac-capture (gitignored here) and still say sub_bullet_depths is 1 or 2; in grammar 29 depths can exceed 2 beneath requirements. Edit in the bob-mac-capture repo (its macOS CI watch rule applies).

[2026-11-22T00:04:50Z · bob-cli-on.6.1.2] PROPOSED FOLLOW-UP: Lift the remaining TWO_LEVEL_CAP lexical helpers for lines admitted beneath requirement chains — tokens.rs parent selectors (a `+que` on a level-3 req line stays literal in both parsers while level 2 opens the parent picker), item.rs target-run child loops, completion.rs child-line contexts, and rewrite.rs sites (req-rewrite may need these). dependencies.rs scan_item_dependencies was lifted here via the shared LevelGate, because `&` on a deep line was otherwise stripped and silently dropped.

[2026-11-22T00:04:55Z · bob-cli-on.6.1.2] PROPOSED FOLLOW-UP: Give bob capture JSON a code for the remaining generic child-line errors — the main item path still reports empty_child_after_markers, orphaned_nested_bullet, and malformed-line invalid_child_line without a `code` (pre-existing). The four req_* codes and the requirement-hint invalid_child_line are coded. task_reqs::copy holds REQ_IN_DRAWER/PARENT/STATE/DEPTH; req_link copy joins it with its first use in existing-target-writes.

[2026-11-22T00:04:59Z · bob-cli-on.6.1.2] PROPOSED FOLLOW-UP: just docs-check still fails only in tools/docs/tests/test_contracts.py (3 tests; contract registry 55 vs 54), identical on the clean base tree. Already recorded on bob-cli-on; docs lint, generated drift, strict build, URLs, and lychee all pass with this change.

[2026-11-22T00:05:12Z · bob-cli-on.6.1.2] req-positions done. Added capture_language/req_bullets.rs: ReqHost::from_kind/from_mode, a lexical LevelGate for the parser loops, and resolve() (roles Note/Req{depth}/DrawerHeader/DrawerEntry/ProjectRow/Refused; checks position -> req_state -> req_depth; refused subtrees silent; empty req placeholder vs empty_child_after_markers). bob capture main and task-list paths admit level>=3 beneath req chains, record AuthoredSubBullet.req, and refuse req_in_drawer/req_parent/req_state/req_depth with JSON codes (plus invalid_child_line with the requirement hint); forced --task/--task-ref/--drawer re-resolve in plan.rs; a placeholder-only @route+id reads like Ensure Next in both parsers. capture-parse emits req_marker spans with wire depth via EditorItemParse.req_markers, diagnostics on each bullet line, %n stays Ineligible. Copy hoisted to task_reqs::copy (writers use it). Interim writes keep authored depth (multi-note human preview no longer flattens). Item dependency scan uses the same gate. GRAMMAR_REVISION 29 with help, tests, and docs (capture.md requirement-bullets section, capture-syntax, json-outputs, compatibility, task-requirements §5, generated CLI refs). Verified: cargo fmt check, just lint (exit 0), full cargo test --workspace (43 binaries, 0 failures; 32 new language tests in tests/reqs.rs, 19 new CLI tests in parse_reqs.rs and reqs_refusals.rs incl. dry-run/capture-parse code parity and depth-3+ writes for new task, multi-note, same-line, project-note row), just docs-gen (no further drift), docs-check passes except the 3 pre-existing test_contracts.py failures that reproduce on the clean base. No epic symbols.

## Dependencies

- **Depends on:** [bob-cli-on.6.1.1](bob-cli-on.6.1.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.6.1.3](bob-cli-on.6.1.3.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.6.1.5](bob-cli-on.6.1.5.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.2/README.md) | [bob-cli-on.6.1.2](bob-cli-on.6.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7cc9493`](https://github.com/bobs-org/bob-cli/commit/7cc94933c2b3922e9a4c6eb80c9fc8415ce09311) | feat(capture)!: admit requirement bullets with req\_marker spans (grammar 29) | [bob-cli-on.6.1.2](bob-cli-on.6.1.2.md) | 2026-11-21 19:06:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.6.1.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.2/README.md

<!-- sase:referenced-by:end -->
