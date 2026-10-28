# Bead: bob-cli-dl.1 — Cancel-label contract (§17), config reference, and shared cancel vectors

[Bead Pages](../README.md) / [bob-cli-dl](README.md) / bob-cli-dl.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2r.linker.w0.md) · **Assignee:** `bob-cli-dl.1` · **Size:** medium
**Created:** 2026-10-28 08:15:26 EDT · **Closed:** 2026-10-28 08:35:31 EDT
**Plan:** [202610/relation\_cancel\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_cancel_labels.md)

## Description

cancel-contract: write docs/task-relations.md §17 Cancel labels (rule, config, source table, writes, verdicts, indication strings, JSON, refusal codes), amend §§2/8/13.2/14 and the hooks, capture, projects, configuration, json-outputs, and glossary docs, and commit tests/fixtures/task_cancel/vectors.json. The vectors' cancel and prune bytes are generated from nav's existing Task Card Cancel planners, and the rule, key, and config sections are hand-authored.

## Notes

[2026-10-28T12:35:31Z · bob-cli-dl.1] Wrote docs/task-relations.md §17 (CL1–CL8) and amended §§2/8/13.2/14/15 plus capture, projects, hooks, configuration, and json-outputs. just docs-check passed. tests/fixtures/task_cancel/vectors.json parses with cancel (15), prune (9), rule (34), key (10), and config (10); cargo test vectors_file_has_required_sections passed. cancel/prune bytes generated from bob-plugins 12d4c0e planTaskCancelBatch (reason empty) and planDeferredPomodoroLinkCleanup and match CL4 (cash.md upsert, no new Cancel Log, dedicated-bullet/token prune). glossary.md left generated: memory_glossary_term is no.

## Dependencies

- **Blocks:** [bob-cli-dl.2](bob-cli-dl.2.md) ◐ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dl.5](bob-cli-dl.5.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dl.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dl.1.md) | [bob-cli-dl.1](bob-cli-dl.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`52bff01`](https://github.com/bobs-org/bob-cli/commit/52bff0161befe3ce9656117547920caaf3129644) | feat(relations): add cancel-label contract, config docs, and shared vectors | [bob-cli-dl.1](bob-cli-dl.1.md) | 2026-10-28 09:03:56 EDT |
