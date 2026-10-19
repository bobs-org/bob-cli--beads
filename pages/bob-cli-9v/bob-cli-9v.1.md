# Bead: bob-cli-9v.1 — Portable RefsCore model, geometry, and 5-per-page default

[Bead Pages](../README.md) / [bob-cli-9v](README.md) / bob-cli-9v.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11v.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11v.w0.md) · **Assignee:** `bob-cli-9v.1` · **Size:** medium
**Created:** 2026-10-19 12:32:44 EDT · **Closed:** 2026-10-19 12:54:33 EDT
**Plan:** [202610/refs\_reading\_room.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_reading_room.md)

## Description

refs-core-model: decode image fields from ref show, define the generalized preview feed (image highlights, attached images, unavailable images, standalone notes), add pure panel/inspector geometry, image sizing, and vault-path resolution in RefsCore with Linux tests, and raise the page size default to 5.

## Notes

[2026-10-19T16:54:33Z · bob-cli-9v.1] Implemented RefsCore image decoding and feed models, image sizing and vault-path helpers, panel geometry, five-item paging, and the selected standalone-notes include behavior. Verified just portable-check (1,431 tests), Mac Scripts/bundle.sh, just typecheck-tests, and no remaining epic symbols. CI remains for the land step after this uncommitted work reaches origin.

## Dependencies

- **Blocks:** [bob-cli-9v.2](bob-cli-9v.2.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-9v.3](bob-cli-9v.3.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9v.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9v.1/README.md) | [bob-cli-9v.1](bob-cli-9v.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@c424756`](https://github.com/bobs-org/bob-mac-capture/commit/c4247566fb4e8c5f796ff3e8ef109b3d2760b982) | feat(refs): add portable image and panel models | [bob-cli-9v.1](bob-cli-9v.1.md) | 2026-10-19 12:55:03 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9v.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9v.1/README.md

<!-- sase:referenced-by:end -->
