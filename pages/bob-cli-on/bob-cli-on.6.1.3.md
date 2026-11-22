# Bead: bob-cli-on.6.1.3 — Requirements in the blocks capture creates

[Bead Pages](../README.md) / [bob-cli-on.6.1](bob-cli-on.6.1.md) / bob-cli-on.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.md) · **Assignee:** `bob-cli-on.6.1.3` · **Size:** medium
**Created:** 2026-11-21 13:50:29 EST · **Closed:** 2026-11-21 20:29:00 EST
**Plan:** [202611/capture\_req\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_req_bullets.md)

## Description

new-block-writes: render new tasks, list tasks, Pomodoro-created tasks, and project-note rows so reqs sit in the reqs zone and notes follow the NOTES rule through task_block_layout, and report an additive requirements summary in JSON and human output.

## Notes

[2026-11-22T01:28:44Z · bob-cli-on.6.1.3] PROPOSED FOLLOW-UP: just docs-check contract-registry tests fail on clean HEAD 17eae49c independently of this phase (tools/docs/tests/test_contracts.py expects 54 contracts / README table SHA 34f4f8a4; live registry is 55 including task-requirements.md / walks.md, table SHA f23b0e44). Same failure already noted on bob-cli-on.10.1.5; closed bob-cli-hs is obsolete for this new baseline.

[2026-11-22T01:29:00Z · bob-cli-on.6.1.3] new-block-writes: canonicalize_new_req_block (plan_tidy, notes_drawer_birth=with_first_note) on new Task/TaskWithBlockId/Pomodoro-created blocks and each project-note ## Tasks row; additive JSON requirements[] + human ⌗⌗ summary. CLI tests/cli/capture/reqs_new.rs (9) plus unit canonicalize tests pass; cargo test --test cli 3954 passed; cargo fmt/clippy passed; just docs-gen. Existing-task/@route+id left to bob-cli-on.6.1.4. just docs-check 3 contract-registry tests fail identically on clean HEAD 17eae49c (filed PROPOSED FOLLOW-UP citing bob-cli-on.10.1.5).

## Dependencies

- **Depends on:** [bob-cli-on.6.1.2](bob-cli-on.6.1.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.6.1.4](bob-cli-on.6.1.4.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.3/README.md) | [bob-cli-on.6.1.3](bob-cli-on.6.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0a623b7`](https://github.com/bobs-org/bob-cli/commit/0a623b7036fbc9ccb86ebd4ef28889374affc604) | feat(capture): write new-task requirement bullets into the reqs zone | [bob-cli-on.6.1.3](bob-cli-on.6.1.3.md) | 2026-11-21 20:30:10 EST |
