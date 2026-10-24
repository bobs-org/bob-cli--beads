# Bead: bob-cli-bc.9 — Obsidian api.themes and theme pills

[Bead Pages](../README.md) / [bob-cli-bc](README.md) / bob-cli-bc.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2c.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2c.linker.w1.md) · **Assignee:** `bob-cli-bc.9` · **Size:** medium
**Created:** 2026-10-24 07:52:22 EDT · **Closed:** 2026-10-24 09:15:21 EDT
**Plan:** [202610/pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_themes.md)

## Description

obsidian-colors: add the ledger-tools themes API with JS mirrors, shared hue tokens, and pills in Live Preview, Reading view, the plan block, and Stats.

## Notes

[2026-10-24T13:15:21Z · bob-cli-bc.9] obsidian-colors landed in bob-plugins (uncommitted, v1.66.0): api.themes v1 (cached bob themes list fetch with stale-while-revalidate single flight, sync hueFor/componentsOf/historyRows/similarTo, hide/unhide/color/rename writers via --via bob-ledger-tools, onChange), JS mirrors of hue/fold/PT7-BD rank pinned by byte-identical vectors (11/11 new tests pass), --bob-hue-* tokens + pill/muted/swatch CSS, Live Preview marks with cursor-line unknown-neutral rule, Reading pill post-processor, plan-block pill line, Stats theme-hue bars (exempt/other gray), Toggle Pomodoro theme colors command, docs + plugin-apis. Verified: npm test 3548/3548, build check, docs inventory + docs-check (448) green, live-vault probe agrees with bob themes for BOB/JOB/DEV/LOVE/GTD/BLOG (81 themes, tooltips with day counts), deployed via bob plugins sync -p bob-ledger-tools and syntax-checked. No epic-symbol leftovers. Writes resolve unsupported until bc.3 prefs lands the CLI writers (expected sequencing, no new bead).

## Dependencies

- **Blocks:** [bob-cli-bc.10](bob-cli-bc.10.md) ◐ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bc.2](bob-cli-bc.2.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bc.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.9/README.md) | [bob-cli-bc.9](bob-cli-bc.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d2699df`](https://github.com/bobs-org/bob-plugins/commit/d2699df8c5a6bcba72f45a58661cafc9991f3860) | feat(ledger-tools): add api.themes v1 and theme pills rendering | [bob-cli-bc.9](bob-cli-bc.9.md) | 2026-10-24 09:17:01 EDT |
