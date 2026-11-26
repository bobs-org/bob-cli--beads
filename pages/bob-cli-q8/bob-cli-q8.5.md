# Bead: bob-cli-q8.5 — Nav tie planner, mirrored vectors, and absorption in the dependency writers

[Bead Pages](../README.md) / [bob-cli-q8](README.md) / bob-cli-q8.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6f.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6f.linker.w0.md) · **Assignee:** `bob-cli-q8.5` · **Size:** medium
**Created:** 2026-11-25 18:16:42 EST · **Closed:** 2026-11-25 21:19:45 EST
**Plan:** [202611/plain\_link\_dependency\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/plain_link_dependency_ties.md)

## Description

nav-tie-planner: add the pure JS twins and planTieChange in bob-navigation-hotkeys, pinned by mirrored PT vectors. Every existing nav dependency writer (Depends on, Blocks, counted, marked, api) then absorbs plain links.

## Notes

[2026-11-26T02:19:03Z · bob-cli-q8.5] PROPOSED FOLLOW-UP: writer-file suite red at HEAD from settle commit dbebfbd4 (bob-cli-q4.10.1.5); 19 tests in test-navigation-dependencies-writer.cjs fail with commit-failed including new DW20-22, plus 3 in task-settle-adapter/relation-complete files; all reproduce identically on the clean tree

[2026-11-26T02:19:20Z · bob-cli-q8.5] PROPOSED FOLLOW-UP: just docs-check mount collision pre-existing (bob-plugins index.md vs committed landing page, reproduces with docs changes stashed); plus 2 date-hardcoded cycler open-line failures (2026-11-25 vs today) and stale committed bob-ledger-tools bundle breaking npm run build:check

[2026-11-26T02:19:27Z · bob-cli-q8.5] PROPOSED FOLLOW-UP: vault bob-ledger-tools stamp is another running agent (bob-cli_10) uncommitted deploy; sync -F declined per deployment rule, bob-navigation-hotkeys deploys clean (up to date)

[2026-11-26T02:19:45Z · bob-cli-q8.5] Nav tie planner done: 087/088 fragments (dropPlainLinkEntries byte-exact on PT1-12, classifyPairTies on PT13-21, planTieChange with PT22-39 vectors incl. ctrl_shift_l=yes), absorption in applyDependencyEdit/applyBlocksEdit/same-note marked batches with merged BLOCKS+tie follow-ups, DW20-22 + RBP12-13 tests, docs §22/§6.6/§15.6 + validation.md, glossary one-liner, bob plugins sync current. Verified: 22/22 new tests, 138/138 across touched suites, 8208 lib tests, 33 ties tests. Writer-file DW red + docs-check/build:check failures reproduce identically on clean HEAD (upstream settle work) and are recorded as follow-ups.

## Dependencies

- **Depends on:** [bob-cli-q8.1](bob-cli-q8.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q8.6](bob-cli-q8.6.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.5/README.md) | [bob-cli-q8.5](bob-cli-q8.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f6e333d`](https://github.com/bobs-org/bob-cli/commit/f6e333d58ce52291831aa668ac094da37f5f6d62) | feat(relations): publish plain-link tie vectors PT22-39 and writer absorption contract | [bob-cli-q8.5](bob-cli-q8.5.md) | 2026-11-25 21:21:16 EST |
| bob-plugins | [`bob-plugins@9ee4822`](https://github.com/bobs-org/bob-plugins/commit/9ee4822981650324ce391015bfc8fa2b6aa9bba8) | feat(nav): tie planner twins, planTieChange, and absorption in dependency writers | [bob-cli-q8.5](bob-cli-q8.5.md) | 2026-11-25 21:22:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q8.5][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.5/README.md

<!-- sase:referenced-by:end -->
