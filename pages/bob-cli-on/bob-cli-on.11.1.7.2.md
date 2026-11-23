# Bead: bob-cli-on.11.1.7.2 — Open the card for idless owners, add real-Obsidian e2e, and finish docs

[Bead Pages](../README.md) / [bob-cli-on.11.1.7](bob-cli-on.11.1.7.md) / bob-cli-on.11.1.7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.11.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.land.md) · **Assignee:** `bob-cli-on.11.1.7.2` · **Size:** medium
**Created:** 2026-11-22 20:02:20 EST · **Closed:** 2026-11-23 00:11:54 EST
**Plan:** [202611/obsidian\_req\_close\_card\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_close_card_repairs.md)

## Description

idless_acceptance: route idless owners with Pending reqs through a requirement-only card pass, add real-Obsidian close-card e2e scenarios, finish the bob-cli and bob-plugins docs, run the combined gates, and deploy both plugins.

## Notes

[2026-11-23T05:11:44Z · bob-cli-on.11.1.7.2--6] VERIFICATION AND DEPLOYMENT (2026-11-23; monitor 16hpvrb8fdz2; gate exit 0): plugin build and build:check passed. Raw npm test reported 8,909 passed, 2 failed, 4 skipped; the only failures were the tracked event-link-times 25 ms node (47.3 ms) and frees-marks 25 ms node (65 ms) under full-suite load. Their isolated same-file controls passed 40/40 (3.7 ms and 18.3 ms respectively); adjusted plugin test exit was 0. Real Obsidian requirement-close E2E passed all six scenarios with failed=[]. Plugin docs:check passed (447 passed, 1 skipped); bob-cli docs-check passed and bob-cli just check exited 0; combined gate_failed=0. Deployment completed without force for task-status-cycler and bob-navigation-hotkeys. bob plugins list reports task-status-cycler 1.58.1 and bob-navigation-hotkeys 2.107.0 synced and enabled (11 synced overall; one unrelated bob-ledger-tools drift). sase bead epic-symbols bob-cli-on.11.1.7.2 returned no entries.

[2026-11-23T05:11:54Z · bob-cli-on.11.1.7.2--6] Completed idless close-card acceptance, real-Obsidian E2E, docs, final gates, and deployment. Monitor 16hpvrb8fdz2 passed all non-flake gates; only the two tracked 25 ms timing nodes failed under full load and both isolated controls passed. task-status-cycler 1.58.1 and bob-navigation-hotkeys 2.107.0 are synced. Epic-symbol check was clear; parent beads remain open.

## Dependencies

- **Depends on:** [bob-cli-on.11.1.7.1](bob-cli-on.11.1.7.1.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11.1.7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.7.2.md) | [bob-cli-on.11.1.7.2](bob-cli-on.11.1.7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bf00529`](https://github.com/bobs-org/bob-cli/commit/bf005290ab7e2da5f019102b16ff81d495fe6855) | docs(task-requirements): document requirement close behavior | [bob-cli-on.11.1.7.2](bob-cli-on.11.1.7.2.md) | 2026-11-22 21:33:47 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.7.2--2][1] | Review phase scope and prior verification notes before resolving failed gates | 1 |
| read-by | [agent:bob-cli-on.11.1.7.2--3][1] | Need the assigned subphase scope and acceptance criteria before resolving its failed e2e and finalizing closeout | 1 |
| read-by | [agent:bob-cli-on.11.1.7.2--5][1] | Need the assigned phase scope and existing evidence before recording the latest gates and deployment | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.7.2.md

<!-- sase:referenced-by:end -->
