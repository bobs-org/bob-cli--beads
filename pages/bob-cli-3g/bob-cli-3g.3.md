# Bead: bob-cli-3g.3 — Navigation tier notices, walk anchor, and lane-aware refresh row

[Bead Pages](../README.md) / [bob-cli-3g](README.md) / bob-cli-3g.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0v7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0v7.md) · **Assignee:** `bob-cli-3g.3` · **Size:** medium
**Created:** 2026-10-01 18:28:57 EDT · **Closed:** 2026-10-01 19:45:08 EDT
**Plan:** [202610/tiered\_morning\_review\_walk.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/tiered_morning_review_walk.md)

## Description

nav-walk: give bob-navigation-hotkeys tier-aware jump notices, a commitments-done boundary notice, a robust walk anchor for advancing after stamps and releases, and a refresh row that reads the lane interval from the api.

## Notes

[2026-10-01T23:45:08Z · bob-cli-3g.3] nav-walk landed as bob-plugins ede89d3 (nav 1.50.0): tier-aware jump notices with tier rank + lane second line, Commitments-done/ROTTEN-next boundary, walk anchor (cursor-first, anchor successor/predecessor, fixes [s-after-stamp and release-then-]s), lane-aware refresh row via intervalForLine with once-Ready suffix and v3 fallback, upkeep meter on empty/stamp notices. Verified: npm test 1185/1185 green (13 new nav-walk tests), npm run validate 6/6, deployed via bob plugins sync (vault shows 1.50.0), epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-3g.2](bob-cli-3g.2.md) ✓ · ⧖ 2026-10-01
- **Blocks:** [bob-cli-3g.4](bob-cli-3g.4.md) ✓ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3g.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3g.3/README.md) | [bob-cli-3g.3](bob-cli-3g.3.md) | 0 |
