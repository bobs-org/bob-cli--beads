# Bead: bob-cli-7c.3 — bob capture --pull-in, offer JSON, and the Mac guard

[Bead Pages](../README.md) / [bob-cli-7c](README.md) / bob-cli-7c.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.11.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.11.linker.w0.md) · **Assignee:** `bob-cli-7c.3` · **Size:** large
**Created:** 2026-10-13 09:48:12 EDT · **Closed:** 2026-10-13 13:56:37 EDT
**Plan:** [202610/successor\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_offers.md)

## Description

rust_capture: add -p/--pull-in and the hidden --require-pull-in-choice to bob capture, thread the selection through every close path and the batch net pass, emit offer/pull_in JSON and numbered human rows, and cover the sase_foo case and the SO vectors with integration tests.

## Notes

[2026-10-13T17:56:37Z · bob-cli-7c.3--2] Verified capture --pull-in successor selection: just check passed (fmt, clippy, full cargo test) on monitor 9ksnd7t7trgd; cargo fmt --check still green; sase bead epic-symbols bob-cli-7c.3 reported no leftovers. SO1–SO6, SO13–SO19, SO26/27/29 plus dry-run parity covered in tests/cli/capture/successor_offers.rs.

## Dependencies

- **Depends on:** [bob-cli-7c.2](bob-cli-7c.2.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.7](bob-cli-7c.7.md) ◐ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.8](bob-cli-7c.8.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7c.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.3.md) | [bob-cli-7c.3](bob-cli-7c.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e7a0c7b`](https://github.com/bobs-org/bob-cli/commit/e7a0c7b588494bd46a67a5a9cdd73dd87906416c) | feat(capture): select successor offers with --pull-in | [bob-cli-7c.3](bob-cli-7c.3.md) | 2026-10-13 13:57:52 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7c.3--2][1] | Need assigned bead scope to decide close vs keep after verification recovery | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.3.md

<!-- sase:referenced-by:end -->
