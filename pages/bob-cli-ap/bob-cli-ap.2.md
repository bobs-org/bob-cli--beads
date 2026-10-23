# Bead: bob-cli-ap.2 — Expose group pieces in bob ref show

[Bead Pages](../README.md) / [bob-cli-ap](README.md) / bob-cli-ap.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12y.md) · **Assignee:** `bob-cli-ap.2` · **Size:** small
**Created:** 2026-10-23 05:11:20 EDT · **Closed:** 2026-10-23 06:15:19 EDT
**Plan:** [202610/tucked\_continuation\_groups.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/tucked_continuation_groups.md)

## Description

show-pieces: add an additive `pieces` array to `bob ref show` JSON for groups, keep the flattened top-level fields, and print each piece with its own comment and a page seam in the human and Markdown formats; document it in docs/ref.md.

## Notes

[2026-10-23T10:15:19Z · bob-cli-ap.2] Exposed group pieces in bob ref show: additive pieces array in JSON (omitted for singles), dim seam lines in human output, italic seam lines in Markdown, -c keeps follower-commented groups with all pieces. Verified: new CLI test show_exposes_group_pieces_with_seams_and_omits_them_for_singles passes, all 20 ref_library::show tests pass, just docs-check passes (447 passed, 1 skipped), just check exits 0. epic-symbols empty. Documented in docs/ref.md.

## Dependencies

- **Depends on:** [bob-cli-ap.1](bob-cli-ap.1.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-ap.3](bob-cli-ap.3.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ap.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ap.2/README.md) | [bob-cli-ap.2](bob-cli-ap.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f2c2453`](https://github.com/bobs-org/bob-cli/commit/f2c24531b5796878af1bff47d984bccababec6bf) | feat(ref): expose annotation group pieces with seams in show | [bob-cli-ap.2](bob-cli-ap.2.md) | 2026-10-23 06:16:21 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ap.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ap.2/README.md

<!-- sase:referenced-by:end -->
