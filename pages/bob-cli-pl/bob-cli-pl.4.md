# Bead: bob-cli-pl.4 — Area Card and Project Card painted from local data (bob-plugins)

[Bead Pages](../README.md) / [bob-cli-pl](README.md) / bob-cli-pl.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5y.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5y.linker.w1.md) · **Assignee:** `bob-cli-pl.4` · **Size:** large
**Created:** 2026-11-22 20:56:40 EST · **Closed:** 2026-11-24 15:39:43 EST
**Plan:** [202611/area\_project\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_cards.md)

## Description

home-cards: add the area and project species and one shared home adapter that paints kicker, crumb, title, subtitle or lifecycle line, authored chips, the Ready readout, the pf foot with where-marks, collapse, and material, with mount rules, fail-open, e2e, screenshots, and docs. Native Properties stays visible.

## Notes

[2026-11-23T02:02:52Z · bob-cli-pl.4] Launch prerequisite unmet: plan:202611/area_project_cards.md explicitly requires bob-cli-pf to be CLOSED before any phase starts and says to stop, note this phase, and change no files otherwise. Audited read shows bob-cli-pf IN_PROGRESS; the opened bob-plugins checkout at c8deb534 has no docs/property-editor.md yet. No prior phase work notes were present, no implementation or plan files were changed, and this phase was not reopened or closed. Adding the missing prerequisite edge and staging a zero-weight wait; after bob-cli-pf closes successfully, refresh the landed APIs, author/validate/revalidate/propose the required implementation plan, then complete bob-cli-pl.4.

[2026-11-24T19:15:45Z · bob-cli-pl.4.1.land] Child landing audit at bob-plugins 71cf808a: home presentation/host/foot are present and focused home/offline/cache tests pass 82/82; pl.4.1 remains open for a bounded repair tale (policy value validity, nested ^prj scan, hue and inbox adapters, host boundaries, complete real-app acceptance). Current seams are homePropertyCardHost(), homeCardModelFor(), homeCardOpenSetting(filePath,key) -> openPropertyEditor({filePath,key,mode:browse}), homeCardFootSpec()/homeCardFootExtra()/homeCardFootHandlers(), scheduleHomeCardRefresh(), and per-path homeCardIsCollapsed()/homeCardSetCollapsed(). Kit bindings are bare - for drawer and + for Property Editor; no home == registration or native Properties hiding. The tale will close pl.4.1, mark its plan done, then verify and close only this phase. Preserve b4023b85 writer retirement/test listener integration. No epic-symbol entries currently on this phase.

[2026-11-24T20:40:19Z · bob-cli-pl.4.1.land] Child epic bob-cli-pl.4.1 closed after finishing original home-cards acceptance from plan:202611/area_project_cards.md: local Area/Project cards, native Properties visible, project-task interaction unchanged, `card_structure_counts=no`.

Host/foot entry points: homePropertyCardHost(), homeCardModelFor(), homeCardOpenSetting(filePath,key) -> openPropertyEditor({filePath,key,mode:browse}), homeCardFootSpec()/homeCardFootExtra()/homeCardFootHandlers(), scheduleHomeCardRefresh(), homeCardIsCollapsed()/homeCardSetCollapsed(). Kit bindings remain bare `-` for the properties drawer and `+` for Property Editor; no home `==` registration.

Real-app proof: athena xvfb-run PASS 75/75 with 28 inspected screenshots (file:explicit:cb88c4643f511cce58e35444, file:explicit:d802ce1e232a7fed3b693268). Deploy: bob plugins sync copied bob-ledger-tools main.js, 0 skipped, no `-F`. epic-symbols empty. just symvision absent. Leave bob-cli-pl to its lander.

## Dependencies

- **Depends on:** [bob-cli-pf](../bob-cli-pf/README.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pl.5](bob-cli-pl.5.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pl.6](bob-cli-pl.6.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.4.md) | [bob-cli-pl.4](bob-cli-pl.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.4.1.2][1] | Need outer phase scope and decisions | 1 |
| read-by | [agent:bob-cli-pl.5][2] | Check what home-cards landed | 1 |
| read-by | [agent:fx][3] | Research whether the pl epic's dependency on pf is necessary | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.4.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.5/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.fx/README.md

<!-- sase:referenced-by:end -->
