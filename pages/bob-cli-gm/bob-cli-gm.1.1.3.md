# Bead: bob-cli-gm.1.1.3 — Editor member semantics and targets JSON

[Bead Pages](../README.md) / [bob-cli-gm.1.1](bob-cli-gm.1.1.md) / bob-cli-gm.1.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-gm.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.md) · **Assignee:** `bob-cli-gm.1.1.3` · **Size:** medium
**Created:** 2026-11-03 16:48:52 EST · **Closed:** 2026-11-03 18:48:35 EST
**Plan:** [202611/capture\_target\_runs\_finish.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_target_runs_finish.md)

## Description

editor: reuse shared selection and existing editor semantics to produce one item with all target spans, ordered needs, exact diagnostics, and additive targets metadata behind the internal staging option.

## Notes

[2026-11-03T23:48:35Z · bob-cli-gm.1.1.3] Editor target-run fan-in behind enable_target_runs: one EditorItemParse with additive targets, first-member legacy fields, unioned needs, deduplicated spans/diagnostics, exact duplicate/split diagnostics; verified 37 target_runs tests (8 new editor), 33 capture_parse tests (1 new serialization), full capture_language lib 574 green, fmt and clippy clean, default singleton path unchanged, no epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-gm.1.1.2](bob-cli-gm.1.1.2.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gm.1.1.4](bob-cli-gm.1.1.4.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gm.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.1.1.3/README.md) | [bob-cli-gm.1.1.3](bob-cli-gm.1.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6a5b69b`](https://github.com/bobs-org/bob-cli/commit/6a5b69b081ee8d11ebc191d233aebe6f4ebe15fd) | feat(capture): combine editor target runs into one item with targets | [bob-cli-gm.1.1.3](bob-cli-gm.1.1.3.md) | 2026-11-03 18:49:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gm.1.1.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.1.1.3/README.md

<!-- sase:referenced-by:end -->
