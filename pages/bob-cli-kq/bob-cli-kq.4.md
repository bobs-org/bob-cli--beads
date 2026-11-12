# Bead: bob-cli-kq.4 — Durable and race-free vault writes

[Bead Pages](../README.md) / [bob-cli-kq](README.md) / bob-cli-kq.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bo](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bo.md) · **Assignee:** `bob-cli-kq.4` · **Size:** medium
**Created:** 2026-11-12 05:24:40 EST
**Plan:** [202611/security\_audit\_fixes\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes_1.md)

## Description

durable-vault-writes: bind bank ensure's write-guard preimage to its single planning snapshot, install clip attachments via hard_link/create_new, fsync the three non-flushing atomic_write variants and the gkeep token write, and verify ownership of the shared-tmp script-cache fallback.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kq.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kq.4/README.md) | [bob-cli-kq.4](bob-cli-kq.4.md) | 0 |
