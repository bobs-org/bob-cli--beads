# Bead: bob-cli-hl.5.1.1 — Decode merge-in contracts and record fixture responses

[Bead Pages](../README.md) / [bob-cli-hl.5.1](bob-cli-hl.5.1.md) / bob-cli-hl.5.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.md) · **Assignee:** `bob-cli-hl.5.1.1` · **Size:** medium
**Created:** 2026-11-06 01:47:45 EST · **Closed:** 2026-11-06 02:08:52 EST
**Plan:** [202611/capture\_merge\_in\_mac.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_mac.md)

## Description

wire: add tolerant merge_in, diagnostic rewrite, merge_in_pending, block-line origin, and related-link decoding. Record reproducible synthetic Bob responses and portable decoding tests, preserving existing transfer contracts.

## Notes

[2026-11-06T07:08:52Z · bob-cli-hl.5.1.1] Wire phase done in bob-mac-capture checkout: tolerant CaptureMergeIn/CaptureDiagnosticRewrite/CaptureMergeInPending decoding, block-line origin, merge_in related-link kind (merge_in excluded from Similar-tasks display). Recorded 31 deterministic fixtures via Scripts/generate-merge-in-preview-fixtures.sh (BOB_BIN built from bob-cli 5c119a06, clock 2026-11-03, manifest captures commit) plus CaptureMergeInDecodingTests (23 tests). Verified: swift test --filter CaptureMergeInDecodingTests 23/23 pass; just portable-check 2225 tests 0 failures; just check-scripts OK. Existing transfer contracts untouched; no grammar-gate bump. macOS exact-SHA gate left for land agent (no push from this phase).

## Dependencies

- **Blocks:** [bob-cli-hl.5.1.2](bob-cli-hl.5.1.2.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.5.1.1/README.md) | [bob-cli-hl.5.1.1](bob-cli-hl.5.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@b4b343f`](https://github.com/bobs-org/bob-mac-capture/commit/b4b343f81c206d5b378438cda8381ba916e41934) | feat(capture): add merge-in tolerant models, fixtures and decoding tests | [bob-cli-hl.5.1.1](bob-cli-hl.5.1.1.md) | 2026-11-06 02:10:15 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.5.1.1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.5.1.1/README.md

<!-- sase:referenced-by:end -->
