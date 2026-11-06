# Bead: bob-cli-hn.3 — bob capture -x/-X flags, batch post-pass, and receipts

[Bead Pages](../README.md) / [bob-cli-hn](README.md) / bob-cli-hn.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.191](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.191/README.md) · **Assignee:** `bob-cli-hn.3` · **Size:** medium
**Created:** 2026-11-05 18:41:47 EST · **Closed:** 2026-11-05 21:52:46 EST
**Plan:** [202611/successor\_card\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_card_verdicts.md)

## Description

cli: add `-x/--complete-offer` and `-X/--cancel-offer`, resolve and validate verdicts, apply them in a capture post-pass, and emit offer.verdict, pull_in.close, offer_closes[], refusals, human output, help, completion, and docs.

## Notes

[2026-11-06T02:52:16Z · bob-cli-hn.3] PROPOSED FOLLOW-UP: just lint fails on base tree too (tests/cli/capture/merge_in.rs:8 unused TODAY const from bob-cli-hl.4); fix or remove it so just check goes green

[2026-11-06T02:52:20Z · bob-cli-hn.3] PROPOSED FOLLOW-UP: just docs-check lychee fails on base tree too (task-merge page links target/docs/capture#merging-tasks-into-a-new-task-with, file not found); unrelated to verdict docs

[2026-11-06T02:52:24Z · bob-cli-hn.3] PROPOSED FOLLOW-UP: base-tree test failures unrelated to verdicts: kinds duplicate clipboard:count entry, catalog public_leaves + protocol_1 count 72vs73, help root snapshot missing gmail line

[2026-11-06T02:52:32Z · bob-cli-hn.3] PROPOSED FOLLOW-UP: epic-authorized memory supersede (mark decisions:unblocked-tasks-are-offered superseded-in-part) was never applied by the contract phase and now dangles: the superseding record successor-cards-resolve-with-staged-verdicts was declined, so there is nothing to link; needs a sase_memory_write decision

[2026-11-06T02:52:36Z · bob-cli-hn.3] PROPOSED FOLLOW-UP: SV13 disk-preimage race (change between planning and commit) has no deterministic e2e hook since capture plans+commits synchronously; covered by replay-stale refusal instead, consider a test-only commit hook if ever needed

[2026-11-06T02:52:46Z · bob-cli-hn.3] cli phase done: -x/-X flags with probe-based key resolution, conflict/stale/refused refusals (write-free, exit 2/2/1), verdict post-pass after successor net pass with joint recover-only cascade, offer.verdict/not_linked/pull_in.close/offer_closes JSON+human receipts. Verified: 18 new successor_verdicts e2e + 3 copy unit tests pass, note_pull goldens regenerated via official script, fmt clean, full suite shows only base-tree failures (recorded as follow-ups). Work uncommitted for the land agent.

## Dependencies

- **Depends on:** [bob-cli-hn.2](bob-cli-hn.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hn.8](bob-cli-hn.8.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.3/README.md) | [bob-cli-hn.3](bob-cli-hn.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`efbe347`](https://github.com/bobs-org/bob-cli/commit/efbe3470dd1eee15711d639e8f0ead022ff86d27) | feat(capture): implement offer verdict surface with complete and cancel offers | [bob-cli-hn.3](bob-cli-hn.3.md) | 2026-11-05 21:54:15 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hn.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.3/README.md

<!-- sase:referenced-by:end -->
