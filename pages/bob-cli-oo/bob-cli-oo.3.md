# Bead: bob-cli-oo.3 — Pure note normalizer, write planner, and stage preview model

[Bead Pages](../README.md) / [bob-cli-oo](README.md) / bob-cli-oo.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5q.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5q.linker.w0.md) · **Assignee:** `bob-cli-oo.3` · **Size:** small
**Created:** 2026-11-21 12:07:08 EST · **Closed:** 2026-11-21 15:06:32 EST
**Plan:** [202611/bank\_row\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_row_notes.md)

## Description

note-writer: add the pure bankNoteNormalize, bankNoteWritePlan (with round-trip self-check), and bankNoteStagePreview helpers plus their test matrix; ordered after note-caption only to serialize bob-plugins builds and vault syncs.

## Notes

[2026-11-21T20:06:32Z · bob-cli-oo.3--2] Checks that passed:
- bankNoteNormalize, bankNoteWritePlan (round-trip self-check), and bankNoteStagePreview live in plugins/bob-ledger-tools/src/246a-plugin-bank-note-write.js and are exported.
- scripts/test-ledger-tools-bank-note-write.cjs: 6/6 pass (normalizer rewrites, insert/replace/remove across row shapes, CRLF, vector×shape inserts, structured/#task/stale refusals, preview copy).
- npm run build:check: all plugin entrypoints current, including bob-ledger-tools.
- bob plugins sync --repo linked/bob-plugins --no-pull --dry-run -p bob-ledger-tools: vault up to date (0 to copy, 3 unchanged) after the landed-build path for cb70f829 plus rebuild/final sync.
- Isolated rerun of the two full-suite failures: scripts/test-ledger-tools-event-link-times.cjs and scripts/test-ledger-tools-frees-marks.cjs, 40/40 pass. The 25 ms budgets measured 4.3 ms and 18.2 ms; the earlier 69.8 ms / 135 ms misses were host-load flakes during npm test, not a bank-note regression. Dedicated npm run test:perf was 13/13 on that same suite run.
- Shared successor fixture refresh is on origin/master (909b30fd); bob-plugins and bob-cli worktrees are clean.
- sase bead epic-symbols bob-cli-oo.3: no leftover --epic-symbol entries.
Parent epic bob-cli-oo left open.

## Dependencies

- **Depends on:** [bob-cli-oo.2](bob-cli-oo.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oo.4](bob-cli-oo.4.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oo.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oo.3.md) | [bob-cli-oo.3](bob-cli-oo.3.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dfe20ca`](https://github.com/bobs-org/bob-cli/commit/dfe20ca3040b1328b7356083fbb0f8afd4d97d80) | docs(glossary): describe bank row notes | [bob-cli-oo.3](bob-cli-oo.3.md) | 2026-11-21 14:36:44 EST |
| bob-plugins | [`bob-plugins@303e5db`](https://github.com/bobs-org/bob-plugins/commit/303e5dbf534dea3e8225b0f12941e928ddf4490d) | feat(bank): add pure row note write model | [bob-cli-oo.3](bob-cli-oo.3.md) | 2026-11-21 14:44:10 EST |
| bob-plugins | [`bob-plugins@909b30f`](https://github.com/bobs-org/bob-plugins/commit/909b30fdfa004886445f97eed1fa70ec78d103fc) | test(task-status-cycler): refresh shared successor fixture | [bob-cli-oo.3](bob-cli-oo.3.md) | 2026-11-21 14:58:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oo.3--1][1] | Continue the phase after the monitored plugin test result; need scope, notes, and closeout requirements | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oo.3.md

<!-- sase:referenced-by:end -->
