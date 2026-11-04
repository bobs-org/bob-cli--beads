# Bead: bob-cli-gn.3 — \`Z\` on an image-path bullet imports it

[Bead Pages](../README.md) / [bob-cli-gn](README.md) / bob-cli-gn.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.17n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.17n.md) · **Assignee:** `bob-cli-gn.3` · **Size:** small
**Created:** 2026-11-03 14:53:41 EST · **Closed:** 2026-11-03 17:56:39 EST
**Plan:** [202611/image\_zoom\_origins.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/image_zoom_origins.md)

## Description

pathz: detect a bullet that holds only an image path, import it through bob, rewrite it to bob's embed in one undoable edit, and open the viewer on the new image with an "Imported" pill.

## Notes

[2026-11-03T22:55:57Z · bob-cli-gn.3] PROPOSED FOLLOW-UP: test-ledger-tools-keep-inbox "forced check feedback follows the bob refresh result" fails identically on clean base (32 pass/1 fail); unrelated to pathz, needs owner triage

[2026-11-03T22:56:03Z · bob-cli-gn.3] PROPOSED FOLLOW-UP: test-ledger-tools-freshness-namespace "the reload event fires only when the due key set changes" fails identically on clean base (8 pass/1 fail); unrelated to pathz

[2026-11-03T22:56:07Z · bob-cli-gn.3] PROPOSED FOLLOW-UP: test-navigation-hotkeys-schedule-work-log "future scheduling on Pending marks Blocked but still writes the Work Log" fails identically on clean base (date-sensitive: expects [?] got [/]); unrelated to pathz

[2026-11-03T22:56:11Z · bob-cli-gn.3] PROPOSED FOLLOW-UP: test-ledger-tools-note-ready "the startup storm is linear" fails identically on clean base (40 pass/1 fail, scan count 1 vs 2); unrelated to pathz

[2026-11-03T22:56:15Z · bob-cli-gn.3] PROPOSED FOLLOW-UP: test-ledger-tools-task-link-marks-live "lifecycle fragment limit" fails identically on clean base (36 pass/1 fail); unrelated to pathz

[2026-11-03T22:56:21Z · bob-cli-gn.3] PROPOSED FOLLOW-UP: test-ledger-tools-navigation.cjs hangs with no TAP output on both pathz tree and clean base (killed by 60s/100s timeout); unrelated to pathz

[2026-11-03T22:56:25Z · bob-cli-gn.3] PROPOSED FOLLOW-UP: test-ledger-tools-relation-index "relationIndex registers after layout-ready" timing failure reproduces on clean base (11 pass/1 fail both); unrelated to pathz

[2026-11-03T22:56:39Z · bob-cli-gn.3] pathz done in bob-plugins: 679a fragment (findImagePathBullet + importImagePathOnLine, single-flight via zoom) hooked into zoomImageOnLine; new test-navigation-image-zoom-path.cjs 16/16 pass; full suite green except 7 pre-existing base-identical issues recorded as PROPOSED FOLLOW-UP notes; npm run build, docs:gen, docs:check pass; bob plugins sync deployed (2 copied); vimrc comment updated and vault-synced (573c364bd)

## Dependencies

- **Depends on:** [bob-cli-gn.1](bob-cli-gn.1.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-gn.2](bob-cli-gn.2.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gn.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gn.3/README.md) | [bob-cli-gn.3](bob-cli-gn.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7ad20f5`](https://github.com/bobs-org/bob-plugins/commit/7ad20f50c8eb784d827ea41248a0d47ec8d2eb0d) | feat(image-zoom): Z on an image-path bullet imports it | [bob-cli-gn.3](bob-cli-gn.3.md) | 2026-11-03 18:03:13 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gn.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gn.3/README.md

<!-- sase:referenced-by:end -->
