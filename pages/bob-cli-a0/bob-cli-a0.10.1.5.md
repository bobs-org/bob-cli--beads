# Bead: bob-cli-a0.10.1.5 — Mount the plugin reference and verify its complete workflow

[Bead Pages](../README.md) / [bob-cli-a0.10.1](bob-cli-a0.10.1.md) / bob-cli-a0.10.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.10.md) · **Assignee:** `bob-cli-a0.10.1.5` · **Size:** medium
**Created:** 2026-10-19 23:16:01 EDT · **Closed:** 2026-10-20 00:49:07 EDT
**Plan:** [202610/plugin\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plugin_reference.md)

## Description

site-integration: add the two mounts, site entry links, generated-content gate integration, the sibling preview wrapper, and end-to-end verification evidence for the land agent.

## Notes

[2026-10-20T04:48:34Z · bob-cli-a0.10.1.5] Verified site-integration on bob-cli 48f3ef22 and bob-plugins fdf834d. Two mounts in docs/_meta/mounts.yml (docs→reference/plugins, docs/develop→develop/plugins); plugin index.md gitignore exceptions removed; just docs-gen wrote 7 plugins / 76 commands; just docs-check passed (lint, generated drift, strict Zensical, 97 URLs, lychee, 69 search-smoke cases including install plugins → /reference/plugins/#install and Yank absolute path with tilde → /reference/plugins/bob-navigation-hotkeys/#registered-commands, tutorial, 344 unit tests); just docs-build-material passed; BOB_CLI_DIR=<this checkout> npm run docs:check passed; npm run validate 7/7; wrapper tests 5/5; edit URIs target github.com/bobs-org/bob-plugins for mounted pages including hubs; source hubs once (Obsidian plugins / Plugin development); developer pages not duplicated under Reference. bob plugins sync succeeded against canonical ~/projects/github/bobs-org/bob-plugins (fast-forward, 0 copied / 19 unchanged) — linked uncommitted docs are not the sync source. Limitations: live urls.txt not published yet; publish workflow has no setup-node (missing Node fails the generator clearly).

[2026-10-20T04:48:51Z · bob-cli-a0.10.1.5] PROPOSED FOLLOW-UP: bob-plugins npm test has 6 pre-existing runtime failures unchanged by this docs work (unblocked-glyph x4 bob-cli-6v; Keep counts once bob-cli-6w; forward conversion BLOCKS Work_ship#^prj bob-cli-7i); stage ranker 16ms budget also flakes. Reproduced on unmodified plugin source/tests; docs:check/validate still pass. Does not block this phase.

[2026-10-20T04:49:07Z · bob-cli-a0.10.1.5] Mounted both bob-plugins docs trees, wired inventory into docs-gen/docs-check, added sibling docs:check wrapper. Verified: just docs-gen (7 plugins/76 commands), just docs-check, just docs-build-material, BOB_CLI_DIR npm run docs:check, npm run validate 7/7, wrapper tests 5/5, search smoke, edit URIs, gitignored copies, bob plugins sync recorded. epic-symbols empty. Pre-existing npm test failures filed as PROPOSED FOLLOW-UP (bob-cli-6v/6w/7i).

## Dependencies

- **Depends on:** [bob-cli-a0.10.1.1](bob-cli-a0.10.1.1.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.10.1.4](bob-cli-a0.10.1.4.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.10.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.5/README.md) | [bob-cli-a0.10.1.5](bob-cli-a0.10.1.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b1f98d9`](https://github.com/bobs-org/bob-cli/commit/b1f98d9908d943f5eacd74837d3f52a8388b9d61) | feat(docs): mount the Obsidian plugin reference into the Bob site | [bob-cli-a0.10.1.5](bob-cli-a0.10.1.5.md) | 2026-10-20 00:52:16 EDT |
| bob-plugins | [`bob-plugins@2af765d`](https://github.com/bobs-org/bob-plugins/commit/2af765dda968d9332e7a4b51c07be8b1ff106c46) | docs: add sibling docs-check wrapper and cross-mount site URLs | [bob-cli-a0.10.1.5](bob-cli-a0.10.1.5.md) | 2026-10-20 00:53:38 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.10.1.5][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-a0.10.1.land--1][2] | Need integration phase verification evidence for the child epic close note | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.10.1.land.md

<!-- sase:referenced-by:end -->
