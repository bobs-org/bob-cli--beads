# Bead: bob-cli-3g.4 — Config, vault ritual, memory, and live rollout

[Bead Pages](../README.md) / [bob-cli-3g](README.md) / bob-cli-3g.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0v7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0v7.md) · **Assignee:** `bob-cli-3g.4` · **Size:** medium
**Created:** 2026-10-01 18:28:57 EDT · **Closed:** 2026-10-01 19:58:40 EDT
**Plan:** [202610/tiered\_morning\_review\_walk.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/tiered_morning_review_walk.md)

## Description

rollout: add the config block, rewrite the morning ritual in docs and vault, record the decision and glossary memory, install and deploy, verify live, read-only census of stamps, and close ^wip-next-refresh.

## Notes

[2026-10-01T23:58:28Z · bob-cli-3g.4] VERIFICATION GATE (headless agent, Obsidian GUI unavailable): on athena/apollo Obsidian + Mac where available, verify: ]s from non-queue cursor lands on NEW first; walk visits PENDING-NEXT-RETURNED-ROTTEN with tier notices; Alt+Shift+F on last commitment shows Commitments done; Alt+N on lane task then ]s continues to next; [s after stamp goes backwards; due lane tasks show refresh marks with lane tooltip; status bar new text/modes; refresh row shows (next lane); ROTTEN/NEW chips + READY counts unchanged vs pre-deploy snapshot; api.freshness.queue() agrees with bob freshness list -f json on first 20 keys + tier counts; ledger-tools config reports invalid:false. Midnight rollover only via test harness.

[2026-10-01T23:58:40Z · bob-cli-3g.4] Rollout landed+verified headless: chezmoi freshness block (7/1/1) applied to ~/.config/bob/config.yml; bob installed from tree, schema_version 3 with pending/next intervals in JSON; lane rows live (BOB_NOW=2026-10-02 probe: 51 pending + 28 next tiers, null state/bucket); vault ritual (gtd_daily, rotten intro/table/tally cols) + docs 13 landing line synced via vault-sync; trial window 2026-10-05-18 stands; census read-only (0 refresh fields, 0 task_refresh notes, fresh lines Ready199/Pending51/Next26/Blocked264, walk new2/pending0/next0 live); decision review-walk-is-tiered + glossary update + memory init regenerated; wip-next-refresh closed [x] 2026-10-01; just all (fmt+clippy+test) green; hooks dry-run shows only the task-close fallout. GUI checks recorded as VERIFICATION GATE note; plugins already deployed (ledger-tools 1.17.0 ns-v4, nav 1.50.0).

## Dependencies

- **Depends on:** [bob-cli-3g.3](bob-cli-3g.3.md) ✓ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3g.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3g.4/README.md) | [bob-cli-3g.4](bob-cli-3g.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9e548bb`](https://github.com/bobs-org/bob-cli/commit/9e548bba484fb76f951c067c21c593c689811cd8) | feat(freshness): land tiered review walk NEW PENDING NEXT RETURNED ROTTEN | [bob-cli-3g.4](bob-cli-3g.4.md) | 2026-10-01 20:07:42 EDT |
