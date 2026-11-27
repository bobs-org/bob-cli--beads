# Bead: bob-cli-q5.5.1 — Snooze display marks and plan chip

[Bead Pages](../README.md) / [bob-cli-q5.5](bob-cli-q5.5.md) / bob-cli-q5.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.5.md) · **Assignee:** `bob-cli-q5.5.1.land`
**Created:** 2026-11-26 15:37:08 EST · **Closed:** 2026-11-27 01:24:39 EST
**Plan:** [202611/snooze\_display\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_display_marks.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/snooze_display_marks.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_display_marks.md

<!-- sase:links:end -->

## Description

Complete bob-cli-q5.5 with live snoozed definition marks, woken-link pills, Snoozed row and heading paint, an independent plan chip, and verified light/dark Obsidian evidence without changing note bytes or Today semantics.

## Notes

[2026-11-27T03:43:51Z · bob-cli-q5.5.1.land] LAND REVIEW (bob-cli-q5.5.1.land). Verified: all 6 phases closed; bob-cli ba21e4c2 contract + 70 SM vectors; bob-plugins 27157a49/72917260/514f7992/b7f17a51/73d028e5; marks.json byte-identical to bob-cli canonical; 53/53 snooze unit + e2e self-test pass at bob-plugins a4bd99f2; build:check clean; vault bob-ledger-tools main.js/styles.css/manifest byte-identical to a4bd99f2; no epic-symbols for q5.5.1 or q5.5. Integration (bob-cli, this turn): docs/snooze-marks.md JavaScript mirror now names the landed fragments/tests/e2e (plan-era wording removed), docs/today-marks.md notes the shared slot + Today toggle gating clocks, docs/plan.md Snoozed forecast links the plugin chip. REMAINING EPIC WORK (caused by definition-marks 27157a49, deployed): screenshots live-light/live-dark/hover show the definition clock time wrapping one digit per line in the fixed 1.2em inline-flex box and overlapping neighbouring lines; CSS tone selectors .bob-snooze-mark--asleep/--due/--blocked never match emitted classes --indigo/--amber/--muted so no state color paints; due clocks never show the visible '· due' word (element takes bare HH:MM, ::after shows only time); glyph is the color emoji with mask:none instead of the Lucide alarm-clock mask tinted currentColor (definition clock and woken pill). The e2e passed because it reads class names and data attributes, not rendered layout/computed color. Planned as a lander tale. FOLLOW-UP TRIAGE: (1) vault-format.md 6030/6000 budget (q5.5.1.4 #1, .5 #1, .6 #2) -> +1 on existing bob-cli-oc; root cause ebc45fec (bob-cli-qm.7) already a DISCOVERED ISSUE on active epic bob-cli-qm; not caused by this epic. (2) Reading-view Today tomatoes never attach (q5.5.1.6 #1) -> new task bob-cli-qs (bug, large, ready); land agent reproduced it on the pre-epic bundle feaa5b42 (report file:explicit:9c81ddbaa8df1a6b70768210), so not caused by this epic. (3) Deploy-blocked notes (q5.5.1.2 #1, q5.5.1.3 #1) -> declined: resolved by q5.5.1.6 deploy, vault verified byte-identical. (4) ENOSPC /tmp (q5.5.1.2 #2) -> declined as a task: host hygiene, not repo code; /tmp (32G tmpfs) is again 100% full from ad-hoc agent acceptance clones (bob-settings-acceptance-* ~11G from 2026-11-25, bob-cli-*-q5-build ~6.6G); reported to Bryan for cleanup. Gates this turn: bob-cli docs build/links/urls pass; lint and 2 tools/docs tests fail only on the pre-existing vault-format budget (bob-cli-oc); just check: 3 failures, none from this epic (wispr_summary pdftotext kicker = bob-cli-q9, +1 recorded; 2 live highlights PDF tests = ENOSPC writing /tmp).

[2026-11-27T06:24:39Z · bob-cli-q5.5.1.land--a] Verified all six phases and 70 SM vectors are complete. bob-plugins fix 24f38233 corrects the clock width, state colors, due label, and masked Lucide glyph; the post-fix real-Obsidian report attached to bob-cli-q5.5 has 82/83 checks passing, with the sole failure reading-tomato-regression (known pre-epic behavior tracked by bob-cli-qs). Inspected Live Preview and Reading light/dark, hover, narrow, plan-chip, and a11y screenshots. npm run build:check passed. Pre/post-sync startup smoke reports have pass=true and failures=[] though their monitor wrappers exited 1 despite the PASS output; the post-deploy check is ok=true with zero drift and all 12 plugins synced. The deployed main.js and styles.css byte-match bob-plugins source at c476086a. Post-deploy report file:explicit:02441f8e4443975b75eab2cb is attached to bob-cli-q5.5. Epic-symbol scans are empty. Prior notes retain the unrelated vault-format budget failure (bob-cli-oc) and /tmp ENOSPC failures.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.5.1.land.md) | [bob-cli-q5.5.1](bob-cli-q5.5.1.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dfb5e75`](https://github.com/bobs-org/bob-cli/commit/dfb5e7550051ce797bcb7d2de665900c0eaf2fde) | docs(snooze): describe the landed snooze-marks mirror and cross-link Today marks and plan | [bob-cli-q5.5.1](bob-cli-q5.5.1.md) | 2026-11-26 22:46:13 EST |
| bob-cli | [`d9f5774`](https://github.com/bobs-org/bob-cli/commit/d9f57741c248db678bcf43b56eade3b16a2e88f4) | docs: describe snooze clock labels and glyph contract | [bob-cli-q5.5.1](bob-cli-q5.5.1.md) | 2026-11-26 23:11:29 EST |
| bob-cli--plans | [`bob-cli--plans@dbb59a2`](https://github.com/bobs-org/bob-cli--plans/commit/dbb59a2832260f1198fd2260d6646ef43ab7568b) | docs(plan): mark snooze display epic done | [bob-cli-q5.5.1](bob-cli-q5.5.1.md) | 2026-11-27 01:26:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.5.1.2][1] | Need parent epic scope and notes | 1 |
| read-by | [agent:bob-cli-q5.5.1.3][2] | Need governing decisions and prior phase notes for the woken-pills scope | 1 |
| read-by | [agent:bob-cli-q5.5.1.land][3] | Need the epic scope, children, and linked plan file | 1 |
| read-by | [agent:bob-cli-q5.5.1.land--5][3] | Verify phase completion and existing acceptance evidence before deciding closure | 1 |
| read-by | [agent:bob-cli-q5.5.1.land--a][3] | Check whether the clock-render follow-up evidence has been recorded and whether it is resolved | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.5.1.land.md

<!-- sase:referenced-by:end -->
