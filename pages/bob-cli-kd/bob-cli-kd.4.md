# Bead: bob-cli-kd.4 — Weekly QFX import that writes only what you missed

[Bead Pages](../README.md) / [bob-cli-kd](README.md) / bob-cli-kd.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1be.md) · **Assignee:** `bob-cli-kd.4` · **Size:** large
**Created:** 2026-11-11 11:24:16 EST
**Plan:** [202611/bank\_daily\_acknowledgment.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md)

## Description

bank-import: parse Wells Fargo QFX (OFX 1.x SGML and 2.x XML) plus one CSV profile; resolve accounts without numbers; journal hashed identities per host; match typed rows; name rows from rules, learned payees, and restaurant records; write unchecked rows in one guarded, committed transaction with an exact dry run; add the weekly PRE chore.

## Dependencies

- **Depends on:** [bob-cli-kd.3](bob-cli-kd.3.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-kd.5](bob-cli-kd.5.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.md) | [bob-cli-kd.4](bob-cli-kd.4.md) | 0 |
