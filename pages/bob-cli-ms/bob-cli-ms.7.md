# Bead: bob-cli-ms.7 — Entry points, == on records, and the Properties hide

[Bead Pages](../README.md) / [bob-cli-ms](README.md) / bob-cli-ms.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.55.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.55.linker.w0.md) · **Assignee:** `bob-cli-ms.7` · **Size:** medium
**Created:** 2026-11-17 11:29:54 EST · **Closed:** 2026-11-17 21:53:07 EST
**Plan:** [202611/record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card.md)

## Description

record-entry: wire the sheet's Edit, row, chip, ghost, and missing affordances; == on records; the edit-record palette command; Ctrl+Shift+P in navigation hotkeys; the Command Mode row; and switch on the fail-open Properties hide (and the inline-title decision).

## Notes

[2026-11-17T21:56:38Z · eo.f0--code] Per approved plan:202611/record_card_field_jump_co_landing.md (reviewer: record_card_digits=pick, climb_keeps_field=yes, scoped_force=yes).

6. Deploy discipline. Vault unwedged at f80d0dd (clean origin/master, 1.130.0; old stamp bob-cli_15 dirty b0a9c89, backup /home/bryan/.local/state/bob-cli/plugin-backups/20261117-165532). Fetch+merge origin/master and npm run build before every sync; sync final tree. Refusal rule: Bryan pre-authorizes -F for bob-ledger-tools, bob-navigation-hotkeys, bob-command-mode for rest of both epics only when stamped root exists+clean, HEAD ancestor of origin/master, author phase closed, deploying clean origin/master (stash, ff, build:check, sync -F, pop, rebuild, sync again). Note old stamp + backup afterwards; otherwise AGENTS.md.

7. Merge friction. Keep both epics' test:unit entries; rebuild main.js, never hand-merge; ms takes next free minor.

[2026-11-18T02:52:44Z · bob-cli-ms.7] PROPOSED FOLLOW-UP: Pin record-sheet rollover test to fixture date — scripts/test-ledger-tools-record-sheet.cjs midnight rollover fails any day other than 2026-11-17 because setupRecordSheet resets recordSheetDay to real today; fails identically on clean base.

[2026-11-18T02:52:50Z · bob-cli-ms.7] PROPOSED FOLLOW-UP: Triage perf-budget flakes under full-suite load — 4 wall-clock tests (event-link-times 200-link builds, frees-marks ledger build) fail in full npm run test:unit but pass in isolation on both trees; fails identically on clean base.

[2026-11-18T02:52:56Z · bob-cli-ms.7] PROPOSED FOLLOW-UP: Regenerate bob-cli docs/reference/glossary.md — docs:check reports generated drift on clean base too (lint passes); out of record-entry scope which touches only the plugin repo.

[2026-11-18T02:53:07Z · bob-cli-ms.7] record-entry done and deployed: sheet Edit/row/chip/ghost/missing affordances with keyboard activation, == opens Record Card on canonical records (bank-month keeps reindent), Ctrl+Shift+P record-parent branch, Command Mode edit-record row, fail-open Properties hide (+inline-title, embeds exempt). Tests: 14 new pass; full plugin suite 7292/7300 with only the 5 pre-existing base-identical failures (recorded as follow-ups). Gates: build, docs:gen, validate, docs:check lint pass; glossary drift pre-existing. Versions 1.133.0/2.87.0/0.2.0. Sync: 7 copied, backups 20261117-215148, no -F. just check not re-run (zero Rust changes; c50f8895 verified green by ms.6).

## Dependencies

- **Depends on:** [bob-cli-ms.6](bob-cli-ms.6.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.7/README.md) | [bob-cli-ms.7](bob-cli-ms.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f8a8619`](https://github.com/bobs-org/bob-plugins/commit/f8a86196b4b97a92262a71f3872bccd77a85f3ef) | feat(record-sheet): sheet affordances, record card entrypoints and properties hide | [bob-cli-ms.7](bob-cli-ms.7.md) | 2026-11-17 21:55:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ms.7][1] | Need the phase scope and design file | 2 |
| read-by | [agent:eo.f0--code][2] | Need phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.eo.f0.md

<!-- sase:referenced-by:end -->
