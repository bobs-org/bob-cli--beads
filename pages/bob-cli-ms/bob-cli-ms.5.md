# Bead: bob-cli-ms.5 — Record Card shell, browse keys, choices, and discrete actions

[Bead Pages](../README.md) / [bob-cli-ms](README.md) / bob-cli-ms.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.55.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.55.linker.w0.md) · **Assignee:** `bob-cli-ms.5` · **Size:** large
**Created:** 2026-11-17 11:29:54 EST · **Closed:** 2026-11-17 17:05:34 EST
**Plan:** [202611/record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card.md)

## Description

record-card: keyboard-first Record Card modal in the Task Card / Schema Card idiom with browse navigation, the choices pick list, digits, t, Ctrl+D, Undo, the YAML excursion, = to the album Schema Card, the status rule, hint strip, All actions menu, and live region.

## Notes

[2026-11-17T21:56:19Z · eo.f0--code] Per approved plan:202611/record_card_field_jump_co_landing.md (reviewer: record_card_digits=pick, climb_keeps_field=yes, scoped_force=yes).

1. Digits. record_card_digits=pick: keep the plan's key table. On a choices row, 1-9 pick that choice and save. On any other row a digit does nothing and the status line teaches 'Digits pick a choice on choice fields'. It never moves the selection.

2. Shift+J/K. record_card_digits=pick: in browse mode, Shift+J/K step to the next/previous field and clamp at the ends (no wrap). On a miss bump through mu's schemaCardBump (241xb) and announce 'No next field' / 'No previous field'. On a hit announce '<Label>, field N of M' through the card's live region. Silent on event.repeat, follow reduced motion, inert in stages, inputs, and IME composition. Never write. Leave out of the hint strip; list in docs/record-card.md key table.

3. = climbs to the same field. climb_keeps_field=yes: = calls openAlbumSchemaEntry({filePath, field: <selected field key>}). Thread the field through openAlbumSchemaCard into the modal's starting selectedKey (field:<key>), falling back to stats when that target is missing. 241y is 973 lines, keep the change to a few lines. Test: = on Status opens the Schema Card on Status, Shift+J then moves to the next field, unknown key opens on Album details.

4. CSS isolation. Never set bob-album-schema-dialog or bob-album-schema-dialog-body on the Record Card. mu.2's transparent-row, gutter, keycap, and group-break rules key off those classes. Use bob-record-card-*. Reuse mu's bump and announcer helpers for feedback.

5. Docs. In docs/record-card.md state in one sentence: 'Digits here pick a choice; on the album Schema Card they jump to field N.' bob-ledger-tools.md and bob-navigation-hotkeys.md are at their 6000-word caps: put detail in record-card.md, link from those pages, trim to fit. Never raise a budget.

6. Deploy discipline. Vault unwedged at f80d0dd (clean origin/master, 1.130.0; old stamp bob-cli_15 dirty b0a9c89, backup /home/bryan/.local/state/bob-cli/plugin-backups/20261117-165532). Right before every bob plugins sync, fetch and merge origin/master and run npm run build. Sync your final tree so the vault build is what lands. Refusal rule: Bryan pre-authorizes -F for bob-ledger-tools, bob-navigation-hotkeys, bob-command-mode for the rest of these two epics only, only when ALL hold: stamped source_root exists and is clean; its HEAD is an ancestor of origin/master; author's phase bead is closed; you deploy a clean up-to-date origin/master (stash, fast-forward, npm run build:check, sync -F, pop, rebuild, sync again without -F). Afterwards note old stamp + backup dir on your bead. Otherwise follow AGENTS.md.

7. Merge friction. The test:unit list in package.json is one line, so keep both epics' entries. Rebuild main.js and never hand-merge it. ms bumps the bob-ledger-tools minor version, mu does not, so take the next free minor.

[2026-11-17T22:05:25Z · bob-cli-ms.5] PROPOSED FOLLOW-UP: npm test timing budgets flake under parallel load — event-link-times 189.7ms, frees-marks 100ms, keep-moving-marks-surface 1472.2ms, off-clock-link-chips 120.1ms vs 25ms. Isolated on clean f80d0dd they passed. Tracked: bob-cli-km, bob-cli-io, bob-cli-ki, bob-cli-ju.

PROPOSED FOLLOW-UP: just docs-check / plugins docs:check fails on docs/reference/json-outputs.md 6089/6000 words. Unchanged in this phase. Cited by bob-cli-ms.4 and bob-cli-mr.3.1.

PROPOSED FOLLOW-UP: album schema-writer self-test still fails held-lock apply (2 commits, expected 1) with BOB_BIN=/home/bryan/.cargo/bin/bob (bob 0.5.0). Same ms.4 lead; record-writer self-test passed.

[2026-11-17T22:05:34Z · bob-cli-ms.5] Shipped the desktop Record Card in Bob Ledger Tools 1.131.0 (bob-plugins, on f80d0dd plus this phase). Edit record (edit-record) opens a bob-key-card modal over the existing record-sheet gate and guarded createRecordUpdateSession. Browse (j/k, arrows, Tab, Home/End) includes ghosts; choices filter/list/digits apply one field.set with no preview; t sets today; Ctrl+D unsets optionals and refuses required locally; u/Ctrl+Z undoes via inverse_ops; y/Ctrl+E YAML kind=record Done never uses albumYamlDoneDecision; = closes then openAlbumSchemaEntry({filePath: recordPath}); Esc/q/Ctrl+[ share bobCardWireCloseKeys. Stage seam for ms.6: recordOpenStage, recordCardStageKindFor, recordCardCaptureStage/RestoreStage (242q reserved). Verified: 19 record-card unit tests; related record-sheet/update/YAML/schema-card/bank-group-jump green; npm run validate; docs:gen inventories 1.131.0 + Edit record; record-writer self-test with BOB_BIN=/home/bryan/.cargo/bin/bob (bob 0.5.0) passed; offline smoke --self-test passed (not an Obsidian pass). Sync: ff onto landed f80d0dd, then bob plugins sync --repo $PWD --no-pull copied 1.131.0 (no -F). Visual CDP walkthrough left for the land agent. Known suite flakes and json-outputs budget recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-ms.4](bob-cli-ms.4.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-ms.6](bob-cli-ms.6.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.5.md) | [bob-cli-ms.5](bob-cli-ms.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c1da817`](https://github.com/bobs-org/bob-plugins/commit/c1da817c213b0ebf1f3ae4b47b4d41a69230948c) | feat(ledger-tools): add Record Card shell for discrete field edits | [bob-cli-ms.5](bob-cli-ms.5.md) | 2026-11-17 17:52:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ms.5--1][1] | Confirm phase completeness before host-completion submit with bead_action close | 1 |
| read-by | [agent:eo.f0--code][2] | Need phase notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.5.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.eo.f0.md

<!-- sase:referenced-by:end -->
