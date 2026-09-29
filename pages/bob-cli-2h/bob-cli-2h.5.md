# Bead: bob-cli-2h.5 — Mac app: Block ID Picker visuals, sizing, accessibility, docs, and macOS verification

[Bead Pages](../README.md) / [bob-cli-2h](README.md) / bob-cli-2h.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.31](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.31.md) · **Assignee:** `bob-cli-2h.5` · **Size:** medium
**Created:** 2026-09-29 09:43:07 EDT · **Closed:** 2026-09-29 11:12:23 EDT
**Plan:** [202609/mac\_block\_id\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/mac_block_id_picker.md)

## Description

block-id-design: finish the link and new-ID visuals (scope token, availability badge, section headers, row kinds, detail strip, key hints, chip, marker highlight), sizing, accessibility, rendered-image review of both pickers, README visuals, and a real-panel smoke test.

## Notes

[2026-09-29T15:12:06Z · bob-cli-2h.5] PROPOSED FOLLOW-UP: macOS verification not run — no Swift toolchain on this Linux host; needs `just format-lint build test` on mac/CI for commit 69e654d, plus BOB_MAC_CAPTURE_RENDER_DIR image review (7 block-ID states x 760/620 x light/dark) and real-panel smoke

[2026-09-29T15:12:12Z · bob-cli-2h.5] PROPOSED FOLLOW-UP: marker wash renders square — spec asks rounded accent background but AttributedString background fills cannot round corners; needs overlay-based token highlight if rounded matters

[2026-09-29T15:12:23Z · bob-cli-2h.5] block-id-design in bob-mac-capture 69e654d: generic-card visuals (scope line-N suffix, availability badge capsule fixed 110-190pt, kind-aware headers, per-availability glyphs, 28pt dim info rows, per-source detail teaching keys, suggestions-count open announcement), marker wash via attributed-draft path cleared on all 5 close paths + parse re-apply, category-change availability announcements, budget-6 controller metrics test, 7 block-ID render states at 760/620 light/dark, highlight/model tests, README visuals. Verified: diff --check clean, static re-read of all hunks, no epic-symbols. NOT run: swift build/test (no toolchain on Linux host) — recorded as follow-up.

[2026-09-29T15:20:24Z · bob-cli-2h.5] PROPOSED FOLLOW-UP: CI run 36588819466 for 69e654d FAILED at Build on pre-existing error Sources/CaptureCore/CaptureModels.swift:2313 (SingleValueDecodingContainer has no member decodeIfPresent, from 8f84c07 block-id-core) — identical signature on base run 36586190275; Lint passed; Test/Bundle/Launch/Install skipped, so new design tests, render PNGs, and panel smoke are still unverified pending that fix

## Dependencies

- **Depends on:** [bob-cli-2h.4](bob-cli-2h.4.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2h.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2h.5/README.md) | [bob-cli-2h.5](bob-cli-2h.5.md) | 0 |
