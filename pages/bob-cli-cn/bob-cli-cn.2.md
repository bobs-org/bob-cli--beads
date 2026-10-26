# Bead: bob-cli-cn.2 — Day strip — paint bob's typical line under the four numeric facts

[Bead Pages](../README.md) / [bob-cli-cn](README.md) / bob-cli-cn.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5d.linker.w0.md) · **Assignee:** `bob-cli-cn.2` · **Size:** medium
**Created:** 2026-10-26 13:12:28 EDT · **Closed:** 2026-10-26 14:31:14 EDT
**Plan:** [202610/day\_strip\_typical\_day.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/day_strip_typical_day.md)

## Description

strip-line: in bob-plugins bob-ledger-tools, build a pure `ref` model from `point.typical` and paint an aria-hidden reference line with SVG ▲/▼/= marks on every fact. Keep the line's space on every fact. Put bob's words in the fact's aria-label and tooltip. Require day-grouped reports for cache reuse, and repaint when only the reference changes. Extend the unit tests and the preview harness (new states, alignment, clipping, contrast, measured budgets). Update the plugin docs and the bob-cli Day strip contract, bump the plugin version, then sync.

## Notes

[2026-10-26T18:30:56Z · bob-cli-cn.2] Live parity (local cargo debug bob, not installed) via dayStripModel on 2026-10-26: Oct 6 Worked 5h 00m ▲ typical 4h 25m, Reviewed not-tracked so blank reserved line (D has no finite value), Done 86 ▲ typical 7, Created 15 ▼ typical 17. Oct 22 all below (Worked 1h 15m ▼ typical 4h 10m; Reviewed 43 ▼ 58; Done 9 ▼ 23; Created 3 ▼ 26). Oct 25 Worked 3h 25m ▼ typical 4h 10m, Reviewed 75 ▲ 54, Done 17 ▼ 19, Created 9 ▼ 23 (matches research prose; typical.value equals rolling_median at D-1 on every numeric fact). Today no marks, typical floor Worked 4h 10m / Reviewed 54 / Done 17 / Created 22. Painted ref.display and mark matched bob typical on every finite-value fact. Plugin synced 1.77.0 to the vault (--no-pull from the linked checkout); installed bob still lacks typical so deployed strips show blank reserved lines until the release train.

[2026-10-26T18:31:00Z · bob-cli-cn.2] PROPOSED FOLLOW-UP: just docs-check fails on undocumented BOB_TEST_FIXTURE_PDF in src/native/highlights_ref/source_store.rs:194 — reproduces on the clean base tree; already tracked on bob-cli-ce.6/8/9, bob-cli-c9.6, bob-cli-cc.9.

[2026-10-26T18:31:14Z · bob-cli-cn.2] Verified: dayStripRef paints bob typical under the four numeric facts (SVG marks, reserved height, aria-hidden); week/month default cache refused and re-selects -g day; paintedKey includes typical; 108 unit tests pass; Chromium preview 246 cells 0 failures 0 overflow at 132/198 and 100/166; live parity Oct 6/22/25/today matches typical.display, relation, and rolling_median(D-1); plugin 1.77.0 synced. Pre-existing BOB_TEST_FIXTURE_PDF docs lint recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-cn.1](bob-cli-cn.1.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-cn.3](bob-cli-cn.3.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cn.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cn.2/README.md) | [bob-cli-cn.2](bob-cli-cn.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bd9c7a8`](https://github.com/bobs-org/bob-cli/commit/bd9c7a8c5b061c64b2f14d1f601f7c4d64358cf4) | docs(stats): describe the Day strip typical line | [bob-cli-cn.2](bob-cli-cn.2.md) | 2026-10-26 14:32:15 EDT |
