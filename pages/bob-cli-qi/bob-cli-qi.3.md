# Bead: bob-cli-qi.3 — Delete the bank/area arbitration and restore the single-owner Bank Card

[Bead Pages](../README.md) / [bob-cli-qi](README.md) / bob-cli-qi.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gn.md) · **Assignee:** `bob-cli-qi.3` · **Size:** medium
**Created:** 2026-11-26 10:06:12 EST · **Closed:** 2026-11-26 10:52:26 EST
**Plan:** [202611/bank\_hub\_demotion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_hub_demotion.md)

## Description

plugin-single-owner: delete 249db and every bank/area arbitration hook in bob-ledger-tools, restore the bank.md home-card exclusion, and gate bank on props_v1. Bank becomes a no-settings Property Editor kind whatever bob reports. Settle the 240r foot lifecycle by a species-agnostic test, convert the hybrid unit and e2e cases, fix the baseline harness blockers, then build, test, and sync.

## Notes

[2026-11-26T15:46:58Z · bob-cli-qi.3--1] PROPOSED FOLLOW-UP: Repair the block-id-prompt generated bundle/source mismatch — `npm test` on clean bob-plugins HEAD `4e0a8fd0e96453a6c92ca8293dfa0c964d1f6111` exits 1 before unit/perf tests because `node scripts/build-plugins.mjs --check` reports `plugins/block-id-prompt/main.js` stale; this plugin is outside the bank phase.

[2026-11-26T15:52:20Z · bob-cli-qi.3--1] 240r verification: `node --test scripts/test-ledger-tools-property-card-foot-adapters.cjs` passed 9/9. The species-agnostic Album pane test closes one pane, prunes only its detached mount, keeps the peer foot actionable, then reopens the same note with a fresh foot beside the peer; both panes share disclosure state. `BOB_CLI_DIR=... npm run docs:check` passed (447 passed, 1 skipped); `bob plugins sync` completed without `-F`; `bob plugins list` reports 12 synced, 0 drift; the required arbitration guard returned no matches; `sase bead epic-symbols bob-cli-qi.3` reports no entries. The full `npm test` clean-base stale-bundle failure is recorded in a separate PROPOSED FOLLOW-UP note.

[2026-11-26T15:52:26Z · bob-cli-qi.3--1] Verified plugin single-owner phase: docs:check passed; no-force plugin sync and 12-plugin zero-drift list passed; arbitration guard empty; 240r species-agnostic Album close/reopen test passed in the 9/9 foot-adapter suite. Full npm test was blocked before unit/perf tests by the unrelated clean-base block-id-prompt stale bundle at 4e0a8fd0e96453a6c92ca8293dfa0c964d1f6111; recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-qi.4](bob-cli-qi.4.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qi.5](bob-cli-qi.5.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qi.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qi.3.md) | [bob-cli-qi.3](bob-cli-qi.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8e6a5a6`](https://github.com/bobs-org/bob-plugins/commit/8e6a5a61908bb5eac13584536fa6f564b7464617) | refactor(plugins): restore single-owner Bank Card | [bob-cli-qi.3](bob-cli-qi.3.md) | 2026-11-26 10:40:24 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qi.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qi.land.md

<!-- sase:referenced-by:end -->
