# Bead: bob-cli-gb.8 — Vault landing: install everywhere, rewrite legacy rows to #off, turn on love.md, verify

[Bead Pages](../README.md) / [bob-cli-gb](README.md) / bob-cli-gb.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.31.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.31.linker.w0.md) · **Assignee:** `bob-cli-gb.8` · **Size:** small
**Created:** 2026-11-02 17:38:45 EST · **Closed:** 2026-11-03 06:06:34 EST
**Plan:** [202611/off\_on\_tags\_and\_offclock\_areas.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_on_tags_and_offclock_areas.md)

## Description

vault-landing: confirm every host runs the new bob and plugins, rewrite re-scanned legacy Event Task rows to #off, add offclock: true to love.md, list Google titles to retitle, verify stats and drift, and close ^off-tag.

## Notes

[2026-11-03T05:13:18Z · bob-cli-gb.8] Mac SSH to kellys-macbook-pro timed out. Starting just install-all on apollo and athena from ~/projects/github/bobs-org/bob-cli (and the matching athena checkout). Will retry Mac and will not edit the vault until every reachable host is on the new bob/plugins, and until Bryan confirms if the Mac is still down.

[2026-11-03T05:25:47Z · bob-cli-gb.8--1] Host status after install retry: apollo just install-all succeeded (bob-cli 2bf5e759→f9f4c706, plugins 8/8 at 9185779). athena bob-cli installed at f9f4c706; plugins dry-run refused to overwrite bob-ledger-tools deployed dirty from bob-cli_15 at a28d1af. Forced `bob plugins sync -p bob-ledger-tools -F` from canonical ~/projects/github/bobs-org/bob-plugins HEAD 9185779 (clock + marks commits are on master); after that preview is clean and all 8 plugins match 9185779. Capture dry-run `Walk the dog #off` succeeds on apollo and athena; deployed bob-ledger-tools and task-status-cycler contain taskEffectiveOffClock on both. Mac SSH to kellys-macbook-pro (and mac alias) still times out. Vault not edited.

[2026-11-03T10:54:56Z · bob-cli-gb.8--2] Mac is reachable via ssh mac (bbugyi). Bryan chose wait-until-Mac. Starting just install-all on the Mac from ~/projects/github/bobs-org/bob-cli. Vault still not edited.

[2026-11-03T11:06:04Z · bob-cli-gb.8--3] Hosts confirmed: apollo/athena bob-cli f9f4c706 (GitHub master now 05e355ee, descendant) + plugins with taskEffectiveOffClock; Mac ssh mac as bbugyi bob-cli 05e355ee (contains f9f4c706) plugins 175aced (contains 9185779). Capture dry-run Walk the dog #off succeeds on all three. Vault 7178580f: four Event Task #offclock→#off (Halloween, Grocery Store, Swings, Lincoln Park) and love.md offclock: true. Vault-sync pushed. ^off-tag completed d0f324b0. Verify: stats -k off-clock groups family/abby under love; capture start Park walk @love:park-walk-gb8= previews 25m off-clock via love; reconcile --dry-run already in sync. clock_drift=1 (closed rows keep keys after love default). Coming-week gcal list (athena snapshot 2026-11-01): no titles to retitle — none carry #offclock/#off-clock/#untracked. (virtual) CFG Appt already off via vault #off @body; Wedding Anniversary and Little Gym have no root/tag (once @love/@family/@abby they inherit). Past Google titles still using #offclock — drop the tag (family/abby inherit via love): Halloween at Aunt Jenny's!, Grocery Store w/ Abby, Swings!, Lincoln Park w/ Abby. Never edited Google. Plugin docs mounts unchanged; skipped docs-gen. epic-symbols: none.

[2026-11-03T11:06:17Z · bob-cli-gb.8--3] PROPOSED FOLLOW-UP: Mac just install-all failed at bob-mac-capture signing (login keychain locked over SSH, errSecInternalComponent). bob-cli and plugins installed; rerun just install for bob-mac-capture from a GUI Terminal or after security unlock-keychain.

[2026-11-03T11:06:23Z · bob-cli-gb.8--3] PROPOSED FOLLOW-UP: bob stats clock_drift warning copy still says "linked tasks' #offclock tags" after #off became canonical (display-only; drift count itself is 1).

[2026-11-03T11:06:34Z · bob-cli-gb.8--3] Vault landing done. Hosts: apollo/athena bob-cli f9f4c706 + plugins taskEffectiveOffClock; Mac 05e355ee/175aced (contains epic SHAs); capture #off dry-run ok on all three. Rewrote 4 Event Task #offclock→#off; love.md offclock true; vault-sync 7178580f. ^off-tag completed d0f324b0. Verified stats off-clock under love, capture start off-clock via love, reconcile dry-run in sync, clock_drift=1. Coming-week Google titles: none to retitle; past #offclock titles listed on the bead for Bryan to drop. epic-symbols none. Did not close parent epic.

## Dependencies

- **Depends on:** [bob-cli-gb.2](bob-cli-gb.2.md) ✓ · ⧖ 2026-11-02
- **Depends on:** [bob-cli-gb.3](bob-cli-gb.3.md) ✓ · ⧖ 2026-11-02
- **Depends on:** [bob-cli-gb.4](bob-cli-gb.4.md) ✓ · ⧖ 2026-11-02
- **Depends on:** [bob-cli-gb.5](bob-cli-gb.5.md) ✓ · ⧖ 2026-11-02
- **Depends on:** [bob-cli-gb.7](bob-cli-gb.7.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gb.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gb.8.md) | [bob-cli-gb.8](bob-cli-gb.8.md) | 0 |
