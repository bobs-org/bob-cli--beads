# Bead: bob-cli-gj.2.1.4 — Note-pull conformance fixtures and performance evidence

[Bead Pages](../README.md) / [bob-cli-gj.2.1](bob-cli-gj.2.1.md) / bob-cli-gj.2.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-gj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gj.2.md) · **Assignee:** `bob-cli-gj.2.1.4` · **Size:** medium
**Created:** 2026-11-03 12:31:13 EST · **Closed:** 2026-11-03 17:24:05 EST
**Plan:** [202611/note\_pull\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_pull_cli.md)

## Description

verification: complete section 7, audit NP1–NP28, add CLI fixture assertions, generate real-bob JSON fixtures for the Mac phase, verify dry-run parity and write-free refusals, measure release latency on an isolated vault copy, and run just check plus just docs-check. Prepare closure evidence for bob-cli-gj.2; this phase closes only its own bead.

## Notes

[2026-11-03T20:17:39Z · 17p] COORDINATION NOTE: master at a95d5d8f did not compile because note_pull: None appeared twice in plan_capture_item's sub-bullet CaptureItemResult literal (src/native/capture/plan.rs). The fix commit keeps the leading copy, right after "result: CaptureItemResult {", and drops the trailing copy after relation_groups. If your branch already deleted the leading copy to get a build, restore it and delete the trailing one instead. Otherwise the rebase removes both copies and master breaks a third time. Run cargo check --all-targets --locked on your rebased tip before you land.

[2026-11-03T20:58:39Z · 17p.f0] COORDINATION NOTE #2: master from 3d1822be on does not compile (E0063, missing note_pull in plan_capture_item's sub-bullet CaptureItemResult literal in src/native/capture/plan.rs), so your base fails too. The fix commit restores note_pull: None as the literal's first field, on its own line directly after "result: CaptureItemResult {" with the same indentation as "ok: true,". Do not add note_pull anywhere else in that literal. If you already re-added it locally, it must be that exact line in that exact place: git merges an identical addition into one copy, but any other placement rebases cleanly into a duplicate (E0062, a fourth break). Safest: drop your local edit to that literal and build on the current master. Run cargo check --all-targets --locked on your rebased tip before you land.

[2026-11-03T22:23:50Z · bob-cli-gj.2.1.4--4] PROPOSED FOLLOW-UP: Reduce required dependency-snapshot latency on large note pulls — final release p95 on the 6,853-note isolated vault is 82.60 ms for @sase against the 70 ms target; profiling after catalog fast paths found one eligible dependency-bearing resident still requires the vault-wide proof scan. The @mac_inbox source note has no open task and measures the empty-pull refusal at 44.88 ms.

[2026-11-03T22:24:05Z · bob-cli-gj.2.1.4--4] Verified NP1–NP28 CLI fixture suite and performance evidence; focused capture_language (521), note_pull (34), CLI note_pull (6), cargo check --all-targets --locked, and canonical sase tool run check passed. docs-check reaches only two published attachment URL obligations and fails identically on clean base 3d1822be. Release p95: sase 82.60 ms vs 70 ms target; mac_inbox empty-pull refusal 44.88 ms. Recorded fixture handoff on bob-cli-gj.3 and proposed latency follow-up here; no epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-gj.2.1.3](bob-cli-gj.2.1.3.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gj.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gj.2.1.4.md) | [bob-cli-gj.2.1.4](bob-cli-gj.2.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`093dcea`](https://github.com/bobs-org/bob-cli/commit/093dceade9085d57cbd4cdda96478258bed779b9) | feat(capture): add note-pull conformance evidence | [bob-cli-gj.2.1.4](bob-cli-gj.2.1.4.md) | 2026-11-03 17:25:17 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gh.8][1] | Determine whether the existing note-pull phase tracks the clean-base compiler failure | 1 |
| read-by | [agent:bob-cli-gj.2.1.4--4][2] | Need the phase scope, design file, and prior recorded work before completing verification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.8/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gj.2.1.4.md

<!-- sase:referenced-by:end -->
