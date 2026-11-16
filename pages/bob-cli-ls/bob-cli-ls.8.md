# Bead: bob-cli-ls.8 — Category card subscription linker

[Bead Pages](../README.md) / [bob-cli-ls](README.md) / bob-cli-ls.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cp.md) · **Assignee:** `bob-cli-ls.8` · **Size:** medium
**Created:** 2026-11-15 13:11:22 EST · **Closed:** 2026-11-15 21:10:25 EST
**Plan:** [202611/bank\_subscriptions\_album.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_subscriptions_album.md)

## Description

linker: add the slash picker, the context strip, and the New subscription sheet to the Category card, and connect ghost-chip clicks to them.

## Notes

[2026-11-16T01:37:06Z · bob-cli-ls.8] PROPOSED FOLLOW-UP: Reduce the generated bob-ledger-tools reference page below its 6,000-word cap; docs:check already fails on the clean base at 6,146 words and measures 6,209 with this phase. No existing tracking bead was identified.

[2026-11-16T02:10:25Z · bob-cli-ls.8--2] Verified source commit a6eaea6: npm run build:check passed; focused Category-card and subscription-linker tests passed 38/38; pre-sync Obsidian startup smoke passed; guarded sync deployed bob-ledger-tools 1.118.0; post-sync deployed-vault smoke passed with all four editor cases, relation indexing ready, no runtime errors or crashes, and deployed assets matching source hashes. sase bead epic-symbols bob-cli-ls.8 reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-ls.6](bob-cli-ls.6.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-ls.7](bob-cli-ls.7.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ls.9](bob-cli-ls.9.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.8.md) | [bob-cli-ls.8](bob-cli-ls.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a6eaea6`](https://github.com/bobs-org/bob-plugins/commit/a6eaea6601cbd9c891d34ab6f49e8b55697cb8c5) | feat(bank): link subscriptions from the Category card | [bob-cli-ls.8](bob-cli-ls.8.md) | 2026-11-15 20:58:39 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ls.8--1][1] | Need the phase scope, design, decisions, and prior work notes before resuming deployment | 2 |
| read-by | [agent:bob-cli-ls.9][2] | See whether linker unit test registration was already proposed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.8.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.9/README.md

<!-- sase:referenced-by:end -->
