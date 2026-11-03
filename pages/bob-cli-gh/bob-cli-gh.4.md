# Bead: bob-cli-gh.4 — Vault adoption — bob periods migrate, problems report, nightly check

[Bead Pages](../README.md) / [bob-cli-gh](README.md) / bob-cli-gh.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.34.linker.w0` · **Assignee:** `bob-cli-gh.4` · **Size:** medium
**Created:** 2026-11-03 10:55:43 EST · **Closed:** 2026-11-03 12:59:21 EST
**Plan:** [202611/period\_notes\_and\_stats\_strips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_notes_and_stats_strips.md)

## Description

migrate: `bob periods migrate` (dry run by default, one verified commit with `-a`) that creates the ISO-2026 tree, adopts 2026.md, re-parents year notes and daily notes, and adds the week nav link; `bob periods list -p` problems; and a report-only nightly step.

## Notes

[2026-11-03T17:59:21Z · bob-cli-gh.4] Verified vault adoption: FileRewrite Option before-image creates; bob periods migrate dry-run default and -a one verified vault_rewrite commit (stats parity + zero dangling_daily_parent); list -p reports dangling_daily_parent, missing_period_note, unscaffolded, wrong_parent, task_rows, stale_instructions; report-only nightly period-notes step after articles; just all and just docs-check green; no leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-gh.2](bob-cli-gh.2.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gh.9](bob-cli-gh.9.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gh.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.4/README.md) | [bob-cli-gh.4](bob-cli-gh.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5a1ccf5`](https://github.com/bobs-org/bob-cli/commit/5a1ccf593bb743a9f08c003af550a4b473504540) | feat(periods): adopt the period-note tree (migrate, list -p, nightly) | [bob-cli-gh.4](bob-cli-gh.4.md) | 2026-11-03 13:00:24 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gh.4][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.4/README.md

<!-- sase:referenced-by:end -->
