# Bead: bob-cli-k3.4.1.2 — Album-aware records commands and membership checks

[Bead Pages](../README.md) / [bob-cli-k3.4.1](bob-cli-k3.4.1.md) / bob-cli-k3.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-k3.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.4.md) · **Assignee:** `bob-cli-k3.4.1.2` · **Size:** medium
**Created:** 2026-11-11 09:19:33 EST · **Closed:** 2026-11-11 11:19:01 EST
**Plan:** [202611/album\_record\_consumers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_record_consumers.md)

## Description

records-surface: route records commands through the shared context, accept noun and stem selectors, add source and album output, retain invalid collection counts, and implement album membership and checkbox checks.

## Notes

[2026-11-11T15:36:24Z · bob-cli-k3.4.1.2] Verified album-aware records CLI on isolated vaults: noun/stem selectors, -b over BOB_DIR, broken album suppressing config, healthy album despite malformed config/neighbor, canonical [[record]] plus record_type_legacy, parent/checkbox/orphan/missing-stub, malformed schema counts, byte-exact create and span-preserving update with dry-run equality, broken-album members not orphans. just lint green. just check via prepared monitor.

[2026-11-11T16:19:01Z · bob-cli-k3.4.1.2--2] Verified album-aware records CLI on isolated vaults: noun/stem selectors, -b over BOB_DIR, broken album suppressing config, healthy album despite malformed neighbor, canonical [[record]] plus record_type_legacy, parent/checkbox/orphan/missing-stub, malformed schema counts, byte-exact create and span-preserving update with dry-run equality, broken-album members not orphans. Root help snapshots match. just check (sase tool run check 075822f0ee1567d32188ce6125793f24) passed. No leftover --epic-symbol entries. Parent epic left open.

## Dependencies

- **Depends on:** [bob-cli-k3.4.1.1](bob-cli-k3.4.1.1.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.4.1.2.md) | [bob-cli-k3.4.1.2](bob-cli-k3.4.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c36e6e7`](https://github.com/bobs-org/bob-cli/commit/c36e6e752d36828f6bd73e09cb095d7c70d25498) | feat(records): add album-aware records commands and membership checks | [bob-cli-k3.4.1.2](bob-cli-k3.4.1.2.md) | 2026-11-11 11:19:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k3.4.1.2--2][1] | Need the phase scope, notes, and design after green check failed to land | 1 |
| read-by | [agent:bob-cli-k3.4.1.3][2] | Need sibling phase scope to avoid conflicts | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.4.1.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.4.1.3/README.md

<!-- sase:referenced-by:end -->
