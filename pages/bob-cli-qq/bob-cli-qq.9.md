# Bead: bob-cli-qq.9 — Switch cabinets on, docs, approved memory, and clean deploy

[Bead Pages](../README.md) / [bob-cli-qq](README.md) / bob-cli-qq.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6m.linker.w0.md) · **Assignee:** `bob-cli-qq.9` · **Size:** medium
**Created:** 2026-11-26 16:09:03 EST · **Closed:** 2026-11-27 17:43:38 EST
**Plan:** [202611/property\_card\_cabinets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_cabinets.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:b43b18736a494f39c0fdc3fc | go-live post-switch smoke evidence from bob-cli-qq.10.5 |
| related | file:explicit:c3a82701e970e5187726a714 | go-live post-switch smoke evidence from bob-cli-qq.10.5 |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

go-live: once the gating sibling go-lives have closed, delete the gate and update the docs in both repos. Write the new cabinets reference page and the approved memory (glossary:cabinet and the selected card strands and record). Then run the family passive proof, `bob plugins sync`, and a post-switch smoke that includes the prose Outline cabinet.

## Notes

[2026-11-27T22:43:38Z · bob-cli-qq.10.6] docs-memory done: bob-plugins 680ee414 adds docs/cabinets.md, updates the family pages, and brings bob-ledger-tools.md under the 6000-word cap (5569); npm run docs:check green and bob plugins sync clean. Memory: glossary:cabinet added; glossary:property-card, area-card, project-card updated for cabinets and _; decisions:cabinets-absorb-catalogs-at-render-time added; sase memory init + just docs-gen + just docs-check green in bob-cli. Switch-on smoke evidence retained from 10.5 (file:explicit:b43a18736a494f39c0fdcfc, file:explicit:c3a82701e970e5187726a714); GO on bob-cli-qq.8 covers content parity. No bob-cli code changed.

## Dependencies

- **Depends on:** [bob-cli-qm.7](../bob-cli-qm/bob-cli-qm.7.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qp.8](../bob-cli-qp/bob-cli-qp.8.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qq.8](bob-cli-qq.8.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.9/README.md) | [bob-cli-qq.9](bob-cli-qq.9.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qp.land][1] | Check whether cabinets go-live is actively editing the cabinets e2e runner that still writes the removed refCardPreview gate key | 3 |
| read-by | [agent:bob-cli-qq.10.6][2] | check go-live bead status before docs-memory close | 1 |
| read-by | [agent:bob-cli-qq.7][3] | list epic children statuses | 1 |
| read-by | [agent:research.6o.cld][4] | Need the in-progress cabinet epic children state to plan parallel link-walk work | 1 |
| read-by | [agent:research.6o.final][5] | Consolidating link-walk research: need current cabinets finishing-phase status to sequence parallel work | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qp.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.6/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.7/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6o.cld/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6o.final/README.md

<!-- sase:referenced-by:end -->
