# Bead: bob-cli-1n.6 — Prove the acceptance matrix end to end, then cut over

[Bead Pages](../README.md) / [bob-cli-1n](README.md) / bob-cli-1n.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ez](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ez.md) · **Assignee:** `bob-cli-1n.6` · **Size:** medium
**Created:** 2026-08-27 12:48:58 EDT · **Closed:** 2026-08-27 17:23:45 EDT
**Plan:** [202608/vault\_git\_sync.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/vault_git_sync.md)

## Description

cutover: run every acceptance test across both real machines, disable Obsidian Sync on athena and the MacBook, restore nightly maintenance, write the runbook, and supersede the competing Obsidian Sync restoration epic.

## Notes

[2026-08-27T18:53:31Z · bob-cli-1n.6] ACCEPTANCE: Dry-run window passed with triggers disabled (athena clean, MacBook reported local edits that were committed through bob vault-sync); real serial cycles converged both vaults at 827b8c8f, then subsequent Mac user edits plus Obsidian Sync core-plugin disable converged at 8b467b5a. Matrix #3 concurrent different notes passed, #4 non-overlapping edits to one note merged on both machines, and #5 same-line edit produced _conflicts/_sync_acceptance/bob-cli-1n-20260827T184732Z/same-line.athena-2026-08-27T145303-0400.md with no exact git conflict markers and the conflict-only task hidden from dash.md/blocked.md.

[2026-08-27T18:54:36Z · bob-cli-1n.6] ACCEPTANCE: Matrix #6 both-added future daily note 2099/20990101.md produced one quarantined AA conflict copy and converged at 57c4c329; #7 forced a real non-fast-forward push race with a temporary pre-push hook and bob vault-sync retried successfully with push_retries=1, converging at 8522d324; #8 simulated both machines edited while disconnected from the sync loop, then reconciled both files cleanly on both machines at 9a7c72ea.

[2026-08-27T18:57:23Z · bob-cli-1n.6] ACCEPTANCE: Matrix #9 delete-vs-modify passed at 50663e5b; #10 binary conflict was rerun with tracked .png content after .bin proved ignored by the vault, and produced an uncorrupted local conflict copy while the working file took the remote bytes at e262c515; #11 a 96 MiB tracked .png was refused locally with exit 1 before staging or push; #12 an intentionally interrupted conflicted merge was recovered by the next bob vault-sync cycle with interrupted_merge_recovered=true at 452c0c3f; #13 no-change cycle left HEAD unchanged and status files_committed=0.

[2026-08-27T19:01:30Z · bob-cli-1n.6] ACCEPTANCE: After cutover, enabled and started athena bob-vault-sync.service, bootstrapped MacBook LaunchAgent, disabled ob-sync-bob.service, restored the 03:30 bob nightly crontab, and verified Obsidian Sync core plugin is false in the vault config. Matrix #1 MacBook edit propagated to athena via triggers in 22s and #2 athena edit propagated to the MacBook via triggers in 20s; both converged at bc8c4912.

[2026-08-27T21:22:27Z · bob-cli-1n.6--3] ACCEPTANCE: Remaining matrix summary for #15-#18 plus #14 caveat. #15 bob nightly passed on athena: a Mac-authored done-task probe put athena behind at 97ead745; `bob nightly` performed the leading vault-sync pull, `move-done-tasks`, and trailing vault-sync push, ending at 3fe3eb51. #16 xlib bridge initially exposed the Mac `home` LAN alias timeout; after patching managed `bob_xlib_pull` to try `home` then `xhome` and applying it live, the Mac wrapper pulled a fresh PDF from athena `xlib/`, removed the source, moved it to Mac `lib/`, generated the `ref/` note, and converged both vaults at 8a234f9e. #17 Mac `bob plugins sync` reported six plugins up to date and `block-id-prompt` main.js/manifest.json/styles.css hashes matched athena. Cleanup removed 25 tracked acceptance artifacts, and both machines were rechecked clean and level at HEAD/upstream 2d23b813 with 0 dirty lines. #18 10-minute idle CPU did not pass the stated <=1.5% average requirement: Athena 300 samples avg 0.588%, max 28.500%, nonzero 215/300; Mac 300 samples avg 1.875%, max 142.700%, nonzero 25/300. #14 is not a literal pass: no full athena reboot was performed; Mac offline/wake evidence is limited to monitor v1e4g3vwp11w showing BatchMode SSH timeout for attempts 1-84 and recovery at attempt 85 with `bob vault-sync status` clean. Repo verification: `just all` passed, and `sase bead epic-symbols bob-cli-1n.6` reported no entries. Leaving bob-cli-1n.6 open because #18 missed the Mac average threshold and #14 remains only partially evidenced.

[2026-08-27T21:23:45Z · bob-cli-1n.6--3] Auto-closed by `sase stitch create` after create_commit landed 4c00ada ("docs(vault-sync): add Bob vault Git sync runbook"). No verification is implied by this note. Reopen with `sase bead open bob-cli-1n.6`, or pass `-B|--do-not-close-bead` on mid-flight commits.

## Dependencies

- **Depends on:** [bob-cli-1n.5](bob-cli-1n.5.md) ✓ · ⧖ 2026-08-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1n.6](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.bob-cli-1n.6.md) | [bob-cli-1n.6](bob-cli-1n.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4c00ada`](https://github.com/bobs-org/bob-cli/commit/4c00adadd155660957544c32ac00ef0cf26e360e) | docs(vault-sync): add Bob vault Git sync runbook | [bob-cli-1n.6](bob-cli-1n.6.md) | 2026-08-27 17:23:25 EDT |
