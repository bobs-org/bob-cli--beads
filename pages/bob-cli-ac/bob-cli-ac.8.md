# Bead: bob-cli-ac.8 — End-state verification and Bryan's go-live report

[Bead Pages](../README.md) / [bob-cli-ac](README.md) / bob-cli-ac.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.w1.md) · **Size:** small
**Created:** 2026-10-20 18:36:54 EDT · **Closed:** 2026-10-21 00:17:41 EDT
**Plan:** [202610/crates\_io\_release\_train.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/crates_io_release_train.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:69aedc409000fc76103efc6e | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

handoff: verify CI, the train, and the docs against what landed, finish any pending rehearsal dispatch, and publish an artifact report of Bryan's remaining steps.

## Notes

[2026-10-21T04:15:11Z · bob-cli-ac.8--1] PROPOSED FOLLOW-UP: after the tag-to-ref binaries fix lands on master, re-dispatch the Release workflow with override_reason and confirm 4 binary archives attach to v0.2.0 (same-day re-dispatch without override must print SKIP).

[2026-10-21T04:15:16Z · bob-cli-ac.8--1] PROPOSED FOLLOW-UP: post-go-live, switch download/install docs from GitHub Releases wording to crates.io install now that the rehearsal archives exist.

[2026-10-21T04:15:21Z · bob-cli-ac.8--1] PROPOSED FOLLOW-UP: evaluate splitting oversized binary assets into a separate assets crate if Release archives approach GitHub size limits.

[2026-10-21T04:17:41Z · bob-cli-ac.8--1] Rehearsal Release 39540723503: plan/ci/release green, tag + Release v0.2.0 created with seeded notes, no bump commit; both binaries jobs failed on invalid tag: input to upload-rust-binary-action. Fixed with ref: refs/tags/<tag> in .github/workflows/release.yml (just check green: fmt, clippy, 3000+ tests; release-tools 48 tests). Handoff artifact file:explicit:69aedc409000fc76103efc6e. Binaries attach pending one post-landing re-dispatch with override_reason (recorded as PROPOSED FOLLOW-UP); same-day skip check and go-live steps in the report.

## Dependencies

- **Depends on:** [bob-cli-ac.5](bob-cli-ac.5.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-ac.7](bob-cli-ac.7.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ac.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ac.8.md) | [bob-cli-ac.8](bob-cli-ac.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1257c2e`](https://github.com/bobs-org/bob-cli/commit/1257c2e8d90cfaec4e8d6ad14edc457637685dac) | ci(release): upload binaries via ref instead of unsupported tag input | [bob-cli-ac.8](bob-cli-ac.8.md) | 2026-10-21 00:18:44 EDT |
