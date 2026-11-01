# Bead: bob-cli-ey.3.1.2 — Remove retired Mac capture paths and migrate their scenarios

[Bead Pages](../README.md) / [bob-cli-ey.3.1](bob-cli-ey.3.1.md) / bob-cli-ey.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.3.md) · **Assignee:** `bob-cli-ey.3.1.2` · **Size:** medium
**Created:** 2026-10-31 23:32:59 EDT · **Closed:** 2026-11-01 01:13:23 EDT
**Plan:** [202610/mac\_directives.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_directives.md)

## Description

retire-syntax: delete template-start rewrites, the template route row, global parent routing, and retired span mappings; migrate affected fake-bob scenarios, generated fixtures, tests, and documentation to percent directives.

## Notes

[2026-11-01T05:13:23Z · bob-cli-ey.3.1.2--a] Retired template-start rewrites, template route row, global parent routing, and retired span mappings in bob-mac-capture; migrated fake-bob scenarios, regenerated grammar-2 fixtures (directive-*, task-type-*, capture-templates-*), tests, and docs to percent directives. Verified: portable-check on isolated athena scratch copy passes (1853 tests, 0 failures); just docs-check and just check-scripts pass locally; retirement sweep (@template, TemplateStart, start_template, global_sub_bullet, stay literal, old listen/clip/note spellings, template.header, clip.header) is clean; epic-symbols empty. macOS targets unverified (mac SSH timed out: bundle.sh and typecheck-tests not run).

## Dependencies

- **Depends on:** [bob-cli-ey.3.1.1](bob-cli-ey.3.1.1.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.3.1.3](bob-cli-ey.3.1.3.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.3.1.2.md) | [bob-cli-ey.3.1.2](bob-cli-ey.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@a580c0d`](https://github.com/bobs-org/bob-mac-capture/commit/a580c0d9c342debdef4e94d2df623c207411128d) | refactor(mac-capture)!: retire template-start and global-parent paths, migrate scenarios to percent directives | [bob-cli-ey.3.1.2](bob-cli-ey.3.1.2.md) | 2026-11-01 01:14:09 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.3.1.2--a][1] | Need the phase scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.3.1.2.md

<!-- sase:referenced-by:end -->
