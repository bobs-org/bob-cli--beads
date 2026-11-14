# Bead: bob-cli-lk.2 — Line-shift-proof archive confirmation identity

[Bead Pages](../README.md) / [bob-cli-lk](README.md) / bob-cli-lk.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e1.md) · **Assignee:** `bob-cli-lk.2` · **Size:** small
**Created:** 2026-11-14 11:42:09 EST · **Closed:** 2026-11-14 14:18:52 EST
**Plan:** [202611/gmail\_archive\_merge\_and\_reply\_reopen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_merge_and_reply_reopen.md)

## Description

digest-identity: the -c digest and fresh_matches_close match tasks by block id or row-text hash instead of line number, with DIGEST_VERSION 2 and tolerant parsing of legacy locators. It also notes the fix on bob-cli-kx.

## Notes

[2026-11-14T19:18:52Z · bob-cli-lk.2] Implemented DIGEST_VERSION 2 with line-independent block-ID/row-hash task identity; retained line fallback for legacy hashless locators. Verified targeted archive tests, full library and CLI tests, Gmail archive integration tests, formatting, and a green rerun of just check. Recorded the digest resolution on bob-cli-kx.

## Dependencies

- **Depends on:** [bob-cli-lk.1](bob-cli-lk.1.md) ✓ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lk.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.2/README.md) | [bob-cli-lk.2](bob-cli-lk.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7ffc825`](https://github.com/bobs-org/bob-cli/commit/7ffc8251782f87288e97421fd3b63058e5332f91) | fix(gmail): make archive confirmation line-shift proof | [bob-cli-lk.2](bob-cli-lk.2.md) | 2026-11-14 14:22:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lk.2][1] | Need the phase scope, prior notes, epic decisions, and design file before implementing | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.2/README.md

<!-- sase:referenced-by:end -->
