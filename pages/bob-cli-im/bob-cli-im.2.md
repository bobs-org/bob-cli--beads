# Bead: bob-cli-im.2 — Trailing \`+\` after bare names is timing; \`#\` spells names ending in \`+\`

[Bead Pages](../README.md) / [bob-cli-im](README.md) / bob-cli-im.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5x.linker.w0.md) · **Assignee:** `bob-cli-im.2` · **Size:** medium
**Created:** 2026-11-08 05:50:21 EST
**Plan:** [202611/start\_timing\_later\_offset.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/start_timing_later_offset.md)

## Description

bare_plus: a bare start name now ends at its last byte that is neither a digit nor `+`, so `=fix2+`, `=fix+3`, `=bugs+2`, and `@foo:bar=fix2+` are timing while `=bob+decks` and `=bob+2fa` are unchanged. Refuse `=c++`/`=fix++` with a three-way hint, make `=#c++` legal, teach `x=fix+`, keep timing in completion round trips, emit trailing timing in bare-name fit drafts, fix the stale `=bugs+2` docs, add the differential test, bump the grammar revision, and record decisions:start-timing-is-signed.

## Dependencies

- **Depends on:** [bob-cli-im.1](bob-cli-im.1.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-im.3](bob-cli-im.3.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-im.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-im.2/README.md) | [bob-cli-im.2](bob-cli-im.2.md) | 0 |
