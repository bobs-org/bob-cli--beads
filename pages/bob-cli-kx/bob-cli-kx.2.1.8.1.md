# Bead: bob-cli-kx.2.1.8.1 — Frozen IDs, receipt identity, and journal ownership

[Bead Pages](../README.md) / [bob-cli-kx.2.1.8](bob-cli-kx.2.1.8.md) / bob-cli-kx.2.1.8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.1.land.md) · **Assignee:** `bob-cli-kx.2.1.8.1` · **Size:** medium
**Created:** 2026-11-12 23:51:15 EST · **Closed:** 2026-11-13 01:02:06 EST
**Plan:** [202611/gmail\_archive\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_landing_repairs.md)

## Description

ownership: Make planning, apply, and recovery use the close's frozen saved IDs; record and match the real receipt label ID; re-baseline on an archive_label change; accept [?] in open observations; stop reopen/re-close false recoveries; surface cross-host holds; add real label-diff property tests. Implement section 1.

## Notes

[2026-11-13T06:02:06Z · bob-cli-kx.2.1.8.1--3] Verified: cargo fmt --all -- --check; just lint; cargo test --lib archive_ (137 passed); gmail_archive_apply (15), gmail_archive_preview (3), gmail_transport (4), gmail_sync (41), and gmail_shell (69) integration tests passed. epic-symbols reported no entries.

## Dependencies

- **Blocks:** [bob-cli-kx.2.1.8.2](bob-cli-kx.2.1.8.2.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2.1.8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.1.8.1.md) | [bob-cli-kx.2.1.8.1](bob-cli-kx.2.1.8.1.md) | 0 |
