# Bead: bob-cli-no.1 — bob expands ~ and glob patterns in bank import FILE operands

[Bead Pages](../README.md) / [bob-cli-no](README.md) / bob-cli-no.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5j.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5j.linker.w0.md) · **Assignee:** `bob-cli-no.1` · **Size:** medium
**Created:** 2026-11-19 14:47:06 EST · **Closed:** 2026-11-19 15:47:27 EST
**Plan:** [202611/bank\_import\_delete.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_import_delete.md)

## Description

expand: add a shared native::host_paths operand expander (tilde, literal-first glob, dedupe, no-match refusal) and adopt it in bob bank import. Also light up the "bank" Command Mode invalidation tag, filter completion to exports, add a macOS privacy hint for unreadable files, and document file patterns.

## Notes

[2026-11-19T20:46:38Z · bob-cli-no.1] PROPOSED FOLLOW-UP: use host_paths::expand_operands for bob attachments import and bob ref create — those host-file operands still need Command Mode tilde and glob expansion.

[2026-11-19T20:46:53Z · bob-cli-no.1] PROPOSED FOLLOW-UP: repair the clean-base library failures — catalog public-leaf coverage, periods update completion decisions, and ordered intention planning each fail on HEAD, so just check remains red.

[2026-11-19T20:47:01Z · bob-cli-no.1] PROPOSED FOLLOW-UP: repair the clean-base docs mount collision — the bob-plugins source ships reference/plugins/index.md alongside the committed landing page, so just docs-check remains red.

[2026-11-19T20:47:27Z · bob-cli-no.1] Implemented shared native host-path tilde/glob expansion and wired bank import, invalidation, completions, privacy diagnostics, tests, and docs. Verified 12 helper tests, 25 bank CLI tests, docs generation, formatting/Clippy, and 3,842 CLI tests. Full library suite has three failures reproduced on clean base; docs-check mount collision also reproduced on clean base. Epic symbols were empty.

## Dependencies

- **Blocks:** [bob-cli-no.2](bob-cli-no.2.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-no.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-no.1/README.md) | [bob-cli-no.1](bob-cli-no.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5b547f1`](https://github.com/bobs-org/bob-cli/commit/5b547f13c87a93b56271aecc159c164642eab7ce) | feat(bank): expand import file operands | [bob-cli-no.1](bob-cli-no.1.md) | 2026-11-19 15:49:47 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-no.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-no.1/README.md

<!-- sase:referenced-by:end -->
