# Bead: bob-cli-66.1 — bob capture-pomodoros --tasks returns the resolved agenda

[Bead Pages](../README.md) / [bob-cli-66](README.md) / bob-cli-66.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.48.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.48.linker.w0.md) · **Assignee:** `bob-cli-66.1` · **Size:** medium
**Created:** 2026-10-09 17:42:22 EDT · **Closed:** 2026-10-09 18:22:38 EDT
**Plan:** [202610/idle\_capture\_pomodoro\_agenda.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/idle_capture_pomodoro_agenda.md)

## Description

cli-agenda: add the additive `-t/--tasks` flag to `bob capture-pomodoros`. It returns roles, role-specific operator numbers, resolved Task Links with clean titles, statuses, and log-tagged block lines, plus ledger notes, session notes, retired counts, the date, and a completed summary. One memoized pass, deterministic bytes, colored human output, docs, golden fixtures, and a read-count perf gate.

## Notes

[2026-10-09T22:19:39Z · bob-cli-66.1] cli-agenda done: -t/--tasks on bob capture-pomodoros returns date, completed_summary, and per-entry role/starts_at/ends_at/retired_link_count/notes/items with full resolution enum, memoized one-read-per-note-per-mode pass, deterministic bytes, colored human output, docs/capture.md contract, 6 goldens in tests/fixtures/capture_pomodoros/, read-count gate (8 reads for 25 links/4 notes/2 modes), <250ms September-shape guard. just check green (2144 lib + 1305 cli). hyperfine release: live vault mean 5.1ms p95 8.8ms (target <=15ms); heavy fixture mean 4.3ms p95 5.2ms (target <=30ms).

[2026-10-09T22:22:38Z · bob-cli-66.1] cli-agenda verified: just check green (2144 lib incl 30 agenda tests, 1305 cli incl 9 agenda goldens/parity tests); =x/= numbering parity proven against dry-run lineups; default JSON byte-identical; hyperfine release live 5.1ms mean/8.8ms p95, heavy 4.3ms mean/5.2ms p95; no epic-symbol leftovers

## Dependencies

- **Blocks:** [bob-cli-66.2](bob-cli-66.2.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-66.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-66.1/README.md) | [bob-cli-66.1](bob-cli-66.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6562b71`](https://github.com/bobs-org/bob-cli/commit/6562b71410672b9a32c790cd8215152d3fbe7eec) | feat(agenda): add -t/--tasks resolved agenda to bob capture-pomodoros | [bob-cli-66.1](bob-cli-66.1.md) | 2026-10-09 18:23:54 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-66.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-66.1/README.md

<!-- sase:referenced-by:end -->
