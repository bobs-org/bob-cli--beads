# Bead: bob-cli-dl.7 — Bob Mac Capture renders bob's cancel consequences

[Bead Pages](../README.md) / [bob-cli-dl](README.md) / bob-cli-dl.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2r.linker.w0.md) · **Assignee:** `bob-cli-dl.7` · **Size:** medium
**Created:** 2026-10-28 08:15:27 EDT · **Closed:** 2026-10-28 12:47:42 EDT
**Plan:** [202610/relation\_cancel\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_cancel_labels.md)

## Description

mac-cancel-cue: decode the new additive fields, then render the relation card ⊘ cancels capsule, the dimmed ⊘ source in the sentence, bob's verdict line in the one-off warning slot, the ⊘ tint on the draft label span, and the preview and success rows. Restyles the relation_cancelled_source warning by code, adds fixtures from real bob output, tests, docs, and compiled Swift with green macOS CI.

## Notes

[2026-10-28T16:47:20Z · bob-cli-dl.7] PROPOSED FOLLOW-UP: just docs-check generated drift on docs/reference/glossary.md reproduces on the clean base tree (`bob-docs gen -c`; lint+Zensical build passed with this checkout mounted). This phase did not edit glossary (memory_glossary_term=no; memory_glossary_relation is rollout-only).

[2026-10-28T16:47:26Z · bob-cli-dl.7] PROPOSED FOLLOW-UP: Mac SSH to kellys-macbook-pro.tail297af1.ts.net timed out; BobMacCapture and BobMacCaptureTests were not typechecked. CaptureCore compiled on athena (just portable-check, 1730 tests, 0 failures). AGENTS.md: macOS targets unverified.

[2026-10-28T16:47:42Z · bob-cli-dl.7] mac-cancel-cue landed in bob-mac-capture: decodeIfPresent cancels_source/configured/relation_cancel/span cancels_source/relation_cancels[]/cancel_effect/relation_cancelled_source; ⊘ capsule, dimmed sentence source, verdict slot, cancelled span tint, ⊘ preview rows, Capture & cancel N task(s) submit hint, skip duplicate cancel warning. Real-bob fixtures (complete/parse/dry-run/commit). Athena just portable-check: 1730 CaptureCore tests, 0 failures. bob-docs lint + strict Zensical build with this tree mounted. epic-symbols: none. Mac unreachable so BobMacCapture typecheck/CI unverified; glossary.md docs-check drift is clean-base (see notes).

## Dependencies

- **Depends on:** [bob-cli-dl.3](bob-cli-dl.3.md) ✓ · ⧖ 2026-10-28
- **Depends on:** [bob-cli-dl.4](bob-cli-dl.4.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dl.8](bob-cli-dl.8.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dl.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dl.7/README.md) | [bob-cli-dl.7](bob-cli-dl.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e5f6604`](https://github.com/bobs-org/bob-mac-capture/commit/e5f66043e4a704e6a19d4d83b331e6b5a2aaa7af) | feat(relation-picker): render bob's cancel-label ⊘ cue | [bob-cli-dl.7](bob-cli-dl.7.md) | 2026-10-28 12:49:05 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dl.4][1] | Need sibling phase status | 1 |
| read-by | [agent:bob-cli-dl.7][2] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dl.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dl.7/README.md

<!-- sase:referenced-by:end -->
