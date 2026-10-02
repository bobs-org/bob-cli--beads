# Bead: bob-cli-3l.2 — Bob Mac Capture decoding, fixtures, and docs

[Bead Pages](../README.md) / [bob-cli-3l](README.md) / bob-cli-3l.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.47](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.47.md) · **Assignee:** `bob-cli-3l.2` · **Size:** small
**Created:** 2026-10-02 15:17:49 EDT · **Closed:** 2026-10-02 15:53:57 EDT
**Plan:** [202610/unnumbered\_close\_log\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/unnumbered_close_log_bullets.md)

## Description

mac: decode an absent `log[].index` as nil, add real-bob parse and preview fixtures plus tests for unnumbered bullets, and rewrite the README's Work Log bullet contract and syntax text; no grammar logic moves into Swift.

## Notes

[2026-10-02T19:53:57Z · bob-cli-3l.2] mac phase done in bob-mac-capture checkout: PomodoroCloseLogEntry.index is Int? (missing decodes nil); 4 real-bob fixtures (parse positional/unresolved/mixed + dry-run preview with typed_work_log on both worked rows) with fake-bob branches; 5 CaptureCore + 2 panel-model tests; README Work Log contract/syntax rewritten and hint fixed to inline =x 2 form. No Swift toolchain on host so macOS CI is the gate; verified compile-safety by grep (no prod code reads .index), fixture validity, fake-bob dispatch runs, and every new test assertion against real-bob JSON. epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-3l.1](bob-cli-3l.1.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3l.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3l.2/README.md) | [bob-cli-3l.2](bob-cli-3l.2.md) | 0 |
