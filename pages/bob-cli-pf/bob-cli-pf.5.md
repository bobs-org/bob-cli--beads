# Bead: bob-cli-pf.5 — Rename, reorder, multi-select, copy/paste, filter, kind change, YAML stage (bob-plugins)

[Bead Pages](../README.md) / [bob-cli-pf](README.md) / bob-cli-pf.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5v.linker.w0.md) · **Assignee:** `bob-cli-pf.5` · **Size:** large
**Created:** 2026-11-22 14:35:12 EST · **Closed:** 2026-11-23 20:30:13 EST
**Plan:** [202611/card\_owned\_frontmatter.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/card_owned_frontmatter.md)

## Description

editor-parity: completes native Properties parity and beyond in =+ with rename, reorder, multi-select batch ops, YAML copy and overwrite-previewed paste, filter, feature-detected kind and vault type change, and a validated YAML stage.

## Notes

[2026-11-23T17:38:10Z · bob-cli-pf.5] PROPOSED FOLLOW-UP: Repair the parent plan research reference — audited reading of research:202611/card_owned_frontmatter/card_owned_frontmatter.md returned missing on 2026-11-23. The approved parent plan and landed code provide sufficient scope for this phase; the land agent should repair or replace the stale reference.

[2026-11-24T01:30:38Z · bob-cli-pf.5.1.land] Closed automatically by the bob-cli-pf.5.1 land agent's close of the delegated child epic. Verified that child epic bob-cli-pf.5.1 delivered every behavior this phase requires, in bob-plugins 25d8fe61..305b637c plus bob-cli 8d82c621: rename (r), source-order reorder (Alt+J/K through prop.move), marks/V-range multi-select with one-batch delete, source-exact YAML copy and New/Replace/Skipped overwrite-previewed paste, the key/value filter with reorder lockout, kind conversion plus a feature-detected metadataTypeManager vault-type change behind a separate confirmation, and the validated multiline YAML stage. Evidence: 407/407 focused property-editor tests; build:check and docs:check green; cargo props 54/54; the real-Obsidian report file:explicit:62ca3f23086f9033d49ae4ef passes 263/263 with 0 errors; the deployed ledger-tools bundle equals HEAD. No epic symbols. Note #1 (stale research reference) is left for the bob-cli-pf land agent to triage.

## Dependencies

- **Depends on:** [bob-cli-pf.4](bob-cli-pf.4.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pf.6](bob-cli-pf.6.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.5.md) | [bob-cli-pf.5](bob-cli-pf.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.5.1.5][1] | Need phase notes, remaining work, and approved parent decisions/design context | 1 |
| read-by | [agent:bob-cli-pf.5.1.land][2] | Need the parent link and phase scope to verify the child plan completed it | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.land/README.md

<!-- sase:referenced-by:end -->
