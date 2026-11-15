# Bead: bob-cli-ls.2.1.3 — Guarded loaders, row JSON, suggestions, and documentation

[Bead Pages](../README.md) / [bob-cli-ls.2.1](bob-cli-ls.2.1.md) / bob-cli-ls.2.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ls.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.md) · **Assignee:** `bob-cli-ls.2.1.3` · **Size:** medium
**Created:** 2026-11-15 13:23:49 EST · **Closed:** 2026-11-15 16:49:26 EST
**Plan:** [202611/subscription\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subscription_core.md)

## Description

integrate: generalize the guarded restaurant loader, integrate the shared subscription snapshot into list/report/import row JSON and category suggestions, surface bounded availability warnings, document the contract, and verify the full core scope.

## Notes

[2026-11-15T21:49:06Z · bob-cli-ls.2.1.3] PROPOSED FOLLOW-UP: just docs-check fails on docs/reference/plugins/bob-ledger-tools.md budget (6055 words vs 6000 cap); file is git-ignored and untouched by this phase, failure is independent of subscription core changes

[2026-11-15T21:49:26Z · bob-cli-ls.2.1.3] Integrate phase done: guarded record-link loader (restaurants+subscriptions, one RecordContext, byte-guarded parse, invalid warns once), shared subscription projection into list/report/import row JSON (subscription/bank_recurring/candidate, drift/price/state, rule>subscription>learned/bank, hidden/unknown never suggested), bounded bank_subscription_album_invalid warning in list/report JSON+human and bank check, docs Subscriptions+row JSON+suggestion sources, tests: lib bank 223 pass, subscriptions 38 pass, projection 8 pass, cli bank 13 pass, fmt+clippy clean, epic-symbols clean; just docs-check fails only on ignored plugins doc budget (recorded as follow-up)

## Dependencies

- **Depends on:** [bob-cli-ls.2.1.1](bob-cli-ls.2.1.1.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-ls.2.1.2](bob-cli-ls.2.1.2.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.2.1.3/README.md) | [bob-cli-ls.2.1.3](bob-cli-ls.2.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`055f9b6`](https://github.com/bobs-org/bob-cli/commit/055f9b6e0558c8458ac37a20d0533f22ac4d5d77) | feat(bank): integrate subscription core into rows, suggestions, and docs | [bob-cli-ls.2.1.3](bob-cli-ls.2.1.3.md) | 2026-11-15 16:51:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ls.2.1.3][1] | Need remaining integrate scope and notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.2.1.3/README.md

<!-- sase:referenced-by:end -->
