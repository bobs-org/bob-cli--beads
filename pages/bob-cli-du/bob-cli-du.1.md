# Bead: bob-cli-du.1 — Complete-label contract (§18), reverse-rename contract, inverse pairs, and shared vectors

[Bead Pages](../README.md) / [bob-cli-du](README.md) / bob-cli-du.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.aw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.aw.md) · **Assignee:** `bob-cli-du.1` · **Size:** medium
**Created:** 2026-10-28 14:49:53 EDT · **Closed:** 2026-10-28 15:11:51 EDT
**Plan:** [202610/relation\_complete\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_complete_labels.md)

## Description

complete-contract: write docs/task-relations.md §18 and RV10, amend §§1/2/8/10/13.2/14/15 and the capture, config, JSON, dependency, and project docs, add the two inverse pairs in Rust, and add tests/fixtures/relation_complete/vectors.json generated from the cycler's Done bytes.

## Notes

[2026-10-28T19:11:27Z · bob-cli-du.1] PROPOSED FOLLOW-UP: add Complete label to docs/reference/glossary.md at rollout — that page is generated from the glossary memory web, so this phase cannot add the term without a new strand; only glossary:task-relation is authorized, and that edit belongs to rollout.

[2026-10-28T19:11:51Z · bob-cli-du.1] Wrote docs/task-relations.md §18 (CP1–CP8) and RV10, amended §§1/2/6/8/10/13/14/15/17 CL2 and capture/config/JSON/dependency/project docs with offer_successors=yes. Added implemented by⇄implements and verified by⇄verifies to inverse_phrase plus catalog cases. Landed tests/fixtures/relation_complete/vectors.json (done generated from bob-plugins e395721 rewriteTaskLineForLocalFallback; rule/key/config hand-authored). just docs-check passed; relation_complete_vector_sections_exist and complete_task_tree_root_rewrite_matches_every_non_refused_done_case passed; inverse_phrases_match_the_contract_table and vector_catalogs_scan_every_scope passed. Glossary.md left to rollout (generated page).

## Dependencies

- **Blocks:** [bob-cli-du.2](bob-cli-du.2.md) ◐ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-du.5](bob-cli-du.5.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.1/README.md) | [bob-cli-du.1](bob-cli-du.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`847a3c5`](https://github.com/bobs-org/bob-cli/commit/847a3c5341ea70f00b4ca6f85c0d405cee8836fe) | feat(relations): add complete-label contract, reverse-rename, and shared vectors | [bob-cli-du.1](bob-cli-du.1.md) | 2026-10-28 15:13:07 EDT |
