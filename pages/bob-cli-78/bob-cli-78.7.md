# Bead: bob-cli-78.7 — Cycler and block-id-prompt honour the cascade and pull in parents

[Bead Pages](../README.md) / [bob-cli-78](README.md) / bob-cli-78.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.71](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.71.md) · **Assignee:** `bob-cli-78.7` · **Size:** medium
**Created:** 2026-10-13 03:14:28 EDT · **Closed:** 2026-10-13 03:51:53 EDT
**Plan:** [202610/subproject\_cascade.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/subproject_cascade.md)

## Description

cycler: make task-status-cycler and block-id-prompt read a tagged ^prj as an inherited reason, refuse Alt+]/Alt+[ on it, implement pull-in step 3 and trigger (c), and add subtree recovery only under close_recovers_subprojects.

## Notes

[2026-10-13T07:51:27Z · bob-cli-78.7] PROPOSED FOLLOW-UP: Update glossary:project-task to say sub-projects inherit ancestor project blocking; skipped because memory_glossary=no.

[2026-10-13T07:51:32Z · bob-cli-78.7] PROPOSED FOLLOW-UP: Triage clean-base npm test failures: four unblocked-glyph cases in test-ledger-tools-unblocked-glyph.cjs and Keep counts once in test-navigation-decision-card-handlers.cjs; all five reproduce on clean HEAD.

[2026-10-13T07:51:53Z · bob-cli-78.7] Implemented inherited project-blocking guards and parent pull-in for the cycler/block-id-prompt; focused suite 132/132, build and validate passed, both plugins synced. Full npm test has five unrelated failures reproduced on clean HEAD and recorded as follow-ups; epic-symbol check found none.

## Dependencies

- **Depends on:** [bob-cli-78.1](bob-cli-78.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-78.8](bob-cli-78.8.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-78.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-78.7/README.md) | [bob-cli-78.7](bob-cli-78.7.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`23dbefe`](https://github.com/bobs-org/bob-cli/commit/23dbefe507eac92896f660512733b1040371a8f9) | docs(memory): record subproject blocking cascade | [bob-cli-78.7](bob-cli-78.7.md) | 2026-10-13 03:52:50 EDT |
| bob-plugins | [`bob-plugins@53ec2eb`](https://github.com/bobs-org/bob-plugins/commit/53ec2eb1c8cc12413c757c06d4a2d6b4ef5ac85d) | feat(plugins): honor inherited project blocking | [bob-cli-78.7](bob-cli-78.7.md) | 2026-10-13 03:53:52 EDT |
