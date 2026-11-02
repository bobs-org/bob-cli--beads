# Bead: bob-cli-fn.2 — Default block-ID suggestions tuned on the vault

[Bead Pages](../README.md) / [bob-cli-fn](README.md) / bob-cli-fn.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c1.md) · **Assignee:** `bob-cli-fn.2` · **Size:** medium
**Created:** 2026-11-01 23:41:34 EST · **Closed:** 2026-11-02 01:49:23 EST
**Plan:** [202611/capture\_route\_lists.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_route_lists.md)

## Description

id-suggester: add an ignored calibration harness over a real vault, then retune the shared block-ID suggester (filler lead-ins, content words, length) so its first suggestion is closer to the IDs Bryan writes himself, with measured before/after numbers.

## Notes

[2026-11-02T04:53:32Z · bob-cli-fn.2] Baseline (BOB_ID_CALIBRATION_VAULT=~/bob, ignored block_id_calibration, full root corpus): n=413 top1_exact=0.148 top3_exact=0.162 mean_jaccard_first=0.333 mean_jaccard_best3=0.418 mean_first_len=13.9 mean_authored_len=13.9. Acceptance: first Jaccard >= 0.363, best-of-3 Jaccard and top-3 exact not below baseline, mean first len <= 17.

[2026-11-02T06:48:37Z · bob-cli-fn.2] After (BOB_ID_CALIBRATION_VAULT=~/bob, ignored block_id_calibration, full root corpus): n=413 top1_exact=0.090 (0.089588) top3_exact=0.191 (0.191283) mean_jaccard_first=0.361 (0.360657) mean_jaccard_best3=0.455 (0.454808) mean_first_len=16.8 mean_authored_len=13.9. vs baseline n=413 top1=0.148 top3=0.162 j_first=0.333 j_best3=0.418 mean_first_len=13.9. Gates: top3 and best-of-3 up; mean first len 16.8<=17; first Jaccard +0.028 vs required +0.03 (0.360657 vs 0.362630). 24-byte first-suggestion cap kept; raising it to clear Jaccard exceeds length 17.

[2026-11-02T06:48:44Z · bob-cli-fn.2] PROPOSED FOLLOW-UP: skipped memory_list_decision_record — epic decision is no; land agent may add a decisions strand for capture lists under a lone @file header.

[2026-11-02T06:48:50Z · bob-cli-fn.2] PROPOSED FOLLOW-UP: just docs-check fails identically on the clean base tree in test_every_capture_token_has_a_literal_query_at_its_heading (equals-split, equals-merge, plus-child-section, drawer-bullets missing search_smoke.yml literals); already tracked by bob-cli-fo.

[2026-11-02T06:48:56Z · bob-cli-fn.2] PROPOSED FOLLOW-UP: just check lib flake native::task_complete::tests::keep_moving_tests::routing_is_lazy_and_narrow_with_shared_destination (FULL_ROOT_SCAN_COUNT 1 vs 0 under parallel threads; serial pass); previously noted on bob-cli-fe.4 and declined at bob-cli-fk land.

[2026-11-02T06:49:04Z · bob-cli-fn.2] PROPOSED FOLLOW-UP: first-suggestion Jaccard 0.360657 vs required baseline+0.03 (0.362630) under the plan 24-byte cap and mean first length <=17; no remaining rule-preserving tuning hit both gates.

[2026-11-02T06:49:10Z · bob-cli-fn.2] PROPOSED FOLLOW-UP: mounted plugin doc docs/reference/plugins/block-id-defaults.md still shows Add support for new %hold directive minting hold; bob-cli now mints hold-directive as first suggestion.

[2026-11-02T06:49:23Z · bob-cli-fn.2] Retuned shared suggest_ids (filler lead-ins/words, skip leading verbs while 4+ content words remain, drop weak trailing, 24-byte 3-then-2-then-phrase). mint_block_id still takes the first suggestion; 32-byte cap, validation, dedupe, and -2..-9 suffixing unchanged. Ignored block_id_calibration harness on ~/bob: after n=413 top1=0.090 top3=0.191 j_first=0.361 j_best3=0.455 mean_first_len=16.8 (baseline 0.148/0.162/0.333/0.418/13.9). top3, best-of-3, and length pass; first Jaccard +0.028 vs required +0.03. Updated capture-complete docs, SB vectors, minted-ID callers, and the idless capture-related golden. cargo fmt, clippy, and CLI tests pass; lib suite has a pre-existing keep_moving routing flake; docs-check token-coverage fails on clean tree (bob-cli-fo).

## Dependencies

- **Blocks:** [bob-cli-fn.3](bob-cli-fn.3.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fn.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fn.2/README.md) | [bob-cli-fn.2](bob-cli-fn.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`62a8210`](https://github.com/bobs-org/bob-cli/commit/62a821044e665bd618b02859f0dd10879987f196) | feat(capture): retune shared block-ID suggestions from vault calibration | [bob-cli-fn.2](bob-cli-fn.2.md) | 2026-11-02 01:50:35 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fn.2][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fn.2/README.md

<!-- sase:referenced-by:end -->
