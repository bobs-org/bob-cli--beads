# Bead: bob-cli-52.1 — Typed, non-printing URL ingest extracted from bob ref create

[Bead Pages](../README.md) / [bob-cli-52](README.md) / bob-cli-52.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.1` · **Size:** medium
**Created:** 2026-10-07 08:11:16 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

ingest: extract a typed URL ingest API from `ref create`. It returns created, already-in-library, and already-queued outcomes, or a typed error kind with a retryable flag. It uses fixed reading-queue defaults, a machine-wide ingest lock, and fsync on install. `ref create` output and exit codes stay byte-identical. Also add the shared ⚠️ fallback-note helper.

## Dependencies

- **Blocks:** [bob-cli-52.5](bob-cli-52.5.md) ◐ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.6](bob-cli-52.6.md) ◐ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.1/README.md) | [bob-cli-52.1](bob-cli-52.1.md) | 0 |
