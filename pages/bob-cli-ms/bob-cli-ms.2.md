# Bead: bob-cli-ms.2 — Guarded JSON envelope for bob records update

[Bead Pages](../README.md) / [bob-cli-ms](README.md) / bob-cli-ms.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.55.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.55.linker.w0.md) · **Assignee:** `bob-cli-ms.2` · **Size:** medium
**Created:** 2026-11-17 11:29:54 EST · **Closed:** 2026-11-17 15:39:13 EST
**Plan:** [202611/record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card.md)

## Description

record-envelope: add bob records update -i FILE, a guarded envelope of typed field.set/field.unset ops with an expect fingerprint, inverse ops, group consequence, and typed refusals (stale_record repaints in one call), plus an albums list capability flag, docs, tests, and just install.

## Notes

[2026-11-17T20:29:38Z · bob-cli-ms.2] PROPOSED FOLLOW-UP: docs-check lint budget over cap on docs/reference/json-outputs.md (6058 words on clean base, 6089 with the required envelope row; cap 6000) — same systemic overage already noted on bob-cli-lm.5; needs a docs budget trim, not a phase fix

[2026-11-17T20:39:13Z · bob-cli-ms.2] Guarded bob records update -i FILE envelope landed and verified. New records/protocol.rs parses the envelope (duplicate-key/field, unknown key/version/op, wrong type, empty-string-set refusals); ops convert to planner inputs with literal list members (new SuppliedLiteralValues variant through schema/plan/render, so comma members round-trip). execute_update -i branch checks expect before planning; stale_record embeds the current record object for one-call repaint; success/no-op/dry-run/refusal share the typed JSON doc (changed, changes, fingerprints, inverse_ops, groups, consequence, album_index, warnings, error). bob albums list|check -f json now carries capabilities [record_values_v1]. Completion kinds entry added for the new flag. Tests: 9 new CLI tests (set/unset/list/no-op, empty ops, stale+record, 4 typed + 6 protocol refusals, numbers/comma-lists/undo round-trip, dry-run/stdin/conflicts, CRLF/BOM, capability) plus protocol unit tests; lib 7292 passed, cli 3713 passed twice, clippy/fmt clean, docs-gen run, just install done and installed bob verified. docs-check lint budget failure is pre-existing on clean base (6058>6000, tracked on bob-cli-lm.5) and recorded as PROPOSED FOLLOW-UP on this bead. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-ms.1](bob-cli-ms.1.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-ms.4](bob-cli-ms.4.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.2/README.md) | [bob-cli-ms.2](bob-cli-ms.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`48a3116`](https://github.com/bobs-org/bob-cli/commit/48a3116d8aacce34fc3093c97048dcdcd913f7c1) | feat(records): guarded JSON envelope for bob records update | [bob-cli-ms.2](bob-cli-ms.2.md) | 2026-11-17 15:41:57 EST |
