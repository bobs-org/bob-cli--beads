# Bead: bob-cli-q6.5 — The \`\_\` key reaches record, area, and project folds

[Bead Pages](../README.md) / [bob-cli-q6](README.md) / bob-cli-q6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g2.md) · **Assignee:** `bob-cli-q6.5` · **Size:** medium
**Created:** 2026-11-25 12:49:32 EST · **Closed:** 2026-11-25 16:39:24 EST
**Plan:** [202611/bank\_property\_card\_fold.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_property_card_fold.md)

## Description

fold-family: register record, area, and project folds with the kit (look per family_fold_look), give the foot's `-` disclosure the same hover keycap, and cover each kind in unit and e2e tests and docs.

## Notes

[2026-11-25T21:39:00Z · bob-cli-q6.5] PROPOSED FOLLOW-UP: docs:check lint fails on origin for bob-navigation-hotkeys.md (6068/6000) and bob-ledger-tools.md (already 6002 before this phase; bank-fold copy on master then 6026). Reproduces on clean tree; do not keep fold-family open.

[2026-11-25T21:39:24Z · bob-cli-q6.5] Compact fold-family: record/area/project chevrons use the shared kit (boolean-compat Maps, hidden aria-controls shells, hover _ keycaps); foot - keycap when keyLive. Unit tests cover FromStored, compact decorate, registration, and shifted _ on record/area/project plus day/period fall-through. npm test 9649 pass / 0 fail / 4 skip; perf 26/26. Offline home/record e2e wrappers green. Live Obsidian _ round trips not run. Docs name _ on inventory, record, and area/project pages. Bumped 1.164.0 (bank-fold) to 1.165.0; bob plugins sync --no-pull -p bob-ledger-tools after ff-only onto fbe5fd8/1c2534c. docs:check still fails origin budgets (nav 6068, ledger 6026 after bank-fold copy); noted as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-q6.1](bob-cli-q6.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q6.6](bob-cli-q6.6.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q6.5/README.md) | [bob-cli-q6.5](bob-cli-q6.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a71a59d`](https://github.com/bobs-org/bob-plugins/commit/a71a59dba5f13bb4831af19bb336a60b77c7654f) | feat(bob-ledger-tools): fold record, area, and project details with \_ | [bob-cli-q6.5](bob-cli-q6.5.md) | 2026-11-25 16:40:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q6.5][1] | Need notes and remaining work JSON | 7 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q6.5/README.md

<!-- sase:referenced-by:end -->
