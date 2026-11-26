# Bead: bob-cli-q8.7 — applyTieChange — release, reverse, and convert writes

[Bead Pages](../README.md) / [bob-cli-q8](README.md) / bob-cli-q8.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6f.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6f.linker.w0.md) · **Assignee:** `bob-cli-q8.7` · **Size:** medium
**Created:** 2026-11-25 18:16:43 EST · **Closed:** 2026-11-25 23:31:42 EST
**Plan:** [202611/plain\_link\_dependency\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/plain_link_dependency_ties.md)

## Description

nav-tie-writer: one guarded writer runs any planned tie change. It writes the dependency side first, keeps same-note changes in one undo step, reports honest notices and follow-up suffixes, and fixes reopenDependencyStageFresh.

## Notes

[2026-11-26T04:19:23Z · bob-cli-q8.7] PROPOSED FOLLOW-UP: Repair the pre-existing requirement/drawer layout vector failures — scripts/test-task-status-cycler-task-reqs-vectors.cjs has 24 failures on both this tree and the clean base plugin bundle (verified); no matching task bead was found.

[2026-11-26T04:31:42Z · bob-cli-q8.7] Verified 10 focused tie-change writer tests, plugin build and build:check, 26 performance tests, docs inventory and docs:check (447 passed, 1 skipped), and plugin sync. test:unit has 24 requirement/drawer vector failures reproduced with the clean base bundle; recorded as PROPOSED FOLLOW-UP. Epic symbols are clear.

## Dependencies

- **Depends on:** [bob-cli-q8.2](bob-cli-q8.2.md) ✓ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q8.6](bob-cli-q8.6.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q8.8](bob-cli-q8.8.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.7/README.md) | [bob-cli-q8.7](bob-cli-q8.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`01dee47`](https://github.com/bobs-org/bob-cli/commit/01dee47a01b6b24aa35175370d50bbe7b5fd779c) | docs(tasks): document tie conversion writes | [bob-cli-q8.7](bob-cli-q8.7.md) | 2026-11-25 23:33:24 EST |
