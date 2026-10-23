# Bead: bob-cli-at.1 — macOS file-coordination primitive

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.1` · **Size:** medium
**Created:** 2026-10-23 11:44:15 EDT · **Closed:** 2026-10-23 12:43:43 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

coordinate: add `native::file_coordination`, a bounded `.forMerging` coordinated write. On macOS it is `NSFileCoordinator` through objc2, objc2-foundation, and block2 (macOS-only dependencies), with a watchdog that calls `cancel()` when the budget expires and returns Granted/Held/Failed truthfully. Elsewhere it runs the closure directly. Add a macOS-only test that compiles a small Swift NSDocument presenter fixture with `swiftc` and proves three cases: no presenter writes; a dirty presenter saves first and reloads clean; a blocked presenter is held within the budget with no write. Nothing calls the primitive yet.

## Notes

[2026-10-23T16:29:30Z · bob-cli-at.1] Implementation complete: native::file_coordination provides coordinate_merging_write(path, budget, FnOnce() -> T), Coordination::{Granted,Held,Failed}, TimedOut.waited, and IS_COORDINATED for direct/coordinated reporting. macOS-only objc2 dependencies and a cancel-only Send wrapper implement ForMerging; shared atomic gate prevents late writes and preserves running accessors. No production caller yet; bob-cli-at.3 should remove the temporary module dead_code allowance when integrating. Verified 8 Linux targeted tests and all 9 tests in a minimal Mac harness, including actual swiftc NSDocument dirty-save/reload and blocked-6s/budget-2s case. Full Linux just check and full Mac clippy/targeted tests remain for final verification.

[2026-10-23T16:43:43Z · bob-cli-at.1--1] Completed and reviewed the standalone native::file_coordination primitive against the approved coordinate phase. macOS uses ForMerging with a cancel-only watchdog, an atomic start/timeout gate, truthful Granted/Held/Failed results, and panic containment; other platforms invoke the accessor directly. Monitor ba25g8e15sp7 completed with exit 0: Linux just check passed (5303 tests passed, 0 failed, 1 ignored), and full-project macOS Clippy plus all 9 coordination tests passed. The actual Swift NSDocument fixture ran without skipping and verified no-presenter writes, dirty-presenter save-before-write and clean reload, and a 6-second blocked presenter held within about 3 seconds for a 2-second budget with no write and a successful later save. The verification script removed the Mac scratch copy successfully. Diff reviewed; git diff --check passed; no epic-symbol entries remain. No production caller is included; bob-cli-at.3 should remove the documented temporary module dead_code allowance when integrating. Parent epic remains open.

## Dependencies

- **Blocks:** [bob-cli-at.3](bob-cli-at.3.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-at.1.md) | [bob-cli-at.1](bob-cli-at.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0aec807`](https://github.com/bobs-org/bob-cli/commit/0aec807c422c4a1d3d1be6ba5daa078473242071) | feat(native): add bounded macOS file coordination | [bob-cli-at.1](bob-cli-at.1.md) | 2026-10-23 12:44:36 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-at.1--1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-at.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-at.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.land/README.md

<!-- sase:referenced-by:end -->
