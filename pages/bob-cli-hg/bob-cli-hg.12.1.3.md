# Bead: bob-cli-hg.12.1.3 — Draft transport, persistence, and exact preview

[Bead Pages](../README.md) / [bob-cli-hg.12.1](bob-cli-hg.12.1.md) / bob-cli-hg.12.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.md) · **Assignee:** `bob-cli-hg.12.1.3` · **Size:** medium
**Created:** 2026-11-06 07:12:29 EST · **Closed:** 2026-11-06 12:15:40 EST
**Plan:** [202611/gmail\_compose.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_compose.md)

## Description

gmail-drafts: implement remote create/update/readback, compose scope checks, durable identity, and canonical preview/digest without exposing send; see section 4.3.

## Notes

[2026-11-06T16:27:40Z · bob-cli-hg.12.1.3] PROPOSED FOLLOW-UP: Repair the pre-existing docs contract snapshot mismatch: test_readme_table_matches_original_contract_index_snapshot expects a different hash than the unchanged docs/README.md table.

[2026-11-06T17:15:40Z · bob-cli-hg.12.1.3--3] Verified just check passed, including all 5 gmail_draft tests. just docs-check passed lint, generated drift, strict build, links, tutorial, and media; docs tests had 446 passed, 1 skipped, and only the pre-existing README contract-table snapshot hash mismatch already recorded as a PROPOSED FOLLOW-UP. Epic symbols: none.

## Dependencies

- **Depends on:** [bob-cli-hg.12.1.2](bob-cli-hg.12.1.2.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hg.12.1.4](bob-cli-hg.12.1.4.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.12.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.1.3.md) | [bob-cli-hg.12.1.3](bob-cli-hg.12.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b6a9624`](https://github.com/bobs-org/bob-cli/commit/b6a962435aa73b8a06d1fe654ebcf1f58caa3658) | feat(gmail): add safe draft create and update flow | [bob-cli-hg.12.1.3](bob-cli-hg.12.1.3.md) | 2026-11-06 12:41:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.12.1.3--3][1] | Need the latest phase notes, scope, and verification record before closing | 1 |
| read-by | [agent:bob-cli-hg.12.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.1.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.land/README.md

<!-- sase:referenced-by:end -->
