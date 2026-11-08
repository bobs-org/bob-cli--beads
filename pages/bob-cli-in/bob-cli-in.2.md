# Bead: bob-cli-in.2 — Host-local, idempotent commit and journal recovery

[Bead Pages](../README.md) / [bob-cli-in](README.md) / bob-cli-in.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19v.md) · **Assignee:** `bob-cli-in.2` · **Size:** medium
**Created:** 2026-11-08 06:23:52 EST
**Plan:** [202611/gmail\_sync\_ii3\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_ii3_completion.md)

## Description

recovery: move the sync recovery evidence to host-local state, make its replay idempotent per event and ownership-checked per path, stop writing auxiliary files on runs that save no note, keep in-flight filings from being filed twice, and add the temporary-Git-vault recovery tests.

## Dependencies

- **Depends on:** [bob-cli-in.1](bob-cli-in.1.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-in.3](bob-cli-in.3.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-in.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-in.2/README.md) | [bob-cli-in.2](bob-cli-in.2.md) | 0 |
