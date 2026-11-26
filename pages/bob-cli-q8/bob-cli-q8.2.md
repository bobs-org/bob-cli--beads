# Bead: bob-cli-q8.2 — Reconcile fold and merge pruning

[Bead Pages](../README.md) / [bob-cli-q8](README.md) / bob-cli-q8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6f.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6f.linker.w0.md) · **Assignee:** `bob-cli-q8.2` · **Size:** medium
**Created:** 2026-11-25 18:16:42 EST · **Closed:** 2026-11-25 20:43:03 EST
**Plan:** [202611/plain\_link\_dependency\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/plain_link_dependency_ties.md)

## Description

reconcile-fold: bob task reconcile drops plain LINKS entries on dependency-joined pairs and reports absorbed_plain_links. bob task merge prunes the overlaps its repointing would create. Dry-run the fold against the live vault without applying it.

## Notes

[2026-11-26T01:41:42Z · bob-cli-q8.2] PROPOSED FOLLOW-UP: Refresh the clean bob-plugins docs inventory: its generator reports stale docs/bob-ledger-tools.md and docs/index.md, and bob-docs check reproduces the same generated-drift failure. This is already tracked by bob-cli-q8.4; it is outside q8.2 scope.

[2026-11-26T01:43:03Z · bob-cli-q8.2] Implemented reconcile plain-link folding, merge pruning, absorbed_plain_links JSON/human reports, LR27-LR35 and MG21 coverage, docs, and the authorized Task Relation glossary update. Verified cargo check, focused relation tests (35/35), MG21 (1/1), reconcile drift tests (15/15), cargo fmt --check, git diff --check, and the read-only live-vault dry run (ok=true; one row at bob.md:59; no writes). docs-check passes lint and reports only clean-base bob-plugins generated inventory drift, noted on this bead with existing tracking bob-cli-q8.4. epic-symbols found no leftovers.

## Dependencies

- **Depends on:** [bob-cli-q8.1](bob-cli-q8.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q8.7](bob-cli-q8.7.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.2/README.md) | [bob-cli-q8.2](bob-cli-q8.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5d08882`](https://github.com/bobs-org/bob-cli/commit/5d088829b3f9cfb397aea7852d7be147d76b8b77) | feat(task-relations): fold dependency overlaps during reconcile and merge | [bob-cli-q8.2](bob-cli-q8.2.md) | 2026-11-25 20:45:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q8.2][1] | Need the phase scope, design file, prior notes, and governing epic decisions before implementation | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.2/README.md

<!-- sase:referenced-by:end -->
