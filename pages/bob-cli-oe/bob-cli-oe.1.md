# Bead: bob-cli-oe.1 — bob capture --jump-offer and the jump JSON contract

[Bead Pages](../README.md) / [bob-cli-oe](README.md) / bob-cli-oe.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5m.linker.w0.md) · **Assignee:** `bob-cli-oe.1` · **Size:** medium
**Created:** 2026-11-20 17:03:14 EST · **Closed:** 2026-11-20 17:51:32 EST
**Plan:** [202611/successor\_jump\_pin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_pin.md)

## Description

cli-jump-offer: add `-j, --jump-offer <N|KEY>` to `bob capture`, the `pull_in.jump.supported` capability, the write-free `offer_jump_stale` refusal, and a top-level `jump` object resolved from final staged text (routed moves, block IDs, cleaned description), with dry-run parity, contract vectors, and docs §12.24 plus the picker v5 rows.

## Notes

[2026-11-20T22:51:14Z · bob-cli-oe.1] PROPOSED FOLLOW-UP: Trim docs/reference/vault-format.md by at least 16 words to meet the 6,000-word reference budget; just docs-check reports 6,016 words on the unchanged HEAD file, and no matching task bead exists.

[2026-11-20T22:51:32Z · bob-cli-oe.1] Implemented --jump-offer, staged-text jump resolution, pull_in.jump capability, stale-selector refusal, docs, generated CLI reference, and JS1–JS10 coverage. Verified cargo check --tests; 1,935 capture CLI tests and 35 help tests passed. just docs-gen passed. just docs-check remains blocked by unchanged docs/reference/vault-format.md at 6,016/6,000 words; recorded proposed follow-up. No epic symbols remain.

## Dependencies

- **Blocks:** [bob-cli-oe.6](bob-cli-oe.6.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oe.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.1/README.md) | [bob-cli-oe.1](bob-cli-oe.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`853246f`](https://github.com/bobs-org/bob-cli/commit/853246f0ee582f4559767323c101dd2d2597cf91) | feat(capture): add successor jump offer contract | [bob-cli-oe.1](bob-cli-oe.1.md) | 2026-11-20 17:53:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oe.1][1] | Need the epic design, phase notes, and prior-work status before implementation | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oe.1/README.md

<!-- sase:referenced-by:end -->
