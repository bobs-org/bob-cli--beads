# Bead: bob-cli-5x.3 — Scan lane in RefsLibrary and scan behavior in RefsPanelModel

[Bead Pages](../README.md) / [bob-cli-5x](README.md) / bob-cli-5x.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z1.md) · **Assignee:** `bob-cli-5x.3` · **Size:** medium
**Created:** 2026-10-09 12:26:29 EDT
**Plan:** [202610/bob\_refs\_scan\_keymap.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_scan_keymap.md)

## Description

refs-scan-service: run the scan on its own lane with a long timeout, defer watcher refreshes while it runs, publish the outcome only after a post-scan snapshot pass, then re-rank, select the first new reference, raise banners, and queue hidden notices in the panel model, with fake-bob coverage.

## Dependencies

- **Depends on:** [bob-cli-5x.2](bob-cli-5x.2.md) ◐ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5x.4](bob-cli-5x.4.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5x.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5x.3/README.md) | [bob-cli-5x.3](bob-cli-5x.3.md) | 0 |
