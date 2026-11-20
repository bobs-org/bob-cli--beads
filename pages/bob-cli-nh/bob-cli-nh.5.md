# Bead: bob-cli-nh.5 — Migration step and scaffolds without the old sections

[Bead Pages](../README.md) / [bob-cli-nh](README.md) / bob-cli-nh.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ef](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ef.md) · **Assignee:** `bob-cli-nh.5` · **Size:** medium
**Created:** 2026-11-19 09:35:22 EST · **Closed:** 2026-11-19 18:09:32 EST
**Plan:** [202611/period\_intentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_intentions.md)

## Description

migrate: add the intentions step to `bob periods migrate`. One dry-run-first, idempotent vault_rewrite moves the daily Headline and Reflection, week Intentions, quarter Outcomes, year Theme + Outcomes, `## Reflection`, and the Review opener into frontmatter. It reports placeholders and conflicts. Scaffolds stop emitting the old sections. Fixture-vault goldens mirror the live shapes.

## Notes

[2026-11-19T23:09:11Z · bob-cli-nh.5] PROPOSED FOLLOW-UP: Pre-existing lib failures (capture_complete drawers/output x3, catalog public_leaves, completion kinds, periods update planning) reproduce on clean base; not caused by migrate step

[2026-11-19T23:09:16Z · bob-cli-nh.5] PROPOSED FOLLOW-UP: Pre-existing CLI capture complete_drawers failure reproduces on clean base; same root as lib capture_complete

[2026-11-19T23:09:21Z · bob-cli-nh.5] PROPOSED FOLLOW-UP: Pre-existing docs-check lint budget overruns in docs/reference/mac-capture/capture-previews.md and keyboard.md reproduce on clean base

[2026-11-19T23:09:32Z · bob-cli-nh.5] Migrate intentions step done: dry-run-first idempotent vault_rewrite moves Headline/Reflection/Intentions/Outcomes/Theme/Review-opener to frontmatter with placeholder/conflict/nested reports; scaffolds drop old sections (goldens refreshed); structure_ok accepts old+new; docs/periods.md Migration+anatomy updated and docs-gen run; verified via migrate_intentions unit tests (10), new CLI fixture test (dry-run/apply/rerun, per-state digests, placeholders/conflicts, nested, out-of-range, monthly untouched), plus just fmt+clippy clean; remaining failures (6 lib, 1 CLI capture, docs-check budget) reproduce on base and recorded as follow-ups

## Dependencies

- **Depends on:** [bob-cli-nh.1](bob-cli-nh.1.md) ✓ · ⧖ 2026-11-19
- **Depends on:** [bob-cli-nh.3](bob-cli-nh.3.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nh.8](bob-cli-nh.8.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nh.9](bob-cli-nh.9.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.5/README.md) | [bob-cli-nh.5](bob-cli-nh.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`eaa52d0`](https://github.com/bobs-org/bob-cli/commit/eaa52d06c8f99c1f08b6068e10d3a10b0b47cca0) | feat(periods): add intentions step to migrate and new scaffolds | [bob-cli-nh.5](bob-cli-nh.5.md) | 2026-11-19 18:10:58 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.5][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-nh.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.land.md

<!-- sase:referenced-by:end -->
