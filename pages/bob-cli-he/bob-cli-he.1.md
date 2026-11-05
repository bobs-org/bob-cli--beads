# Bead: bob-cli-he.1 — History providers, Alfred adapter, Clipy fixes, and config selection

[Bead Pages](../README.md) / [bob-cli-he](README.md) / bob-cli-he.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5r.linker.w0.md) · **Assignee:** `bob-cli-he.1` · **Size:** medium
**Created:** 2026-11-05 10:29:53 EST · **Closed:** 2026-11-05 11:44:47 EST
**Plan:** [202611/percent\_c\_history\_agreement.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/percent_c_history_agreement.md)

## Description

providers: add the HistoryEntry provider boundary, a read-only Alfred adapter, the Clipy tie-break/flavor/concealed fixes, and capture.clipboard_history selection.

## Notes

[2026-11-05T16:16:03Z · bob-cli-he.1] PROPOSED FOLLOW-UP: just docs-check tutorial gate fails identically on clean base (TUTORIAL_FENCE 12 docs/start/first-bob-day.md:117, =#focus retired error); needs a tutorial/content fix outside this phase

[2026-11-05T16:44:21Z · bob-cli-he.1] macOS CI gate (run 42065661442 on this phase snapshot): package success, lint success, Lint macOS-only targets success (proves alfred.rs/clipy.rs compile on the macOS target); macOS Run tests did not finish because the single-turn timebox expired and I cancelled the run to stop burning CI; remote ci/precommit branch deleted. Full `just check` (fmt+clippy+workspace tests) passes locally.

[2026-11-05T16:44:47Z · bob-cli-he.1] Providers phase done and verified. New history.rs provider boundary (HistoryEntry/EntryKind/ProviderError/HistoryProvider + pure env>config>auto selection with source); new read-only alfred.rs adapter (Cocoa epoch +978307200, ts/rowid order, dataType 0 text else NotText, busy_timeout, Missing/Busy/Unsupported); clipy.rs fixes (rowid tie-break, lazy skip of concealed/transient uncounted, one canonical flavor with multi-asset join, binary-only rows NotText, at from updateAt); capture.clipboard_history + clipboard_history_command parsed independently of max_saved_templates; interim wiring reads first candidate, keeps merge, indexed file-or-image errors; cli help + capture.md + configuration.md + docs-gen golden updated. Verified: just check fully green (fmt, clippy -D unused, full workspace tests incl 30 capture_clip + 9 config + new config-selection CLI test + existing no-provider/history-failure CLI tests); docs-check gates green except pre-existing first-bob-day tutorial failure identical on clean base (recorded as follow-up); macOS CI on this snapshot: package/lint/macOS-only-targets lint green, full macOS test run cancelled on single-turn timebox and recorded (run 42065661442, branch deleted). No Cargo/Changelog edits. No epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-he.2](bob-cli-he.2.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-he.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-he.1/README.md) | [bob-cli-he.1](bob-cli-he.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5a6519f`](https://github.com/bobs-org/bob-cli/commit/5a6519f1914714fca543ead8c1e4a39d3832a1e9) | feat(capture): add clipboard history providers (history boundary, Alfred and Clipy adapters) | [bob-cli-he.1](bob-cli-he.1.md) | 2026-11-05 11:47:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-he.1][1] | check status and notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-he.1/README.md

<!-- sase:referenced-by:end -->
