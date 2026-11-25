# Bead: bob-cli-q6.1 — Shared fold kit, the \`\_\` key, the command, and album Schema

[Bead Pages](../README.md) / [bob-cli-q6](README.md) / bob-cli-q6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g2.md) · **Assignee:** `bob-cli-q6.1` · **Size:** medium
**Created:** 2026-11-25 12:49:31 EST · **Closed:** 2026-11-25 16:04:04 EST
**Plan:** [202611/bank\_property\_card\_fold.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_property_card_fold.md)

## Description

fold-core: add the 240s fold kit (state helper, node-based registry, fold row), species foldDefault, the guarded `_` arm and toggle-card-details command plus Command Mode row, and move album Schema onto the kit with tests, e2e, docs, and the vimrc comment.

## Notes

[2026-11-25T20:47:36Z · bob-cli-q6.1--4] PROPOSED FOLLOW-UP: Bring the two Bob plugin documentation pages under their word budgets — docs/develop/plugins/plugin-apis.md is 9,276 words against an 8,000 cap (1,276 over), and docs/reference/plugins/bob-navigation-hotkeys.md is 6,068 against a 6,000 cap (68 over). npm run docs:check fails at lint on those budgets; both files are unchanged in this workspace (neither is modified in git status or diff).

[2026-11-25T21:03:04Z · bob-cli-q6.1--4] PROPOSED FOLLOW-UP: Updated docs:check evidence after the linked repo fast-forward: docs/develop/plugins/plugin-apis.md is 9,279 words against an 8,000 cap (1,279 over); docs/reference/plugins/bob-ledger-tools.md is 6,002 against 6,000 (2 over); docs/reference/plugins/bob-navigation-hotkeys.md is 6,068 against 6,000 (68 over). The final check fails at lint. All three files are clean in this checkout's git status and diff.

[2026-11-25T21:03:11Z · bob-cli-q6.1--4] PROPOSED FOLLOW-UP: Investigate the plugin suite's host-sensitive performance budgets. Three npm test attempts each missed one different timing threshold: 41.258 ms vs 25 ms for the 200-link/2,000-task build; 16.17 ms vs 16 ms CPU charged to a 50 ms parked sleep; and taskLinks keystroke p95 12.7 ms vs 12 ms under host load 125.7/65.7/54.1 on 64 CPUs. The final attempt passed all unit tests (9,567 passed, 4 skipped) and 25/26 performance checks.

[2026-11-25T21:03:16Z · bob-cli-q6.1--4] PROPOSED FOLLOW-UP: Resolve the existing vault Git warning for .obsidian/plugins/bob-emoji. The final plugin sync reported 4 tracked files there, including data.json, main.js, and manifest.json; coordinate ignore and index cleanup across hosts because plugin sync does not untrack vault files.

[2026-11-25T21:04:04Z · bob-cli-q6.1--4] Verified: npm run build succeeded after the fast-forward. Real Obsidian album UI walkthrough, using TMPDIR=/tmp and the cache-built bob 0.6.0, passed 133 checks with 0 failed. npm test ran three times; the full suite was not green because each run missed one different performance threshold. Run 1: 200-link/2,000-task build measured 41.258 ms against 25 ms; 26/26 perf checks passed. Run 2: 50 ms parked sleep charged 16.17 ms CPU against 16 ms; 26/26 perf checks passed. Run 3: 9,567 unit tests passed and 4 skipped; 25/26 perf checks passed, with taskLinks keystroke p95 12.7 ms against 12 ms under host load 125.7/65.7/54.1 on 64 CPUs. Final docs:check failed on budgets: docs/develop/plugins/plugin-apis.md 9,279/8,000 (1,279 over), docs/reference/plugins/bob-ledger-tools.md 6,002/6,000 (2 over), docs/reference/plugins/bob-navigation-hotkeys.md 6,068/6,000 (68 over); all three pages are clean in this checkout’s git status/diff and follow-up notes are recorded. After fast-forwarding to 77bb466e and clean-syncing the protected plugin builds, final bob plugins sync succeeded: 3 copied, 31 unchanged, 0 skipped, 0 errors; it retained the existing bob-emoji tracked-files warning. Final epic-symbols check: no entries for bob-cli-q6.1.

## Dependencies

- **Blocks:** [bob-cli-q6.2](bob-cli-q6.2.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q6.5](bob-cli-q6.5.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q6.1.md) | [bob-cli-q6.1](bob-cli-q6.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1ff10aa`](https://github.com/bobs-org/bob-plugins/commit/1ff10aa40e7f0b5a1c290bbdfb1897466168fcd3) | feat(bob-ledger-tools): add shared property-card folding | [bob-cli-q6.1](bob-cli-q6.1.md) | 2026-11-25 13:59:27 EST |
| bob-plugins | [`bob-plugins@bdb85e3`](https://github.com/bobs-org/bob-plugins/commit/bdb85e34dca948c36e547937d45df3caabb5d50a) | fix(plugins): refine album schema and rebuild bundles | [bob-cli-q6.1](bob-cli-q6.1.md) | 2026-11-25 16:05:52 EST |
