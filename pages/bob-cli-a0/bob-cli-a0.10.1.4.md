# Bead: bob-cli-a0.10.1.4 — Preserve README topics and create the plugin front door

[Bead Pages](../README.md) / [bob-cli-a0.10.1](bob-cli-a0.10.1.md) / bob-cli-a0.10.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.10.md) · **Assignee:** `bob-cli-a0.10.1.4` · **Size:** medium
**Created:** 2026-10-19 23:16:01 EDT · **Closed:** 2026-10-20 00:04:05 EDT
**Plan:** [202610/plugin\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plugin_reference.md)

## Description

topic-migration: migrate the remaining README topics and development material, add both source navigation files, audit coverage, and shorten the README only after every detail has a home.

## Notes

[2026-10-20T04:03:43Z · bob-cli-a0.10.1.4] Completed the README and plugin docs phase in bob-plugins. Replaced the README monolith with a concise front door while preserving the generated requirements region. Added the shared topic guides for Block ID defaults, BLOCKS mirrors, Task Card, Go To task URI, Open Notes URI, highlights, and Templater trigger; added flat source nav lists at docs/nav.yml and docs/develop/nav.yml; added the develop hub and architecture, validation, plugin APIs, dependency migration, and deployment guides; linked related topics from the plugin pages. Used synthetic identifiers and verified same-tree and cross-mounted links. No bob-cli files changed.

Verification: npm run validate passed (plugin build check, docs inventory, and manifests); npm run docs:inventory:check passed; custom local Markdown and mounted bob-cli link checks passed; git diff --check passed. npm test ran 3206 tests: 3199 passed and 7 failed. On a clean archive of base 7e749018b39a96d9d1a8972a74144cc27034fe48, the same six non-timing failures reproduced: four unblocked-glyph cases (already tracked by bob-cli-6v), Keep counts once (bob-cli-6w), and reverse project conversion BLOCKS link (bob-cli-7i). The stage-entry performance budget case failed once at 17.87ms against 16ms on the changed tree and passed on clean base at 16.755ms. A synthetic vault passed migration dry-run without edits and --write adoption of a dependency field into the canonical Depends-On line. Isolated bob plugins sync copied all managed files; required sync to /home/bryan/bob completed with 0 copied, 0 skipped, and 19 unchanged. URI activation remains a manual GUI check.

PROPOSED FOLLOW-UP: Investigate the intermittent dependency stage-entry performance budget miss (17.87ms against 16ms); it passed on the clean base at 16.755ms, and no matching bead was found.

[2026-10-20T04:04:05Z · bob-cli-a0.10.1.4] README and topic/develop docs are complete; npm run validate and docs inventory passed; links, migration rehearsal, isolated sync, and required bob plugins sync were checked. Full suite has six known clean-base failures tracked by bob-cli-6v, bob-cli-6w, bob-cli-7i, plus one stage-entry timing miss recorded as PROPOSED FOLLOW-UP. Epic symbols: none.

## Dependencies

- **Depends on:** [bob-cli-a0.10.1.3](bob-cli-a0.10.1.3.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.10.1.5](bob-cli-a0.10.1.5.md) ◐ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.10.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.4/README.md) | [bob-cli-a0.10.1.4](bob-cli-a0.10.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.10.1.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.4/README.md

<!-- sase:referenced-by:end -->
