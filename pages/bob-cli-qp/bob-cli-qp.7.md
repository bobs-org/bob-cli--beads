# Bead: bob-cli-qp.7 — Real-Obsidian acceptance and screenshot review

[Bead Pages](../README.md) / [bob-cli-qp](README.md) / bob-cli-qp.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6l.linker.w0.md) · **Assignee:** `bob-cli-qp.7` · **Size:** medium
**Created:** 2026-11-26 14:22:09 EST · **Closed:** 2026-11-27 00:11:28 EST
**Plan:** [202611/ref\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_cards.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:4f6ec6de1f7e3ef296d67c86 | attached via sase artifact create --bead |
| related | file:explicit:65cd84a81d3610f4285ddd5c | attached via sase artifact create --bead |
| related | file:explicit:71e7c7a55117ffd98b5fec4b | attached via sase artifact create --bead |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

ref-acceptance: after bob-cli-qm.6 closes, extend the takeover harness as a sibling runner. Prove takeover, single ownership, native restoration, passivity, data, and editor flows. Review the light, dark, narrow, wide, forced-colors, and grayscale screenshot matrix beside the other family cards.

## Notes

[2026-11-26T21:29:22Z · bob-cli-qq.1] COORDINATION: cabinets kit adds the 240w* cabinet-owned gate/model/state/provider/collector, plus role-aware fold changes in 240s and state binding in 240r; later cabinets phases add gate-guarded hunks in 240o, 248m, and styles.css. Rendering and behavior remain current while cabinetsPreview is absent. Please keep these guarded hunks through go-live cleanup. Cabinets go-live waits for bob-cli-qm.7 and bob-cli-qp.8.

[2026-11-27T05:10:19Z · bob-cli-qp.7] ACCEPTANCE GO: real Obsidian 1.15.1 (athena, Xvfb) with isolated profile + disposable Git vault, refCardPreview on; bob 0.6.0 debug build of clean bob-cli master ebc45fec (has ref-props; props_v1 + props_ref_contract_v1 confirmed); bob-plugins f279186d + this change (ledger-tools 1.172.1). Sibling runner scripts/obsidian-ref-card-acceptance-e2e.cjs (+ new -flows.cjs) imports the takeover lib, never forks it. 54/54 checks: takeover LP+Reading on 14 fixtures; single owner (hub, mixed, assets, ref_history, bad YAML, closed gate = native); native restoration (source, embed, hover, canvas, print, mobile, failed mount, unload/disable, source/cache mismatch, rename and scan-rewrite while open); capability (props_v1 pending/absent/failed keep native, no ref contract -> title fallback, failing report -> identity-only, late snapshot keeps layout, stale kept); data vs real bob ref list (lanes incl. Legacy, annotations, vN, arXiv copy, Today pill, LP annotation jump, PDF+Listen on Linux, missing-PDF lint); editor (6 rows set/undo, clear or set-only refusal, Title H1 retitle, PDF-marker + link-text effects, owned routes, protected-key refusals, Esc/q/Ctrl+[ ladder); keys (==, +, -, _, gg/k/Up, Tab); passive (0 writes/spawns, protected hashes + PDF bytes unchanged; 0 console errors). 59/59 screenshots inspected and approved; per-kind icons stay (no bookmark switch). Evidence: file:explicit:71e7c7a55117ffd98b5fec4b (reviewed report), file:explicit:65cd84a81d3610f4285ddd5c (run+build log), file:explicit:4f6ec6de1f7e3ef296d67c86 (screenshots). REPAIRS (bob-plugins): LP annotation jump no-op (CM EditorView path); readout row shifted ~20px on report arrival (reserved row + text-like chips); byline separators cramped; narrow snoozed lane overflowed card edge (ellipsis); legacy lane glyph lacked VS16; Ref Card gg/k/Up landed above the hidden title (new 249w capture+clamp guard); cabinets 240wg atomicRanges returned arrays, throwing on every LP cursor motion. Fixtures: legacy notes gain status legacy, Highlights comments use the Comment prefix, blog gains parent. npm test green (10164 pass), build:check green, bob plugins sync clean (no -F).

[2026-11-27T05:10:34Z · bob-cli-qp.7] PROPOSED FOLLOW-UP: cabinets atomicRanges repair needs a cabinets-side regression check — 240wg returned plain arrays from EditorView.atomicRanges (registered unconditionally at plugin load since a4bd99f2), so every Live Preview Vim/arrow motion threw TypeError ".between is not a function" in the deployed vault; fixed here with propertyCardCabinetAbsorbAtomicRangeSet + unit test; the bob-cli-qq acceptance runner should also fail on console errors.

[2026-11-27T05:10:41Z · bob-cli-qp.7] PROPOSED FOLLOW-UP: verify the home-card Vim visible-body guard (249db) in real Obsidian — it intercepts via Prec.highest domEventHandlers, but Obsidian Vim consumes keydown first (the same design did not engage for the Ref Card, which now uses a document capture listener plus post-motion clamp in 249w); Notebook and Prose cards have no guard at all; unify the three into one shared kit helper after the go-lives.

[2026-11-27T05:10:47Z · bob-cli-qp.7] PROPOSED FOLLOW-UP: athena /tmp tmpfs is 100% full (other agents' leftovers: /tmp/bob-settings-acceptance-*, /tmp/bob-cli-{clean,dirty}-q5-build, /tmp/bob-bank-editor-routing-*); Xvfb cannot compile its keymap so xvfb-run real-Obsidian e2e runs fail there; this run used unshare -Urm with a disk-backed /tmp bind mount; clean up or give e2e runners a disk TMPDIR.

[2026-11-27T05:10:54Z · bob-cli-qp.7] PROPOSED FOLLOW-UP: at narrow widths (≤420px) the shared title-block actions row (fold toggle, 240g kit) wraps beneath the dek on every family card; consider pinning actions to the kicker row.

[2026-11-27T05:11:00Z · bob-cli-qp.7] PROPOSED FOLLOW-UP: docs-check fails on clean trees: bob-cli docs/reference/vault-format.md is over the 6000-word reference budget (6030); already tracked by bob-cli-oc.

[2026-11-27T05:11:06Z · bob-cli-qp.7] OBSERVATION: one intermediate native run (before the namespace/X changes) saw protected album fixtures (body.md, dup.md, eat.md, eat/corner-bistro.md, snacks.md) change during the passive matrix; it did not recur in the 7 later runs; the runner now records per-phase hash checkpoints and diffs so a recurrence is localized.

[2026-11-27T05:11:28Z · bob-cli-qp.7] GO: real Obsidian 1.15.1 acceptance on athena, 54/54 checks (takeover, single owner, native restoration, capability, data vs real bob ref list, editor, keys, passive; 0 console errors) and 59/59 screenshots inspected and approved (light/dark x narrow/wide x LP/Reading for 5 samples, family album/notebook/prose/area, forced-colors + grayscale species distinction: keep per-kind icons, native source recovery). bob 0.6.0 from clean bob-cli master ebc45fec; bob-plugins f279186d + repairs (LP annotation jump, readout layout shift, byline spacing, narrow lane ellipsis, legacy glyph VS16, 249w Ref Card gg/k/Up guard, cabinets atomicRanges RangeSet). npm test green (10164 pass), build:check green, bob plugins sync clean. Evidence file:explicit:71e7c7a55117ffd98b5fec4b, file:explicit:65cd84a81d3610f4285ddd5c, file:explicit:4f6ec6de1f7e3ef296d67c86.

## Dependencies

- **Depends on:** [bob-cli-qp.5](bob-cli-qp.5.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qp.6](bob-cli-qp.6.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qp.8](bob-cli-qp.8.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qp.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qp.7/README.md) | [bob-cli-qp.7](bob-cli-qp.7.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d32d7a9`](https://github.com/bobs-org/bob-plugins/commit/d32d7a9823b0fcdca753c8dce8f714c479a7c238) | test(ref-card): add native acceptance review harness | [bob-cli-qp.7](bob-cli-qp.7.md) | 2026-11-26 18:22:23 EST |
| bob-plugins | [`bob-plugins@880ee82`](https://github.com/bobs-org/bob-plugins/commit/880ee823efd98f3f2507b2624de84a508ea24d10) | test(ref-card): capture native launch diagnostics | [bob-cli-qp.7](bob-cli-qp.7.md) | 2026-11-26 19:38:43 EST |
| bob-plugins | [`bob-plugins@2bd92b1`](https://github.com/bobs-org/bob-plugins/commit/2bd92b19a42054ba6b11aba0c4a997d412b6ed48) | fix(ref-card): pass real-Obsidian acceptance and repair review defects | [bob-cli-qp.7](bob-cli-qp.7.md) | 2026-11-27 00:12:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qp.7][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-qp.7--1][1] | Need exact remaining-work notes before rerunning acceptance | 4 |
| read-by | [agent:bob-cli-qp.8][2] | Review acceptance evidence and close notes for go-live handoff | 2 |
| read-by | [agent:bob-cli-qp.8--1][2] | Collect ref acceptance evidence refs for the go-live provenance note | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qp.7.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qp.8.md

<!-- sase:referenced-by:end -->
