# Bead: bob-cli-lk.1 — Follow merge edges and surface remaining holds

[Bead Pages](../README.md) / [bob-cli-lk](README.md) / bob-cli-lk.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e1.md) · **Assignee:** `bob-cli-lk.1` · **Size:** medium
**Created:** 2026-11-14 11:42:09 EST · **Closed:** 2026-11-14 13:33:04 EST
**Plan:** [202611/gmail\_archive\_merge\_and\_reply\_reopen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_merge_and_reply_reopen.md)

## Description

merge-follow: resolve each merged-into source to its target task through the shared relation resolver. Archive evidence then uses those effective linkers. Section tombstones count as closed. Unresolved merges and unknown statuses become alert-once archive[] review rows plus a doctor count.

## Notes

[2026-11-14T18:31:51Z · bob-cli-lk.1] Held-reason audit: review rows cover merge_unresolved, unknown, and silent-persistent identity. watching/not_enrolled/incoming_move stay out of review. incomplete/unsafe already doctor/warn. fetch_failed/unresolvable already warn+fail.

[2026-11-14T18:32:08Z · bob-cli-lk.1] PROPOSED FOLLOW-UP: just docs-check fails identically on clean base — mount bob-plugins -> reference/plugins ships index.md, colliding with committed docs/reference/plugins/index.md

[2026-11-14T18:32:26Z · bob-cli-lk.1] PROPOSED FOLLOW-UP: CLI test capture::complete_themes::configured_shell_describes_never_used_and_unconfigured_create fails on clean base at tests/cli/capture/complete_themes.rs:308 (empty stdout)

[2026-11-14T18:32:41Z · bob-cli-lk.1] PROPOSED FOLLOW-UP: CLI test articles::article_note_completion_shows_section_count flaked empty completion in the parallel just check suite; isolated pass on dirty tree and clean base

[2026-11-14T18:33:04Z · bob-cli-lk.1] Merge-follow implemented: follow merged-into via shared relation resolver (depth 8); section tombstones ClosedPositive; unresolved → merge_unresolved review rows (unknown + silent identity too). Alert-once via archive_review_seen/archive_review_count; doctor reports N held for review. Lib + gmail archive/sync integration tests pass; fmt/clippy green; just docs-gen green. just check two CLI failures: theme test fails on clean base; article completion flaked (isolated pass). just docs-check bob-plugins index.md collision on clean base. No Gmail writes; no --epic-symbol leftovers. Held-reason: review=merge_unresolved|unknown|identity.

## Dependencies

- **Blocks:** [bob-cli-lk.2](bob-cli-lk.2.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-lk.3](bob-cli-lk.3.md) ◐ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lk.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.1/README.md) | [bob-cli-lk.1](bob-cli-lk.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`47fac4b`](https://github.com/bobs-org/bob-cli/commit/47fac4b0ff0fe82fb1396e949d217fc8e2b3af2f) | feat(gmail): follow merge edges and surface remaining archive holds | [bob-cli-lk.1](bob-cli-lk.1.md) | 2026-11-14 13:35:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lk.1][1] | Need the phase scope, design file, notes, and DECISIONS | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.1/README.md

<!-- sase:referenced-by:end -->
