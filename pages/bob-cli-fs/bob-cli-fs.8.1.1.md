# Bead: bob-cli-fs.8.1.1 — Relation policy, pure rule, and shared copy

[Bead Pages](../README.md) / [bob-cli-fs.8.1](bob-cli-fs.8.1.md) / bob-cli-fs.8.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-fs.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.8.md) · **Assignee:** `bob-cli-fs.8.1.1` · **Size:** medium
**Created:** 2026-11-02 07:08:24 EST · **Closed:** 2026-11-02 07:27:04 EST
**Plan:** [202611/cycler\_relation\_successors.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/cycler_relation_successors.md)

## Description

relation_core: implement the cycler's cached successor-label policy, pure R1-R7 planner for Done and parked events, copy helpers, and fixture expansion without enabling runtime offers.

## Notes

[2026-11-02T12:27:04Z · bob-cli-fs.8.1.1] relation_core landed in bob-plugins task-status-cycler only: cached three-list successor-label policy (Obsidian parseYaml + harness stub), pure planSuccessorRelations R1-R7 for Done and parked, copy helpers with 48-scalar truncation, byte-identical vectors.json (21137), and registered test-task-status-cycler-relation-successors.cjs. Verified: 12 config + cache/no-throw, 4 key, 31 copy, all 25 rule vectors including cases, disabled planSuccessors unchanged (no relation_successors), fake relationIndex public edge shape without verdicts, fragments 753/315/293 under cap, build --check and docs inventory current, related successor/offers/keep-moving/relations/wiring/polish/project-pull-in/theme-write tests green. Runtime offers stay unwired. SA14/SA18 merge deferred to offer_pipeline with adapter notes. Synced cycler with bob plugins sync --repo <checkout> --no-pull -p task-status-cycler -F (stale uncommitted deploy from bob-cli_12).

## Dependencies

- **Blocks:** [bob-cli-fs.8.1.2](bob-cli-fs.8.1.2.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.8.1.1/README.md) | [bob-cli-fs.8.1.1](bob-cli-fs.8.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@4447723`](https://github.com/bobs-org/bob-plugins/commit/4447723dd13eeb09eab9f14f316c306780cafe4d) | feat(task-status-cycler): add relation successor policy, planner, and copy | [bob-cli-fs.8.1.1](bob-cli-fs.8.1.1.md) | 2026-11-02 07:34:01 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fs.8.1.1][1] | Need full phase description, notes, DECISIONS, and design file path | 5 |
| read-by | [agent:bob-cli-fs.8.1.2][2] | need prior phase evidence to avoid redo | 1 |
| read-by | [agent:bob-cli-fs.8.1.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.8.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.8.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.8.1.land.md

<!-- sase:referenced-by:end -->
