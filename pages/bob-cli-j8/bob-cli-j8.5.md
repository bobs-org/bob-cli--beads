# Bead: bob-cli-j8.5 — Notebook completion, block IDs, and the @@ collapse assist

[Bead Pages](../README.md) / [bob-cli-j8](README.md) / bob-cli-j8.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3x.linker.w0.md) · **Assignee:** `bob-cli-j8.5` · **Size:** large
**Created:** 2026-11-09 12:11:27 EST · **Closed:** 2026-11-10 02:19:40 EST
**Plan:** [202611/bob\_notebooks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_notebooks.md)

## Description

capture-notebook-assist: give capture-complete notebook route rows, `##` section rows with a create row, `@nb^` ID suggestions marked `destination_kind`, `@nb+` note-bullet rows with ID minting through capture-task-id, an enabled `%n` row on sealed items, and (per collapse_assist) the capture-rewrite `@@route` collapse.

## Notes

[2026-11-10T07:19:32Z · bob-cli-j8.5] Implemented notebook capture assist per plan:202611/notebook_capture_assist.md. Collapse rule collapse_global_destination with 7 triggers ahead of aliases; notebook H2-only sections with additive notebook_section_create row and ^id-suffix trimming; block-ID destination_kind notebook via threaded policy; note-scoped @nb+ rows with item_kind note over shared notebook_bullets scan plus capture-task-id notebook assignment returning parent_replacement @nb+ID and item_kind note; %n New notebook row independent of Pomodoro. Help updated (capture-task-id, capture-rewrite) with just docs-gen fixtures; docs/capture.md, docs/reference/json-outputs.md, docs/notebooks.md updated. Memory correction glossary:capture-alias applied (removed @ routes from / literal list; named @route collapse beside @ absorption) with sase memory init republished. Verified: focused suites green (rewrite 81, completion 86, capture_complete 188+, task_id notebook), just check exit=0. just docs-check fails identically on clean base (exit=2, bob-mac-capture mount collides with docs/reference/mac-capture/index.md) — unrelated/environmental, no phase left open for it. Epic-symbols: none.

[2026-11-10T07:19:40Z · bob-cli-j8.5] Implemented and verified: collapse_global_destination rewrites, notebook section rows with create row, notebook-aware block IDs, @nb+ note rows with item_kind note, capture-task-id notebook assignment with @nb+ID parent_replacement, %n New notebook directive, updated help/docs with regenerated fixtures, and the glossary:capture-alias memory correction. just check green; docs-check unrelated failure documented on the bead.

## Dependencies

- **Depends on:** [bob-cli-j8.4](bob-cli-j8.4.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j8.8](bob-cli-j8.8.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.5.md) | [bob-cli-j8.5](bob-cli-j8.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`93cf930`](https://github.com/bobs-org/bob-cli/commit/93cf930ca2a8221bdbe4b1dad602ef49669f3f18) | feat(capture)!: complete notebook capture assistance | [bob-cli-j8.5](bob-cli-j8.5.md) | 2026-11-10 02:30:29 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j8.7][1] | Check whether the parallel ledger-tools phase will touch the same fragments | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.7/README.md

<!-- sase:referenced-by:end -->
