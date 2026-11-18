# Bead: bob-cli-nb.5 — Mac cron cutover

[Bead Pages](../README.md) / [bob-cli-nb](README.md) / bob-cli-nb.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1e2.md) · **Assignee:** `bob-cli-nb.5` · **Size:** small
**Created:** 2026-11-18 13:06:51 EST · **Closed:** 2026-11-18 18:25:46 EST
**Plan:** [202611/bob\_tick.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_tick.md)

## Description

mac_cutover: once the Mac's bob has the gates build (wait with a monitor if not), replace the four Mac cron jobs with one */5 bob-tick job, delete the Highlights shell wrapper and its test, update the Mac-schedule doc sections, converge with cronctl, verify, and remove the stale bob_sync wrappers.

## Notes

[2026-11-18T22:25:45Z · bob-cli-nb.5] PROPOSED FOLLOW-UP: change the gtd_daily #pre #sync chore to bob tick -a after a soak week

[2026-11-18T22:25:50Z · bob-cli-nb.5] PROPOSED FOLLOW-UP: set tick.writer and gcal.writer once bob-cli-ew lands

[2026-11-18T22:25:54Z · bob-cli-nb.5] PROPOSED FOLLOW-UP: Bob Mac Capture health badge reading last.json and org.bobs.bob.tick-finished

[2026-11-18T22:25:59Z · bob-cli-nb.5] PROPOSED FOLLOW-UP: per-PDF unchanged-skip cache inside bob ref scan

[2026-11-18T22:26:03Z · bob-cli-nb.5] Mac 2026-11-18: bob 0.5.0 has tick engine only, no refs gate object; cutover gated on Bryan installing the gates build (just install-all or release train). Stale wrappers: athena ~/bin/bob_sync absent, apollo exact-match wrapper deleted.

[2026-11-18T23:25:46Z · bob-cli-nb.5--1] Mac gates build verified live (refs gate present via bob tick -d -f json). Chezmoi: four Mac cron jobs replaced by one */5 bob-tick job; Highlights wrapper and its test deleted; cronctl check ok, diff shows 4 jobs out / 1 in, dry-run resolves bob tick cleanly. Docs: vault-git-sync Mac maintenance + xlib sections, gcal/gmail Where-it-runs, highlights Scheduled Scan all rewritten to the live tick schedule; just docs-check passed (447 passed). Stale wrappers re-verified absent on athena and apollo. Converge staged via post-commit cronctl apply mac monitor; Mac asleep means pending, converges at its next chezmoi update -a.

## Dependencies

- **Depends on:** [bob-cli-nb.2](bob-cli-nb.2.md) ✓ · ⧖ 2026-11-18
- **Depends on:** [bob-cli-nb.3](bob-cli-nb.3.md) ✓ · ⧖ 2026-11-18
- **Depends on:** [bob-cli-nb.4](bob-cli-nb.4.md) ✓ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nb.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nb.5.md) | [bob-cli-nb.5](bob-cli-nb.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a1e876c`](https://github.com/bobs-org/bob-cli/commit/a1e876cc80368d973f05a8c6c00cdab8743654dc) | docs(mac): describe bob-tick schedule replacing four cron jobs | [bob-cli-nb.5](bob-cli-nb.5.md) | 2026-11-18 18:30:40 EST |
| chezmoi | [`chezmoi@f8acd58`](https://github.com/bbugyi200/dotfiles/commit/f8acd58c49879066883aff1c04161c49e525c6d9) | feat(cron): replace four mac bob jobs with one bob-tick job | [bob-cli-nb.5](bob-cli-nb.5.md) | 2026-11-18 18:31:04 EST |
