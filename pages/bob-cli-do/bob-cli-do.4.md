# Bead: bob-cli-do.4 — Name duplicated-task copies in ref scan failures

[Bead Pages](../README.md) / [bob-cli-do](README.md) / bob-cli-do.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.157.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.157.f0.md) · **Assignee:** `bob-cli-do.4` · **Size:** small
**Created:** 2026-10-28 10:46:06 EDT · **Closed:** 2026-10-28 13:29:37 EDT
**Plan:** [202610/clobbered\_note\_repair\_and\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/clobbered_note_repair_and_guards.md)

## Description

ref-scan-copy-hint: make multiple_open_ref_tasks say when the claimants are copies of one task, and group repeated refusals into one cause line pointing at the clobber runbook.

## Notes

[2026-10-28T17:21:13Z · bob-cli-do.4] PROPOSED FOLLOW-UP: Regenerate stale glossary documentation — just docs-check passes lint but fails generated drift with "out of date: docs/reference/glossary.md (run just docs-gen)". Reproduced identically on untouched base b8df2f48 in an isolated worktree and on the phase tree; also reported by bob-cli-dl.7 and bob-cli-dk. No memory files or generated glossary were changed by this phase.

[2026-10-28T17:26:43Z · bob-cli-do.4] PROPOSED FOLLOW-UP: Capture-related synthetic draft timing gate still flakes under the full suite — check run f9d3fb57f9ada3da1680791bcbf3d156 failed native::capture_related::tests::synthetic_vault_draft_contract_is_under_250ms at src/native/capture_related/tests.rs:578 (paired excess 517.54 ms versus the current 500 ms bound). It passed unchanged immediately in isolation (1.12 s total). Prior tracking: bob-cli-ca and its paired-baseline fix phase bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.1; this phase changes no capture-related code.

[2026-10-28T17:29:37Z · bob-cli-do.4] Verified same-block-ID copy hints (including known parent), distinct/missing-ID exclusions, grouped claimant-note causes in human/error output, unchanged scan JSON fields, and refusal byte preservation. Full just check passed via sase tool run 6dda6f4fd3b209fa1e6f3cff9e65b629. No epic-symbol entries remain. just docs-check passes lint but has identical pre-existing glossary generated drift on clean base b8df2f48; recorded as PROPOSED FOLLOW-UP. Earlier capture-related timing flake passed unchanged in isolation and in the final full gate; recorded with prior tracking references.

## Dependencies

- **Depends on:** [bob-cli-do.3](bob-cli-do.3.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-do.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-do.4/README.md) | [bob-cli-do.4](bob-cli-do.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0f1898e`](https://github.com/bobs-org/bob-cli/commit/0f1898ee7b98a663ded6c0684af7ea6910248c86) | fix(ref): explain copied reading tasks in scan failures | [bob-cli-do.4](bob-cli-do.4.md) | 2026-10-28 13:30:25 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-do.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-do.4/README.md

<!-- sase:referenced-by:end -->
