# Bead: bob-cli-ey.7.1 — bob-cli drawer writes, retype, capture output, and refusal codes

[Bead Pages](../README.md) / [bob-cli-ey.7](bob-cli-ey.7.md) / bob-cli-ey.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.land.md) · **Assignee:** `bob-cli-ey.7.1` · **Size:** medium
**Created:** 2026-11-01 03:50:53 EST · **Closed:** 2026-11-01 04:45:41 EST
**Plan:** [202611/finish\_capture\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_capture_drawers.md)

## Description

drawer-writes: let a separate #type on a body-bearing @route+id item retype the target in the same transaction. Fix the stray blank line written when a drawer is created. Replace parent_section with a per-item drawer {title, key, created} object and show 'new drawer' plus the type row in human and dry-run output. Add title/key to drawer spans, JSON codes to every drawer refusal, and the drawer_near_catalog warning.

## Notes

[2026-11-01T09:45:41Z · bob-cli-ey.7.1] drawer-writes landed: separate #type retypes +id target in same transaction (D8 relocation, one atomic batch); blank-line on drawer creation fixed (header no longer double-newlines, simplified create branch); parent_section replaced by drawer {title,key,created} (null for plain child) with human 'new drawer' + type row; drawer spans carry title/key; refusal codes for invalid_drawer/drawer_text/ambiguous/reserved/near_duplicate/drawer_toggle/R3; drawer_near_catalog warning via capture warnings. Verified: cargo test -p bob-obsidian --test cli 2605 passed, cargo test --lib capture_language 444 passed, just docs-check passed (447), git grep parent_section clean, landing smokes for writes (retype BUILD->FIX, new-drawer bytes without blank line, drawer_text/reserved/near_duplicate/ambiguous codes, warning, toggle code) pass. No Cargo.toml/CHANGELOG edits.

## Dependencies

- **Blocks:** [bob-cli-ey.7.2](bob-cli-ey.7.2.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-ey.7.4](bob-cli-ey.7.4.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.7.1/README.md) | [bob-cli-ey.7.1](bob-cli-ey.7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f2b599c`](https://github.com/bobs-org/bob-cli/commit/f2b599c4a26ce49a5fc525d32c5a7975003de9aa) | feat(capture)!: drawer writes, retype, and drawer JSON contract | [bob-cli-ey.7.1](bob-cli-ey.7.1.md) | 2026-11-01 04:47:00 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.7.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.7.1/README.md

<!-- sase:referenced-by:end -->
