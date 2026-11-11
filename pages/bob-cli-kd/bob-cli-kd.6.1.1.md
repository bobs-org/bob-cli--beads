# Bead: bob-cli-kd.6.1.1 — Bank JSON data service and shared presentation models

[Bead Pages](../README.md) / [bob-cli-kd.6.1](bob-cli-kd.6.1.md) / bob-cli-kd.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kd.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.6.md) · **Assignee:** `bob-cli-kd.6.1.1` · **Size:** medium
**Created:** 2026-11-11 14:27:33 EST · **Closed:** 2026-11-11 14:56:09 EST
**Plan:** [202611/bank\_obsidian.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_obsidian.md)

## Description

bank-ui-data: implement the bank JSON boundary, cached reads, invalidation, source-location helpers, and synthetic fixtures in bob-plugins. Follow the bank-ui-data section.

## Notes

[2026-11-11T19:55:58Z · bob-cli-kd.6.1.1] PROPOSED FOLLOW-UP: bob plugins sync on this host fails for every plugin before copy — bob 0.5.0 git check-ignore rejects --literal-pathspecs (pathspec magic not supported: literal); workspace bob-cli already adds --no-literal-pathspecs. Vault deploy of the bank data service waits on that CLI landing. Reproduced with --repo this checkout -p bob-ledger-tools and with the default repo (10 plugins, 0 copied).

[2026-11-11T19:56:09Z · bob-cli-kd.6.1.1] Bank JSON data service landed in bob-plugins: decode/source/data fragments, synthetic fixtures, argv/cache/invalidation/source-span tests (28 pass), command-mode bank tag, additive api.bank v1. npm run build, build:check, and docs:inventory:check pass. bob plugins sync did not copy (pre-existing bob 0.5.0 git check-ignore literal-pathspecs failure; recorded as PROPOSED FOLLOW-UP).

## Dependencies

- **Blocks:** [bob-cli-kd.6.1.2](bob-cli-kd.6.1.2.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.1/README.md) | [bob-cli-kd.6.1.1](bob-cli-kd.6.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.6.1.1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.1/README.md

<!-- sase:referenced-by:end -->
