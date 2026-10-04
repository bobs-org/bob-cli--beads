# Bead: bob-cli-48.6 — Ritual rewrite, deploy, and live verification

[Bead Pages](../README.md) / [bob-cli-48](README.md) / bob-cli-48.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.07.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.07.linker.w1.md) · **Assignee:** `bob-cli-48.6` · **Size:** small
**Created:** 2026-10-04 09:05:23 EDT · **Closed:** 2026-10-04 11:29:30 EDT
**Plan:** [202610/gtd\_pre\_post\_review\_tiers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gtd_pre_post_review_tiers.md)

## Description

rollout: rewrite the Morning review chore as a closeout, update the ritual docs and rollout log, install bob, confirm the synced plugins, verify the live walk, and record any GUI checks that cannot run as a verification gate.

## Notes

[2026-10-04T15:29:17Z · bob-cli-48.6] VERIFICATION GATE: remaining Obsidian GUI walk (apollo/athena have no usable Obsidian display; Mac Obsidian was running but SSH later timed out so this agent could not drive keys): from a non-queue cursor, ]s lands on the first PRE chore with the PRE notice; Alt+Shift+F completes each PRE chore through Tasks (next occurrence appears, no [fresh::], walk lands on the next chore) through all seven including one still [?] before hooks; after PRE the walk reaches NEW; commitments → ROTTEN boundary shows · ]S closes the review; ]S lands on Morning review with its counts; Alt+F closes it with Review closed — …; api.freshness.queue() agrees with bob freshness list -f json on the first 20 keys and tier counts; NEW/ROTTEN chips match the pre-deploy snapshot (headless ready totals already matched: counted 98, crowded 4, rotten 77). Also remaining: Mac bob plugins sync — last inspect showed ledger 1.28.2 / nav 2.2.1 / cycler 1.24.0 before the lid closed.

[2026-10-04T15:29:22Z · bob-cli-48.6] PROPOSED FOLLOW-UP: Deploy PRE/POST plugins on the Mac — last SSH inspect showed bob-ledger-tools 1.28.2 and bob-navigation-hotkeys 2.2.1 (cycler already 1.24.0); later ssh to kellys-macbook-pro timed out. Run bob plugins sync there and reload Obsidian so the live ]s walk has namespace v7 / nav 2.3.0.

[2026-10-04T15:29:30Z · bob-cli-48.6] Installed schema 9 bob on apollo and athena; freshness list JSON pre_due=7 post_due=1 in gtd_daily file order, walk 131→139, due/new/rotten/fresh unchanged; human PRE first, closeout divider, POST last. Synced ledger 1.29.0 / nav 2.3.0 / cycler 1.24.0 byte-identical on apollo and athena. Rewrote Morning review closeout and vault-synced (ee370271) to ~/bob. Ritual docs §6/§13 and getting-started updated. hooks --dry-run showed no feature-induced rewrites. Remaining Obsidian GUI walk and Mac plugin sync recorded as a verification gate.

## Dependencies

- **Depends on:** [bob-cli-48.2](bob-cli-48.2.md) ✓ · ⧖ 2026-10-04
- **Depends on:** [bob-cli-48.3](bob-cli-48.3.md) ✓ · ⧖ 2026-10-04
- **Depends on:** [bob-cli-48.4](bob-cli-48.4.md) ✓ · ⧖ 2026-10-04
- **Depends on:** [bob-cli-48.5](bob-cli-48.5.md) ✓ · ⧖ 2026-10-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-48.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-48.6/README.md) | [bob-cli-48.6](bob-cli-48.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b1e8d30`](https://github.com/bobs-org/bob-cli/commit/b1e8d30e92270986672b8e7e89055f56e1382eeb) | docs(freshness): rewrite morning ritual for PRE/POST closeout | [bob-cli-48.6](bob-cli-48.6.md) | 2026-10-04 11:30:38 EDT |
