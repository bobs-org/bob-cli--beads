# Bead: bob-cli-5x.1 — bob ref scan gains a JSON report and a writer lock

[Bead Pages](../README.md) / [bob-cli-5x](README.md) / bob-cli-5x.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z1.md) · **Assignee:** `bob-cli-5x.1` · **Size:** medium
**Created:** 2026-10-09 12:26:28 EDT
**Plan:** [202610/bob\_refs\_scan\_keymap.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_scan_keymap.md)

## Description

cli-scan-json: add `-f/--format human|json` to `bob ref scan` with a versioned envelope that names every created and updated note, a pure-JSON stdout (hook chatter goes to stderr), coded hard-failure envelopes, and an exclusive lock that serializes writing scans; document it and cover it with CLI tests.

## Dependencies

- **Blocks:** [bob-cli-5x.4](bob-cli-5x.4.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5x.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5x.1/README.md) | [bob-cli-5x.1](bob-cli-5x.1.md) | 0 |
