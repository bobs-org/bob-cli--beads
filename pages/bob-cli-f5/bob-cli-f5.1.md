# Bead: bob-cli-f5.1 — Contract, pure core, ring glyphs, and visual preview

[Bead Pages](../README.md) / [bob-cli-f5](README.md) / bob-cli-f5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16q.md) · **Assignee:** `bob-cli-f5.1` · **Size:** medium
**Created:** 2026-11-01 09:24:20 EST · **Closed:** 2026-11-01 09:48:10 EST
**Plan:** [202611/task\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_link_marks.md)

## Description

core: write the bob-cli display contract with conformance vectors, add the pure bob-ledger-tools core (link scanner, line context, target-line parser, state and tooltip models), define the ring glyph family in CSS, and tune it with a light/dark preview harness.

## Notes

[2026-11-01T14:48:00Z · bob-cli-f5.1] PROPOSED FOLLOW-UP: 5 npm-test failures reproduce on clean base (freshness reload event, gcal create listener, keep-inbox forced check, note-ready startup storm, relation-index startup replay); track as flakes/infra, not phase core

[2026-11-01T14:48:10Z · bob-cli-f5.1] Core done: docs/task-link-marks.md + registry/nav/README/vault-format/plan + docs-check pass; bob-plugins 148 pure core (TS/TC/TR/TT), styles.css ring family, preview light/dark pass, node conformance 5/5 pass, build pass; npm full suite has 5 pre-existing base failures (noted); sync refused due to concurrent uncommitted vault builds, no force

## Dependencies

- **Blocks:** [bob-cli-f5.2](bob-cli-f5.2.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-f5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.1/README.md) | [bob-cli-f5.1](bob-cli-f5.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a1233eb`](https://github.com/bobs-org/bob-cli/commit/a1233eb8f4fa3bded9df99d3f289328b15e1681f) | feat(task-link-marks): display contract, registry, and docs links | [bob-cli-f5.1](bob-cli-f5.1.md) | 2026-11-01 09:49:06 EST |
| bob-plugins | [`bob-plugins@a67b8cd`](https://github.com/bobs-org/bob-plugins/commit/a67b8cddff9b4638e4b4c2342642063ef176c77b) | feat(task-link-marks): pure core, ring CSS, preview, and conformance tests | [bob-cli-f5.1](bob-cli-f5.1.md) | 2026-11-01 09:49:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f5.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.1/README.md

<!-- sase:referenced-by:end -->
