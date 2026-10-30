# Bead: bob-cli-e6.4 — plan.default\_type and canonical types config

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.4` · **Size:** medium
**Created:** 2026-10-29 16:16:33 EDT · **Closed:** 2026-10-29 18:59:43 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

default-type: add plan.default_type as the last cascade step, accept types: and plan.reading_type as canonical config keys, resolve new captures from the staged line, and set CHORE in chezmoi.

## Notes

[2026-10-29T22:59:26Z · bob-cli-e6.4--1] PROPOSED FOLLOW-UP: Refresh 12 bob-obsidian CLI assertions that fail on clean HEAD — Clean-base `cargo test -p bob-obsidian --lib --test cli` passes 3921 library tests (1 ignored), while 12 CLI tests fail identically to the full check: stale theme wording/field assertions plus the themes-split catalog alias expectation. These are present before bob-cli-e6.4 changes.

[2026-10-29T22:59:43Z · bob-cli-e6.4--1] Implemented the default type cascade, canonical types/reading_type config keys, staged-line resolution, default-type lint, docs, and CHORE in chezmoi. Config parser tests passed (12/12) and the staged-field capture test passed. The full check still reports 12 CLI failures reproduced on clean HEAD; recorded as PROPOSED FOLLOW-UP. No epic symbols remained.

## Dependencies

- **Depends on:** [bob-cli-e6.2](bob-cli-e6.2.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e6.5](bob-cli-e6.5.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-e6.4.md) | [bob-cli-e6.4](bob-cli-e6.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`66ddba9`](https://github.com/bobs-org/bob-cli/commit/66ddba93b03804bc07abd581ef7cb22ccd35d984) | feat(config): add global default task type | [bob-cli-e6.4](bob-cli-e6.4.md) | 2026-10-29 19:01:21 EDT |
| chezmoi | [`chezmoi@5389ff9`](https://github.com/bbugyi200/dotfiles/commit/5389ff9f34e4eb035c8d32a730e73fb90bc39cf8) | feat(bob-config): set CHORE as default task type | [bob-cli-e6.4](bob-cli-e6.4.md) | 2026-10-29 19:03:36 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.4--1][1] | Check whether an earlier phase agent left remaining work in notes | 2 |
| read-by | [agent:bob-cli-e6.8][2] | check whether default-type deferred chezmoi default_type to js-mirror | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-e6.4.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.8/README.md

<!-- sase:referenced-by:end -->
