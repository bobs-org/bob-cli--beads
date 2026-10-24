# Bead: bob-cli-an.6.6.6.4 — Commit only the relation label the user authored

[Bead Pages](../README.md) / [bob-cli-an.6.6.6](bob-cli-an.6.6.6.md) / bob-cli-an.6.6.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.4` · **Size:** medium
**Created:** 2026-10-24 05:39:22 EDT · **Closed:** 2026-10-24 06:08:24 EDT
**Plan:** [202610/backlog\_batch4\_ci\_identity\_capture\_flags\_plugin\_tests\_relation\_race.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch4_ci_identity_capture_flags_plugin_tests_relation_race.md)

## Description

relation-label-race: resolve bob-cli-al by tying Bob Mac Capture relation label suggestions to the request and authored label that produced them.

## Notes

[2026-10-24T10:08:10Z · bob-cli-an.6.6.6.4] Baseline: bob-cli-al reproduced from description + harness file:explicit:dd078a92f55551184b77dfc7 (authored=new commits |old). Generation guard existed in fetch handler but submit committed any typed row and the completion handler overwrote rows without any label check. Fix (bob-mac-capture, thin-client safe): prompt state gains suggestionAuthoredLabel; every label edit/cycle untags rows; submit commits only a fresh typed/match row else bob-grammar authored replacement (|label / |"multi word", mirroring collapse+quoted_form); probe responses gated on generation+draft+authoredLabel via testable applyRelationLabelSuggestions; completion handler adopts only query-matching rows and never clobbers fresh rows; Inserts/canSubmit gated on freshness. Tests: 9 new in CaptureRelationPanelTests (pending/immediate-Return, fresh-quoted, edit-invalidation, stale-gen drop, label-mismatch drop, spelling units, delayed+out-of-order async with fake-bob) + 2 probe fixtures/branches. Validation: mac just typecheck-tests exit 0; Linux swift build + swift test 1554 pass; fake-bob branches exercised; helper logic executed (6/6 incl. bob parity). XCTest execution itself not run here (mac has no XCTest, Linux has no AppKit) — left for CI/lander. Task bead bob-cli-al left OPEN for the lander.

[2026-10-24T10:08:24Z · bob-cli-an.6.6.6.4] Verified: mac just typecheck-tests exit 0 on the patched tree; Linux swift build --build-tests + swift test 1554/1554 pass; new fake-bob probe branches return typed-old/typed-new relation_label JSON; authored-replacement helper executed 6/6 incl. parity with bob normalize_relation_label; 9 new race regressions added (sync submit/gate/spelling + delayed/out-of-order async). XCTest execution itself not possible here (no XCTest on mac CLT, no AppKit on Linux) — CI/lander to run. Task bob-cli-al left open for the lander; no epic-symbol leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.4/README.md) | [bob-cli-an.6.6.6.4](bob-cli-an.6.6.6.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@22598dc`](https://github.com/bobs-org/bob-mac-capture/commit/22598dc09f6b4b937259e716eab29a8c263e0ca7) | fix(capture): tie relation-label suggestions to the authored label | [bob-cli-an.6.6.6.4](bob-cli-an.6.6.6.4.md) | 2026-10-24 06:09:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.4][1] | phase notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.4/README.md

<!-- sase:referenced-by:end -->
