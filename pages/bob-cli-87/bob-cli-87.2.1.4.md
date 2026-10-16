# Bead: bob-cli-87.2.1.4 — Bounded transclusions and complete projection verification

[Bead Pages](../README.md) / [bob-cli-87.2.1](bob-cli-87.2.1.md) / bob-cli-87.2.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.md) · **Assignee:** `bob-cli-87.2.1.4` · **Size:** medium
**Created:** 2026-10-16 07:26:13 EDT · **Closed:** 2026-10-16 10:31:36 EDT
**Plan:** [202610/snapshot\_view\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/snapshot_view_core.md)

## Description

transclusions: assemble one-level full-note, heading, and block transclusions; enforce cycle and size guards; finalize source-aware anchors, diagnostics, and summary accounting. Complete the end-to-end golden and read-once invariant suite.

## Notes

[2026-10-16T14:31:25Z · bob-cli-87.2.1.4--3] PROPOSED FOLLOW-UP: just check has two clean-base failures in command metadata coverage. On detached clean HEAD 8da6615, native::completion::kinds::tests::every_value_arg_has_a_decision reproduced the missing capture-templates delete:template, save:template-origin, and show:template kinds; runner::tests::every_native_command_is_on_exactly_one_canonical_path reproduced 36 commands versus expected 31. The assigned transclusion tests passed.

[2026-10-16T14:31:36Z · bob-cli-87.2.1.4--3] Verified the full-note, heading, and block embeds; exact 64 KiB and 1,500-line boundaries pass while each over-limit case is rejected; self and multi-note cycles, nested embeds, and missing or ambiguous fragments fall back without expansion or fake anchors. Repeated embeds namespace colliding anchors, reuse cached source reads, and remain consistent after source mutation; projection leaves the synthetic vault unchanged. The generated transclusion golden, focused transclusion tests (8), and note_snapshot suite (81) passed, including Pandoc AST checks for spans, divs, links, images, anchors, and preserved code. just check reaches two unrelated command-metadata failures; both reproduced on clean HEAD 8da6615 and are recorded above as PROPOSED FOLLOW-UP. epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-87.2.1.3](bob-cli-87.2.1.3.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.1.4.md) | [bob-cli-87.2.1.4](bob-cli-87.2.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a086cd9`](https://github.com/bobs-org/bob-cli/commit/a086cd9b405cb7ede559163c8625f09aa2605ecd) | feat(note-snapshot): complete bounded transclusions | [bob-cli-87.2.1.4](bob-cli-87.2.1.4.md) | 2026-10-16 10:32:21 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.2.1.4--3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.1.4.md

<!-- sase:referenced-by:end -->
