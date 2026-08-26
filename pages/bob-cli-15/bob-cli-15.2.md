# Bead: bob-cli-15.2 — Ephemeral cache reclamation on /

[Bead Pages](../README.md) / [bob-cli-15](README.md) / bob-cli-15.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0dy](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.0dy/README.md) · **Assignee:** `bob-cli-15.2` · **Size:** medium
**Created:** 2026-08-26 08:19:52 EDT · **Closed:** 2026-08-26 09:40:49 EDT
**Plan:** [202608/disk\_space\_reclamation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/disk_space_reclamation.md)

## Description

rootreclaim: purge regenerable caches and stale temp data on the root filesystem - Docker, APT archives, journald, /var/tmp, the uv cache, disabled snap revisions, and root's own caches.

## Notes

[2026-08-26T12:48:44Z · bob-cli-15.2] BLOCKED: Created confirmation gate custom-2509bf01-2ff3-403e-9b25-ffd9846981da for rootreclaim cleanup; it remained pending at 2026-08-26 08:47 EDT, so no destructive cleanup command was run and this phase was not closed.

[2026-08-26T12:48:45Z · bob-cli-15.2] PROPOSED FOLLOW-UP: Fix sase gate wait timeout cancellation - wait for custom-2509bf01-2ff3-403e-9b25-ffd9846981da exceeded gate_timeout_seconds and Ctrl-C showed cancel_gate blocked on .response.lock, leaving the gate pending.

[2026-08-26T13:28:27Z · bob-cli-15.2] BLOCKED: Created confirmation gate custom-e19c8d1e-93cc-4ed4-91d7-de6f578f524e for rootreclaim cleanup; it timed out with no selected option, so no destructive cleanup command was run and this phase was not closed.

[2026-08-26T13:40:49Z · bob-cli-15.2] Approved gate custom-18b515e9-ad74-4646-965b-93120c3271cd ran rootreclaim cleanup. Verified df -h / /mnt/hercules => / 466G used, 401G avail, 54%; /mnt/hercules 9.8T used, 528G avail, 95%. Verified APT cache 932K, root .cache/.npm 4K each, journald 391.8M with SystemMaxUse=500M drop-in, Prometheus retention 30d, snap disabled revisions removed and refresh.retain=2, Docker build cache/local volumes 0B, uv cache prune completed with 5.4G remaining in-use cache, /var/tmp 30d tmpfiles rule present with only 4K supervisor older than 30d.

## Dependencies

- **Blocks:** [bob-cli-15.7](bob-cli-15.7.md) ✓ · ⧖ 2026-08-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-15.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-15.2/README.md) | [bob-cli-15.2](bob-cli-15.2.md) | 0 |
