# Bead: bob-cli-gm.1.1.1 — Shared target selection and source-preserving member views

[Bead Pages](../README.md) / [bob-cli-gm.1.1](bob-cli-gm.1.1.md) / bob-cli-gm.1.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-gm.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.md) · **Assignee:** `bob-cli-gm.1.1.1` · **Size:** medium
**Created:** 2026-11-03 16:48:52 EST · **Closed:** 2026-11-03 17:23:04 EST
**Plan:** [202611/capture\_target\_runs\_finish.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_target_runs_finish.md)

## Description

selection: build and test shared target-run selection, terminal extraction, refusal metadata, and byte-preserving member views while keeping public parsing behavior unchanged.

## Notes

[2026-11-03T22:23:04Z · bob-cli-gm.1.1.1] Selection implemented in capture_language/target_runs.rs with shared run selection, duplicate/split identity and messages, run-aware terminal extraction, and byte-preserving member views; internal enable_target_runs defaults false at all production entry points with opt-in tests only. Strict duplicate_capture_target and split_capture_targets wired through parse_capture_item; editor adapter shares same evidence. Added 19 focused tests covering leading/trailing/child/whole-line, 2-3 members, mixed drawer/toggle suffixes, partial/malformed members, Unicode offsets, schedule/priority interleaving, duplicate/split, and literal @a+x @b:y / @a+x @bob cases plus default-path unchanged and list-bullet retention. Verified: cargo test capture_language 556 passed, cargo fmt --check clean, cargo clippy workspace gate clean (warnings only).

## Dependencies

- **Blocks:** [bob-cli-gm.1.1.2](bob-cli-gm.1.1.2.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gm.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.1.1.1/README.md) | [bob-cli-gm.1.1.1](bob-cli-gm.1.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d1f3484`](https://github.com/bobs-org/bob-cli/commit/d1f3484200081294a96bcd029654b7545d7b7305) | feat(capture): add shared target-run selection staging | [bob-cli-gm.1.1.1](bob-cli-gm.1.1.1.md) | 2026-11-03 17:24:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gm.1.1.1][1] | Need phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gm.1.1.1/README.md

<!-- sase:referenced-by:end -->
