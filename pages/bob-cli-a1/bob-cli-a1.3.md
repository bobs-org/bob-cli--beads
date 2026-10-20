# Bead: bob-cli-a1.3 — Zoom command, Z binding, docs, and deploy

[Bead Pages](../README.md) / [bob-cli-a1](README.md) / bob-cli-a1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.26.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.26.linker.w0.md) · **Assignee:** `bob-cli-a1.3` · **Size:** medium
**Created:** 2026-10-20 09:07:41 EDT · **Closed:** 2026-10-20 09:47:50 EDT
**Plan:** [202610/z\_image\_zoom.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/z_image_zoom.md)

## Description

wire: register "Zoom image on cursor line", open the viewer from the resolver, restore the source editor on close, bump the manifest, document the gesture, map nmap Z in the vault vimrc, deploy with bob plugins sync, and hand Bryan the Mac smoke checklist.

## Notes

[2026-10-20T13:44:50Z · bob-cli-a1.3] PROPOSED FOLLOW-UP: Add the image zoom decision record — the automatic image_zoom_record=no decision did not authorize editing decisions, so the accepted read-only viewer and native-path policy remains undocumented in the decisions web.

[2026-10-20T13:44:59Z · bob-cli-a1.3] PROPOSED FOLLOW-UP: Repair six clean-base plugin test failures — reproduced unchanged at HEAD: four in test-ledger-tools-unblocked-glyph.cjs (tracked by bob-cli-6v), one in test-navigation-decision-card-handlers.cjs (tracked by bob-cli-6w), and one in test-navigation-hotkeys-forward-promotion.cjs (tracked by bob-cli-7i).

[2026-10-20T13:47:50Z · bob-cli-a1.3] Implemented and deployed the Zoom image on cursor line command, editor restoration, docs, and plugin 2.47.0. Targeted command tests, npm run validate, npm run docs:check, and git diff --check pass; six npm test failures reproduce identically on clean HEAD and are recorded with their existing beads. Plugin sync is up to date; the vault has exactly one Z mapping and its HEAD matches origin/master.

## Dependencies

- **Depends on:** [bob-cli-a1.1](bob-cli-a1.1.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a1.2](bob-cli-a1.2.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a1.3/README.md) | [bob-cli-a1.3](bob-cli-a1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@049f466`](https://github.com/bobs-org/bob-plugins/commit/049f4663d777a764cacbd69ae66a9503b8b7832f) | feat(bob-navigation-hotkeys): add read-only image zoom command | [bob-cli-a1.3](bob-cli-a1.3.md) | 2026-10-20 09:49:11 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a1.3][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a1.3/README.md

<!-- sase:referenced-by:end -->
