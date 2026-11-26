# Bead: bob-cli-qj.1 — Rename the Rust article engine to prose

[Bead Pages](../README.md) / [bob-cli-qj](README.md) / bob-cli-qj.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6i.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6i.linker.w0.md) · **Assignee:** `bob-cli-qj.1` · **Size:** small
**Created:** 2026-11-26 10:56:26 EST · **Closed:** 2026-11-26 12:13:57 EST
**Plan:** [202611/prose\_note\_type.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_note_type.md)

## Description

engine-rename: move the article engine module and its Rust identifiers to prose names, with byte-identical CLI, JSON, help, and docs output.

## Notes

[2026-11-26T17:13:46Z · bob-cli-qj.1] PROPOSED FOLLOW-UP: 34 lib + 39 cli drawer/capture test failures reproduce identically on clean base (verified via worktree at 478d5233); unrelated to engine rename, likely tracked by drawer-migration work -r recording pre-existing failures seen during verify

[2026-11-26T17:13:57Z · bob-cli-qj.1] Engine renamed: src/native/articles -> src/native/prose, all Rust identifiers to prose names, serialized wire field summary.articles kept. Verified: cargo fmt/clippy clean, 39 prose lib + 28 cli prose tests pass, docs-reference golden + just docs-gen byte-identical, rg shows only literals/comments/tests/legacy wire name. Commit bd0a0221. 34 lib + 39 cli failures are pre-existing on clean base (identical sets).

## Dependencies

- **Blocks:** [bob-cli-qj.2](bob-cli-qj.2.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.1/README.md) | [bob-cli-qj.1](bob-cli-qj.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cf414ce`](https://github.com/bobs-org/bob-cli/commit/cf414ce15c5489203abf81d308d9359d30214510) | refactor(prose): rename the article engine module to prose | [bob-cli-qj.1](bob-cli-qj.1.md) | 2026-11-26 12:15:08 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.6k.cld][1] | Check phase progress to plan parallel prose/notebook card work | 1 |
| read-by | [agent:research.6k.gem][2] | Inspect in-progress phase details and progress notes of qi and qj epics | 1 |
| read-by | [agent:research.6k.grk][3] | Need whether qj.1 adds a prose NoteKind in props, which would affect prose-card classification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.cld/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.gem/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.grk/README.md

<!-- sase:referenced-by:end -->
