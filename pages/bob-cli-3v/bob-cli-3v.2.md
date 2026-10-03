# Bead: bob-cli-3v.2 — Ledger keep helper and folded marks

[Bead Pages](../README.md) / [bob-cli-3v](README.md) / bob-cli-3v.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4o](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4o.md) · **Assignee:** `bob-cli-3v.2` · **Size:** medium
**Created:** 2026-10-03 10:36:59 EDT · **Closed:** 2026-10-03 11:09:22 EDT
**Plan:** [202610/rotten\_keep\_streak.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/rotten_keep_streak.md)

## Description

ledger-marks: mirror the contract in freshness namespace v5, add the sole increment helper, and render accessible folded pips with truthful decision annotations.

## Notes

[2026-10-03T15:09:22Z · bob-cli-3v.2] ledger-marks done: freshness namespace v5 with sole keepLine helper (counted increment saturating at 999, valid-prior-fresh guard; generic stampers clear); decay config normalization + 2026-10-19 activation + decide mirrored from Rust; queue rows carry keeps/decide, counts carry decide; folded keep pips in both mark renderers with capped dots, +N overflow, count-truthful tooltips (leaf/key-hint gated to decision-card); manifest 1.23.0 + API docs. Verified: npm test 1476 pass/0 fail (new 44-test keeps suite registered), npm run validate 6/6, cargo test freshness ok. One unrelated nav stage ranker perf assertion flaked at 16.03ms under full-suite load and passed solo at 6ms in an untouched file.

## Dependencies

- **Depends on:** [bob-cli-3v.1](bob-cli-3v.1.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3v.3](bob-cli-3v.3.md) ◐ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3v.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3v.2/README.md) | [bob-cli-3v.2](bob-cli-3v.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ca611d2`](https://github.com/bobs-org/bob-cli/commit/ca611d2884f00ff310e072c77ba3f25b4ea5cc0d) | feat(freshness): ledger keep helper and folded marks for bob-cli-3v.2 | [bob-cli-3v.2](bob-cli-3v.2.md) | 2026-10-03 11:10:34 EDT |
| bob-plugins | [`bob-plugins@67e9409`](https://github.com/bobs-org/bob-plugins/commit/67e9409b7a3d4b0e6e1f0520b8a769eaa6999019) | feat(freshness): keep-streak namespace v5, keepLine, and folded pips for bob-cli-3v.2 | [bob-cli-3v.2](bob-cli-3v.2.md) | 2026-10-03 11:12:12 EDT |
