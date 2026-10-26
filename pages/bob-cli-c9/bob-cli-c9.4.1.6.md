# Bead: bob-cli-c9.4.1.6 — Enable single-URL overwrite across web capture routes

[Bead Pages](../README.md) / [bob-cli-c9.4.1](bob-cli-c9.4.1.md) / bob-cli-c9.4.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.md) · **Assignee:** `bob-cli-c9.4.1.6` · **Size:** medium
**Created:** 2026-10-25 22:34:44 EDT · **Closed:** 2026-10-26 01:49:44 EDT
**Plan:** [202610/unannotated\_reference\_overwrite.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/unannotated_reference_overwrite.md)

## Description

web: connect article, saved-HTML, PDF-URL, and arXiv capture to the same staged overwrite transaction and preserve redirect, duplicate-before-fetch, and listen semantics.

## Notes

[2026-10-26T05:49:37Z · bob-cli-c9.4.1.6] PROPOSED FOLLOW-UP: lib test native::capture_related::tests::synthetic_vault_query_is_under_250ms failed once under full-suite load (250ms threshold) then passed solo and on full lib rerun (3531 passed); consider a flake task bead if it recurs

[2026-10-26T05:49:44Z · bob-cli-c9.4.1.6] Web overwrite done: article/saved-HTML (clip::capture_article_overwrite), PDF-URL (overwrite_pdf_url), and arXiv (overwrite_arxiv) now flow through the staged overwrite transaction with pre-fetch eligibility (no network for annotated/incompatible), post-fetch redirect validation (refuse_redirected_overwrite), locked recheck via executor, and preserved -L attach vs -f-overwrite-L narrate semantics; hidden clip alias shares create semantics. Triage allows filed URLs; collections still refuse. Verified: 9 new tests in tests/cli/highlights/overwrite_web.rs pass; repurposed create.rs filed-URL test and removed obsolete local unavailable test; cargo fmt clean, clippy gate clean, lib 3531 passed, cli binary 2159 passed, just docs-gen/docs-check passed.

## Dependencies

- **Depends on:** [bob-cli-c9.4.1.5](bob-cli-c9.4.1.5.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-c9.4.1.7](bob-cli-c9.4.1.7.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.4.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.6/README.md) | [bob-cli-c9.4.1.6](bob-cli-c9.4.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`57e74dc`](https://github.com/bobs-org/bob-cli/commit/57e74dcab9aa1432aea4bb0322d65fa270935148) | feat(highlights): enable single-URL overwrite across web capture routes | [bob-cli-c9.4.1.6](bob-cli-c9.4.1.6.md) | 2026-10-26 01:50:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.4.1.6][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.6/README.md

<!-- sase:referenced-by:end -->
