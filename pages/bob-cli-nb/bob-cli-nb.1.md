# Bead: bob-cli-nb.1 — Engine, CLI, and the three views

[Bead Pages](../README.md) / [bob-cli-nb](README.md) / bob-cli-nb.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1e2.md) · **Assignee:** `bob-cli-nb.1` · **Size:** medium
**Created:** 2026-11-18 13:06:51 EST · **Closed:** 2026-11-18 15:55:31 EST
**Plan:** [202611/bob\_tick.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_tick.md)

## Description

engine: add src/native/tick/ with the strict tick: config block, the fixed six-step catalog, the pure planner, atomic host-local state, the run lock, subprocess supervision (SIGTERM, grace, SIGKILL; signal forwarding), generic exit-code outcomes, the run, -d, -s, -q, and -f json views, the last.json receipt with a Darwin notification, writer pinning, CLI registration in the Vault section, generated CLI docs, and fake-step integration tests.

## Notes

[2026-11-18T18:24:04Z · bob-cli-nb.1] Implementation includes a one-line correction to the pre-existing records integration test compile error (tests/cli/records.rs:1629 compared &String with owned String). The initial cargo check --tests diagnosed it on an otherwise unchanged test file; correction removes the unnecessary borrow so CLI verification can run.

[2026-11-18T18:31:27Z · bob-cli-nb.1] Engine implementation is complete: strict tick config, six-step pure scheduling, persisted follow-up intent, atomic private state/receipts, run lock, process-group timeouts and signal forwarding, CLI/help/completion/catalog, human/plan/status/quiet/JSON views, shared Darwin notifier, and fake-step tests. Verified 16 targeted CLI tests (14 tick plus root help and catalog), cargo fmt --check, just docs-gen, and bob-docs lint. Added config/planner and subprocess grace/interrupt unit tests for the full gate. No epic-symbol entries. Full repository check is running; full docs-check and required scripts/dev/macos-ci-check remain verification work before closing only this phase. Linked docs sources were opened through sase repo and remain clean; no memory notes edited.

[2026-11-18T18:35:06Z · bob-cli-nb.1] Full check e9176399d5503c5e17496431cd65004c stopped at five pre-existing Clippy errors in untouched src/native/albums/report.rs and albums/walk.rs. Applied mechanical then_some, collapsed-condition, and String::from corrections (no behavior change) to unblock the required gates. The full check must be rerun with these fixes; targeted tick tests/docs generation/lint already passed.

[2026-11-18T18:49:21Z · bob-cli-nb.1--1] Verification follow-up: monitor n37gn6qn9kpr / ToolRun 3f29c7dfe18828a4f73296c4a2d040bc passed formatting and Clippy, then reported six failing assertions (7373 lib tests and 3806 CLI tests passed). Fixed the tick-induced clipboard help assertion to match command rows, not the earlier gcal mention in tick prose. Updated five existing album/record assertions to the documented walk-writer contract already in base c02d405d: staged neighbour edits, immediately current walk with no sync backfill, walk-only bare records, and final batch bytes in created note previews. No production album/record behavior changed. cargo fmt --all -- --check and git diff --check pass. Full check, docs-check, and exact-tree macOS gate will rerun under a monitor; close only this phase after those results pass.

[2026-11-18T19:56:44Z · bob-cli-nb.1--2] Verification monitor 7xq7kmat7wrf / ToolRun 2643e06d5f123addcc2dc6f510f917de passed just check (including 7375 lib tests and 3810 CLI tests, zero failures) and all full docs-check gates (447 documentation tests passed, one dependency-gated skip). Exact-tree snapshot b1f835741234f64a7314a2f495215908b6453b4b ran at https://github.com/bobs-org/bob-cli/actions/runs/44376083850: Linux tests, lint, package and macOS lint passed. macOS job 135055507284 started 19:06:57Z, spent 9m22s in Clippy, began cargo test at 19:17:19Z, and was cancelled at the 45-minute job limit while rustc was still compiling; no test executables had started and no compile error was reported. Increased only the macOS test-job budget to 90 minutes; actionlint and git diff --check pass. Rerunning the exact-tree gate with a 7200-second outer deadline; phase remains open until verification is reviewed. No memory changes.

[2026-11-18T20:55:31Z · bob-cli-nb.1--3] Engine/CLI phase verified and complete. Monitor 7xq7kmat7wrf / ToolRun 2643e06d5f123addcc2dc6f510f917de passed just check (7375 library and 3810 CLI tests, zero failures) and full docs-check (447 documentation tests passed, one dependency-gated skip). Final monitor 0tzh87kznqkv / ToolRun d85ce7278453cbbebca7883d6f303582 exited 0: https://github.com/bobs-org/bob-cli/actions/runs/44385949581 passed the entire workflow and required macOS lint, tests, and archive-move presenter cases on snapshot bb24e631b9924a530169ec539916544b0b323fa2; temporary branch deletion verified. Current worktree tree 9a6e5d112b87dcb1ff8da287aef73d4ff5fe511c exactly matches that snapshot. macOS timeout increased to 90 minutes to allow cold compilation; Linux retains 45. git diff --check passes. Reran epic-symbols: no entries. No unresolved failures or memory changes. Closing only bob-cli-nb.1; parent and ancestors remain open.

## Dependencies

- **Blocks:** [bob-cli-nb.2](bob-cli-nb.2.md) ✓ · ⧖ 2026-11-18
- **Blocks:** [bob-cli-nb.3](bob-cli-nb.3.md) ✓ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nb.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nb.1.md) | [bob-cli-nb.1](bob-cli-nb.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bb864f8`](https://github.com/bobs-org/bob-cli/commit/bb864f88f72f82c954b745b4ea14e0e5d724c0df) | feat(tick): add the ordered background work engine and CLI views | [bob-cli-nb.1](bob-cli-nb.1.md) | 2026-11-18 16:10:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nb.1--3][1] | Review phase scope, prior evidence, and remaining closure obligations | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nb.1.md

<!-- sase:referenced-by:end -->
