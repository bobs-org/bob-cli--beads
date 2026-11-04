# Bead: bob-cli-h0.8 — Move card submit flow, chaining, refusals, preview hints, and docs

[Bead Pages](../README.md) / [bob-cli-h0](README.md) / bob-cli-h0.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.37.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.37.linker.w0.md) · **Assignee:** `bob-cli-h0.8` · **Size:** medium
**Created:** 2026-11-04 08:50:24 EST · **Closed:** 2026-11-04 15:53:52 EST
**Plan:** [202611/move\_choice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/move_choice.md)

## Description

mac-flow: open the Move card on Return ahead of Pull-In, send `--move-in`, chain Pull-In and inbox routing, reopen on refusals with surviving marks, add the ghost hint, band line, move hint, old-bob gate, notification, and docs.

## Notes

[2026-11-04T20:51:29Z · bob-cli-h0.8] WALKTHROUGHS: No live Mac UI driver was used. Leave these three real-card walkthroughs to Bryan: (1) move three tasks without linking; (2) mix two moves and one link; (3) mark an ID-less task, cancel, and confirm no ID or move was written. Added portable state/real-bob fixture coverage and hosted model/design tests for the same semantics, including a 76-row card; the Mac has CLT-only XCTest stubs, so hosted tests are type-checked here and execute in CI.

[2026-11-04T20:53:52Z · bob-cli-h0.8] Implemented and verified the linked bob-mac-capture Move submit flow before Pull-In/inbox routing, capability-gated --move-in, retained marks and back navigation, fresh-row refusal recovery (including answered dry-run refresh when follow-on metadata is absent), old-bob warning, ghost/band/hint/notification presentation, and docs. Completed required state/router/decoder integration including filtering, explicit answer serialization, reseeding, named-link gating, and moved_tasks.via. Verification: just portable-check on athena passed 2118 tests (1 skipped, 0 failures); real-bob MQ5/MQ11/MQ12/MQ16 previews plus MQ7/MQ10 answered fixtures generated using current bob-cli build; scratch Mac bundle.sh and typecheck-tests passed all four test targets on the final source; just docs-check passed all gates with 447 tests passed and 1 skipped; just check-scripts passed 8 docs-script and 42 CI-script tests. No epic-symbol entries. No memory edited. Live card walkthroughs and the CLT-only hosted-test limitation are recorded in the preceding note; CI executes the hosted tests.

## Dependencies

- **Depends on:** [bob-cli-h0.5](bob-cli-h0.5.md) ✓ · ⧖ 2026-11-04
- **Depends on:** [bob-cli-h0.6](bob-cli-h0.6.md) ✓ · ⧖ 2026-11-04
- **Depends on:** [bob-cli-h0.7](bob-cli-h0.7.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-h0.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.8/README.md) | [bob-cli-h0.8](bob-cli-h0.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@0245a75`](https://github.com/bobs-org/bob-mac-capture/commit/0245a752dde5fabd2e7a86f6ab7ce1ec56822b96) | feat(capture): submit Move choices before Pull-In and inbox routing | [bob-cli-h0.8](bob-cli-h0.8.md) | 2026-11-04 16:03:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h0.8][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.8/README.md

<!-- sase:referenced-by:end -->
