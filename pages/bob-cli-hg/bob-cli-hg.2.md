# Bead: bob-cli-hg.2 — Offline Gmail URL parser, token decoder, and text scanner

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.2` · **Size:** small
**Created:** 2026-11-05 12:37:49 EST · **Closed:** 2026-11-05 13:23:13 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

gmail-ids: pure parsing of every Gmail URL form, the base-40 token decode to API ids, refusal of compose/chat links, and a scanner that finds Gmail URLs (with their wrappers) in Markdown outside code.

## Notes

[2026-11-05T18:23:01Z · bob-cli-hg.2] PROPOSED FOLLOW-UP: just check gate fails identically on clean base tree (rustfmt drift in src/native/plan_budget/mod.rs and src/native/task_status_hooks/sync.rs; clippy collapsible_if at sync.rs:1620 under toolchain 1.95.0) — needs a dedicated format/lint refresh bead, unrelated to gmail-ids

[2026-11-05T18:23:13Z · bob-cli-hg.2] gmail-ids done: src/native/gmail/ids.rs + mod.rs with parse_gmail_url/decode_token/thread_date_hint/canonical_url/find_gmail_urls and 7 unit tests, all passing; module registered in src/native.rs with dead-code allow; my files are rustfmt- and clippy-clean; full just check blocked only by pre-existing base-tree fmt/clippy drift (recorded as PROPOSED FOLLOW-UP)

## Dependencies

- **Blocks:** [bob-cli-hg.6](bob-cli-hg.6.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.2/README.md) | [bob-cli-hg.2](bob-cli-hg.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4a2b7f5`](https://github.com/bobs-org/bob-cli/commit/4a2b7f50204ceec907bec7ec1f74a9ad2582bd51) | feat(gmail): add offline Gmail URL identity parsing | [bob-cli-hg.2](bob-cli-hg.2.md) | 2026-11-05 13:25:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.2][1] | check full description | 2 |
| read-by | [agent:bob-cli-hg.3.1.1][2] | Check whether the prior Gmail phase recorded the same clean-base rustfmt failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.1/README.md

<!-- sase:referenced-by:end -->
