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

[2026-11-18T00:07:46Z · bob-cli-ms.6] Implemented record-stages: all seven typed stages with bob-owned validation, debounced previews, latched Enter, Tab/Shift+Tab save-and-advance, and stale/refresh retention.

Co-landing (ms.5 items 1-4): digits pick-and-save on choices, teach 'Digits pick a choice on choice fields' elsewhere with no move; browse Shift+J/K clamps with schemaCardBump and '<Label>, field N of M' announcements, silent on repeat, reduced-motion aware, inert in stages/inputs/IME/menus, All-actions Previous/Next field, documented in docs/record-card.md (kept out of hint strip); = passes {filePath, field} through openAlbumSchemaEntry/openAlbumSchemaCard to selectedKey field:<key> with stats fallback; CSS uses only bob-record-card-* (verified no bob-album-schema-dialog in record-card sources). Approved sentence in docs/record-card.md: 'Digits here pick a choice; on the album Schema Card they jump to field N.'

Stages (new 242q model+DOM, 242r/242s controller overrides keeping 242p at ~800 lines, all fragments <=1000): list-first then scalar kind+suggest seeding from authoritative property/raw (never labels/defaults); text autos, suggest combobox over full fields[].values with direct exact picks and free-text preview incl. record_value_near warning, link vault suggester preserving aliases/headings/anchors, list chip editor submitting JSON arrays with literal commas, date/number/URL with bob validation only. One field one op; explicit empty optionals unset; cleared required refuses with teaching pattern; local checks presentation-only.

Preview/save/Tab: session.setDraft on actual changes (250ms debounce), current-preview consequence/warning display, verbatim refusal paint, no applyOps bypass for typed drafts; Enter inert while pending/refused, exactly one session.apply() on current success with rapid/repeat guards; Tab consumes in every stage (unchanged wraps with zero writes, changed latches one advance with stage/draft identity, waits for current success, applies once, advances on success incl. no-op; refusal/stale ends pending advance and keeps stage; edit/cancel/field-change/close/composition invalidates; no skip/queue); choices/explicit picks use direct route; new stage starts from applied/read state with overlay+Undo preserved. Shared settlement factored for typed/direct (saving/saved/refusal/stale, report consumption, Undo, overlay, fingerprint+pane-save guard).

Refresh/focus: full draft/chip/candidate/control/caret/field retained across refresh+stale; queued saves invalidated before rebase; re-read/rebase shows stale line with explicit retry scheduling fresh preview (preview-time stale now settled via wrapper hook); schema removal/kind-change/capability loss stops write intent with teaching; no active-input rebuild on status paints; caret/selection preserved; IME nodes never replaced; stage keys precede browse keys; Esc/Ctrl+[ ladder with q outside text controls per decisions:q-and-ctrl-bracket-mirror-esc; cancel/close clears timers/drafts/Tab intent/listeners; late reads/previews never write/reopen; started applies settle with late callbacks ignored.

Tests/docs: new scripts/test-ledger-tools-record-card-stages.cjs (9 tests: seeds, ops, suggest, shift/digits, painters, equality, co-landing, commas, isolation) registered in test:unit; existing record-card 19 pass, record-update/sheet/album 40 pass, obsidian record-writer offline self-test passes; docs/record-card.md completed with stages/save-advance/refusals/keys (approved distinction verbatim); capped front-door pages untouched except generated inventory; Ledger Tools 1.131.0 -> 1.132.0; build/docs:gen/validate pass; BOB_CLI_DIR docs:check passes (strict build + 447 unit tests).

Deploy: fetched+integrated origin/master (0d2fa4b week headlines, b067881 schema keycaps; no conflicts with typed files), rebuilt, re-verified focused tests. bob plugins sync --repo PWD --no-pull: 3 copied, 0 skipped, 28 unchanged, backups in /home/bryan/.local/state/bob-cli/plugin-backups/20261117-190633 (old dirty stamp f80d0dd, new dirty head 0d2fa4b, live manifest 1.132.0). No -F used. Real Obsidian CDP walkthrough not run here (no desktop Obsidian/Xvfb in this container): offline self-tests pass; parent land agent owns full integrated phase-7 CDP proof.

PROPOSED FOLLOW-UP: full bob-cli just check (Rust tree untouched/clean) should run to green before land; perf-budget flakes seen in unrelated suites need baseline triage if they recur.

[2026-11-18T00:27:43Z · bob-cli-ms.6--1] PROPOSED FOLLOW-UP: just check FAILED (exit 101, monitor cppbaazpqftx, 2026-11-18T00:08:17Z, 15m6s) so bead stays open. 7315 passed, 3 failed in -p bob-obsidian --lib: native::catalog::tests::public_leaves_are_entries_or_excluded (public leaf ["records", "tidy"] is neither an entry nor excluded), native::completion::kinds::tests::every_value_arg_has_a_decision (value-taking args without a kinds decision: ["records tidy:type"]), runner::tests::every_native_command_is_on_exactly_one_canonical_path (left 92 vs right 91). All three trace to cfc3177c feat(records) adding the records tidy command (tidy.rs, runner.rs, completion tree) without the catalog/completion/runner expected-table updates. Workspace at 2a58d067 already contains cfc3177c and is 3 behind origin/master (da13fee3 top), whose 3 newer commits do not touch this gap, so the failure is pre-existing/outside the record-card typed-stages scope (bob-plugins JS only, Rust tree untouched). Fix belongs on the Rust records track: register records/tidy in catalog entries/excluded, add the tidy:type kinds decision, and update the runner canonical-path expectation. Evidence: sase monitor show cppbaazpqftx --all-lines. -r Recording just check failure as follow-up per monitor instruction; bead stays open

## Dependencies

- **Depends on:** [bob-cli-ms.5](bob-cli-ms.5.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-ms.7](bob-cli-ms.7.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.6.md) | [bob-cli-ms.6](bob-cli-ms.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ba2b090`](https://github.com/bobs-org/bob-plugins/commit/ba2b09061153621311f179c102cfcab8c1b8e0b7) | feat(record-card): typed stages with Tab fill-out | [bob-cli-ms.6](bob-cli-ms.6.md) | 2026-11-17 19:29:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:eo.f0--code][1] | Need phase scope | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.eo.f0.md

<!-- sase:referenced-by:end -->
