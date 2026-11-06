# Bead: bob-cli-hl.4 — Pickers, rewrite toggle, and Similar tasks

[Bead Pages](../README.md) / [bob-cli-hl](README.md) / bob-cli-hl.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.190](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.190.md) · **Assignee:** `bob-cli-hl.4` · **Size:** medium
**Created:** 2026-11-05 18:05:40 EST · **Closed:** 2026-11-05 20:18:08 EST
**Plan:** [202611/capture\_merge\_in\_arrow.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_arrow.md)

## Description

assist: give `<` source slots a merge-only picker with ID-less rows and comma multi-pick, the `+` separator toggle, and capture-related source exclusion with a marker anchor before the arrow.

## Notes

[2026-11-06T01:17:49Z · bob-cli-hl.4] PROPOSED FOLLOW-UP: Fix the base-tree `just check` Clippy error: unused `TODAY` in tests/cli/capture/merge_in.rs:8 (present unchanged in HEAD 53c1d1ad). The `just docs-check` glossary drift is already recorded on parent bob-cli-hl note #1 and belongs to phase bob-cli-hl.6; no duplicate follow-up filed.

[2026-11-06T01:18:08Z · bob-cli-hl.4] Implemented merge-in source pickers, rewrite toggles, typed-source exclusion, row details, ID-less source flows, and related-action anchoring. Verified 37 merge-in-filtered lib tests pass and git diff --check is clean. just check stops at the base-tree unused TODAY Clippy error in tests/cli/capture/merge_in.rs:8 (recorded PROPOSED FOLLOW-UP); just docs-check reports the glossary drift already tracked on bob-cli-hl note #1 for phase .6. epic-symbols reported none.

## Dependencies

- **Depends on:** [bob-cli-hl.2](bob-cli-hl.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hl.5](bob-cli-hl.5.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.4/README.md) | [bob-cli-hl.4](bob-cli-hl.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5ab0ec2`](https://github.com/bobs-org/bob-cli/commit/5ab0ec228cbdcaae59058e5fd0204f5cedff47ec) | feat(capture): add merge-in source picker assistance | [bob-cli-hl.4](bob-cli-hl.4.md) | 2026-11-05 20:19:56 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.4][1] | Confirm assigned phase closure and its verification note | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.4/README.md

<!-- sase:referenced-by:end -->
