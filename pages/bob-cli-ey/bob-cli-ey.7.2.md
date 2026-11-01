# Bead: bob-cli-ey.7.2 — bob-cli full drawer completion menu and drawer vocabulary sweep

[Bead Pages](../README.md) / [bob-cli-ey.7](bob-cli-ey.7.md) / bob-cli-ey.7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.land.md) · **Assignee:** `bob-cli-ey.7.2` · **Size:** medium
**Created:** 2026-11-01 03:50:53 EST · **Closed:** 2026-11-01 05:47:26 EST
**Plan:** [202611/finish\_capture\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_capture_drawers.md)

## Description

drawer-menu: build the drawer completion menu: task, recent, and new groups; bob-authored detail, consequence, and refused copy; a replacement that covers the # and the name; and initial_selection none on an empty query. Rename the leftover 'task sections' shell group and docs wording to drawers.

## Notes

[2026-11-01T10:47:20Z · bob-cli-ey.7.2] PROPOSED FOLLOW-UP: drawer catalog rewrites its cache file on every rescan — load_drawer_catalog (capture_drawers.rs) starts cache_dirty = true, so each 60 s TTL expiry re-serializes the whole cache even when no note changed (stale-TTL drawer menu ~32 ms vs ~15 ms warm on a 400-note fixture); initialize cache_dirty from whether any per-file entry was rescanned or dropped.

[2026-11-01T10:47:26Z · bob-cli-ey.7.2] Drawer menu shipped in bob-cli: new capture_complete/drawers.rs builds task / recent / new groups; bob-authored detail ('2 notes', '1 note', 'empty', 'used in 12 notes · 3 days ago') and consequence ('Adds after "2 GB RAM" in REQUIREMENTS', 'Adds to X', 'Creates X under ^bar', '## ' forms on ^prj); refused comes from the same resolve_drawer_for_write/resolve_h2_for_write the commit uses (reserved copy now names the real key, was hardcoded LINKS); replacement is #slug only when the slug round-trips to the same drawer on the full target list, else #"TITLE"; Drawer field replacement now starts at the # and covers quoted literals (closed-literal query decodes without the closing quote); cursor_after; initial_selection none on empty query (drawer query now reported as 'query'); missing/duplicate/non-task target = diagnostic + no rows; ^prj keeps H2 task rows and also gets recent/new. Shell 'task sections' group -> 'drawers' in shell.rs, providers.rs, tests, docs/completion.md; sweep grep leaves only alias registration/test, justfile smoke, mkdocs redirect, decision-record text, grouped_task_sections family and one narrow --task-section negative test. Docs: capture.md, completion.md, json-outputs.md, capture-complete --help; just docs-gen + docs-check pass. Tests: new unit suite capture_complete/tests/drawers.rs, tests/cli/capture/complete_drawers.rs (incl. accept-row-then-dry-run round trip proving menu == commit), language field tests, capture_drawers helper tests; just check passes (fmt, clippy, 4265 lib + 2612 cli tests). Latency (release, 400 notes x 5 tasks x 3 drawers, XDG cache isolated): drawer menu warm 15.3 ms (empty) / 13.7 ms (typed) vs task_type 9.0 ms warm = +6 ms (target <=~20 ms); stale-60s-TTL rescan 31.7 ms; cold (no cache) 105 ms median on that heavier fixture (ey.2 recorded 19.6 cold / 23.7 warm on its fixture, so not directly comparable; old drawer menu never touched the catalog). Wire breaks (for feat(capture)! + BREAKING CHANGE footer): drawer row group 'drawers' -> 'task', replacement/replacement.start now cover the #, drawer row replacement carries leading '#'. Mac phase bob-cli-ey.7.4 should regenerate fixtures from this commit. No Cargo.toml/CHANGELOG edits.

## Dependencies

- **Depends on:** [bob-cli-ey.7.1](bob-cli-ey.7.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-ey.7.4](bob-cli-ey.7.4.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.7.2/README.md) | [bob-cli-ey.7.2](bob-cli-ey.7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c7afa6d`](https://github.com/bobs-org/bob-cli/commit/c7afa6d0a11609a23c4b6d6e1341a967f01e4bc3) | feat(capture)!: full drawer completion menu and drawer vocabulary sweep | [bob-cli-ey.7.2](bob-cli-ey.7.2.md) | 2026-11-01 05:48:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.7.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.7.2/README.md

<!-- sase:referenced-by:end -->
