# Bead: bob-cli-fv.1 — Inert note-text escaper

[Bead Pages](../README.md) / [bob-cli-fv](README.md) / bob-cli-fv.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5o.linker.w0.md) · **Assignee:** `bob-cli-fv.1` · **Size:** small
**Created:** 2026-11-02 09:28:50 EST · **Closed:** 2026-11-02 09:48:12 EST
**Plan:** [202611/gcal\_description\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_description_bullets.md)

## Description

note-escaper: lift gkeep's escape_child_text into task_text_escape.rs unchanged and add escape_note_text / escape_note_inline, which make imported prose inert.

## Notes

[2026-11-02T14:48:12Z · bob-cli-fv.1] note-escaper done: lifted escape_child_text/escape_leading_marker/is_thematic_break/is_code_fence into task_text_escape.rs byte-identical (181 gkeep tests pass unchanged, highlights_ref/ingest.rs re-pointed); added escape_note_inline/escape_note_text with hostile-sample and ordinary-prose unit tests (6/6 pass); just check green (fmt+clippy+workspace tests, 26 suites ok). New fns carry cfg_attr(not(test), allow(dead_code)) until bullet-renderer consumes them.

## Dependencies

- **Blocks:** [bob-cli-fv.5](bob-cli-fv.5.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fv.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fv.1/README.md) | [bob-cli-fv.1](bob-cli-fv.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0dfaeaa`](https://github.com/bobs-org/bob-cli/commit/0dfaeaa3429af245ac7957df87c1abdeea6a8bc6) | feat(native): add shared task\_text\_escape module for note escaping | [bob-cli-fv.1](bob-cli-fv.1.md) | 2026-11-02 09:49:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fv.1][1] | check full desc | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fv.1/README.md

<!-- sase:referenced-by:end -->
