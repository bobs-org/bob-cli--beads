# Bead: bob-cli-e8.4 — Capture stages mention mirrors in its batch

[Bead Pages](../README.md) / [bob-cli-e8](README.md) / bob-cli-e8.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2v.linker.w0.md) · **Assignee:** `bob-cli-e8.4` · **Size:** medium
**Created:** 2026-10-29 17:20:22 EDT · **Closed:** 2026-10-30 09:41:22 EDT
**Plan:** [202610/inline\_task\_mentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inline_task_mentions.md)

## Previously Closed

> ↺ Closed 2026-10-30T02:57:48Z · done
>
> (none)
>
> Reopened 2026-10-30T13:12:33Z by `sase bead open`

## Description

cli-capture: diff the mention pairs of every note a capture writes and stage the targets' LINKED FROM entries and source mints in the same all-or-nothing batch.

## Notes

[2026-10-30T02:30:13Z · bob-cli-e8.4] Capture mention-mirror post-pass landed: plan_mention_mirrors after inbox routes, before trackers finish. 8/8 capture::mentions tests pass (new-task mint+T mirror, sub-bullet parent, ~ wins, & suppresses, archived skip no mint S, mentions-off no-op, no-block-links JSON byte-identical, rollback). epic-symbols: none. just check still to run.

[2026-10-30T02:57:48Z · bob-cli-e8.4--1] Capture mention-mirror post-pass after inbox routes: 8/8 capture::mentions tests pass (new-task mint+T mirror, sub-bullet parent, ~ wins, & suppresses, archived skip no mint S, mentions-off no-op, no-block-links JSON byte-identical, rollback). Pinned archive_closed_window_respects_mtime stale mtime before BOB_NOW=2026-10-20 window so just check is unblocked. epic-symbols: none.

[2026-10-30T13:10:08Z · bob-cli-e8.4] CLOSED-BEAD LAUNCH: agent bob-cli-e8.4 launched against this closed bead; status left closed.
Launch submitted 2026-10-30T13:08:32.878439Z; run 20261030090835.
Prior close: 2026-10-30T02:57:48Z · done.

[2026-10-30T13:12:42Z · bob-cli-e8.4] Recovery verification: f47c639fb4f7e833608297c615605799bd896ed2 exists only at refs/sase/recovery/raw-commits/20261029230659 and is not an ancestor of current master f40a625a. Current HEAD lacks relations_mentions.rs and tests/cli/capture/mentions.rs; no deletion appears in history. Reopened to restore the existing phase diff, resolve integration issues, and verify before closing.

[2026-10-30T13:37:28Z · bob-cli-e8.4] Restored the unlanded f47c639f capture phase diff on current master. Manual temporary-vault repro found duplicate-title pair collapse and same-note mirror insertion shifting subsequent source mints; fixed both and per-item mint attribution. Added accurate mention deltas for relation upgrades and postimage uncertainty guards for removals. Tests now include 13 capture mention cases plus the removal-uncertainty unit vector; dry-run helpers assert Markdown is unchanged and no-block-link JSON compares exact bytes. just docs-check passed (447 tests, 1 expected skip; all gates passed). Initial restored-tree just check passed (ToolRun a8f9ace91614f6186a57b82dbd913df4). Final fixed-tree check is running as ToolRun 46435c40944b48f0e40e59b6c6563ea1; fmt/clippy passed, tests compiled, new uncertainty unit test passed. No epic-symbol entries remain. Remaining work: read final check result, repair any failures, then explicitly close this reopened bead and submit sase_final.

[2026-10-30T13:41:22Z · bob-cli-e8.4] Recovered f47c639f from the SASE raw-commit recovery ref because it had never landed on master. Capture now stages mention source mints and target LINKED FROM deltas atomically after inbox routes. Fixed duplicate-title identities, same-note mint ordering, per-item mint attribution, relation-upgrade mention deltas, and postimage uncertainty preservation. Final just check passed: ToolRun 46435c40944b48f0e40e59b6c6563ea1, 4063 library tests, 2514 CLI tests including all 13 capture mention cases, and all other suites; formatting/clippy passed. just docs-check passed every implemented gate (447 documentation tests, 1 expected skip). git diff --check passed. sase bead epic-symbols confirms no leftovers. No memory edits; parent epic remains open.

## Dependencies

- **Depends on:** [bob-cli-e8.3](bob-cli-e8.3.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e8.9](bob-cli-e8.9.md) ◐ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.4/README.md) | [bob-cli-e8.4](bob-cli-e8.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`22a8c84`](https://github.com/bobs-org/bob-cli/commit/22a8c84fb3d6853d537ba663d0c10b371f1a5769) | feat(capture): stage task mention mirrors atomically | [bob-cli-e8.4](bob-cli-e8.4.md) | 2026-10-30 09:42:42 EDT |
