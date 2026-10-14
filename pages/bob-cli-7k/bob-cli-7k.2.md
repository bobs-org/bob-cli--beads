# Bead: bob-cli-7k.2 — RefsCore decoding, copy catalog, formats, key map, and card state machine

[Bead Pages](../README.md) / [bob-cli-7k](README.md) / bob-cli-7k.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.19.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.19.linker.w0.md) · **Assignee:** `bob-cli-7k.2` · **Size:** medium
**Created:** 2026-10-14 09:32:31 EDT · **Closed:** 2026-10-14 09:48:59 EDT
**Plan:** [202610/refs\_ctrl\_y\_copy\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_ctrl_y_copy_card.md)

## Description

refs-copy-core: in bob-mac-capture's portable RefsCore, decode marker_id, research_ref, annotation block_id/link, and own_notes; build the pure fixed-letter copy catalog, payload formatters, card layout capacity, key map, and the RefsCopyCard state machine, all Linux-tested.

## Notes

[2026-10-14T13:48:59Z · bob-cli-7k.2] Implemented the RefsCore decoder additions, copy catalog and formats, layout, key map, and card state machine with tests. Verified by just portable-check on Athena: 1,139 tests passed. epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-7k.3](bob-cli-7k.3.md) ✓ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7k.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.2/README.md) | [bob-cli-7k.2](bob-cli-7k.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@060d77b`](https://github.com/bobs-org/bob-mac-capture/commit/060d77b41a79df7b529c9085f184b76928c0cbbb) | feat(refs-core): implement copy catalog and card state machine | [bob-cli-7k.2](bob-cli-7k.2.md) | 2026-10-14 09:50:04 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7k.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.2/README.md

<!-- sase:referenced-by:end -->
