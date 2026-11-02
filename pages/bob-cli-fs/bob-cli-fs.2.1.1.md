# Bead: bob-cli-fs.2.1.1 — Successor-label policy and shared copy

[Bead Pages](../README.md) / [bob-cli-fs.2.1](bob-cli-fs.2.1.md) / bob-cli-fs.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-fs.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.2.md) · **Assignee:** `bob-cli-fs.2.1.1` · **Size:** medium
**Created:** 2026-11-02 06:30:50 EST · **Closed:** 2026-11-02 07:00:05 EST
**Plan:** [202611/relation\_successor\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/relation_successor_core.md)

## Description

policy_copy: add the three-effect relation policy and typed copy builders, with every config, key, and copy vector exercised.

## Notes

[2026-11-02T11:43:08Z · bob-cli-fs.2.1.1] PROPOSED FOLLOW-UP: Sync the corrected SU-P22 48-character inclusive truncation expectation to bob-plugins and verify fixture parity — the prior shared vector expected 49 total characters, while the approved plan caps text at 48 including the ellipsis.

[2026-11-02T11:45:02Z · bob-cli-fs.2.1.1] PROPOSED FOLLOW-UP: Sync the corrected relation-successor fixture vectors to bob-plugins and verify byte parity — SA23 also used an unquoted colon label in YAML, so its intended successor/complete overlap could not be parsed.

[2026-11-02T11:59:52Z · bob-cli-fs.2.1.1] POLICY_COPY API for classifier: RelationsConfig now exposes successor_labels, label_effect, and label_for_inverse; close_effect and close_label_for_inverse remain Cancel/Complete-only. The shared module exports RelationTarget, RelationEvent (Parked/Done plus optional slot), structured RelationHeldReason/RelationHeldRow, and typed copy inputs/builders from task_complete::relation_successors::copy. Tests load config, key, and all copy vectors through the production APIs in relation_successor_vectors.rs.

[2026-11-02T12:00:05Z · bob-cli-fs.2.1.1] Implemented successor label policy and typed copy builders; config/key/copy vectors pass (including overlap warning bytes and Unicode truncation), and cancel, complete, inverse, formatting, and lint checks pass. epic-symbols reports no leftovers.

## Dependencies

- **Blocks:** [bob-cli-fs.2.1.2](bob-cli-fs.2.1.2.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.1/README.md) | [bob-cli-fs.2.1.1](bob-cli-fs.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c3a2e62`](https://github.com/bobs-org/bob-cli/commit/c3a2e62acdec4ca22dc740038862ce5648156461) | feat(task-relations): add successor-label policy and shared copy | [bob-cli-fs.2.1.1](bob-cli-fs.2.1.1.md) | 2026-11-02 07:00:54 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fs.2.1.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.1/README.md

<!-- sase:referenced-by:end -->
