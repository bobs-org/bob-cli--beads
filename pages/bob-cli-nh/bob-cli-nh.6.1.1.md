# Bead: bob-cli-nh.6.1.1 — Shared property ownership and card editor registry

[Bead Pages](../README.md) / [bob-cli-nh.6.1](bob-cli-nh.6.1.md) / bob-cli-nh.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.md) · **Assignee:** `bob-cli-nh.6.1.1` · **Size:** medium
**Created:** 2026-11-19 09:44:34 EST · **Closed:** 2026-11-19 11:34:45 EST
**Plan:** [202611/property\_card\_kit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_kit.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:5366ba3f1c91e381b416eb0b | attached via sase artifact create --bead |
| related | file:explicit:6ef537cd9927c600b96c5526 | attached via sase artifact create --bead |
| related | file:explicit:b351243735380bbef6047244 | attached via sase artifact create --bead |
| related | file:explicit:d19bd1571d8869c3fbd0f94c | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

ownership: capture the unchanged album, record, and bank acceptance baseline, generalize selective property hiding into propertyCardOwnKeys, and replace the closed double-equals dispatch with registerPropertyCard. Migrate all three cards, preserving existing assertions, gates, command identities, and editor behavior.

## Notes

[2026-11-19T15:07:13Z · bob-cli-nh.6.1.1] Ownership implementation landed (uncommitted): shared propertyCardOwnKeys + registerPropertyCard in bob-plugins; album/record/bank migrated; record assertions preserved; album/bank unbounded CSS replaced with owned-row rules. Unit gates green: build, build:check, docs:inventory:check, validate 11/11, focused card suites pass (double-equals extended + new ownership file: 33/33). Full npm test: only flaky unrelated perf-budget failures (pass in isolation). Evidence: file:explicit:0f3ef158298d15417a5fa040 -r Record ownership phase implementation and verification

[2026-11-19T15:07:19Z · bob-cli-nh.6.1.1] REMAINING (did not fit this turn): 1) bob plugins sync REFUSED correctly (vault holds uncommitted bob-cli_11 build, agent still RUNNING) - sync from clean tree after it lands, no -F. 2) Real Obsidian e2e (album/record full-scope/bank) not run: no checkout-built bob binary and CDP suites exceed single-turn ceiling; run on athena with BOB_BIN from final checkout (BOB_CLI_DIR + provenance per docs/develop/validation.md), preserve reports/screenshots as artifacts. Close this phase only after 1-2 land green. -r Record remaining sync and e2e work

[2026-11-19T15:07:27Z · bob-cli-nh.6.1.1] PROPOSED FOLLOW-UP: run the three real Obsidian e2e suites (album, record full-scope, bank) on athena from a checkout-built bob binary and preserve reports/screenshots as artifacts before the kit land. -r Triage e2e acceptance follow-up

[2026-11-19T15:07:32Z · bob-cli-nh.6.1.1] PROPOSED FOLLOW-UP: bob plugins sync from a clean tree after the ws11 uncommitted bob-ledger-tools build lands (no -F while that agent runs). -r Triage deploy follow-up

[2026-11-19T16:29:34Z · bob-cli-nh.6.1.1] Real-Obsidian acceptance run (athena, bob-cli 5b4c2636 clean debug bob sha256 452229ac…, same fixtures/harness) found 2 regressions in landed ccfc12b, now fixed in bob-plugins (committed by this turn): (1) album/bank released ownership scope-wide, so a pane's stale Reading binding for an earlier note unhid the current card's rows (album record-prop-hidden-on-album failed; record properties-hidden-after-plugin-reenable failed) and record's clear could wipe another card's newer owner -> per-adapter path-tagged mount slots (propertyCardSlotOwn/Release/ReleaseAll) releasing only the adapter's own generation-bound handle; record keeps only its handle (dead copy painter removed). (2) album/bank Live Preview scope is .markdown-source-view, which the shared API denies, so LP never hid record/bank (bank hub-bank-property-hidden failed) -> own on view.dom (.cm-editor) and one bounded ungated CSS rule for tagged rows; record CSS unchanged. Final vs baseline 36d4801: album 120/121 = base (new record-prop-hidden-on-album-live check added; fails on ccfc12b), bank 75/78 = base, record full 144/144 x2 = base, 0 console exceptions; screenshots album 36/36 + bank 20/20 byte-identical, record 22/25 identical with 3 proven timing-noise diffs. npm test 7397 pass 0 fail, validate 11/11, ownership unit tests 13/13. Evidence: file:explicit:5366ba3f1c91e381b416eb0b (summary), file:explicit:d19bd1571d8869c3fbd0f94c (baseline bundle), file:explicit:6ef537cd9927c600b96c5526 (final bundle). -r Record ownership phase acceptance evidence and fixes

