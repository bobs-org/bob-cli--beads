# Bead: bob-cli-a0.11.1.3 — Import CI panel images and add Mac documentation preview tooling

[Bead Pages](../README.md) / [bob-cli-a0.11.1](bob-cli-a0.11.1.md) / bob-cli-a0.11.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.11.md) · **Assignee:** `bob-cli-a0.11.1.3` · **Size:** medium
**Created:** 2026-10-20 03:05:22 EDT · **Closed:** 2026-10-20 06:59:22 EDT
**Plan:** [202610/mac\_capture\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_reference.md)

## Description

rendered-media: Add Scripts/docs-media.sh to import a curated set of real synthetic CI renders with provenance, Scripts/docs-check.sh and just recipes, focused script tests, render-fixture contributor instructions, and the Mac AGENTS.md docs instruction. Use real panel images in the mounted reference and bob-cli homepage.

## Notes

[2026-10-20T08:09:51Z · bob-cli-a0.11.1.3--1] README-to-destination: Idle agenda -> bob-mac-capture/docs/idle-agenda.md (agenda render); Live Preview and Clipboard Semantics -> docs/capture-previews.md (task completion render); Bob Refs -> docs/refs.md (Refs panel render); CI -> docs/develop/ci.md and docs/develop/render-fixtures.md (fixture provenance and refresh); homepage Mac panel -> bob-cli/docs/index.md via the mounted reference/mac-capture/images/capture-agenda.png.

[2026-10-20T10:39:41Z · bob-cli-a0.11.1.3] Implementation is complete in the current workspace and linked bob-mac-capture checkout; final full docs gates and Athena portable-check are the only pending work, delegated to a verification monitor. Scripts/docs-media.sh plus its Python helper imports six reviewed synthetic PNGs from successful master CI run 39330761089 (c81e00a3a4c6da272ac7591341fd85355162ce53), with complete source/date provenance and failure-safe replacement; Scripts/docs-check.sh follows the inspected plugin wrapper and preserves overrides, paths, source forwarding, and exit status. Eight stdlib script tests passed, including failure-preservation and rollback cases, and actual import succeeded. Strict Zensical and Material builds passed; browser checks passed all 32 combinations (four pages, two themes, 1280/360px) for exclusive light/dark visibility, decoded images, natural aspect ratio, and viewport fit. Inspected native renders, fixtures, and representative desktop/narrow screenshots for readability/privacy; linked images open originals for small text. Lint and git diff --check passed. No epic symbols remain. README mapping: Idle agenda -> docs/idle-agenda.md; Live Preview/Clipboard -> docs/capture-previews.md; Bob Refs -> docs/refs.md; CI -> docs/develop/ci.md plus render-fixtures.md. Homepage uses mounted agenda assets, and existing bob-cli-owned developer hub links the fixture page. No Swift, README, memory, or plugin changes. Remaining checks can be finished by one verification agent; no implementation decomposition is needed.

[2026-10-20T10:59:22Z · bob-cli-a0.11.1.3--1] Completed six curated synthetic CI renders with source/date provenance, failure-safe media importer, docs-check wrapper and recipes, contributor instructions, mounted reference images, and homepage agenda. Fixed final-gate media lint mismatch by ignoring only gitignored mounted residue during unassembled checks; regression tests preserve authored-image and assembled provenance enforcement. Verified both full docs-check entry points, all 58 lint tests and eight script tests, earlier strict Zensical and Material builds and all 32 browser image cases, actual CI import, manifest parity, and Athena portable-check (1,445 tests passed). No Swift changes. README mapping: Idle agenda -> idle-agenda.md; Live Preview/Clipboard -> capture-previews.md; Bob Refs -> refs.md; CI -> develop/ci.md and develop/render-fixtures.md; homepage uses mounted agenda images. No epic symbols remain; only this phase is closed.

## Dependencies

- **Depends on:** [bob-cli-a0.11.1.2](bob-cli-a0.11.1.2.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a0.11.1.4](bob-cli-a0.11.1.4.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.11.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.11.1.3.md) | [bob-cli-a0.11.1.3](bob-cli-a0.11.1.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d4b1ab3`](https://github.com/bobs-org/bob-cli/commit/d4b1ab31c3b24a97577ab2d0758a2000dbc00374) | docs(mac-capture): show mounted panel images and fix media lint | [bob-cli-a0.11.1.3](bob-cli-a0.11.1.3.md) | 2026-10-20 07:00:20 EDT |
| bob-mac-capture | [`bob-mac-capture@bd9b1e2`](https://github.com/bobs-org/bob-mac-capture/commit/bd9b1e23374868b92b75f3d8a040c7a59308bd46) | docs: import synthetic CI panel renders and add preview tooling | [bob-cli-a0.11.1.3](bob-cli-a0.11.1.3.md) | 2026-10-20 07:02:17 EDT |
