# Bead: bob-cli-at.2 — Coordination config, reading-activity probe, and budgets

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.2` · **Size:** small
**Created:** 2026-10-23 11:44:15 EDT · **Closed:** 2026-10-23 12:20:17 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

policy: parse `highlights.coordinate_pdf_writes` (bool, default false) into `HighlightsConfig`. Add a reading-activity probe: on macOS, `lsappinfo` for the frontmost bundle id (any `net.highlightsapp.*`) and `ioreg` `HIDIdleTime`, each bounded at 2 s; elsewhere it always reports not reading. The output parsers are pure and unit-tested, a probe failure reports unknown, and internal env overrides exist for tests. Add the budget constants: 10 s per PDF, a 30 s scan cap, and a 30 s reading window, each with an internal env override. Bundle these into one `PdfWritePolicy` value, built once per command. Nothing consumes it yet.

## Notes

[2026-10-23T16:20:17Z · bob-cli-at.2--2] Verified policy phase: HighlightsConfig parses highlights.coordinate_pdf_writes (default false); PdfWritePolicy bundles that flag with 10s/30s/30s budgets, lazy macOS lsappinfo+ioreg reading probe (2s bound, unknown on failure, Away off macOS), pure unit-tested parsers, and internal env overrides. Module is staged (nothing consumes it). just check passed (monitor 33727rqxjwv7, exit 0). No --epic-symbol leftovers. Decision strand left to bob-cli-at.7 as the plan's accept phase owns it; --attended is executor (bob-cli-at.3).

## Dependencies

- **Blocks:** [bob-cli-at.3](bob-cli-at.3.md) ◐ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-at.2.md) | [bob-cli-at.2](bob-cli-at.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6480e7c`](https://github.com/bobs-org/bob-cli/commit/6480e7cc7c84d168559cad6b4d3ec9c5831af3d6) | feat(highlights-ref): stage PDF write policy and reading-activity probe | [bob-cli-at.2](bob-cli-at.2.md) | 2026-10-23 12:21:55 EDT |