[2026-11-19T16:29:50Z · bob-cli-nh.6.1.1] PROPOSED FOLLOW-UP: Obsidian CDP e2e runners abort under SASE's long agent TMPDIR — every owned Obsidian launch (album/bank/record suites) dies at startup with Chromium FATAL "Socket path too long: <agent-tmp>/scoped_dir…/SingletonSocket"; runners should pass a short TMPDIR to the spawned Obsidian (same root cause as closed bob-cli-5b for the web-clip adapter). Workaround used: TMPDIR=/tmp/<short>. -r Triage e2e runner TMPDIR follow-up

[2026-11-19T16:29:55Z · bob-cli-nh.6.1.1] PROPOSED FOLLOW-UP: album UI e2e schema-field-jump-ctrl-j fails identically on clean base bob-plugins 36d4801 and on the final tree ("Stats Ctrl+J -> stats (field 1 field:status; real key moved=false)"); cmd: BOB_BIN=<bob-cli 5b4c2636 debug> TMPDIR=/tmp/<short> xvfb-run -a node scripts/obsidian-album-ui-e2e.cjs -e /snap/obsidian/current/app/obsidian. No tracking bead found. -r Triage pre-existing album e2e failure

[2026-11-19T16:30:00Z · bob-cli-nh.6.1.1] PROPOSED FOLLOW-UP: bank UI e2e invalid-fence and walk-learn-coffee/walk-learn-accept (RangeError: Invalid line number 0 in 15-line document) fail identically on clean base 36d4801 and the final tree; already tracked by bob-cli-m6 and bob-cli-m7 (+1 corroboration, athena 2026-11-19). -r Corroborate tracked bank e2e failures

[2026-11-19T16:30:04Z · bob-cli-nh.6.1.1] PROPOSED FOLLOW-UP: perf flake — scripts/test-ledger-tools-event-link-times.cjs "one build over a 200-link ledger stays under 25 ms" failed once in full parallel npm test, passed 3/3 isolated; same family as open bob-cli-ki (keep-moving marks 200-link gate) and earlier na.6/na.7 reports; no open bead covers event-link-times specifically. -r Triage perf flake follow-up

[2026-11-19T16:34:45Z · bob-cli-nh.6.1.1--1] Shared property-card ownership + card editor registry landed in bob-plugins as ccfc12b plus regression fix 8d6fd78 (per-adapter path-tagged mount slots so a prior note's Reading release cannot unhide the current card; album/bank Live Preview ownership on .cm-editor with one bounded CSS rule; record's dead row painter removed). Real-Obsidian acceptance vs unchanged base 36d4801 on bob-cli 5b4c2636: album 120/121, bank 75/78, record 144/144 (x2, 0 console exceptions); remaining failures identical on base (bank ones tracked by bob-cli-m6/m7); album 36/36 and bank 20/20 screenshots pixel-identical, record 22/25 with 3 timing-noise diffs; npm test 7397 pass/0 fail, validate 11/11; new unit tests and album Live Preview e2e check fail on ccfc12b and pass on the fix. Summary file:explicit:5366ba3f1c91e381b416eb0b, baseline bundle file:explicit:d19bd1571d8869c3fbd0f94c, final bundle file:explicit:6ef537cd9927c600b96c5526. Deployed bob-ledger-tools 1.140.0 via bob plugins sync from a clean tree at 8d6fd78 (== origin/master): .bob-deploy.json dirty=clean source_head=8d6fd78 state=complete; vault sha256 equals committed files: main.js 45ff8e61..., styles.css 57e5e3f9..., manifest.json 750bb941....

## Dependencies

- **Blocks:** [bob-cli-nh.6.1.2](bob-cli-nh.6.1.2.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.1.md) | [bob-cli-nh.6.1.1](bob-cli-nh.6.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.6.1.1][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.1.md

<!-- sase:referenced-by:end -->
