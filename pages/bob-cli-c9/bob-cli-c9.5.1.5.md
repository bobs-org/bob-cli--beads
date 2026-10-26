# Bead: bob-cli-c9.5.1.5 — Verify user behavior and extend Mac acceptance documentation

[Bead Pages](../README.md) / [bob-cli-c9.5.1](bob-cli-c9.5.1.md) / bob-cli-c9.5.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.5.md) · **Assignee:** `bob-cli-c9.5.1.5` · **Size:** medium
**Created:** 2026-10-26 07:41:50 EDT · **Closed:** 2026-10-26 10:37:05 EDT
**Plan:** [202610/annotated\_reference\_overwrite.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/annotated_reference_overwrite.md)

## Description

acceptance: Add cross-cutting recapture regressions, pin processed annotation identity, extend the isolated Highlights acceptance kit, and update create/sync docs. Run the prescribed local gates and prepare evidence for the child epic land agent. Real Highlights acceptance is a manual Mac step, never a Linux claim.

## Notes

[2026-10-26T14:37:05Z · bob-cli-c9.5.1.5] Verified annotated overwrite acceptance on Linux: CLI suite tests/cli/highlights/overwrite_annotated.rs (7 tests) refuses text-highlight, image-sidecar, .assets-only, and inbound-link annotated targets before fake fetch/adapter and leaves vault bytes unchanged; coordination key-on still refuses off macOS; dry-run previews annotated archives and writes nothing; dirty inbound and open note-task refusals win over the host gate; -o still wins with recapture's in-place path message; exact-set collections refuse annotated members before the adapter. Unit execute tests processed_highlight_identity_survives_overwrite_and_rescan and two_annotated_overwrites_keep_newest_first_archives_and_task pin [h::]/^h- identity, no duplicate follow-up, two newest-first archives, and preserved task identity via FakeCoordinator. Gate annotated_execution_refusal is last after dirty/ignored. Kit scripts/dev/highlights_coordination_acceptance keeps original steps 1-10 and enablement verdict, then guided annotated overwrite 11-15 with replacement PDF named after the filed stem plus Info /Title; bash -n and --self-test 10/10 (key-off/Linux refusal, annotated dry-run, simulated replaced_capture). just docs-gen and just docs-check passed; docs/highlights-create.md and docs/highlights-ref-sync.md cover Mac eligibility, archives, [h::] survival, holds, and runbook. Recapture after_help already truthful; no CLI help change. Real Highlights acceptance is a manual Mac step, never a Linux claim. No --epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-c9.5.1.4](bob-cli-c9.5.1.4.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.5.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.5/README.md) | [bob-cli-c9.5.1.5](bob-cli-c9.5.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8a1679e`](https://github.com/bobs-org/bob-cli/commit/8a1679e553009b4c939995dc231144ae92fc6ac7) | test(highlights): cover annotated overwrite refusals and Mac kit | [bob-cli-c9.5.1.5](bob-cli-c9.5.1.5.md) | 2026-10-26 10:38:11 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.5.1.5][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.5.1.5/README.md

<!-- sase:referenced-by:end -->
