# Bead: bob-cli-oe.8.1 — bob capture jump landing finds the right ID-less task

[Bead Pages](../README.md) / [bob-cli-oe.8](bob-cli-oe.8.md) / bob-cli-oe.8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-oe.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oe.land.md) · **Assignee:** `bob-cli-oe.8.1` · **Size:** small
**Created:** 2026-11-20 21:39:29 EST · **Closed:** 2026-11-20 22:17:00 EST
**Plan:** [202611/successor\_jump\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_repairs.md)

## Description

cli-jump-identity: make the top-level jump landing settle a correct identity for every ID-less offer row, failing closed to a null landing; use the duplicate-refusing block-ID lookup; add the missing JS vectors; and complete §12.24 with the shared semantics, commit table, and precedence.

## Notes

[2026-11-21T03:16:42Z · bob-cli-oe.8.1] PROPOSED FOLLOW-UP: just docs-check still fails on docs/reference/vault-format.md 6016/6000 — reproduces on the clean tree, file untouched here, already tracked as bob-cli-oc

[2026-11-21T03:17:00Z · bob-cli-oe.8.1] Jump landing settles every ID-less offer via a shared ordinal helper and duplicate-refusing block-ID lookup; JS1/JS9 tightened; JS11–JS15 added (JS14 unit). Verified: successor_jump 14; jump unit twins/dup/JS14; help_options 35; flag_guard 11; note_pull 12; cargo test --lib -- capture 2160; just lint green. just docs-check fails only on known vault-format.md budget (bob-cli-oc). §12.24 shared semantics, commit table, and precedence landed. No epic symbols.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oe.8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oe.8.1.md) | [bob-cli-oe.8.1](bob-cli-oe.8.1.md) | 0 |
