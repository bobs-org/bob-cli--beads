# Bead: bob-cli-lc.6 — The Category card, the walk, and Bank set category

[Bead Pages](../README.md) / [bob-cli-lc](README.md) / bob-cli-lc.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c7.md) · **Assignee:** `bob-cli-lc.6` · **Size:** medium
**Created:** 2026-11-13 10:55:28 EST · **Closed:** 2026-11-13 14:09:39 EST
**Plan:** [202611/bank\_weekly\_category\_walk.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_weekly_category_walk.md)

## Description

card-ui: render the Category card in the key-card family, wire api.bank v2 claimRowClose and setCategory, commit, advance, refresh suggestions after each filing, show the end-of-run notice, add Bank: set category, hide hidden categories from [cat:: suggestions, and land waiting-pill jumps at the payee.

## Notes

[2026-11-13T19:09:18Z · bob-cli-lc.6] PROPOSED FOLLOW-UP: existing verification issues remain tracked by bob-cli-il and bob-cli-jz (docs:check: Ledger Tools 6115/6000 and navigation-hotkeys 6021/6000) and bob-cli-ki (keep-moving 200-link timing assertion failed at 631.5 ms in full npm test; isolated file passed 14/14). The unit suite otherwise passed 6519/6522 tests with two skips; build check, generated docs inventory, and five perf tests passed.

[2026-11-13T19:09:39Z · bob-cli-lc.6] Implemented and deployed api.bank v2 Category card, one-gesture claim-and-file, set-category command, hidden-category filtering, payee landing, and end-of-walk reporting. npm build and docs inventory passed; feature tests are included in the passing unit suite. Logged existing docs budget and full-suite timing failures as proposed follow-ups linked to bob-cli-il, bob-cli-jz, and bob-cli-ki. epic-symbol check was clear.

## Dependencies

- **Depends on:** [bob-cli-lc.5](bob-cli-lc.5.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-lc.7](bob-cli-lc.7.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lc.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.6/README.md) | [bob-cli-lc.6](bob-cli-lc.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a1dee92`](https://github.com/bobs-org/bob-cli/commit/a1dee92f8b77e889cab63adfeb67423ea0a598ff) | docs(memory): document bank category gesture | [bob-cli-lc.6](bob-cli-lc.6.md) | 2026-11-13 14:12:00 EST |
| bob-plugins | [`bob-plugins@0b1000b`](https://github.com/bobs-org/bob-plugins/commit/0b1000bd344e1d065793fe0b8ef4f96fa07f9027) | feat(bank): add Category card workflow | [bob-cli-lc.6](bob-cli-lc.6.md) | 2026-11-13 14:12:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lc.5][1] | Need to see card-ui scope to avoid overlap with card-model | 1 |
| read-by | [agent:bob-cli-lc.6][2] | Check phase notes for earlier work and remaining scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lc.6/README.md

<!-- sase:referenced-by:end -->
