# Bead: bob-cli-ms.3 — Read-only record sheet under the H1 (Live Preview and Reading)

[Bead Pages](../README.md) / [bob-cli-ms](README.md) / bob-cli-ms.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.55.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.55.linker.w0.md) · **Assignee:** `bob-cli-ms.3` · **Size:** large
**Created:** 2026-11-17 11:29:54 EST · **Closed:** 2026-11-17 13:49:10 EST
**Plan:** [202611/record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card.md)

## Description

record-sheet: render the record sheet after the first H1 of canonical album records from metadataCache and the cached album report (no subprocess on open), covering values by kind, lint, ghost chips, a read-only fold, a created footer, collapse, subscription docking, light/dark/375px, and a tested hide gate that is not yet applied.

## Notes

[2026-11-17T18:49:10Z · bob-cli-ms.3] Shipped the read-only record sheet in bob-ledger-tools 1.129.0 (plan:202611/record_sheet.md). Canonical desktop album records paint a sheet under the first H1 in Live Preview and Reading from metadataCache plus the cached album report. Hide class stays dormant. Subscription headers yield and dock. YAML `y` jumps without a Schema Card excursion.

Verified:
- 15 record-sheet unit tests pass, including midnight-rollover (no hanging timeout).
- 158 related tests pass (record-sheet + album-header/entrypoints/records + subscription surfaces + note-ready + period-strip/charts). The last three used to hang because setupRecordSheet scheduled a repeating 60s albumSetTimeout on every onload(); midnight now rides the existing window-gated plugin rollover.
- Isolated keep-moving / event-link-times / frees-marks budget tests pass (60/60).
- npm run validate and BOB_CLI_DIR docs:check pass.
- 375px light/dark fixture rendered with wkhtmltoimage (labels stack, missing pill, ghost chips, 8px radius).
- Deployed with `bob plugins sync --repo $PWD --no-pull -p bob-ledger-tools` to ~/bob (backup 20261117-134830).

PROPOSED FOLLOW-UP: keep-moving / event-link-times / frees-marks 25ms (and KT1 1000ms) budget tests flake under full `npm test` process-isolation load (elapsed 344–3436ms on this run) and pass in isolation (6.8–123ms). Load-sensitive, not a record-sheet regression.

## Dependencies

- **Blocks:** [bob-cli-ms.4](bob-cli-ms.4.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.3.md) | [bob-cli-ms.3](bob-cli-ms.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@60b5602`](https://github.com/bobs-org/bob-plugins/commit/60b5602130e4655efdf0b2dda2e6c1afcc5234ae) | feat(ledger-tools): render a read-only record sheet under album H1s | [bob-cli-ms.3](bob-cli-ms.3.md) | 2026-11-17 14:39:27 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ms.3--1][1] | Need assigned phase status, notes, and close eligibility after host-completion refusal | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.3.md

<!-- sase:referenced-by:end -->
