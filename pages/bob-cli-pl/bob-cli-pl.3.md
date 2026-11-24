# Bead: bob-cli-pl.3 — The settings contract in bob props show, dry-run effects, and list issues (bob-cli)

[Bead Pages](../README.md) / [bob-cli-pl](README.md) / bob-cli-pl.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5y.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5y.linker.w1.md) · **Assignee:** `bob-cli-pl.3` · **Size:** medium
**Created:** 2026-11-22 20:56:40 EST · **Closed:** 2026-11-24 12:13:57 EST
**Plan:** [202611/area\_project\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_cards.md)

## Description

contract-reads: expose each setting's stage, choices, declared and effective value with its source, the ^prj line facts, dry-run consequence effects, per-row contract_issues in areas/projects list, the props_contract_v1 capability, and docs.

## Notes

[2026-11-24T17:13:09Z · bob-cli-pl.3] PROPOSED FOLLOW-UP: just docs-check fails identically on clean master — zensical --strict: develop/plugins/architecture.md links to missing docs/area-and-project-cards.md (home-cards page, not this phase)

[2026-11-24T17:13:57Z · bob-cli-pl.3] Verified: bob props show JSON+text Settings contract (inherited hue, shadowed clock, ready_cap off, root/blocked/terminal prj, bank.md); dry-run effects name catalog syncs; areas/projects list add contract_issues; catalog features include props_contract_v1; 13 contract unit tests + 16 CLI contract tests + 67 props lib tests + areas/projects list JSON; cargo fmt; just docs-gen. just docs-check lint+drift pass; zensical missing area-and-project-cards.md reproduces on clean master (PROPOSED FOLLOW-UP).

## Dependencies

- **Depends on:** [bob-cli-pl.2](bob-cli-pl.2.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pl.5](bob-cli-pl.5.md) ◐ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pl.6](bob-cli-pl.6.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.3/README.md) | [bob-cli-pl.3](bob-cli-pl.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4b23bbe`](https://github.com/bobs-org/bob-cli/commit/4b23bbef29a3dd932158930c40bc1d0c8d5be2f2) | feat(props): expose the area and project settings contract | [bob-cli-pl.3](bob-cli-pl.3.md) | 2026-11-24 12:18:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.3][1] | Need notes, remaining work, and whether earlier agents already landed contract-reads | 4 |
| read-by | [agent:fx][2] | Research whether the pl epic's dependency on pf is necessary | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.fx/README.md

<!-- sase:referenced-by:end -->
