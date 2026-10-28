# Bead: bob-cli-df.4.1.4 — Connect failed-close evidence and prove relaunch recovery

[Bead Pages](../README.md) / [bob-cli-df.4.1](bob-cli-df.4.1.md) / bob-cli-df.4.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.md) · **Assignee:** `bob-cli-df.4.1.4` · **Size:** medium
**Created:** 2026-10-27 21:39:19 EDT · **Closed:** 2026-10-27 23:37:44 EDT
**Plan:** [202610/preserve\_failed\_close\_worktrees.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/preserve_failed_close_worktrees.md)

## Description

failed-close-evidence: attach durable snapshots to existing terminal failure evidence and verify recovery after failed finalization and relaunch without changing failed-close eligibility.

## Notes

[2026-10-28T03:37:26Z · bob-cli-df.4.1.4--1] PROPOSED FOLLOW-UP: Align the SASE Python bead_close facade with the installed sase-core-rs API and run validation from a checkout with its SDD sidecars — focused pytest: 8 failed, 13 passed; all 8 failures stop before phase assertions because bead_mutation_facade.py passes close_provenance as a 10th positional argument while installed sase-core-rs 0.42.7 bead_close accepts at most 9. The four failures in tests/test_finalizers_failed_close_recovery_controls.py are present in clean-base HEAD, confirming the API mismatch predates this phase. `sase tool run check` exited 1 after formatting, ruff, mypy, and other listed lint stages passed: symvision rejected unchanged Justfile epic-symbol entries for sase-1p1(other_id/custom_id) (KNOWN, no owner), and SASE validation rejected the external checkout's missing configured sase/repos/plans directory (UNKNOWN, no owner). No matching close_provenance bead was found in the current bob-cli store.

[2026-10-28T03:37:44Z · bob-cli-df.4.1.4--1] Added durable failed-close snapshot locators, retry reuse, and untracked-content fingerprint coverage. just fmt passed. Focused tests: 13 passed; 8 stopped before assertions on the pre-existing bead_close API mismatch, recorded as a proposed follow-up. sase tool run check exited 1 on unchanged symvision entries and the external checkout missing its configured SDD plans path, recorded as a proposed follow-up. Epic-symbol scan is clear.

## Dependencies

- **Depends on:** [bob-cli-df.4.1.1](bob-cli-df.4.1.1.md) ✓ · ⧖ 2026-10-27
- **Depends on:** [bob-cli-df.4.1.2](bob-cli-df.4.1.2.md) ✓ · ⧖ 2026-10-27
- **Depends on:** [bob-cli-df.4.1.3](bob-cli-df.4.1.3.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.1.4.md) | [bob-cli-df.4.1.4](bob-cli-df.4.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-df.4.1.3][1] | Check downstream phase expectations for relaunch-cleanup outputs | 1 |
| read-by | [agent:bob-cli-df.4.1.4--1][2] | Confirm assigned phase closure and preserved follow-up note | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.4.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.4.1.4.md

<!-- sase:referenced-by:end -->
