# Bead: bob-cli-hl.5.1.2 — Integrate merge-in source pickers and explicit diagnostic rewrites

[Bead Pages](../README.md) / [bob-cli-hl.5.1](bob-cli-hl.5.1.md) / bob-cli-hl.5.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.md) · **Assignee:** `bob-cli-hl.5.1.2` · **Size:** medium
**Created:** 2026-11-06 01:47:45 EST · **Closed:** 2026-11-06 02:47:56 EST
**Plan:** [202611/capture\_merge\_in\_mac.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_mac.md)

## Description

editor: add a distinct merge-in source picker role, Bob-authored continuations and Add block ID splicing, span colors, revision-safe pending state, and a generic explicit diagnostic rewrite action. Keep incomplete captures unsubmitable.

## Notes

[2026-11-06T07:47:48Z · bob-cli-hl.5.1.2--1] PROPOSED FOLLOW-UP: Fix the baseline SimilarTasksBandView switch for CaptureRelatedLinkKind.mergeIn during bob-cli-hl.5.1.5 integrated Mac verification — the identical Build error reproduces on clean base b4b343f81c206d5b378438cda8381ba916e41934 (CI run 42179109017) and editor snapshot a04a2303781a893b80b863ab2ed6b11b362e8d0c (run 42182120044).

[2026-11-06T07:47:56Z · bob-cli-hl.5.1.2--1] Completed merge-in source picker role, Bob-authored parent replacement/Add block ID splicing, revision-bound pending state, span colors, and explicit Unicode-safe diagnostic rewrites. Focused portable tests passed (135); just portable-check passed (2,227 tests, one skipped). Exact-SHA macOS CI build fails only on the pre-existing SimilarTasksBandView missing .mergeIn switch case; confirmed identical failure on clean base SHA b4b343f81c206d5b378438cda8381ba916e41934 in CI run 42179109017. Recorded the rollout-phase follow-up; epic-symbols reports none.

## Dependencies

- **Depends on:** [bob-cli-hl.5.1.1](bob-cli-hl.5.1.1.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hl.5.1.3](bob-cli-hl.5.1.3.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.5.1.2.md) | [bob-cli-hl.5.1.2](bob-cli-hl.5.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@8c956ca`](https://github.com/bobs-org/bob-mac-capture/commit/8c956ca52b704bb4e3b0add118445470ae186eae) | feat(capture): add merge-in source picker and diagnostic rewrite actions | [bob-cli-hl.5.1.2](bob-cli-hl.5.1.2.md) | 2026-11-06 02:49:38 EST |
