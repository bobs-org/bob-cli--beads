# Bead: bob-cli-ab.4 — Mac related lane, settle policy, and setting

[Bead Pages](../README.md) / [bob-cli-ab](README.md) / bob-cli-ab.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.27.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.27.linker.w0.md) · **Assignee:** `bob-cli-ab.4` · **Size:** medium
**Created:** 2026-10-20 17:44:13 EDT · **Closed:** 2026-10-20 20:44:26 EDT
**Plan:** [202610/capture\_similar\_tasks\_band.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_similar_tasks_band.md)

## Description

mac_lane: decode the contract, add the cancellable related lane with old-bob fallback, a pure band-state reducer, the 350 ms settle wiring in CapturePanelModel, the Settings toggle, signposts, fake-bob support, and protocol docs.

## Notes

[2026-10-21T00:30:48Z · bob-cli-ab.4] Representative capture-related draft golden for the Mac phases; copied into the fake-bob fixture set: [recapture.json]

[2026-10-21T00:44:26Z · bob-cli-ab.4--1] Implemented the cancellable similar-task lane, tolerant contract models and reducer, setting, signposts, fake-bob support, tests, and protocol docs. Verified just portable-check on athena (1,501 tests, 0 failures), just docs-check (447 passed, 1 skipped; all gates passed), and git diff --check. The Mac scratch bundle/typecheck targets remain unverified because SSH to mac timed out. Confirmed no epic-symbol entries remained and cleaned the athena verification checkout.

## Attachments

- 🌐 recapture.json · application/json · 5.44238 KiB

## Dependencies

- **Depends on:** [bob-cli-ab.2](bob-cli-ab.2.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ab.5](bob-cli-ab.5.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ab.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ab.4.md) | [bob-cli-ab.4](bob-cli-ab.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7a03751`](https://github.com/bobs-org/bob-mac-capture/commit/7a03751a447a95cde4a02657216f8b942196ad89) | feat(capture): add settled similar-task lane | [bob-cli-ab.4](bob-cli-ab.4.md) | 2026-10-20 20:45:09 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ab.4--1][1] | Need the phase scope, design file, and prior notes to finish this reserved phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ab.4.md

<!-- sase:referenced-by:end -->
