# Bead: bob-cli-qq.10.1 — Bring the Reading cabinet paint within the 2x inline budget

[Bead Pages](../README.md) / [bob-cli-qq.10](bob-cli-qq.10.md) / bob-cli-qq.10.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.g7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.g7.md) · **Assignee:** `bob-cli-qq.10.1` · **Size:** medium
**Created:** 2026-11-27 09:12:20 EST
**Plan:** [202611/finish\_property\_card\_cabinets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_property_card_cabinets.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:123bdac55988a28deea913ed | attached via sase artifact create --bead |
| related | file:explicit:3a69f1836bc67ddc486f1621 | attached via sase artifact create --bead |
| related | file:explicit:3b27faf3543ebb5b750e685f | attached via sase artifact create --bead |
| related | file:explicit:67468d1c95e9bee47da0e9c0 | attached via sase artifact create --bead |
| related | file:explicit:6cc489fc30c1c542ac28b45f | attached via sase artifact create --bead |
| related | file:explicit:99cb2b63ed9f9cb99e085f58 | attached via sase artifact create --bead |
| related | file:explicit:d8f654f3081a6cedbf618286 | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

perf: profile the gate-open Reading paint of the 106-record album and the 64-row Projects host. Remove the double render and paint the breakdown confirms, without weakening fail-open or parity. Prove both perf checks pass in two athena runner runs.

## Notes

[2026-11-27T14:21:40Z · bob-cli-qq.10.1] perf profile breakdown (code inspection + attempt-28 runner medians), recorded before choosing the fix.

Gate-open Reading paint path for a catalog host (projects 64 rows; records 106 rows):
1. Obsidian renders the stored callout natively (unavoidable; the gate-closed inline baseline pays this too).
2. The kind's inline Reading painter decorates the native callout synchronously in its
   Markdown postprocessor (priorities 51-53: albums 51, records 52, projects 53, areas similar).
   Cost scales with row count (per-row DOM work over 64/106 rows).
3. The property-card host postprocessor (priority 46/47) batches via setTimeout(0), then
   paintReading mounts the card synchronously: foot build + propertyCardCabinetsAssemble
   (provider applies checks are sync, cached reports) + onMounted claims + Reading
   absorption hides the native callout.
4. The default-open body builds async: propertyCardCabinetRenderCatalog runs a SECOND
   full MarkdownRenderer.render of the same region source plus the same painter again,
   then binds links/hover. The body cache never helps across opens (a body inside another
   mount's container is not orphaned, so the fresh mount re-renders).
5. measureCatalogPaint stops the clock when cabinet-body li rows exist.

Attempt-28 medians (gate open vs inline): Projects 146-147ms vs 65-70ms (2.1-2.25x);
album 127-138ms vs 65-69ms (1.84-2.12x). Cabinet ~= inline + (inline painter + card
mount/stack + body re-render + body paint). The inline painter pass (step 2) is pure
waste under an open gate: its output is hidden by absorption in the same frame (each
painter already paint-then-strips when it sees a mounted stack). Removing it shortens
the measured window by the full painter cost with no new work added.

Chosen fix (plan candidate 1): defer the inline Reading painter for the measured kinds
(projects, records) when the gate is open on an eligible Reading surface. Skip the
synchronous paint; keep widget tracking; one bounded fallback timer (150ms, max 3
re-arms) paints the native callout only if no cabinet absorption covers it by then
(never-claimed, claim failed/released, card never mounted). Live Preview untouched.
Fail-open preserved: every path that shows the stored section paints it exactly as
today, only slightly later; plus 240wj failure branches now call a repaintNative hook
threaded from the kind providers (existing schedule*Refresh loops) so a failed body
still leaves today's painted catalog visible. No 240c surface/retry changes
(reading-miss owns that); no stored-byte or vault-format changes.

[2026-11-27T14:41:43Z · bob-cli-qq.10.1] PROPOSED FOLLOW-UP: test-block-id-prompt-task-links-api-performance typed-keystrokes p95 flakes under suite load (12.0ms vs 12ms budget; fails identically on clean tree) — consider a flaky-test bead or a looser budget

[2026-11-27T15:08:44Z · bob-cli-qq.10.1--1] perf evidence (env-fixed rerun, 2x athena real-Obsidian runs): run1 NO-GO 94p/3f — album PASS cabMed=142/inMed=77/cabMaxLT=0 (1.84x), projects FAIL cabMed=148/inMed=66/cabMaxLT=61 (2.24x over 2x budget); run2 NO-GO 95p/2f — album PASS cabMed=125/inMed=68/cabMaxLT=0 (1.84x), projects PASS cabMed=106/inMed=81/cabMaxLT=53 (1.31x). Both runs also fail area-reading-ready-after-plugin-reload + area-content-parity-gate-closed (area card absent after plugin reload; all 4 kinds, incl. untouched areas/notebooks). Evidence: file:explicit:3a69f1836bc67ddc486f1621 (run1), file:explicit:3b27faf3543ebb5b750e685f (run2), file:explicit:67468d1c95e9bee47da0e9c0 (shots tarball). Env note: first monitor attempt failed with runner-error only (no perf rows) because /tmp/cabinets-undici-deps held undici 8.13.1 (needs node>=22) on athena node v20.19.2; downgraded to undici 6.21.1 to restore CDP.

[2026-11-27T15:20:28Z · bob-cli-qq.10.1--1] clean-base control (HEAD 99458bd9, no perf fix, one athena run): NO-GO 95p/2f — album PASS cabMed=129/inMed=73 (1.77x), projects FAIL cabMed=157/inMed=68/cabMaxLT=63 (2.31x); fails: render-project-reading + perf-64-line-projects-host-within-budget. Same card-absent signature (widgets retries 8, hasSurface false). So the projects budget miss and card-absent flakes reproduce WITHOUT my change (clean is worse: 157 vs deferred 148/106). Diagnosis: deferral helps directionally, but a same-el re-render hits the unconditional paintNow() in the existing-widget branch of 241ae/241t, defeating the deferral; fixing that branch next (perf scope).

[2026-11-27T15:51:19Z · bob-cli-qq.10.1--1] perf iteration 1.172.7 (section-aware same-path skip, 241ae/241t): same-el re-render with unchanged section no longer paints synchronously (deferral/fallback/cabinet own it); new section still repaints so embed fragments cannot keep stale chrome. Unit proof: test-ledger-tools-cabinets-perf 11/11 (2 same-path tests + records section-change case), test-ledger-tools-projects-catalog 28/28 (fragment chrome test green again), build:check clean, bob plugins sync deployed 1.172.7, rsynced to athena /tmp/cabinets-perf-101. Full npm test: 10271/10277, only failure is pre-existing snooze-model-vectors (fails identically on clean HEAD worktree 99458bd9, unrelated path). e2e pair on 1.172.7: run1 ALL 97 checks pass incl. perf album 122/65 (1.88x) + projects 127/64 (1.98x); run2 perf album pass 147/78 (1.88x) but projects FAIL 167/71 (2.35x) + 2 area card-absent flakes (also seen on clean base). Evidence: file:explicit:6cc489fc30c1c542ac28b45f (run1), file:explicit:123bdac55988a28deea913ed (run2), file:explicit:99cb2b63ed9f9cb99e085f58 (shots), clean control file:explicit:d8f654f3081a6cedbf618286. Diagnosis: projects cabinet median swings 106-167ms run-to-run on the identical tree (long task 53-74ms from the body second MarkdownRenderer.render, which deferral does not remove); clean base misses too (157/68). Bar (both perf checks green in BOTH runs) not met — bead stays open for Bryan.

[2026-11-27T15:51:33Z · bob-cli-qq.10.1--1] PROPOSED FOLLOW-UP: projects Reading cabinet still misses the 2x inline budget about half the time on athena (cabinet 106-167ms vs inline 64-81ms; long task 53-74ms from the body second MarkdownRenderer.render in 240wj). Options: reuse the inline DOM for the body instead of re-rendering, or widen/retune the budget for machine variance. Evidence runs file:explicit:6cc489fc30c1c542ac28b45f vs file:explicit:123bdac55988a28deea913ed; clean-base miss file:explicit:d8f654f3081a6cedbf618286.

[2026-11-27T15:51:40Z · bob-cli-qq.10.1--1] PROPOSED FOLLOW-UP: test-snooze-model-vectors mutation vector fails on clean HEAD too (navigation runs all canonical snooze add and drop mutation vectors; expected body without trailing woke line, actual appends ~~1530~~ woke 15:32) — pre-existing, unrelated to perf scope. No tracking task bead found.

## Dependencies

- **Blocks:** [bob-cli-qq.10.4](bob-cli-qq.10.4.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.10.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.10.1.md) | [bob-cli-qq.10.1](bob-cli-qq.10.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@17a64fa`](https://github.com/bobs-org/bob-plugins/commit/17a64fabb6040db49d8fd77bec404d4f513913d7) | perf(ledger-tools): defer gate-open Reading inline paint for projects/records cabinets | [bob-cli-qq.10.1](bob-cli-qq.10.1.md) | 2026-11-27 10:53:10 EST |
