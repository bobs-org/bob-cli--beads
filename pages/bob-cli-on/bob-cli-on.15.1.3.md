# Bead: bob-cli-on.15.1.3 — Preserve requirement choices through preview and submission

[Bead Pages](../README.md) / [bob-cli-on.15.1](bob-cli-on.15.1.md) / bob-cli-on.15.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.md) · **Assignee:** `bob-cli-on.15.1.3` · **Size:** medium
**Created:** 2026-11-22 14:56:48 EST · **Closed:** 2026-11-22 16:55:05 EST
**Plan:** [202611/mac\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_requirement_close_card.md)

## Description

pipeline: thread requirement capability and staged choices through CapturePanelModel snapshots, guarded dispatch, every refusal/retry and inbox-route path, all offer collectors, preview call sites, and notification receipts. Requirement groups alone must open the card. Follow the pipeline section and test stale recovery, executable identity changes, and post-commit jump behavior.

## Notes

[2026-11-22T21:55:05Z · bob-cli-on.15.1.3] Pipeline threads requirement capability and staged choices through CapturePanelModel snapshots, guarded dispatch, refusals/retries, inbox-route, collectors, preview, and notifications. Requirement-only closes open the card. Return commits default Met with --req-choice; Shift-Return uses the no-pull projection; Esc keeps the draft. Verified just portable-check (2699 tests, 0 failures), Mac scratch Scripts/bundle.sh + just typecheck-tests (BobMacCaptureTests including CaptureRequirementPipelineTests type-checked), and CapturePullInClientTests 17 plus CaptureSuccessorOfferRowsTests 7 after making canonicalRequirementGroups public. No leftover --epic-symbol entries.

[2026-11-22T22:23:01Z · bob-cli-on.15.1.3--1] CI recovery: CaptureRequirementPipelineTests pointed fake-bob at Tests/Tests/Fixtures/fake-bob (one directory short of package root). All 10 pipeline tests failed because preview never launched fake-bob, so the Pull-In card never opened. fakeBobPath now matches sibling BobMacCaptureTests helpers and throws if the executable is missing. macos-ci-check restaged after this note.

## Dependencies

- **Depends on:** [bob-cli-on.15.1.2](bob-cli-on.15.1.2.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.15.1.4](bob-cli-on.15.1.4.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.15.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.3.md) | [bob-cli-on.15.1.3](bob-cli-on.15.1.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@3eea97b`](https://github.com/bobs-org/bob-mac-capture/commit/3eea97b2ce3a207c0295adf5b070b90b227833da) | feat(capture): preserve requirement choices through preview and submit | [bob-cli-on.15.1.3](bob-cli-on.15.1.3.md) | 2026-11-22 16:56:40 EST |
| bob-mac-capture | [`bob-mac-capture@69a70da`](https://github.com/bobs-org/bob-mac-capture/commit/69a70dacb4d920d40165d981e1283d86a56cbde4) | test(capture): resolve fake-bob from the package root in pipeline tests | [bob-cli-on.15.1.3](bob-cli-on.15.1.3.md) | 2026-11-22 17:33:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.15.1.3--1][1] | Need closed phase notes and parent DECISIONS before CI test fix | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.3.md

<!-- sase:referenced-by:end -->
