# Bead: bob-cli-a0.10.1 — Publish the generated Obsidian plugin reference

[Bead Pages](../README.md) / [bob-cli-a0.10](bob-cli-a0.10.md) / bob-cli-a0.10.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.10.md) · **Assignee:** `bob-cli-a0.10.1.land`
**Created:** 2026-10-19 23:16:00 EDT · **Closed:** 2026-10-20 01:48:58 EDT
**Plan:** [202610/plugin\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plugin_reference.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/plugin_reference.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plugin_reference.md

<!-- sase:links:end -->

## Description

Complete bob-cli-a0.10 with source-owned documentation for all seven plugins, generated command and version facts, a concise README, and verified reference and development mounts in the Bob site.

## Notes

[2026-10-20T05:21:12Z · bob-cli-a0.10.1.land] LAND TRIAGE (bob-cli-a0.10.1.land): PROPOSED FOLLOW-UPs from .2#1, .3#2, .4#1, .5#2 all describe pre-existing bob-plugins npm test failures not caused by this docs-only epic; each is an existing READY task, corroborated once with +1: bob-cli-6v (unblocked-glyph x4), bob-cli-6w (Keep counts once), bob-cli-7i (project conversion BLOCKS ^prj link), bob-cli-3w (stage-ranker 16ms budget; .4's 'stage-entry 17.87ms, no matching bead' is the same test stage-ranker-filters-1000-synthetic-tasks-under-16-ms-per-keystroke, so no new task). .5#1 limitation 'live urls.txt not published yet' belongs to active epic bob-cli-a0.5.1 (first publish in a0.5.1.5) and was declined as a follow-up. .5#1 limitation 'publish workflow has no setup-node' is caused by this epic (bob-docs check --production now runs the Node inventory generator) and is folded into the remaining-work tale. Discovered while landing: docs-publish.yml/docs-weekly.yml jobs lack runs-on — caused by active epic bob-cli-a0.5.1, recorded there as a DISCOVERED ISSUE note, no task created.

[2026-10-20T05:48:58Z · bob-cli-a0.10.1.land--1] Verified completion of the generated Obsidian plugin reference epic. All five child phases are closed: source-owned mounted hubs preserve authored pages and guardrails; the static inventory generates facts and 76 registered commands for seven plugins; all seven reference pages are complete; README topics were migrated into a concise front door and topic/developer pages while preserving the remaining detail; and both plugin doc trees are mounted and verified end to end.

The land review found that the new compatibility-page link to `reference/plugins/index.md` was missing from the isolated Zensical test fixture. Added the mounted-page stub to that fixture. The initial `just docs-check` then passed on rerun: lint, generated drift, strict Zensical, 97 published URLs, offline lychee, all 80 search cases (including `install plugins` -> `/reference/plugins/#install` and `Yank absolute path with tilde` -> `/reference/plugins/bob-navigation-hotkeys/#registered-commands`), tutorial, media determinism, and all 406 documentation tests. Also verified `just docs-gen`, `just docs-build-material`, plugin `npm run validate`, scanner/wrapper tests, focused publish-workflow tests, and `bob plugins sync --repo <opened bob-plugins checkout> --no-pull` passed. `git diff --check` is clean in bob-cli, bob-plugins, and plans. Current source SHAs: bob-cli `50d0e990`; bob-plugins `2af765d`.

Full plugin `npm test` remains 3199/3206 with seven failures already reproduced on clean base and triaged on this epic: four unblocked-glyph cases (`bob-cli-6v`), Keep counts once (`bob-cli-6w`), reverse project conversion retaining a BLOCKS ^prj link (`bob-cli-7i`), and the stage-ranker 16 ms timing flake (`bob-cli-3w`). LAND TRIAGE also recorded that the unpublished live `urls.txt` belongs to active epic `bob-cli-a0.5.1`; missing `setup-node` in publish workflows is folded into that epic's remaining work; and docs-publish/docs-weekly `runs-on` issues are recorded there as a discovered issue, with no task bead. The already-ready tasks were corroborated; no new task beads were created.

The approved plan `202610/plugin_reference.md` is now marked `status: done`. `just symvision` was attempted but this Justfile has no such recipe, and `just --list` showed no symvision/vision equivalent.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.10.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.10.1.land.md) | [bob-cli-a0.10.1](bob-cli-a0.10.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`417291e`](https://github.com/bobs-org/bob-cli/commit/417291eb618476ced319a510ee9a2bc38ed004c5) | docs(reference): fix plugin links and validate published docs | [bob-cli-a0.10.1](bob-cli-a0.10.1.md) | 2026-10-20 02:07:09 EDT |
| bob-plugins | [`bob-plugins@ff36987`](https://github.com/bobs-org/bob-plugins/commit/ff369873dab5b34c853b4201c6816ef1f362d6b8) | feat(docs): expand plugin reference and inventory checks | [bob-cli-a0.10.1](bob-cli-a0.10.1.md) | 2026-10-20 02:20:13 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.10.1.1][1] | Need epic DECISIONS that this phase must honor | 2 |
| read-by | [agent:bob-cli-a0.10.1.2][2] | Review the epic decisions governing this implementation | 1 |
| read-by | [agent:bob-cli-a0.10.1.3][3] | Need parent epic DECISIONS and phase scope | 1 |
| read-by | [agent:bob-cli-a0.10.1.land--1][4] | Need assigned phase scope and children before closing the approved land phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.10.1.land.md

<!-- sase:referenced-by:end -->
