# Bead: bob-cli-ld.3 — Plugin dual-format SUBOPEN reader and conversion guard

[Bead Pages](../README.md) / [bob-cli-ld](README.md) / bob-cli-ld.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c6.md) · **Assignee:** `bob-cli-ld.3` · **Size:** medium
**Created:** 2026-11-13 10:58:46 EST · **Closed:** 2026-11-13 12:29:14 EST
**Plan:** [202611/subprojects\_catalog\_section.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subprojects_catalog_section.md)

## Description

subopen-reader-plugins: mirror the reader rule in task-status-cycler against the byte-identical vectors, keep nav conversion from copying the callout, and deploy before any writer ships.

## Notes

[2026-11-13T17:28:38Z · bob-cli-ld.3] PROPOSED FOLLOW-UP: bob-plugins npm test 6492/6496 — keep-moving and off-clock 200-link Live Preview budgets failed under full parallel load (255.9 ms and 64.8 ms) and passed isolated 70/70; tracked by bob-cli-ki and bob-cli-ju

[2026-11-13T17:28:56Z · bob-cli-ld.3] PROPOSED FOLLOW-UP: bob-plugins npm run docs:check lint fails on mounted reference/plugins/bob-ledger-tools.md 6136/6000 (unchanged, bob-cli-il) and bob-navigation-hotkeys.md 6082/6000 (already 6055 on HEAD, bob-cli-jz); this phase added 27 words of conversion-guard docs

[2026-11-13T17:29:14Z · bob-cli-ld.3] Verified dual-format SUBOPEN in task-status-cycler 1.51.0 and nav conversion skip in bob-navigation-hotkeys 2.82.0. 089a-project-catalog-rows.js mirrors catalog_rows.rs (catalog first, legacy fallback, JS damage=open); vectors.json SHA-256 c685dd31ee99ded534b8e5c0f0ff9d8679d1dab88c450f48f4e42e05ce8d19a9 matches bob-cli; 085b/089 callers use the helper; 086/256 left legacy-only. Targeted tests 65/65 (catalog, PP29 pull-in, reversal). npm test 6492 pass / 2 fail / 2 skip (load flakes bob-cli-ki/ju; isolated 70/70). docs:inventory:check green; docs-check word caps pre-existing (bob-cli-il/jz). bob plugins sync deployed cycler 1.51.0 and nav 2.82.0 (ancestor stamp 2ee64e6 rewritten, no -F). No epic-symbols. No memory edits.

## Dependencies

- **Depends on:** [bob-cli-ld.2](bob-cli-ld.2.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-ld.7](bob-cli-ld.7.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.3/README.md) | [bob-cli-ld.3](bob-cli-ld.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7b27f05`](https://github.com/bobs-org/bob-plugins/commit/7b27f051620a4cb90618d50557b74b8c53685e4e) | feat(plugins): add dual-format SUBOPEN catalog reader | [bob-cli-ld.3](bob-cli-ld.3.md) | 2026-11-13 12:30:34 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ld.3][1] | Need full description, notes, and design file contents | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.3/README.md

<!-- sase:referenced-by:end -->
