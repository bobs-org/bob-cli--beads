# Bead: bob-cli-nh.6.1 — Extract the shared property-card kit

[Bead Pages](../README.md) / [bob-cli-nh.6](bob-cli-nh.6.md) / bob-cli-nh.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.md) · **Assignee:** `bob-cli-nh.6.1.land`
**Created:** 2026-11-19 09:44:34 EST · **Closed:** 2026-11-19 18:10:20 EST
**Plan:** [202611/property\_card\_kit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_kit.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/property_card_kit.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:14696680ebb0a23080ad9414 | attached via sase artifact create --bead |
| related | file:explicit:dec33b788961cadeb2b4261a | attached via sase artifact create --bead |
| related | file:explicit:e5c34f58f439dc2d795d5d93 | attached via sase artifact create --bead |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_kit.md

<!-- sase:links:end -->

## Description

Album, record, and bank cards share property ownership, editor registration, host lifecycle, and chrome while preserving their behavior and appearance; the verified and deployed kit unblocks the intention-card phase.

## Notes

[2026-11-19T22:29:51Z · bob-cli-nh.6.1.land] LAND AUDIT / REMAINING WORK: Read the epic, all notes on .1/.2/.3, parent phase nh.6 and both linked plans. Reviewed kit commits ccfc12b, 8d6fd78, 946ef56, 2f1e016 and source for ownership, registry, shared host/editor, all three adapters, chrome, tests and extension docs. Existing documented behavior/deploy evidence is substantiated by artifacts 5366ba3f1c91e381b416eb0b, b9fee3d94935c22cdac23dbb and 57b7adc6f806ce185b185519 (original baseline 36d4801; final record 144/144, album 120/121, bank 75/78, exact chrome 24/24; known base failures retained). Parent DECISIONS honored: no memory/declined decision edits in kit, intention UI remains nh.7. Integration audit through plugins 2f1e016 and CLI 992fd33d: intervening copy chips, successor marks, log recall and CLI intention/period/bank work do not add a property-card host or conflict; log-recall lifecycle/mixin/fragment additions coexist. Copy-card row-order was already fixed by d6d2c33 (fresh model suite 59/59). Fresh validate passes 12/12 including generated bundles/inventory. Neither nh.6.1 nor nh.6 has epic-symbol entries; no symvision recipe in current justfile. Two epic-owned gaps block close: (1) registry miss fallback silently restores an unregistered built-in on next ==; target-kind facade remains a closed switch and extra gate kinds use module-global state; (2) shared Reading repaint catches exceptions without removal/release, and editor rebuild exceptions likewise leave old ownership. Scratch failure probes on exact clean 2f1e016: original registry 25/25 plus unregister probe fails 1!=0; original host 12/12 plus Reading/editor cleanup probes both fail true!=false. Durable runnable probes/logs: file:explicit:dec33b788961cadeb2b4261a. A medium tale plans only these repairs and verification, ending with normal nh.6.1 close, available symvision, property_card_kit plan status done, API/evidence handoff and normal close of parent phase nh.6; nh remains open. No production edits made by this lander. Follow-up dispositions will be recorded separately before proposal.

[2026-11-19T22:33:09Z · bob-cli-nh.6.1.land] FOLLOW-UP TRIAGE COMPLETE before tale proposal: Used sase_new_task; read bead/size policies, searched all-status task reports plus same-type CI queries, swept all 55 tasks created in the last week, and inspected active epic scopes and the causally relevant ms.8/child. Every PROPOSED FOLLOW-UP disposition: nh.6.1.1 notes 3/4 acceptance/deploy proposals declined as new work because notes 5/10 and chrome acceptance complete them; note 6 long-TMPDIR launch defect is new small CI task bob-cli-np, linked to closed web-clip-only 5b without reopening that fixed task; note 7 album schema-field-jump-ctrl-j is new large CI task bob-cli-nq (unknown root cause, repeated pre-kit baseline failure); note 8 bank invalid-fence and walk-learn corroborated m6/m7 with attributed evidence; note 9 and nh.6.1.2 note 5 event-link-times timing corroborated exact existing km, not a new ki umbrella; nh.6.1.2 note 2 dependency-stage 382ms/250ms then 33ms isolated corroborated m1. nh.6.1.2 note 4 and nh.6.1.3 note 1 copy-card row-order proposals declined as fixed by upstream d6d2c33 and fresh 59/59 model tests. nh.6.1.2 note 5 record Markdown-neutrality/startup-sync race routed as DISCOVERED ISSUE to active bob-cli-ms.8, whose child .8.3.1.2 introduced the acceptance runner; no unrelated task. nh.6.1.3 note 2 clean-base bank setup Ctrl+K and one-Enter save became separate large CI tasks nr and ns because no shared cause is established; both related to mk coverage but distinct from its missing walkthroughs. nh.6.1.3 notes 2/3 unchanged Mac docs 6171/6027 word budgets corroborated reopened jz. New np/nq/nr/ns are all ready; each names the proposing bead, reproduction, evidence and sizing rationale. Corroborations relay phase observations honestly, not newly claimed CDP/timing runs. No other proposals found. None of these unrelated baseline findings blocks the kit; the two demonstrated registry/host gaps in the preceding LAND AUDIT remain epic work and are the sole repair scope of the validated medium tale sase_plan_property_card_kit_closeout.md. Carry these dispositions into its eventual close note.

[2026-11-19T23:10:20Z · bob-cli-nh.6.1.land] Closeout tale landed on linked bob-plugins atop reviewed 2f1e016 with bob-cli 992fd33d. (1) Registry is now the sole dispatch authority: one shared builtin matcher backs the entries and the schemaDoubleEqualsTargetKind facade, which also accepts an explicit instance registry for extension resolution; the keydown path never re-seeds builtins or consumes Vim on a runtime miss; per-instance extension kinds replaced the module-global list and the gate default is builtins-only with registry kinds passed as allowedKinds. (2) Shared host enforces failure cleanup: a throwing Reading repaint removes that mount through the adapter path-bound removeReading and releases only its generation/path-bound ownership; failed editor construction cleans up with fallback decorations and stays tracked for recovery, failed rebuild cleans up and rethrows; widgets stay tracked so the next refresh recovers. Integration recheck: intervening copy chips, successor marks, log recall, and CLI intention/period/bank work add no competing property-card host or dispatch path. Gates on the repaired tree: build and build:check clean; test:unit 7569 pass 0 fail 2 skipped (double-equals 29/29, host 20/20, ownership 13/13); test:perf 9/9; validate 12/12; both archived LAND probes pass unmodified; docs:check reports only the 2 known over-budget Mac Capture refs 6171/6027 words (tracked by reopened bob-cli-jz, unchanged). Real acceptance on athena with checkout-built Bob 979bdf8993f9866fb6b12e29c8a3e447e74d19b3e49f47f76451d7a706fd5ed9: album 120/121 with only schema-field-jump-ctrl-j (clean-base, bob-cli-nq); record full-scope 144/144; bank 73/78 with invalid-fence and walk-learn-coffee/accept (clean-base, bob-cli-m6/m7) plus queue-card-live/reading missing-import-command pair, proven to be drift from intervening bank queue-card work by rerunning the identical suite on the same HEAD with these repairs stashed (same 73/78, same 5 names; zero repair delta); bank setup 46/47 with setup-group-jump-ctrl-k (bob-cli-nr) plus the known one-Enter arrangement-save timeout (bob-cli-ns); chrome matrix 24/24 exact pixel pairs vs 36d4801. Deployed with bob plugins sync from the opened checkout (exit 0, 1.140.0, main.js dd856af6da73600b and styles 9741733455cc7e2a verified equal in the vault). Evidence: file:explicit:14696680ebb0a23080ad9414 (summary) and file:explicit:e5c34f58f439dc2d795d5d93 (full bundle with reports, provenance, screenshots). Follow-up dispositions carried from the lander triage: nh.6.1.1 notes 3/4 declined (complete via notes 5/10 and chrome evidence); note 6 is bob-cli-np; note 7 is bob-cli-nq; note 8 corroborated m6/m7; note 9 and nh.6.1.2 notes 2/5 corroborated km/m1; copy-chip row-order declined as fixed by d6d2c33 (59/59); record markdown-neutrality routed as DISCOVERED ISSUE to active ms.8; bank setup Ctrl+K and one-Enter save are nr/ns (related to mk, distinct causes); unchanged Mac word budgets corroborated reopened jz. Epic-symbols clean for nh.6.1 and nh.6; no symvision recipe exists in the justfile, recorded as absent rather than claimed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.land.md) | [bob-cli-nh.6.1](bob-cli-nh.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@54eebe7`](https://github.com/bobs-org/bob-cli--plans/commit/54eebe7a0474c4087fb16cbb75eecb991b8fc26c) | chore(plans): mark property\_card\_kit status done | [bob-cli-nh.6.1](bob-cli-nh.6.1.md) | 2026-11-19 18:27:36 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.6.1.1][1] | Need parent epic scope | 1 |
| read-by | [agent:bob-cli-nh.6.1.2][2] | Need epic DECISIONS for host phase | 1 |
| read-by | [agent:bob-cli-nh.6.1.3--3][3] | Verify only the requested phase closed and ancestors remain open | 1 |
| read-by | [agent:bob-cli-nh.6.1.land--1][4] | Need closeout dispositions and evidence refs before closing | 1 |
| read-by | [agent:research.5i.gem][5] | Check exact subphases of property-card kit epic | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.2.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.3.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.6.1.land.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5i.gem/README.md

<!-- sase:referenced-by:end -->
