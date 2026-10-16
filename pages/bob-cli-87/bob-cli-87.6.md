# Bead: bob-cli-87.6 — Image embeds that print well

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10l](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10l.md) · **Assignee:** `bob-cli-87.6` · **Size:** small
**Created:** 2026-10-16 07:13:18 EDT · **Closed:** 2026-10-16 15:55:55 EDT
**Plan:** [202610/note\_snapshots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshots.md)

## Description

images: copy embedded images into scratch, downscaled to at most 1600 px on the long edge. Convert GIF and WebP, and give SVG and broken files a placeholder plus a warning.

## Notes

[2026-10-16T19:55:55Z · bob-cli-87.6] Implemented scratch image preparation with 1600 px Lanczos3 downscaling, GIF/WebP-to-PNG conversion, and SVG/undecodable placeholders with warnings; dry runs report image totals, downscales, and missing paths. Verified with the image unit tests, the vault-note image dry-run CLI test, and git diff --check; epic-symbol check found no leftovers.

## Dependencies

- **Blocks:** [bob-cli-87.11](bob-cli-87.11.md) ◐ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-87.5](bob-cli-87.5.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.6/README.md) | [bob-cli-87.6](bob-cli-87.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a4c9ecf`](https://github.com/bobs-org/bob-cli/commit/a4c9ecf511a4e5ef5cfa29ac1868c00f2579a839) | feat(highlights): prepare note snapshot images for print | [bob-cli-87.6](bob-cli-87.6.md) | 2026-10-16 15:56:34 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.6][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.6/README.md

<!-- sase:referenced-by:end -->
