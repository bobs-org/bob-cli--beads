# Bead: bob-cli-lt.2 — Shared YAML span primitives and the bank entry editor

[Bead Pages](../README.md) / [bob-cli-lt](README.md) / bob-cli-lt.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1co](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1co.md) · **Assignee:** `bob-cli-lt.2` · **Size:** medium
**Created:** 2026-11-15 13:16:08 EST · **Closed:** 2026-11-15 14:29:03 EST
**Plan:** [202611/bank\_setup\_render\_and\_edit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_setup_render_and_edit.md)

## Description

config-spans: extract album-agnostic span primitives and build a style-preserving, entry-granular bank: editor library.

## Notes

[2026-11-15T19:05:48Z · bob-cli-lt.2] PROPOSED FOLLOW-UP: cargo fmt --check fails on tests/gcal_auth.rs:1893 (foreign-1 journal line wrapping) on clean HEAD 9c2c2404, identical without this phase.

[2026-11-15T19:29:03Z · bob-cli-lt.2--1] Verified shared yaml_spans primitives, album editor re-point, and bank config_spans editor. cargo fmt --check passed; 6 yaml_spans, 19 config_spans, and 10 album span tests passed. Full just check on this tree already exited 0. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-lt.4](bob-cli-lt.4.md) ◐ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lt.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-lt.2.md) | [bob-cli-lt.2](bob-cli-lt.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bd9c4c1`](https://github.com/bobs-org/bob-cli/commit/bd9c4c13e7a6a1f64f57baff735f05834f9f8bb1) | feat(bank): extract YAML span primitives and add a bank config editor | [bob-cli-lt.2](bob-cli-lt.2.md) | 2026-11-15 14:30:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lt.2--1][1] | Need phase status after just check passed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-lt.2.md

<!-- sase:referenced-by:end -->
