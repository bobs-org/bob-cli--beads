# Bead: bob-cli-pf.2 — Generic bob props show\|update (bob-cli)

[Bead Pages](../README.md) / [bob-cli-pf](README.md) / bob-cli-pf.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5v.linker.w0.md) · **Assignee:** `bob-cli-pf.2` · **Size:** large
**Created:** 2026-11-22 14:35:12 EST · **Closed:** 2026-11-22 22:53:14 EST
**Plan:** [202611/card\_owned\_frontmatter.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/card_owned_frontmatter.md)

## Description

props-cli: new bob props group on yaml_spans.rs with fingerprinted span ops, role table, typed refusals, byte-exact inverse ops, props_v1 capability, catalog and completion entries, golden byte-preservation tests, docs/props.md contract.

## Notes

[2026-11-22T19:44:23Z · bob-cli-pf.2] PLAN HANDOFF: No earlier props implementation or prior-work notes found at 96a23f50. Authored and validated a child epic with three sequential medium phases: inventory-roles, span-operations, cli-integration. It covers all props-cli scope, semantic fingerprints, role audit, exact-byte undo including absent frontmatter, guarded apply, capability/catalog/completion, tests and docs. No production files changed; the child epic land agent is responsible for completing this phase after verification.

[2026-11-23T03:53:58Z · bob-cli-pf.2.1.land] Child epic bob-cli-pf.2.1 is closed after landing repairs. Generic bob props show|update is implemented and verified: ordered frontmatter inventory, role table, six-op protocol, byte-exact inverse, lock/replan/atomic apply, props_v1 capability, catalog, completion, docs/props.md.

just check exit 0; focused CLI props 18 passed including lock-wait replan; just docs-gen and just docs-check passed. sase bead epic-symbols bob-cli-pf.2 reports no leftover entries. Parent epic bob-cli-pf remains open for its land agent.

## Dependencies

- **Blocks:** [bob-cli-pf.4](bob-cli-pf.4.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.md) | [bob-cli-pf.2](bob-cli-pf.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.5y.cld][1] | Check props-cli phase status and whether role-table audit covers area/project keys | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5y.cld/README.md

<!-- sase:referenced-by:end -->
