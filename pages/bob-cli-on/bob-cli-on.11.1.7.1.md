# Bead: bob-cli-on.11.1.7.1 — Fix verdict, landing, staleness, and range wiring with public-path tests

[Bead Pages](../README.md) / [bob-cli-on.11.1.7](bob-cli-on.11.1.7.md) / bob-cli-on.11.1.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.11.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.land.md) · **Assignee:** `bob-cli-on.11.1.7.1` · **Size:** medium
**Created:** 2026-11-22 20:02:20 EST · **Closed:** 2026-11-22 20:34:57 EST
**Plan:** [202611/obsidian\_req\_close\_card\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_close_card_repairs.md)

## Description

verdict_wiring: map picker reqs to resolver selectors, feed the landing resolver synchronous final texts with exact line text, guard owner blocks from card open through apply, fix counted-range capture, and add the public-path integration matrix.

## Notes

[2026-11-23T01:34:57Z · bob-cli-on.11.1.7.1] Fixed defects 1–4 and the public-path matrix (defect 6) in bob-plugins task-status-cycler. Nav unchanged.

Seam for idless_acceptance:
- Request mapping lives in plugins/task-status-cycler/src/198h-req-close-card-wiring.js as reqCloseCardRequestsFromChoices (picker {key,verdict,reason?} → resolver {selector,verdict,reason?}); applyManagedReqCloseCard in 198g-req-close-integration.js is the call site. Explicit met stays distinct from an absent row. reqCloseCardRequestSelector also accepts an already-mapped selector.
- Owner snapshot lives in planAndApplySuccessorsNow (137-plugin-successor-project.js) at card open: reqCloseOpenNotes from the post-close noteTextsObject, reqCloseOpenOwnerBlocks via reqCloseExpectedOwnerPostimages → reqCloseOwnerPostimagesFromNotes. After revalidateSuccessorPickerChoices, reqCloseRefuseStaleOwnerChoices compares those openBlocks to live postimages from closePassNoteTexts and strips stale owners/requests/jump; ordinary offers still apply.
- Expected texts: after successor edits, daily insertion, and offer-close restores, reqCloseComposeExpectedNotes({openNotes, owners, plan, dailyAfter, restores}) produces expectedNotes; expectedOwnerPostimages are derived from that composed map and passed into applyManagedReqCloseCard, which live-rereads owner+expected paths and refuses req_close_stale when live differs. Never both sides from one live read.
- Landing: resolveManagedReqCloseLanding pre-reads reqCloseLandingNotePaths into a Map, calls resolveReqLanding with a sync (path)=>text|null reader, then reqCloseLandableTarget (0-based line + exact final text for all kinds; blockId only for carried_task; label/description = requirement text).
- Range: captureReqCloseOwnersFromRange (198g) feeds cycleTaskStatusRange (150). Identity-less captureReqCloseOwnersFromText groups each blockId||taskId task as [task]. Fully idless owners remain phase .2.

Verified: npm run build + build:check; 32/32 twin+integration+public-path tests (paths 1–14 including 13b single cycle and 13c completeTaskAtCursor). npm test: 8867 pass / 1 fail / 4 skip over 8872 unit + 17/17 perf. The unit fail is known flake bob-cli-km (test-ledger-tools-event-link-times.cjs “one build over a 200-link ledger stays under 25 ms”, 78.1 ms under load); isolated pass 4.4 ms. Deployed with bob plugins sync --repo this checkout -p task-status-cycler (nav not changed). No --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-on.11.1.7.2](bob-cli-on.11.1.7.2.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11.1.7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.7.1/README.md) | [bob-cli-on.11.1.7.1](bob-cli-on.11.1.7.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.7.1][1] | Need the phase scope and design file | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.7.1/README.md

<!-- sase:referenced-by:end -->
