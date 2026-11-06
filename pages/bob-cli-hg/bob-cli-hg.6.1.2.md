# Bead: bob-cli-hg.6.1.2 — Prepare inert messages and local inline image imports

[Bead Pages](../README.md) / [bob-cli-hg.6.1](bob-cli-hg.6.1.md) / bob-cli-hg.6.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.md) · **Assignee:** `bob-cli-hg.6.1.2` · **Size:** medium
**Created:** 2026-11-05 23:47:35 EST · **Closed:** 2026-11-06 02:34:23 EST
**Plan:** [202611/gmail\_save\_list.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_save_list.md)

## Description

prepare-content: implement in-memory attachment-body hydration through gog's narrowly allowed Discovery read, headers mode, and CID image planning with size caps, hash deduplication, logo suppression, safe paths, and trusted resized embeds. Return prepared content and binary imports without writing.

## Notes

[2026-11-06T07:31:15Z · bob-cli-hg.6.1.2] PROPOSED FOLLOW-UP: clean-base lib failures outside the prepare-content diff: native::catalog public_leaves_are_entries_or_excluded and native::completion every_table_entry_matches_the_tree fail identically with changes stashed (verified this turn); tracked by bob-cli-hp per 6.1.1 notes.

[2026-11-06T07:31:23Z · bob-cli-hg.6.1.2] PROPOSED FOLLOW-UP: clean-base CLI failures outside the prepare-content diff: catalog protocol_1 73-vs-72 and root-help snapshot fail identically with changes stashed (verified this turn); catalog tracked by bob-cli-de per 6.1.1 notes.

[2026-11-06T07:31:28Z · bob-cli-hg.6.1.2] PROPOSED FOLLOW-UP: docs-check test_readme_table_matches_original_contract_index_snapshot fails identically with changes stashed (verified this turn, no known tracker); docs/gmail.md allowlist touch-up in this phase is unrelated to that README table hash.

[2026-11-06T07:34:23Z · bob-cli-hg.6.1.2] prepare-content done: Discovery attachment_bytes via api call attachments.get with serialized params, readonly scope, no-cache and api.call allowlist (fake gog models exact argv and forbids gmail attachment); two-pass hydration fails on remaining needs or transport errors; headers mode zero-fetch with prose stripped; CID planning with 2MiB cap both sides, sha256 dedup, <4KiB cross-message logo suppression, sanitized img/mail/<hex> paths, exact ![[...|400]] embeds, ID-only origin locators. Verified: 147 gmail lib tests incl 15 new prepare + 4 new transport tests pass, 10 gmail shell tests pass, fmt+lint clean; 2 lib, 2 CLI-subset, and 1 docs-check failures reproduce identically on clean base and are recorded as follow-ups.

## Dependencies

- **Depends on:** [bob-cli-hg.6.1.1](bob-cli-hg.6.1.1.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.6.1.3](bob-cli-hg.6.1.3.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.6.1.2/README.md) | [bob-cli-hg.6.1.2](bob-cli-hg.6.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c0d877b`](https://github.com/bobs-org/bob-cli/commit/c0d877be16030b2d2527af869d47dbf845dbe35a) | feat(gmail): prepare thread with attachment\_bytes transport | [bob-cli-hg.6.1.2](bob-cli-hg.6.1.2.md) | 2026-11-06 02:35:56 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.6.1.2][1] | full scope | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.6.1.2/README.md

<!-- sase:referenced-by:end -->
