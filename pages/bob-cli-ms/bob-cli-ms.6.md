# Bead: bob-cli-ms.6 — Typed Record Card stages and Tab fill-out

[Bead Pages](../README.md) / [bob-cli-ms](README.md) / bob-cli-ms.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.55.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.55.linker.w0.md) · **Assignee:** `bob-cli-ms.6` · **Size:** large
**Created:** 2026-11-17 11:29:54 EST
**Plan:** [202611/record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card.md)

## Description

record-stages: text, suggest combobox, date, number, URL, link, and list stages with debounced bob previews, a latched Enter, Tab and Shift+Tab save-and-advance, and taught refusals for required, invalid, and stale edits.

## Notes

[2026-11-17T21:56:31Z · eo.f0--code] Per approved plan:202611/record_card_field_jump_co_landing.md (reviewer: record_card_digits=pick, climb_keeps_field=yes, scoped_force=yes). If ms.5 closed without items 1-4 below, implement them before the stages.

1. Digits. record_card_digits=pick: on a choices row 1-9 pick that choice and save; elsewhere a digit does nothing and the status line teaches 'Digits pick a choice on choice fields'. Never moves selection.

2. Shift+J/K. record_card_digits=pick: browse-mode Shift+J/K step fields, clamp at ends, bump via schemaCardBump (241xb) with 'No next/previous field', announce '<Label>, field N of M', silent on repeat, reduced-motion, inert in stages/inputs/IME, never write. Not in hint strip; list in docs/record-card.md.

3. = climbs to the same field. climb_keeps_field=yes: = calls openAlbumSchemaEntry({filePath, field: <selected key>}), threads through openAlbumSchemaCard into selectedKey (field:<key>), fallback stats. Test = on Status, Shift+J, unknown key.

4. CSS isolation. Never use bob-album-schema-dialog(-body) on the Record Card; use bob-record-card-*. Reuse mu bump/announcer helpers.

5. Docs. One sentence in docs/record-card.md: 'Digits here pick a choice; on the album Schema Card they jump to field N.' Detail stays in record-card.md; link from capped pages; never raise a budget.

6. Deploy discipline. Vault unwedged at f80d0dd (clean origin/master, 1.130.0; old stamp bob-cli_15 dirty b0a9c89, backup /home/bryan/.local/state/bob-cli/plugin-backups/20261117-165532). Fetch+merge origin/master and npm run build before every sync; sync final tree. Refusal rule: Bryan pre-authorizes -F for bob-ledger-tools, bob-navigation-hotkeys, bob-command-mode for rest of both epics only when stamped root exists+clean, HEAD ancestor of origin/master, author phase closed, deploying clean origin/master (stash, ff, build:check, sync -F, pop, rebuild, sync again). Note old stamp + backup afterwards; otherwise AGENTS.md.

7. Merge friction. Keep both epics' test:unit entries (one-line list); rebuild main.js, never hand-merge; ms takes next free minor.

## Dependencies

- **Depends on:** [bob-cli-ms.5](bob-cli-ms.5.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-ms.7](bob-cli-ms.7.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.6/README.md) | [bob-cli-ms.6](bob-cli-ms.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:eo.f0--code][1] | Need phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.eo.f0.md

<!-- sase:referenced-by:end -->
