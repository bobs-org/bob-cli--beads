# Bead: bob-cli-im.2 — Trailing \`+\` after bare names is timing; \`#\` spells names ending in \`+\`

[Bead Pages](../README.md) / [bob-cli-im](README.md) / bob-cli-im.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5x.linker.w0.md) · **Assignee:** `bob-cli-im.2` · **Size:** medium
**Created:** 2026-11-08 05:50:21 EST · **Closed:** 2026-11-08 08:28:06 EST
**Plan:** [202611/start\_timing\_later\_offset.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/start_timing_later_offset.md)

## Description

bare_plus: a bare start name now ends at its last byte that is neither a digit nor `+`, so `=fix2+`, `=fix+3`, `=bugs+2`, and `@foo:bar=fix2+` are timing while `=bob+decks` and `=bob+2fa` are unchanged. Refuse `=c++`/`=fix++` with a three-way hint, make `=#c++` legal, teach `x=fix+`, keep timing in completion round trips, emit trailing timing in bare-name fit drafts, fix the stale `=bugs+2` docs, add the differential test, bump the grammar revision, and record decisions:start-timing-is-signed.

## Notes

[2026-11-08T12:59:56Z · bob-cli-im.2--1] PROPOSED FOLLOW-UP: native::gmail::sync::guard::tests::real_lock_contention_and_release failed once under just check ("release frees the guard") and passed in isolation; likely a suite-load flock flake on the new gmail sync guard, unrelated to grammar 18.

[2026-11-08T13:28:06Z · bob-cli-im.2--2] Closed by explicit `sase stitch create -B close` after create_commit landed b4163548 ("feat(capture): treat trailing plus after a bare start name as later timing"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-im.2` if more work remains.

## Dependencies

- **Depends on:** [bob-cli-im.1](bob-cli-im.1.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-im.3](bob-cli-im.3.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-im.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-im.2.md) | [bob-cli-im.2](bob-cli-im.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b416354`](https://github.com/bobs-org/bob-cli/commit/b4163548b5025573256ad2a9ec5fdedbb526cd53) | feat(capture): treat trailing plus after a bare start name as later timing | [bob-cli-im.2](bob-cli-im.2.md) | 2026-11-08 08:27:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-im.2--2][1] | Need current phase status, notes, and remaining work after green just check | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-im.2.md

<!-- sase:referenced-by:end -->
