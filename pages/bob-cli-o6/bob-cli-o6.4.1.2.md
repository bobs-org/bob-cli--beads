# Bead: bob-cli-o6.4.1.2 — Record card wears the RECORD kicker and sheet tile, mounts in the title slot, and migrates its title selectors onto the kit

[Bead Pages](../README.md) / [bob-cli-o6.4.1](bob-cli-o6.4.1.md) / bob-cli-o6.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-o6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.4.md) · **Assignee:** `bob-cli-o6.4.1.2` · **Size:** large
**Created:** 2026-11-20 13:42:58 EST · **Closed:** 2026-11-20 21:07:32 EST
**Plan:** [202611/collection\_cards\_title\_block.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/collection_cards_title_block.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:2edf25fd83d5065a3b3014d2 | attached via sase artifact create --bead |
| related | file:explicit:889bc05d45700ad156272d37 | attached via sase artifact create --bead |
| related | file:explicit:8a936446acea27130b062c71 | attached via sase artifact create --bead |
| related | file:explicit:8e372fc39a43c7a4771c778e | attached via sase artifact create --bead |
| related | file:explicit:98520cdab33c58285c8eb69e | attached via sase artifact create --bead |
| related | file:explicit:af21f8ba1f5314bedb0dfa65 | attached via sase artifact create --bead |
| related | file:explicit:d10bae27ca21fa092df9a860 | attached via sase artifact create --bead |
| related | file:explicit:d42cb2cd025278e448e5df6c | attached via sase artifact create --bead |
| related | file:explicit:f0c604b18ca234048e388234 | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

record-card: in bob-ledger-tools, rebuild the record sheet header as the kit title block (RECORD kicker with album link and noun, sheet tile, paper material), mount it in the title slot through the album-card adopter glue with the walk rail docked inside and the first-line walk line hidden by a record title recognizer with reveal, move the inline-title and owned-row hiding onto kit classes, update unit, preview, and record e2e checks (never the record-writer harness), update docs, bump, deploy, and run the record e2e scripts on athena.

## Notes

[2026-11-21T01:55:16Z · bob-cli-o6.4.1.2] PROPOSED FOLLOW-UP: event-link 25 ms budget — npm test failed once at scripts/test-ledger-tools-event-link-times.cjs:1095 (one build over a 200-link ledger, took 45.1 ms). Isolated rerun passed at 3.8 ms. Known flake recorded on bob-cli-o6.1, bob-cli-o6.2, and bob-cli-o6.4.1.1; not caused by the record title-slot work.

[2026-11-21T01:55:21Z · bob-cli-o6.4.1.2] PROPOSED FOLLOW-UP: bob-cli docs gate fails: docs/reference/vault-format.md is over budget at 6016 words (cap 6000 for reference/). npm run docs:check from bob-plugins fails identically on a clean origin/master; the bob-plugins pages pass. Same as bob-cli-o6.4.1.1 note #3.

[2026-11-21T02:07:32Z · bob-cli-o6.4.1.2] Record card is the title block. bob-plugins commit 'feat(ledger-tools): record card owns the title block from the title slot' lands at this turn's finalization; bob-ledger-tools 1.148.0 (merged origin/master 6e0d764, kept both docs/index.md version rows). Kit change dropping the legacy bob-record-sheet-owned-property class is the sanctioned migration; other kit use is additive (AdoptRelease is now kind-filtered so album decorate cannot drop a record slot; host buildDecorations(view, update); title-slot measure budget). New fragments: 242ia identity, 242kb title mixin, 242w title recognizer. Record mounts in the title slot through the album adopter glue (kind=record), paints from local identity before the report, joins the body in place, docks the walk rail at the card bottom, and hides the first-body walk line / matching legacy H1 with reveal. Title ownership is independent of row ownership (owns-title vs hides-properties). Gates: build and build:check pass; targeted unit 171/171 after merge; npm test 8000 pass / 1 fail / 4 skipped (8005), the one failure the event-link 25 ms budget (45.1 ms, isolated 3.8 ms, follow-up); test:perf 11/11. docs:check fails only on bob-cli docs/reference/vault-format.md over budget, identical on clean origin/master (follow-up). Real Obsidian on athena (TMPDIR=/tmp, bob 0.5.0, BOB_CLI_DIR=workspace): record-card e2e 180/180 file:explicit:f0c604b18ca234048e388234; walk e2e 16/16 including sheet.parentElement in .cm-sizer / .mod-header file:explicit:8a936446acea27130b062c71. Shots Reading file:explicit:8e372fc39a43c7a4771c778e, Live file:explicit:2edf25fd83d5065a3b3014d2, reveal file:explicit:98520cdab33c58285c8eb69e, 375px file:explicit:af21f8ba1f5314bedb0dfa65, walk Live file:explicit:d42cb2cd025278e448e5df6c. Previews: ADOPTED_KINDS {bank, album, record}; structural 28/28, outcome pass; report file:explicit:889bc05d45700ad156272d37, 1280 expanded file:explicit:d10bae27ca21fa092df9a860. Changed e2e expectations: assertNativeVisibility split into {titleOwned, rowsHidden}; order is card in the title slot (.cm-sizer / .mod-header direct child) before native Properties; identity checks data-card-kind=record, sheet tile, Record: <title>, kicker album link and noun, one aria-level=1; title paints before the report and the body joins the same node; Live Preview reveal of a matching H1 keeps the slot card (cursor on the H1 line); Reading embed cards are demoted and do not own the title (LP embeds never paint because readingRoot is null inside .cm-editor); broken schema still owns the title with rows visible; walk first-body paragraph is kit-hidden (p.bob-property-card-title-source in Reading), rail docks inside the slot card, cursor reveal shows the raw line while the same card and rail stay mounted. Unit expectation changes: pending identity card; no remount on report join; album title rule; slot ownership in both modes; no legacy owned-row class; AdoptRelease of one species leaves the other; album Live Preview decorate does not drop a record slot; Reading embed cards still paint when the host leaf shows a different path. Selector-consumer audit: 241hf closest('.bob-record-sheet') and workflow queries of .workspace-leaf.mod-active .bob-record-sheet still resolve the slotted card; no other plugin queries record-sheet selectors. Deploy: bob plugins sync --repo --no-pull -p bob-ledger-tools without -F; vault main.js, styles.css, manifest.json byte-identical to the 1.148.0 build. Writer harness files untouched (bob-cli-ms and bob-cli-ms.8 still open). No memory edits, no new beads. Never closed bob-cli-o6.4.1, bob-cli-o6.4, bob-cli-o6, or any bob-cli-ms bead.

## Dependencies

- **Depends on:** [bob-cli-o6.4.1.1](bob-cli-o6.4.1.1.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.4.1.2.md) | [bob-cli-o6.4.1.2](bob-cli-o6.4.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b8b7baf`](https://github.com/bobs-org/bob-plugins/commit/b8b7baf440e888cd94c948f5339cd37527928079) | feat(ledger-tools): record card owns the title block from the title slot | [bob-cli-o6.4.1.2](bob-cli-o6.4.1.2.md) | 2026-11-20 21:08:59 EST |
