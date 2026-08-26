# Bead: bob-cli-15.1 — Emergency triage on /mnt/hercules

[Bead Pages](../README.md) / [bob-cli-15](README.md) / bob-cli-15.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0dy](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.0dy/README.md) · **Assignee:** `bob-cli-15.1` · **Size:** small
**Created:** 2026-08-26 08:19:52 EDT · **Closed:** 2026-08-26 09:36:07 EDT
**Plan:** [202608/disk\_space\_reclamation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/disk_space_reclamation.md)

## Description

triage: reclaim immediate headroom on the 100%-full RAID array by clearing interrupted-rotation leftovers and the oldest redundant backup rotations, without touching Plex media.

## Notes

[2026-08-26T13:36:07Z · bob-cli-15.1] Verified /mnt/hercules triage: approved gates deleted only stale home backup rotations yearly-4/yearly-3/yearly-2/monthly-4/monthly-3/monthly-2, no /mnt/hercules/plex paths touched; final df shows /mnt/hercules 11T size, 9.8T used, 528G avail, 95% used, and / 875G size, 467G used, 400G avail, 54% used; no active rsync/backup.sh/mnt-hercules rm after hourly completed; no dot-prefixed interrupted rotation leftovers under /mnt/hercules/backup; epic-symbols reported no entries. Recorded targeted sizes before second delete: yearly-2 46G, monthly-4 52G, monthly-3 54G, monthly-2 60G; broad per-rotation du was attempted twice but did not finish in a practical window.

## Dependencies

- **Blocks:** [bob-cli-15.5](bob-cli-15.5.md) ✓ · ⧖ 2026-08-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-15.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-15.1/README.md) | [bob-cli-15.1](bob-cli-15.1.md) | 0 |
