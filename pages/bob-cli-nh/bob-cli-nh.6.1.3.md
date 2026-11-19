# Bead: bob-cli-nh.6.1.3 — Shared property-card chrome and precise documentation

[Bead Pages](../README.md) / [bob-cli-nh.6.1](bob-cli-nh.6.1.md) / bob-cli-nh.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.md) · **Assignee:** `bob-cli-nh.6.1.3` · **Size:** medium
**Created:** 2026-11-19 09:44:34 EST · **Closed:** 2026-11-19 17:17:19 EST
**Plan:** [202611/property\_card\_kit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_kit.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:57b7adc6f806ce185b185519 | attached via sase artifact create --bead |
| related | file:explicit:a50033287bd8564938d9063a | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

chrome: consolidate property-card chrome and hue tokens without changing pixels, align the three plugin references around card versus card editor, and document the extension API for the intention-card phase. Compare final screenshots to the original baseline, run the complete acceptance gates, and deploy with bob plugins sync. Prepare completion evidence for the land agent; do not close bob-cli-nh.6 or bob-cli-nh from a child phase.

## Notes

[2026-11-19T20:33:06Z · bob-cli-nh.6.1.3--1] PROPOSED FOLLOW-UP: Update the navigation copy-card model row-order expectation for the copy-chip row. Reproduced on clean bob-plugins base SHA 946ef56589c2650807bdf45c3dfd0eb59005c956 with `node --test scripts/test-navigation-copy-card-model.cjs`; scripts/test-navigation-copy-card-model.cjs:558 fails ERR_ASSERTION because expected [path, absolute, file, note, template-2, block-id, template-1] but actual adds copy-chip between note and template-2. The same assertion fails on this phase tree. No existing tracker was found by `sase bead search 'copy-chip row order'` or `sase bead search 'navigation copy card'`.

[2026-11-19T22:16:47Z · bob-cli-nh.6.1.3--3] Evidence refs: `file:explicit:a50033287bd8564938d9063a` (full reports, screenshots, logs, contact sheets, provenance, pixel comparisons) and `file:explicit:57b7adc6f806ce185b185519` (summary).

Final matrix: 24/24 exact pixel pairs against `36d48017f9a16edaf21346fb0276c530836e08f4`. Real Obsidian results: album 120/121 with only baseline `schema-field-jump-ctrl-j`; record 144/144; bank 75/78 with baseline `invalid-fence`, `walk-learn-coffee`, `walk-learn-accept` already tracked by `bob-cli-m6`/`bob-cli-m7`; bank setup 46/47 with `setup-group-jump-ctrl-k`. The bank setup one-Enter arrangement save also timed out with `preview-ready`, `dirty:true`, `undo:false`, saved `[coffee, convenience]`, projected `[convenience, coffee]`. Both bank setup failures reproduced on clean bob-plugins SHA `946ef56589c2650807bdf45c3dfd0eb59005c956`.

PROPOSED FOLLOW-UP: Fix bank setup Ctrl+K group jump and one-Enter arrangement save. Exact clean-base reproduction: `git -C "$PLUGIN" worktree add --detach /tmp/nh613-bob-plugins-clean 946ef56589c2650807bdf45c3dfd0eb59005c956`; create the isolated runner with `sed 's#/tmp/bse2e#/tmp/nh613-clean-base-bank-setup/bse2e#g' "$CLEAN/scripts/obsidian-bank-ui-e2e-setup.cjs" > "$CLEAN/scripts/obsidian-bank-ui-e2e-setup-isolated.cjs"`; run `env TMPDIR=/tmp BOB_CLI_DIR="$ROOT" BOB_BIN="$ROOT/target/debug/bob" BOB_LEDGER_TOOLS_PLUGIN_DIR="$CLEAN/plugins/bob-ledger-tools" xvfb-run -a node "$CLEAN/scripts/obsidian-bank-ui-e2e-setup-isolated.cjs" -e /snap/obsidian/current/app/obsidian -r /tmp/nh613-clean-base-bank-setup/report-isolated.json -o /tmp/nh613-clean-base-bank-setup/shots-isolated`.

Assertions: `setup-group-jump-ctrl-k` expects Ctrl+K to select a `group:` scope, but remains at `category:groceries`; “bank arrangement saved after one Enter” times out with the preview still dirty and no undo. Tracking bead: this phase proposal, `bob-cli-nh.6.1.3`; related existing coverage bead `bob-cli-mk` covers real-Obsidian bank group-arrangement walkthroughs. No dedicated Ctrl+K task tracker was found, and no task bead was created.

Build, build:check, and focused tests passed (130/130). The deployed `main.js`/`styles.css` hashes match the linked checkout. `docs:check` still reports two unchanged, over-budget Mac Capture references (6171 and 6027 words), recorded in the evidence bundle. The earlier clean-base copy-chip row-order proposal remains note #1. No ancestor bead was changed.

[2026-11-19T22:17:19Z · bob-cli-nh.6.1.3--3] Completed shared property-card chrome phase. Final 24/24 pixel matrix exact against 36d4801; record 144/144; album and bank failures match audited baseline; bank setup Ctrl+K/apply failures reproduce on clean 946ef and are recorded as a PROPOSED FOLLOW-UP. Build, build:check, focused tests (130/130), linked-repo sync and deployed hashes verified. Evidence: file:explicit:a50033287bd8564938d9063a and file:explicit:57b7adc6f806ce185b185519. docs:check still reports two unchanged Mac Capture word-budget errors. No ancestors closed.

## Dependencies

- **Depends on:** [bob-cli-nh.6.1.2](bob-cli-nh.6.1.2.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.3.md) | [bob-cli-nh.6.1.3](bob-cli-nh.6.1.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.6.1.3--3][1] | Review phase scope and notes before attaching final acceptance evidence | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.3.md

<!-- sase:referenced-by:end -->
