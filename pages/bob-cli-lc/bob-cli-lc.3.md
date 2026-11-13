# Bead: bob-cli-lc.3 — Category hotkeys, groups, hidden, and row suggestions

[Bead Pages](../README.md) / [bob-cli-lc](README.md) / bob-cli-lc.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c7.md) · **Assignee:** `bob-cli-lc.3` · **Size:** medium
**Created:** 2026-11-13 10:55:28 EST · **Closed:** 2026-11-13 13:00:39 EST
**Plan:** [202611/bank\_weekly\_category\_walk.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_weekly_category_walk.md)

## Description

category-contract: add the mapping form for bank.categories (label, hotkey, group, hidden) with derivation and validation, report hotkey/group/hidden in categories[], add a read-time suggestion {category, source} to every row JSON from one function shared with import, and point import's next step at the walk.

## Notes

[2026-11-13T18:00:10Z · bob-cli-lc.3] PROPOSED FOLLOW-UP: just lint fails identically on the clean base tree with 5 clippy deny-errors in src/native/gmail/unarchive.rs (needless_borrow at 283 twice, 313, 330; useless_conversion at 464) — already tracked by closed bob-cli-kx.3.1.4 / parent bob-cli-kx.

[2026-11-13T18:00:20Z · bob-cli-lc.3] PROPOSED FOLLOW-UP: just docs-check fails identically on the clean base tree: mounted plugins/bob-ledger-tools.md 6136/6000 and bob-navigation-hotkeys.md 6082/6000 — already tracked by closed bob-cli-lc.2.

[2026-11-13T18:00:39Z · bob-cli-lc.3] Verified mapping-form bank.categories (label/hotkey/group/hidden) with derivation and validation; categories[] JSON reports hotkey, group, hidden; shared suggest_category on list/report/import rows (rule > learned > bank, waiting never teach, 4+ digit rules skipped at read time); import Next: names the oldest waiting month plus extra months. cargo test --lib native::bank: 135 passed; cargo test --test cli bank: 8 passed including mapping_categories_report_hotkeys_and_hidden_stays_valid and import_writes_shared_suggestion_and_points_next_at_the_walk. just fmt ok. No --epic-symbol leftovers. just lint and just docs-check fail identically on the clean base tree (recorded as PROPOSED FOLLOW-UP). Did not edit glossary:bank-row or vault bank.md.

## Dependencies

- **Depends on:** [bob-cli-lc.2](bob-cli-lc.2.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-lc.4](bob-cli-lc.4.md) ◐ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-lc.5](bob-cli-lc.5.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.3/README.md) | [bob-cli-lc.3](bob-cli-lc.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1501c0c`](https://github.com/bobs-org/bob-cli/commit/1501c0c3e00792a27df81df4aa85caf73183002f) | feat(bank): add category hotkeys, groups, hidden, and row suggestions | [bob-cli-lc.3](bob-cli-lc.3.md) | 2026-11-13 13:03:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lc.3][1] | Need notes for leftover work before deciding close vs child epic | 8 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.3/README.md

<!-- sase:referenced-by:end -->
