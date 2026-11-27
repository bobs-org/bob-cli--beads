# Bead: bob-cli-qq.10.1 — Bring the Reading cabinet paint within the 2x inline budget

[Bead Pages](../README.md) / [bob-cli-qq.10](bob-cli-qq.10.md) / bob-cli-qq.10.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.g7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.g7.md) · **Assignee:** `bob-cli-qq.10.1` · **Size:** medium
**Created:** 2026-11-27 09:12:20 EST · **Closed:** 2026-11-27 13:52:13 EST
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
| related | file:explicit:99309d341ce63ec6d8668bdf | attached via sase artifact create --bead |
| related | file:explicit:99cb2b63ed9f9cb99e085f58 | attached via sase artifact create --bead |
| related | file:explicit:b003208183d954bfcc1f66ec | attached via sase artifact create --bead |
| related | file:explicit:b29439ea2b9eecb93bc313ee | attached via sase artifact create --bead |
| related | file:explicit:ccb420b8ac54123b122fc74e | attached via sase artifact create --bead |
| related | file:explicit:d8f654f3081a6cedbf618286 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

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

[2026-11-27T18:50:23Z · bob-cli-qq.10.1] perf profile (CDP Profiler + performance.mark timelines inside the real runner, athena): the projects 50-74ms long task was NOT the Reading body render. A Reading leaf keeps its Live Preview editor loaded but hidden (.markdown-source-view display:none); on every open the hidden editor built the full card and rendered the Projects cabinet body through MarkdownRenderer (~40-45ms) before Obsidian rendered the preview. Other costs on the window: propertyCardCabinetHostDigest (paintKey) applied all four kinds and stable-stringified every full report ~16x per open; the earlier inline-paint deferral never applied because Obsidian post-processes Reading sections detached (el.closest fails), so the native callout was always painted and the Reading body re-rendered it (records ~16-20ms). Also found: the Records body never tagged its Reading absorption (claim ran while the card was detached and onOpen re-claimed with no scope), so album Reading showed the stored Records section twice (same on clean master).

[2026-11-27T18:50:39Z · bob-cli-qq.10.1] perf fix (bob-ledger-tools 1.172.9, rebased on bob-plugins 4dd95d52): (1) 240wl deferWhileHidden: an opted-in provider body (host catalogs) in a hidden Live Preview editor builds only when IntersectionObserver sees its panel; records keeps its claim but defers the render the same way. (2) 241al digest memo keyed by source + per-kind report-state identity. (3) 240wd deferral eligibility answers detached sections through ctx.containerEl (embed/popover/card-body containers never defer) and only for area/project (projects) or album (records) frontmatter types; detached-at-fire sections get the bounded retries. (4) 240wj Reading bodies clone the unpainted native callout (Reading-only list chrome stripped) instead of a second MarkdownRenderer pass; painted/embed/mismatched/detached falls back to render. (5) Records Reading claim tags via the host Reading scope (album header threads readingScope) and onOpen keeps a live tagged Reading claim. New tests: scripts/test-ledger-tools-cabinets-reading-paint.cjs (12), cabinets-perf (11, ctx frontmatter added). Focused suites 133/133; npm test 10307/10313 with only test-snooze-model-vectors failing, which fails identically on clean 4dd95d52; build:check + docs inventory clean; bob plugins sync deployed 1.172.9.

[2026-11-27T18:50:46Z · bob-cli-qq.10.1] perf evidence, unmodified runner on athena, 1.172.9: run1 album cab 117/inl 69 (1.70x) projects 107/62 (1.73x), no cabinet long tasks, 99 pass/1 fail; run2 album 109/65 (1.68x) projects 109/59 (1.85x), no cabinet long tasks, 99 pass/1 fail; 0 runtime exceptions, 0 console errors both runs. Both perf-* checks PASS in both runs. The one failure in each run is keys-reading-pick-overlay-lists-numbered-kinds, which also fails on the clean master 4dd95d52 control (that control also fails projects perf 143/68, 2.10x). Earlier runs of an intermediate build (before the records hidden-editor deferral) were noisier: one album 187/73 (two 50-90ms long tasks) and one projects 131/65 (2.02x). Evidence: run1 file:explicit:b29439ea2b9eecb93bc313ee, run2 file:explicit:6f2132b1212738d3a422cce

… and 3025 more characters

## Dependencies

- **Blocks:** [bob-cli-qq.10.4](bob-cli-qq.10.4.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qq.10.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qq.10.1/README.md) | [bob-cli-qq.10.1](bob-cli-qq.10.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@17a64fa`](https://github.com/bobs-org/bob-plugins/commit/17a64fabb6040db49d8fd77bec404d4f513913d7) | perf(ledger-tools): defer gate-open Reading inline paint for projects/records cabinets | [bob-cli-qq.10.1](bob-cli-qq.10.1.md) | 2026-11-27 10:53:10 EST |
| bob-plugins | [`bob-plugins@cb31472`](https://github.com/bobs-org/bob-plugins/commit/cb314726d4b5badf36aa1afcc6ec75303a47fb05) | perf(ledger-tools): keep gate-open Reading cabinet paint within 2x inline | [bob-cli-qq.10.1](bob-cli-qq.10.1.md) | 2026-11-27 14:06:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qq.10.1--1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:research.6o.gem][2] | Check remaining bob-cli-qq work and property-card kit seams for parallel execution analysis | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qq.10.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6o.gem/README.md

<!-- sase:referenced-by:end -->
