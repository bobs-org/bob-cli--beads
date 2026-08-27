# Bead: bob-cli-1e — Remove old\_lib from Obsidian Sync and restore the vault under quota

[Bead Pages](../README.md) / bob-cli-1e

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0en](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0en.md) · **Assignee:** `bob-cli-1e.land`
**Created:** 2026-08-27 08:13:35 EDT · **Closed:** 2026-08-27 09:29:31 EDT
**Plan:** [202608/unsync\_old\_lib.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/unsync_old_lib.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202608/unsync_old_lib.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202608/unsync_old_lib.md

<!-- sase:links:end -->

## Description

The `old_lib/` directory no longer syncs through Obsidian Sync from athena, its 851 MB is gone from the remote vault, every old_lib byte still exists on disk and in a durable backup, and `ob-sync-bob.service` completes sync cycles without `Vault limit exceeded`.

## Notes

[2026-08-27T12:36:20Z · bryanbugyi34@gmail.com] Make sure my macbook's Obsidian is synced properly before closing this epic. My MacBook is accessible over SSH (see the ~/.ssh/config file).

[2026-08-27T13:29:31Z · bob-cli-1e.land] Landed after verifying all five phases against live system state, not just their notes.

VERIFIED. old_lib is fully drained from the remote vault (0 live entries) and every recent ob-sync-bob poll cycle logs 'Excluded folders: old_lib' with zero 'Uploading file old_lib/' lines - including all cycles after the 880 MB MacBook-only backup was added, so athena is not re-uploading it. athena's headless ignoreFolders=['old_lib'] confirmed via ob sync-config. Local data: /home/bryan/bob/old_lib holds 700 files / 1731114877 bytes, byte-identical to /home/bryan/var/backups/bob-old-lib-20260827 (700 files / 1731114877 bytes). Vault Git tracks 698 of the 700 (the 2 omissions exceed GitHub's 100 MiB limit, tracked as bob-cli-1k); vault repo is 0 ahead / 0 behind origin/master. bob-cli commit 9f9049b carries the README row and docs/obsidian-sync-exclusions.md runbook; both present and cargo fmt --check is clean.

MACBOOK EXCLUSION - CORRECTED. Earlier turns reported the MacBook exclusion as unset based on the absence of ~/bob/.obsidian/sync.json. That premise was wrong: desktop Obsidian never writes that file (zero references to it in obsidian-1.13.7.asar), and athena has no sync.json either while definitely excluding old_lib. Desktop Obsidian persists sync settings via db.put('data', ...) into the app's IndexedDB blob store. Reading that record directly shows the MacBook's ignoreFolders = ['lib', 'lit_review', 'old_lib'], written 2026-08-27 09:24. The MacBook is correctly excluding old_lib, satisfying the epic note's requirement that it be synced properly. Plain grep for 'ignoreFolders' returns nothing because surrounding bytes are Snappy-encoded, which is what masked this.

INTEGRATED. No non-epic commits landed in bob-cli since the epic began (9f9049b is the only commit since 08:00), so there was no external drift to reconcile. Integration work was internal: the runbook this epic authored claimed desktop Obsidian stores exclusions in 'vault-local device state', which this turn's verification disproved. Corrected that paragraph and added a 'Verifying a desktop device' section documenting the working IndexedDB read procedure, which was dogfooded against the MacBook and reproduced ['lib','lit_review','old_lib'] exactly. Also broadened the README row from 'excluded from Obsidian Sync on athena' to 'on every device', now that both devices are confirmed.

FOLLOW-UPS. All three PROPOSED FOLLOW-UP notes from bob-cli-1e.5 were filed and remain READY: sync.log rotation (bob-cli-1f), untracked remote-only vault files (bob-cli-1g), and the obsidian.md sync-topology memory update (bob-cli-1h, which also now carries this turn's IndexedDB finding). Three more were filed during landing: quota re-check (bob-cli-1i), bob nightly under a failing sync gate (bob-cli-1j), and the 2 oversized old_lib PDFs (bob-cli-1k). None were declined.

KNOWN OPEN. ob-sync-bob.service still reports 'Vault limit exceeded' because ~851 MB of attachment version history for the deleted PDFs has not yet expired. Per the user's decision this is a wait, not a rebuild; sase bead epic-symbols bob-cli-1e reports no entries.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-1e.1](bob-cli-1e.1.md) | Close the backup gap and gate the destructive window | ✓ closed | small | 2026-08-27 | 1 | 0 |
| [bob-cli-1e.2](bob-cli-1e.2.md) | Evacuate old\_lib and push the deletions to the remote vault | ✓ closed | medium | 2026-08-27 | 1 | 0 |
| [bob-cli-1e.3](bob-cli-1e.3.md) | Set the device-local exclusion and restore old\_lib in place | ✓ closed | small | 2026-08-27 | 1 | 0 |
| [bob-cli-1e.4](bob-cli-1e.4.md) | Verify quota recovery and run the fallback if version history holds | ✓ closed | medium | 2026-08-27 | 1 | 0 |
| [bob-cli-1e.5](bob-cli-1e.5.md) | Document the exclusion and file the discovered follow-ups | ✓ closed | small | 2026-08-27 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-1e: Remove old_lib from Obsidian Sync and restore the vault under quota [closed]"]
    n1["bob-cli-1e.1: Close the backup gap and gate the destructive window [closed]"]
    n2["bob-cli-1e.2: Evacuate old_lib and push the deletions to the remote vault [closed]"]
    n3["bob-cli-1e.3: Set the device-local exclusion and restore old_lib in place [closed]"]
    n4["bob-cli-1e.4: Verify quota recovery and run the fallback if version history holds [closed]"]
    n5["bob-cli-1e.5: Document the exclusion and file the discovered follow-ups [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
    n3 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1e.1](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.bob-cli-1e.1.md) | [bob-cli-1e.1](bob-cli-1e.1.md) | 0 |
| [bbugyi200.athena.bob-cli-1e.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1e.2/README.md) | [bob-cli-1e.2](bob-cli-1e.2.md) | 0 |
| [bbugyi200.athena.bob-cli-1e.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1e.3/README.md) | [bob-cli-1e.3](bob-cli-1e.3.md) | 0 |
| [bbugyi200.athena.bob-cli-1e.4](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.bob-cli-1e.4.md) | [bob-cli-1e.4](bob-cli-1e.4.md) | 0 |
| [bbugyi200.athena.bob-cli-1e.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1e.5/README.md) | [bob-cli-1e.5](bob-cli-1e.5.md) | 1 |
| [bbugyi200.athena.bob-cli-1e.land](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.bob-cli-1e.land.md) | [bob-cli-1e](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9f9049b`](https://github.com/bobs-org/bob-cli/commit/9f9049bad22546e8d949c240ba1c2820842b9b1c) | docs: document obsidian sync exclusions | [bob-cli-1e.5](bob-cli-1e.5.md) | 2026-08-27 08:42:46 EDT |
| bob-cli | [`6be39a7`](https://github.com/bobs-org/bob-cli/commit/6be39a78458b0d4bf39773c6df14411e148d603d) | docs: correct how desktop Obsidian stores sync exclusions | [bob-cli-1e](README.md) | 2026-08-27 09:31:02 EDT |
