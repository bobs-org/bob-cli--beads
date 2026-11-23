# Bead: bob-cli-pf.2.1.2 — Strict property operations and byte-exact undo

[Bead Pages](../README.md) / [bob-cli-pf.2.1](bob-cli-pf.2.1.md) / bob-cli-pf.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.md) · **Assignee:** `bob-cli-pf.2.1.2` · **Size:** medium
**Created:** 2026-11-22 14:47:18 EST · **Closed:** 2026-11-22 19:12:43 EST
**Plan:** [202611/props\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/props_cli.md)

## Description

span-operations: implement the strict six-operation protocol and pure span planner, serialization, role enforcement, candidate verification, and exact inverse operations against the inventory model.

## Notes

[2026-11-22T23:15:59Z · bob-cli-pf.2.1.2] Verified: cargo fmt --all; cargo clippy --workspace --all-targets --all-features with just-check deny gates; cargo test --lib native::props (49 passed, including golden inverse/redo). epic-symbols: none. Host just check is the remaining gate.

[2026-11-22T23:41:00Z · bob-cli-pf.2.1.2--1] PROPOSED FOLLOW-UP: just check flake in tests/gcal_ack.rs — session_timed_presses_answer_each_card and session_write_failure_keeps_earlier_answers failed under full-suite loadavg ~198 (missing .bob/gcal journal after 1200ms; debounce swallowed the second "a" so only 1 of 2 acked). Isolation rerun on this tree passed both. Unrelated to span-operations (props planner). No existing task bead.

[2026-11-23T00:12:43Z · bob-cli-pf.2.1.2--2] Closed by explicit `sase stitch create -B close` after create_commit landed fdd94725 ("feat(props): add strict span operations and byte-exact undo"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-pf.2.1.2` if more work remains.

## Dependencies

- **Depends on:** [bob-cli-pf.2.1.1](bob-cli-pf.2.1.1.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pf.2.1.3](bob-cli-pf.2.1.3.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.1.2.md) | [bob-cli-pf.2.1.2](bob-cli-pf.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fdd9472`](https://github.com/bobs-org/bob-cli/commit/fdd94725e315babce6ff79668d2b01ec97016b72) | feat(props): add strict span operations and byte-exact undo | [bob-cli-pf.2.1.2](bob-cli-pf.2.1.2.md) | 2026-11-22 19:11:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.2.1.2--2][1] | Need phase scope, notes, and proposed follow-up before closing after green just check | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.1.2.md

<!-- sase:referenced-by:end -->
