# Bead: bob-cli-mx.5 — Walk marks store, view, docs, and decision record

[Bead Pages](../README.md) / [bob-cli-mx](README.md) / bob-cli-mx.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.es.md) · **Assignee:** `bob-cli-mx.5` · **Size:** medium
**Created:** 2026-11-17 17:59:53 EST · **Closed:** 2026-11-17 23:47:26 EST
**Plan:** [202611/mac\_walk\_attention\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_walk_attention_marks.md)

## Description

mac-walk-marks: wire the walks store and refresh triggers, paint the marks at the title row's trailing edge with motion, contrast, and no-wrap guarantees, update docs and renders, watch CI green, and write the decision record.

## Notes

[2026-11-18T03:05:42Z · bob-cli-mx.5--1] PROPOSED FOLLOW-UP: Refresh the idle agenda light/dark documentation renders through docs-media after this feature lands on master; the importer only accepts a successful master run, so the precommit CI artifact is not eligible.

[2026-11-18T04:06:21Z · bob-cli-mx.5--4] PROPOSED FOLLOW-UP: Refresh bob-cli docs contract test expectations and the generated README contract-table snapshot. Docs checks failed identically against clean Mac Capture base fee9ffab and current phase pages: registry has 52 contracts vs expected 51, and the README snapshot hash is stale.

## Dependencies

- **Depends on:** [bob-cli-mx.4](bob-cli-mx.4.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mx.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mx.5.md) | [bob-cli-mx.5](bob-cli-mx.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4f801ee`](https://github.com/bobs-org/bob-cli/commit/4f801ee2032c441a3eb0b5b4ce0b53927395076c) | docs(memory): record idle capture walk attention decision | [bob-cli-mx.5](bob-cli-mx.5.md) | 2026-11-17 23:49:14 EST |
| bob-mac-capture | [`bob-mac-capture@a19bdd0`](https://github.com/bobs-org/bob-mac-capture/commit/a19bdd0a4d9802d5eb1fd5b2a0429b478f6398f9) | feat(capture): show walk attention marks in idle agenda | [bob-cli-mx.5](bob-cli-mx.5.md) | 2026-11-17 23:49:43 EST |
