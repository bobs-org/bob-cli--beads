# Bead: bob-cli-ir.4 — Restaurant and podcast schemas go live in config and the vault

[Bead Pages](../README.md) / [bob-cli-ir](README.md) / bob-cli-ir.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1a0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1a0.md) · **Assignee:** `bob-cli-ir.4` · **Size:** small
**Created:** 2026-11-08 11:06:12 EST · **Closed:** 2026-11-08 19:24:19 EST
**Plan:** [202611/record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_notes.md)

## Description

records-vault: add the restaurant and podcast records config through chezmoi, teach eat.base and podcasts.base the to_try status, point the type notes at bob records show, and report the check findings.

## Notes

[2026-11-09T00:24:07Z · bob-cli-ir.4] PROPOSED FOLLOW-UP: just check is red on the clean tree from a clippy redundant-closure deny in src/native/records/cli.rs:112 (landed by bob-cli-ir.3); fix the closure or add an allow so the gate goes green

[2026-11-09T00:24:19Z · bob-cli-ir.4] records-vault done: restaurant+podcast config shipped via chezmoi (0d3e43fb), applied, list shows 92+15; eat.base/podcasts.base/type notes/types.json updated; check finds 8 pre-existing errors + 3 warnings (nothing fixed, per plan); seeded 11 to_try records from maybe_eat.md (1950 Originals skipped, exists), historical line added; records tests green (23 CLI + 91 lib); just check red from pre-existing clippy deny in ir.3 file, recorded as follow-up; vault synced

## Dependencies

- **Depends on:** [bob-cli-ir.3](bob-cli-ir.3.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ir.9](bob-cli-ir.9.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.4/README.md) | [bob-cli-ir.4](bob-cli-ir.4.md) | 0 |
