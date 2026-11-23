# Bead: bob-cli-pf.1.1.5 — Real-Obsidian drawer acceptance and deployment

[Bead Pages](../README.md) / [bob-cli-pf.1.1](bob-cli-pf.1.1.md) / bob-cli-pf.1.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.1.md) · **Assignee:** `bob-cli-pf.1.1.5` · **Size:** medium
**Created:** 2026-11-22 14:45:09 EST · **Closed:** 2026-11-22 20:51:11 EST
**Plan:** [202611/card\_foot\_drawer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/card_foot_drawer.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:c7135143af9a4a7d2df51467 | attached via sase artifact create --bead |
| related | file:explicit:dcd27f31fa7fb913287fdb6a | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

acceptance: add and run the isolated real-Obsidian foot walkthrough, inspect the complete screenshot matrix, verify no-write and no-spawn behavior, run repository gates, and deploy the verified plugins.

## Notes

[2026-11-23T01:50:12Z · bob-cli-pf.1.1.5] PROPOSED FOLLOW-UP: stabilize full-suite timing budgets (event-link-times 138.9ms, frees-marks 160ms vs 25ms) and the period-notes ensure -d cascade stub; all three fail identically on the clean base tree

[2026-11-23T01:50:27Z · bob-cli-pf.1.1.5] PROPOSED FOLLOW-UP: docs:check mount refuses to overwrite authored docs/reference/plugins/albums.md; reproduces identically on the clean base tree

[2026-11-23T01:51:11Z · bob-cli-pf.1.1.5] Real-Obsidian foot acceptance green: isolated scratch vault/profile/CDP run passes 116/116 checks with 27 inspected screenshots covering album/record/day/week/quarter/year/bank feet in Reading and Live Preview, identity-only and collapsed states, duplicate/invalid/missing-created drawers, light/dark/narrow, two panes, palette toggle, == editor open/dismiss, cursor preservation, and scroll-into-view. Note bytes identical for every paint/fold/toggle/collapse gesture; invocation log proves no writer calls and no out-of-allowlist bob spawns; zero console exceptions. Fixed two live-toggle regressions found by the run: (1) record live decorations skipped mount tracking on cached early returns (242v now falls through to re-track; unit test fails-before/passes-after), (2) live mounts orphaned by teardown/detach never re-registered (240p heals on toggle; unit test fails-before/passes-after). Gates: build:check, validate 12/12, docs inventory, focused suites 151/151 pass; full npm test 8848/8856 with 3 clean-base failures recorded as PROPOSED FOLLOW-UPs (2 timing budgets + period-notes cascade), plus docs:check mount refusal also on clean base. Deployed via bob plugins sync (3 copied, 0 skipped, 31 unchanged). Evidence: file:explicit:dcd27f31fa7fb913287fdb6a (report JSON), file:explicit:c7135143af9a4a7d2df51467 (27-PNG matrix).

## Dependencies

- **Depends on:** [bob-cli-pf.1.1.4](bob-cli-pf.1.1.4.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.1.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.1.1.5/README.md) | [bob-cli-pf.1.1.5](bob-cli-pf.1.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c8deb53`](https://github.com/bobs-org/bob-plugins/commit/c8deb534ddd48fe0a89db09ef206137cf9ec8c25) | feat(ledger-tools): add real-Obsidian card-foot acceptance and heal live mount tracking | [bob-cli-pf.1.1.5](bob-cli-pf.1.1.5.md) | 2026-11-22 20:54:57 EST |
