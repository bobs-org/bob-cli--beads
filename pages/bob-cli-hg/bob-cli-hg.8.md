# Bead: bob-cli-hg.8 — Capture recognizes Gmail URLs and links them after submit

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.8` · **Size:** medium
**Created:** 2026-11-05 12:37:49 EST · **Closed:** 2026-11-06 10:47:01 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

capture-gmail: add the gmail_url capture-parse span and dry-run preview data, link already-saved threads offline at submit, and kick a detached single-flight `bob gmail link` worker after commit, with the grammar and docs updated.

## Notes

[2026-11-06T15:18:19Z · bob-cli-hg.8] Implemented Gmail capture spans and offline preview/saved-link substitution (grammar 16), post-commit scoped single-flight worker queue, login/logout local receipts for a zero-gog capture gate, docs and regression tests. Earlier Gmail linker landed at f075147f; no prior phase implementation existed. Verified cargo test --lib gmail::worker: 3 passed; git diff --check clean; epic-symbols reports none. Remaining work fits one coder: run new CLI regressions, regenerate docs, run docs-check and just check, repair any failures, then close only bob-cli-hg.8. No memory edited.

[2026-11-06T15:36:48Z · bob-cli-hg.8--1] PROPOSED FOLLOW-UP: pre-existing docs README snapshot failure, tracked by bob-cli-hs — just docs-check passed lint, generated drift, strict build, URLs, offline links, edit links, search, tutorial, and media; Python suite ended 446 passed, 1 skipped, 1 failed at test_readme_table_matches_original_contract_index_snapshot. Reproduced that exact test on an untouched git archive of base f075147f with its own tools/docs on PYTHONPATH: actual SHA256 96a429d5f5b7eb02484e4806dac0ca688e41858e3187dfbdb26ad994a6107e4a, expected fedc20a035e78ecfd201ce2462d2eccb1683046f66c749477949287aade4fe72, identical to the phase tree. Both docs/README.md and the test are unchanged by this phase.

[2026-11-06T15:47:01Z · bob-cli-hg.8--1] Implemented grammar 16 Gmail spans and offline per-item previews, saved-thread link substitution within capture transactions, and scoped post-commit single-flight linking with queue, login receipt, disable/writer gates, tests, and docs. Reviewed offline isolation and queue races. Fixed documentation lint/navigation/budget errors and redundant-closure Clippy failure. Full sase tool run check passed (7ab517825ea87f4ea60eff87c276fd91): formatting, Clippy, 5401 library tests, 3268 CLI tests, and every other integration/doctest target. The five Gmail capture and three worker tests pass. just docs-gen passed and generated changes were inspected. just docs-check passed every stage except the unchanged README snapshot test; clean-base reproduction and existing tracker bob-cli-hs are recorded in the PROPOSED FOLLOW-UP note (446 docs tests passed, 1 skipped). git diff --check clean; epic-symbols reports no entries. No real Gmail/vault use and no memory edits.

## Dependencies

- **Blocks:** [bob-cli-hg.11](bob-cli-hg.11.md) ◐ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.7](bob-cli-hg.7.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.8.md) | [bob-cli-hg.8](bob-cli-hg.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e096004`](https://github.com/bobs-org/bob-cli/commit/e0960045bf86d88f7f2443b746a7ef48c4643245) | feat(gmail): link captured Gmail URLs without blocking capture | [bob-cli-hg.8](bob-cli-hg.8.md) | 2026-11-06 10:48:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.5s.grk][1] | Need remaining Gmail phase user-facing scopes for the guide | 1 |
| read-by | [agent:research.5s.mus][2] | gmail user guide research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.grk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.mus/README.md

<!-- sase:referenced-by:end -->
