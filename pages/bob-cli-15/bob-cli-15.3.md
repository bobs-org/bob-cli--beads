# Bead: bob-cli-15.3 — Plex video preview thumbnails

[Bead Pages](../README.md) / [bob-cli-15](README.md) / bob-cli-15.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0dy](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.0dy/README.md) · **Assignee:** `bob-cli-15.3` · **Size:** small
**Created:** 2026-08-26 08:19:52 EDT · **Closed:** 2026-08-26 08:45:13 EDT
**Plan:** [202608/disk\_space\_reclamation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/disk_space_reclamation.md)

## Description

plexthumbs: remove the 73.8G of .bif preview thumbnails under /var/lib/plexmediaserver and turn off the generation setting that recreates them.

## Notes

[2026-08-26T12:45:13Z · bob-cli-15.3] Verified the .bif thumbnail cleanup already completed via approved /sase_gate custom-7c517e57 (08:33 EDT): GenerateBIFBehavior=never in Preferences.xml, 0 .bif files remain under Media/ (8,211 deleted, 79,209,555,176 bytes / 73.8G reclaimed per gate result), Metadata/artwork tree untouched, plexmediaserver active and responding (HTTP 200 on /identity). / is now 63% used (326G avail), consistent with reclaim. No epic-symbol entries to resolve.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-15.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-15.3/README.md) | [bob-cli-15.3](bob-cli-15.3.md) | 0 |
