# Bead: bob-cli-q5.5.1.6 — Obsidian display acceptance and screenshot evidence

[Bead Pages](../README.md) / [bob-cli-q5.5.1](bob-cli-q5.5.1.md) / bob-cli-q5.5.1.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.5.md) · **Assignee:** `bob-cli-q5.5.1.6` · **Size:** medium
**Created:** 2026-11-26 15:37:09 EST
**Plan:** [202611/snooze\_display\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_display_marks.md)

## Description

visual-proof: verify the complete display in real Obsidian, capture light and dark states and accessibility evidence, fix display integration defects, and attach results for the land agent.

## Notes

[2026-11-27T01:16:30Z · bob-cli-q5.5.1.6] PROPOSED FOLLOW-UP: Today ledger-link tomatoes never attach in Reading view — 7 stamped rows, 3 unattached invisible `.bob-today-mark` hosts with no LI ancestor (e2e reading-tomato-stamps). Fails identically on the pristine base (run 1, before any plugin edit), so it is not a snooze regression; needs a Today-reading owner.

[2026-11-27T01:16:36Z · bob-cli-q5.5.1.6] PROPOSED FOLLOW-UP: docs gate `docs/reference/vault-format.md` over word budget (6030/6000) fails `just docs-check` on the clean bob-cli tree with no local changes; needs a docs owner to trim or re-budget.

[2026-11-27T01:16:44Z · bob-cli-q5.5.1.6] Snooze display visual proof: real-Obsidian e2e report (71/72 checks pass; reading-tomato-regression is a pre-existing Today-reading defect tracked as a follow-up) plus light/dark screenshots for Live Preview, Reading, rows, plan chip, hover, narrow, and a11y states.

🔒 report.json
🔒 e2e-snooze-marks-live-light.png
🔒 e2e-snooze-marks-live-dark.png
🔒 e2e-snooze-marks-reading-light.png
🔒 e2e-snooze-marks-reading-dark.png
🔒 e2e-snooze-marks-rows.png
🔒 e2e-snooze-marks-rows-dark.png
🔒 e2e-snooze-marks-plan.png
🔒 e2e-snooze-marks-hover.png
🔒 e2e-snooze-marks-narrow.png
🔒 e2e-snooze-marks-a11y.png

[2026-11-27T01:27:33Z · bob-cli-q5.5.1.6] Final visual-proof evidence (heading fix verified): updated report plus rows and live screenshots from the 71/72 run. Only reading-tomato-regression fails — pre-existing Today-reading defect, tracked as follow-up.

🔒 report.json
🔒 e2e-snooze-marks-rows.png
🔒 e2e-snooze-marks-rows-dark.png
🔒 e2e-snooze-marks-live-light.png
🔒 e2e-snooze-marks-reading-light.png

[2026-11-27T02:28:43Z · bob-cli-q5.5.1.6] HANDOFF — visual proof verified, vault deploy still pending. VERIFIED: real-Obsidian e2e scripts/obsidian-snooze-marks-e2e.cjs passes 71/72 in an isolated scratch vault (xvfb + CDP, synthetic notes, stub wake command): definition clocks indigo/amber/muted with exact tooltips, fresh/settled woken pills with exact late/early tooltips and history-line navigation, all row paints + heading summary in Live Preview and Reading, plan chip amber with forecast, both toggles incl Today-toggle gating, plain/Mod clicks, plan-chip jump, retime/link-win/delete liveness without reopening, no renderer errors, no note writes, line-height/toggles/narrow/reduced-motion/forced-colors evidence. Unit: full test:unit 10127 pass 0 fail; validate 12/12; e2e self-test wrapper registered. FIXED (in this phase): (1) Today toggle never gated snooze clocks in Live Preview or Reading (SM-D15) — gate added in 277a/277b plus Today-refresh hook in 275, covered by a new unit test and the e2e; (2) runtime HHMM/time handoff dropped all non-ignored row chips and all live history chips — colon conversion + parsed wake-label lookup in 278a/278b/278c, covered by a new unit test and the e2e; (3) Reading row sweep missed wrapped .el-* blocks — document-order walk in 278b, proven by the e2e. ATTACHED: report.json + light/dark screenshots for Live Preview, Reading, rows, plan, hover, narrow, a11y. REMAINING: `bob plugins sync` from the linked bob-plugins checkout, then close this bead. BLOCKED: the vault holds an uncommitted ws-15 build (guard refuses without -F, which is forbidden); ws-15 land-pipeline workers are still running. When the vault frees: run `bob plugins sync` in the linked checkout (verify `npm run build` first if the tree moved), confirm `bob plugins sync` reports the copy, then `sase bead close bob-cli-q5.5.1.6 --note <verified scope>`.

## Attachments

- 🔒 e2e-snooze-marks-a11y.png · image/png · 1024×800 · 72.8066 KiB (private attachment)
- 🔒 e2e-snooze-marks-hover.png · image/png · 1024×800 · 64.8486 KiB (private attachment)
- 🔒 e2e-snooze-marks-live-dark.png · image/png · 1024×800 · 59.3887 KiB (private attachment)
- 🔒 e2e-snooze-marks-live-light.png · image/png · 1024×800 · 59.2754 KiB (private attachment)
- 🔒 e2e-snooze-marks-narrow.png · image/png · 480×800 · 31.7109 KiB (private attachment)
- 🔒 e2e-snooze-marks-plan.png · image/png · 1024×800 · 29.6484 KiB (private attachment)
- 🔒 e2e-snooze-marks-reading-dark.png · image/png · 1024×800 · 92.2168 KiB (private attachment)
- 🔒 e2e-snooze-marks-reading-light.png · image/png · 1024×800 · 91.166 KiB (private attachment)
- 🔒 e2e-snooze-marks-rows-dark.png · image/png · 1024×800 · 95.9492 KiB (private attachment)
- 🔒 e2e-snooze-marks-rows.png · image/png · 1024×800 · 94.7363 KiB (private attachment)
- 🔒 report.json · application/json · 18.0264 KiB (private attachment)

## Dependencies

- **Depends on:** [bob-cli-q5.5.1.5](bob-cli-q5.5.1.5.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.5.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.6/README.md) | [bob-cli-q5.5.1.6](bob-cli-q5.5.1.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.5.1.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.6/README.md

<!-- sase:referenced-by:end -->
