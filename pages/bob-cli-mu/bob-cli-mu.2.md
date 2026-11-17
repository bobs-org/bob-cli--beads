# Bead: bob-cli-mu.2 — Numbered field keycaps, heading rows, and group rhythm

[Bead Pages](../README.md) / [bob-cli-mu](README.md) / bob-cli-mu.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.57.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.57.linker.w0.md) · **Assignee:** `bob-cli-mu.2` · **Size:** medium
**Created:** 2026-11-17 15:36:25 EST · **Closed:** 2026-11-17 16:25:34 EST
**Plan:** [202611/schema\_card\_field\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_card_field_jumps.md)

## Description

field-visuals: paint keycaps for fields 1–9 with current-group emphasis, make field rows transparent headings, add dialog-scoped group spacing and a shared label axis, add the field hint item and row accessibility, then check geometry and screenshots in real Obsidian and update the visual docs.

## Notes

[2026-11-17T21:25:08Z · bob-cli-mu.2] PROPOSED FOLLOW-UP: Full npm test 25ms ledger-mark budgets flake under suite load — event-link-times, frees-marks, keep-moving-marks-surface, and off-clock-link-chips failed in the parallel run and passed in isolation; already tracked by bob-cli-km, bob-cli-io, bob-cli-ki, and bob-cli-ju.

[2026-11-17T21:25:17Z · bob-cli-mu.2] PROPOSED FOLLOW-UP: npm run docs:check fails on docs/reference/json-outputs.md 6089/6000 words on cached bob-cli master, identical to the clean-base failure already noted on bob-cli-ms.4 and bob-cli-mr.3.1.3.

[2026-11-17T21:25:25Z · bob-cli-mu.2] Vault sync refused: bob-ledger-tools is protected by an uncommitted deploy from bob-cli_15 (b0a9c89, dirty, 2026-11-17T18:48:30Z). Followed the no -F protocol; that checkout is not a running agent. Field-visuals is in the bob-plugins tree for host commit; deploy after that stamp lands or is replaced.

[2026-11-17T21:25:34Z · bob-cli-mu.2] field-visuals: numbered keycaps 1-9 with is-unnumbered column from 10, current-group accent, transparent heading rows, dialog-scoped gutter/label axis and 0.8em group breaks, ⇧J/K 1–N field hint with two kbd keys, Field N of M aria-label and aria-keyshortcuts. Unit tests cover keycaps, re-flow, current-group, hint presence/absence, aria, and no keycaps on the read-only card, inline header, or record sheet. Arrange/place/ghost suites stay green. Real Obsidian e2e was not run: Obsidian and xvfb-run are not installed on this host; geometry probes and light/dark/375 shots are wired in obsidian-album-ui-e2e.cjs. Did not edit decisions:schema-card-digits-are-field-numbers. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-mu.1](bob-cli-mu.1.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mu.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mu.2/README.md) | [bob-cli-mu.2](bob-cli-mu.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e32deb6`](https://github.com/bobs-org/bob-plugins/commit/e32deb60574b3a2d09241e8d87d4501348fbe4c5) | feat(schema-card): number painted fields with hanging keycaps and a field hint | [bob-cli-mu.2](bob-cli-mu.2.md) | 2026-11-17 16:29:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mu.2][1] | Verify bead status and close note after compaction before finalizer | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mu.2/README.md

<!-- sase:referenced-by:end -->
