# Bead: bob-cli-re.5 — Clean spaced Amazon order codes without erasing sub-merchants

[Bead Pages](../README.md) / [bob-cli-re](README.md) / bob-cli-re.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r8.land.md) · **Assignee:** `bob-cli-re.5` · **Size:** small
**Created:** 2026-11-27 15:31:19 EST · **Closed:** 2026-11-27 18:34:04 EST
**Plan:** [202611/task\_bead\_burndown\_3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_3.md)

## Description

spaced-order-code: extend the conservative bank-name cleaner and close bob-cli-qx.

## Notes

[2026-11-27T23:34:04Z · bob-cli-re.5] Extended strip_processor_order_code with a peekable token walk so WORD* CODE drops the star and one short digit-bearing code. Wells Fargo AMAZON RETA* BV5NH / UE4V4 both clean to AMAZON RETA (merchant_key amazon reta); learned naming reuses that key on synthetic import_plan transactions. Preserved DELIVERY *SUSHI, glued codes, trailing lone stars, oversized/non-code suffixes, masked ••••, never-empty fallback. No journal migration. epic-symbols: none. Closed bob-cli-qx. Verified cargo test naming/identity/import_plan and sase tool run check 74177a6e912475955d8cdf4c550280c4 succeeded.

## Dependencies

- **Depends on:** [bob-cli-re.4](bob-cli-re.4.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-re.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.5/README.md) | [bob-cli-re.5](bob-cli-re.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`befff97`](https://github.com/bobs-org/bob-cli/commit/befff97c0ab276059b129ba52bf01174b405c5a9) | fix(bank): strip spaced Amazon processor order codes | [bob-cli-re.5](bob-cli-re.5.md) | 2026-11-27 18:35:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-re.5][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.5/README.md

<!-- sase:referenced-by:end -->
