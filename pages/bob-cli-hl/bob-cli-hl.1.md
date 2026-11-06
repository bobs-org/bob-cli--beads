# Bead: bob-cli-hl.1 — Contract and docs

[Bead Pages](../README.md) / [bob-cli-hl](README.md) / bob-cli-hl.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.190](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.190.md) · **Assignee:** `bob-cli-hl.1` · **Size:** medium
**Created:** 2026-11-05 18:05:39 EST · **Closed:** 2026-11-05 18:17:08 EST
**Plan:** [202611/capture\_merge\_in\_arrow.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_arrow.md)

## Description

contract: write the `<` contract into docs/capture.md, the capture-syntax reference, task-merge.md, and task-relations.md, with MI vectors and search-smoke rows, marked contract-only.

## Notes

[2026-11-05T23:17:01Z · bob-cli-hl.1] PROPOSED FOLLOW-UP: docs-check lint reports 4 undocumented BOB_GMAIL_* env names (BOB_GMAIL_GOG/BROWSER/ASSUME_TTY/CONSENT_SECS in src/native/google/profile.rs); reproduces identically on clean HEAD via bob-docs lint, unrelated to contract docs

[2026-11-05T23:17:08Z · bob-cli-hl.1] Contract docs written: capture.md merge-in section with claim/context tables, codes, rewrite, editor/JSON/shell contracts plus TOC and grammar rows; capture-syntax token row plus minimal merge-in section; search_smoke query for T < @a+x @b+y; json-outputs additive keys; task-merge intro/section8/target.created/copy rows plus MI1-MI18 index; task-relations ML3 row and ML6 equivalence; glossary task-merge lists capture < via authorized memory edit. Verified: test_capture_token_coverage 2 passed, test_search_smoke 8 passed, bob-docs lint shows only 4 pre-existing BOB_GMAIL env errors identical on clean HEAD, reference budgets back under cap (5999/6000 and 6000/6000), epic-symbols clean.

## Dependencies

- **Blocks:** [bob-cli-hl.2](bob-cli-hl.2.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.1/README.md) | [bob-cli-hl.1](bob-cli-hl.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d9e3535`](https://github.com/bobs-org/bob-cli/commit/d9e353595582c3d1c647a1682d241b386fb2a2e0) | docs(capture): contract for merge-in \< capture | [bob-cli-hl.1](bob-cli-hl.1.md) | 2026-11-05 18:18:15 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.1][1] | Check notes for prior work | 3 |
| read-by | [agent:bob-cli-hn.1][2] | Confirm whether the existing documentation-lint issue tracks the docs-check failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.1/README.md

<!-- sase:referenced-by:end -->
