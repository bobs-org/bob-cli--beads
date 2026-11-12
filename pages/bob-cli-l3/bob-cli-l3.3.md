# Bead: bob-cli-l3.3 — Graceful bare-album refusal and a live rewrite button (bob-mac-capture)

[Bead Pages](../README.md) / [bob-cli-l3](README.md) / bob-cli-l3.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.dp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.dp.md) · **Assignee:** `bob-cli-l3.3` · **Size:** medium
**Created:** 2026-11-12 16:11:26 EST
**Plan:** [202611/record\_capture\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_capture_repairs.md)

## Description

mac-preview: give the live preview a dedicated album_holds_no_tasks refusal presentation per the album_refusal_presentation decision, gate the footer rewrite button on parse currency and clear latestParse on reset so it cannot go stale, and cover both with fake-bob dry-run fixture tests.

## Notes

[2026-11-12T22:27:40Z · bob-cli-l3.3] PROPOSED FOLLOW-UP: docs-check lint fails on upstream bob-navigation-hotkeys.md at 6039 words over the 6000 reference cap — file lives in assembled docs context from bob-cli master, untouched by this phase; capture-previews.md itself is clean

[2026-11-12T22:29:05Z · bob-cli-l3.3] mac-preview work complete in linked bob-mac-capture (uncommitted): showBareAlbumRefusal helper + 3 failure-site call sites, currency-gated bareAlbumRewrite used by footer button, latestParse cleared in resetAnalysisState, new record-capture-bare-album.json fixture generated from real bob 0.5.0 plus generator-script/README wiring, 3 hosted tests in CaptureRecordPreviewPanelTests, one docs sentence. Pre-landing gate (Scripts/macos-ci-check) staged in monitor; push + exact-SHA CI watch + epic-symbols + close left to follow-up.

## Dependencies

- **Depends on:** [bob-cli-l3.2](bob-cli-l3.2.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-l3.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-l3.3.md) | [bob-cli-l3.3](bob-cli-l3.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-l5.1][1] | Confirm the existing bead tracking the clean-base docs-check budget failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-l5.1/README.md

<!-- sase:referenced-by:end -->
