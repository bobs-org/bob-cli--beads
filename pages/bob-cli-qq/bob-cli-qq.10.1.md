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
| related | file:explicit:3a69f1836bc67ddc486f1621 | attached via sase artifact create --bead |
| related | file:explicit:3b27faf3543ebb5b750e685f | attached via sase artifact create --bead |
| related | file:explicit:67468d1c95e9bee47da0e9c0 | attached via sase artifact create --bead |
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

## Dependencies

- **Blocks:** [bob-cli-qq.10.4](bob-cli-qq.10.4.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.10.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.10.1.md) | [bob-cli-qq.10.1](bob-cli-qq.10.1.md) | 0 |
