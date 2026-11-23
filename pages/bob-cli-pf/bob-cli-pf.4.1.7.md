# Bead: bob-cli-pf.4.1.7 — Finish the core property editor's landing repairs and real-app acceptance

[Bead Pages](../README.md) / [bob-cli-pf.4.1](bob-cli-pf.4.1.md) / bob-cli-pf.4.1.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.land.md) · **Assignee:** `bob-cli-pf.4.1.7.land`
**Created:** 2026-11-23 03:09:55 EST · **Closed:** 2026-11-23 12:29:38 EST
**Plan:** [202611/property\_editor\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_landing_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/property_editor_landing_repairs.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:100794501f510b52e4d301a2 | attached via sase artifact create --bead |
| related | file:explicit:3dd66eae5b7b4285c7d4a2db | attached via sase artifact create --bead |
| related | file:explicit:6613646d2f833b8c8fd3468b | attached via sase artifact create --bead |
| related | file:explicit:67292147c2af0fb1dbc34095 | attached via sase artifact create --bead |
| related | file:explicit:bfad2cb954f520df8821b7b4 | attached via sase artifact create --bead |
| related | file:explicit:fc123a59cb45c2d89a6be43e | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_landing_repairs.md

<!-- sase:links:end -->

## Description

The =+ property editor survives in-flight writes, keeps the requested row, shows confirmed writes on every surface, and passes a reviewed real-Obsidian run covering every bob-cli-pf.4.1 acceptance bullet.

## Notes

[2026-11-23T16:29:09Z · bob-cli-pf.4.1.7.land] LAND FOLLOW-UP TRIAGE: Reviewed every note on .1-.4, including all five PROPOSED FOLLOW-UP entries. .3 #1 modal-open lifecycle: declined as new work, already repaired by e65cfe03/3bd5c5c2/e06f85e3 and successful real-app runs. .3 #5 cramped shell: declined as new work, addressed by .4 (1408a834/e60541b3/e2e944af/26613027), with explicit four-image review in .4 #7. .4 #4 task-drawers nav: declined as new work, fixed since the proposal by bob-cli f6cf62cf, mkdocs.yml:375. .4 #5 task_reqs README twin drift: reproduced on bob-plugins b2c37102 vs bob-cli f6cf62cf (6/7 tests, canonical README mismatch), caused by drawer-reader commit 37b2080e; DISCOVERED ISSUE recorded on active epic bob-cli-ph, identifying plugin-readers phase bob-cli-ph.2. .4 #6 timing flakes: corroborated existing bob-cli-km and bob-cli-io with +1 and attached .3 acceptance evidence. No new task beads. Parent pf.4.1 prior triage already covers pg, fixed period-date and req-close twins, and nested-checkout fixture artifacts.

[2026-11-23T16:29:22Z · bob-cli-pf.4.1.7.land] LAND AUDIT: Not yet complete. Reviewed all four child notes and both audited real-app reports (writes file:explicit:8fc60a0e749f3dac06629c1b:75 pass/1 conditional skip, 36 exact-byte comparisons; surfaces file:explicit:49ee66906e8ea8acb9a84f58:129 pass, 37 byte comparisons, no plugin errors). Current focused property suites and harness pass 306/306 on bob-plugins b2c37102. Source/commit audit confirms write guards, history/overlays, session registration, typed old-bob refusal, close ladder, recovery targeting, values and shell repairs. Canonical record resolver fix de66b399 matches role gates. Remaining defect: 298m propertyEditorStartYamlExcursion saves only selectedKey; propertyEditorYamlDoneAttempt calls nearest with ordinal:0,line:null and reopens with key only. It loses source position and duplicate occurrence. The stored real report itself shows keep_me deletion returning to type line 2, not nearest edit_me line 3; e2e-surfaces line 251 only checks any selection. Its screenshot review assertion is automated geometry and registered report still says pending inspection; the manual observations exist only in .4 #7. A medium repair tale will retain complete selection through Done and strengthen exact row/occurrence assertions and honest reviewed report evidence, then finish this epic and nested parent closeout. Integration reviewed non-epic commits since 08:09Z across bob-cli (7703011d through f6cf62cf) and bob-plugins (eb236b40, ddbf8bd9, ea00e182, c8846754, b2c37102): task requirements/drawers, docs, and additive tick network classification do not require property-editor changes; shared main.js/CSS changes coexist. No --epic-symbol entries. Epic remains open for the selection/acceptance repair.

[2026-11-23T17:29:38Z · bob-cli-pf.4.1.7.land] YAML Done now stores {key, ordinal, line} on the props excursion, reopens through propertyEditorYamlReopenSelection, and keeps that identity through cache-first rows. Unique keys still omit the jump line so recovery diagnostics win; duplicates keep the selected occurrence after a source-line shift; a deleted row returns to the nearest survivor (edit_me), not the first row.

Athena real-Obsidian e2e: 130/130 pass, 0 skip, 0 plugin errors on bob-cli f6cf62cf (bob sha256 6a027e3c2b22046956df1e41f6f48b538b64763ff97d6313df9561c64728425d) and dirty bob-plugins b2c37102. Assertions include Done reopens the same key, Done lands on nearest remaining edit_me occurrence, and Done reopens the second duplicate title occurrence. Layout probes are visualVerdict layout-probed; PNGs were inspected and recorded as reviewed-pass.

Raw report file:explicit:100794501f510b52e4d301a2; reviewed report file:explicit:67292147c2af0fb1dbc34095; wide-light file:explicit:fc123a59cb45c2d89a6be43e; wide-dark file:explicit:bfad2cb954f520df8821b7b4; narrow-light file:explicit:6613646d2f833b8c8fd3468b; narrow-dark file:explicit:3dd66eae5b7b4285c7d4a2db.

Prior write-safety, row-fidelity, write-path, and surface repairs remain. Focused property suites 311/311. npm run validate and build:check pass. bob plugins sync copied ledger-tools main.js without -F. No --epic-symbol entries. just symvision recipe is absent.

Unrelated clean-base failures, not this repair: task_reqs README twins (already on bob-cli-ph.2); keep-moving stylesheet missing .bob-successor-group.is-keep_moving on bob-plugins HEAD b2c37102; api.taskLinks session-open 55.7ms flake (bob-cli-pg, 37.41ms in isolation); docs-check contract registry 57 vs 56 on bob-cli f6cf62cf; just check clippy::collapsible_if in src/native/task_children.rs:129 and src/native/task_reqs.rs:319 on clean f6cf62cf. No new commits after the audit baselines. Follow-up triage already complete (km/io/pg, ph). pf.5 keeps parity features; pf.6 keeps native takeover.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.4.1.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.7.land.md) | [bob-cli-pf.4.1.7](bob-cli-pf.4.1.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8efc5a6`](https://github.com/bobs-org/bob-plugins/commit/8efc5a6d3caff4747cc73ad4ad7a6063066ba980) | fix(property-editor): preserve YAML Done selection through cache-first reopen | [bob-cli-pf.4.1.7](bob-cli-pf.4.1.7.md) | 2026-11-23 12:34:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.4.1.7.1][1] | parent epic scope for write-safety phase | 1 |
| read-by | [agent:bob-cli-pf.4.1.7.3--3][2] | Read parent acceptance plan context | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.4.1.7.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.7.3.md

<!-- sase:referenced-by:end -->
