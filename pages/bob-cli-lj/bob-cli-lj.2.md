# Bead: bob-cli-lj.2 — Charts decoder and pure panel model

[Bead Pages](../README.md) / [bob-cli-lj](README.md) / bob-cli-lj.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4m.linker.w0.md) · **Assignee:** `bob-cli-lj.2` · **Size:** medium
**Created:** 2026-11-14 09:39:37 EST · **Closed:** 2026-11-14 10:16:32 EST
**Plan:** [202611/bank\_period\_charts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_period_charts.md)

## Description

model: strictly decode `charts` in bob-ledger-tools, add the `-c` fetch spec and older-bob detection, and build the pure panel model (states, encodings, formats, copy, accessibility text) with vector tests.

## Notes

[2026-11-14T15:15:40Z · bob-cli-lj.2] PROPOSED FOLLOW-UP: CI=true Chromium hard-fail in test-command-mode-sheet-sequence-dom — `npm test` fails with "CI requires Chromium on PATH or CHROMIUM_PATH" in this agent env; reproduced identically on clean bob-plugins master. Isolated run of the same file is the only isolated failure on both trees. bob-cli-lh.land note 2 recorded this as an exit-0 skip; do not reopen closed bob-cli-f1.

[2026-11-14T15:15:57Z · bob-cli-lj.2] PROPOSED FOLLOW-UP: Full-suite 25ms mark-perf budgets flake under npm test load — event-link-times (35.8ms), frees-marks (51ms), keep-moving-marks-surface (998.5ms), and off-clock-link-chips (67.8ms) failed in this tree's full `npm test` and passed in isolation on both this tree and clean master. Historical owners: bob-cli-km, bob-cli-ki, bob-cli-ju (see bob-cli-lh.land note 2).

[2026-11-14T15:16:14Z · bob-cli-lj.2] PROPOSED FOLLOW-UP: Share period-identity helper after badge closeout — bankPeriodIdentityMatches lives in 241nc because bob-cli-lh was still IN_PROGRESS and 241n/241na/241nb were off-limits. After closeout lands, extract kind/key/start/end matching so the badge and panel enforce one rule.

[2026-11-14T15:16:32Z · bob-cli-lj.2] Charts decoder and pure panel model landed in bob-plugins. 241h appends -c after -s, adds bankPeriodSpecForStrip (-p -s -c) and a -c-only older-bob recognizer; 241ha strictly decodes charts (absent stays absent, null stays null, malformed is bad-shape); 241nc builds hidden/unavailable/waiting/charts plus encodings, compact labels, categories, not-counted, aria, table twins, and digest. Period identity is kind/key/start/end in 241nc (241n locked). BANK_CACHE_SIZE stays 24. Plugin never adds cents; net copy uses payload net_cents. Verified: npm run build + build:check; 26/26 decode+model tests; related bank-data/badge-hosts 16/16; docs:inventory:check current; bob plugins sync succeeded without -F; no --epic-symbol leftovers. npm test: 6604 pass, 5 fail, 2 skip — Chromium hard-fail and load-flaky 25ms budgets reproduce on clean master (see PROPOSED FOLLOW-UP notes). Did not edit glossary:bank-period-charts or glossary:bank-badge. Did not close parent epic bob-cli-lj.

## Dependencies

- **Blocks:** [bob-cli-lj.3](bob-cli-lj.3.md) ◐ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lj.2/README.md) | [bob-cli-lj.2](bob-cli-lj.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d845e04`](https://github.com/bobs-org/bob-plugins/commit/d845e04dd7bb70ac870831f5512e685eb40d5940) | feat(ledger-tools): decode bank report charts and model the period panel | [bob-cli-lj.2](bob-cli-lj.2.md) | 2026-11-14 10:19:07 EST |
