# Bead: bob-cli-fs.10.1.2 — Render Bob-authored Pull-In groups and select relation offers

[Bead Pages](../README.md) / [bob-cli-fs.10.1](bob-cli-fs.10.1.md) / bob-cli-fs.10.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-fs.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.10.md) · **Assignee:** `bob-cli-fs.10.1.2` · **Size:** medium
**Created:** 2026-11-02 19:46:05 EST · **Closed:** 2026-11-02 20:34:58 EST
**Plan:** [202611/mac\_relation\_successors.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_relation_successors.md)

## Description

chooser: make the Pull-In choice model and card consume Bob's group order and copy, gather relation offers from every capture location, preserve opaque selection keys, and cover relation-only and mixed choices with model and design tests.

## Notes

[2026-11-03T01:34:58Z · bob-cli-fs.10.1.2] Chooser consumes Bob pull_in.groups order and copy (title/capsule/why/tag/fold/glyph), joins sections on (group, project, after, label), gathers relation offers from all four payload locations via allRelationSuccessors, and round-trips opaque keys. CapturePullInChoiceTests, CapturePullInChoiceModelTests, and CapturePullInChoiceDesignTests cover relation-only, mixed order, distinct targets, distinct labels, unknown glyph, Bob copy override, no-copy fallbacks, empty per-item groups, after/second-reason meta, caption/fold height, real parked/toggle/nested/done fixtures, required-choice refusal, and --pull-in none. just portable-check passed on athena (2026 CaptureCore/RefsCore tests, 0 failures). Bounded SSH to mac (ConnectTimeout=8) timed out; macOS BobMacCapture typecheck remains unverified.

## Dependencies

- **Depends on:** [bob-cli-fs.10.1.1](bob-cli-fs.10.1.1.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fs.10.1.3](bob-cli-fs.10.1.3.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.10.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.10.1.2/README.md) | [bob-cli-fs.10.1.2](bob-cli-fs.10.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@52a222a`](https://github.com/bobs-org/bob-mac-capture/commit/52a222ad38211eafaa6afae79a39597fd8d46687) | feat(capture): render Bob-authored Pull-In relation groups | [bob-cli-fs.10.1.2](bob-cli-fs.10.1.2.md) | 2026-11-02 20:37:04 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fs.10.1.2][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.10.1.2/README.md

<!-- sase:referenced-by:end -->
