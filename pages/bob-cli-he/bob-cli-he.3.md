# Bead: bob-cli-he.3 — Report history provider and entry ages

[Bead Pages](../README.md) / [bob-cli-he](README.md) / bob-cli-he.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5r.linker.w0.md) · **Assignee:** `bob-cli-he.3` · **Size:** small
**Created:** 2026-11-05 10:29:53 EST · **Closed:** 2026-11-05 13:28:46 EST
**Plan:** [202611/percent\_c\_history\_agreement.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/percent_c_history_agreement.md)

## Description

provenance: add clip.history {provider, entries[{age_seconds, app}]} to capture JSON and one provenance line to human output.

## Notes

[2026-11-05T18:28:37Z · bob-cli-he.3] PROPOSED FOLLOW-UP: Clear existing workspace fmt/clippy debt — just fmt reports unformatted src/native/config/mod.rs, src/native/plan_budget/mod.rs, and src/native/task_status_hooks/sync.rs; just lint fails on a clippy if-collapse in the unchanged task_status_hooks/sync.rs:1625.

[2026-11-05T18:28:46Z · bob-cli-he.3] Implemented clip.history provider and aligned per-entry age_seconds/app JSON metadata, including null unknowns and clamped ages; added human provenance line and docs. Verified capture history CLI tests, age unit test, CLI regression, rustfmt on changed Rust, docs-check, and no epic-symbol leftovers. just fmt and just lint still fail only on unchanged workspace files; recorded follow-up.

## Dependencies

- **Depends on:** [bob-cli-he.2](bob-cli-he.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-he.4](bob-cli-he.4.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-he.6](bob-cli-he.6.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-he.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-he.3/README.md) | [bob-cli-he.3](bob-cli-he.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`89192e8`](https://github.com/bobs-org/bob-cli/commit/89192e8bada62cd46fc990b1ca9e78a469c68d37) | feat(capture): report clipboard history provider and entry ages | [bob-cli-he.3](bob-cli-he.3.md) | 2026-11-05 13:29:34 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-he.3][1] | Need the phase scope, prior notes, and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-he.3/README.md

<!-- sase:referenced-by:end -->
