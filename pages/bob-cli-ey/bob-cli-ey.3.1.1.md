# Bead: bob-cli-ey.3.1.1 — Decode the directive contract and generate current wire fixtures

[Bead Pages](../README.md) / [bob-cli-ey.3.1](bob-cli-ey.3.1.md) / bob-cli-ey.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.3.md) · **Assignee:** `bob-cli-ey.3.1.1` · **Size:** medium
**Created:** 2026-10-31 23:32:59 EDT · **Closed:** 2026-10-31 23:58:20 EDT
**Plan:** [202610/mac\_directives.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_directives.md)

## Description

wire-fixtures: add grammar, initial_selection, directive spans and candidates, and clip status decoding; migrate template.directive and route-only global destinations; generate truthful directive and clipboard fixtures from the current Bob binary.

## Notes

[2026-11-01T03:58:20Z · bob-cli-ey.3.1.1] wire-fixtures done in bob-mac-capture. Models: parse/completion grammar (nil when absent, never defaulted), completion initial_selection (+opensWithoutSelection), directive span directive/count, directive candidate token/summary/detail (id includes token), clip status/count with required status and mode-only-when-read (header removed), template.directive replacing template.header, route-only CaptureGlobalDestination (mode/blockID/scopeSummary removed; captureUsesGlobalDestination is route-only; notification/panel helpers use destinationLabel). Fixtures: Scripts/generate-directive-fixtures.sh requires explicit BOB_BIN + BOB_CLI_DIR (clean checkout containing b290d833), verifies grammar>=2, isolated vault/config/HOME/clock, mocks BOB_CLIPBOARD_CMD/BOB_CLIPBOARD_HISTORY_CMD, dry-runs only; generated 60 directive-*/clip-* fixtures plus Tests/Fixtures/directive-fixtures-README.md from bob 0.4.0 at bob-cli a1dcb64e (grammar 2); regeneration is byte-identical. Tests: new CaptureDirectiveWireTests (grammar missing/1/2/3/mistyped, directive/count, UTF-8 ranges, disabled rows, unselected menus, template.directive, route-only globals, not_read, history/nested clips, batch captures, refusal codes, Codable round trips); migrated clip/template/global tests off old wire. Verified on athena (Swift 6.0.3, scratch copy): swift build --build-tests OK; swift test 1863 tests 0 failures; swift format lint: no warnings on new/changed lines except 3 pre-existing over-length string lines (CapturePanelModel 13769/13813, BobProcessClientTests 1484). just check-scripts passes locally (script added to docs-test bash -n list); no docs changed so docs-check not needed. macOS targets unverified: mac (kellys-macbook-pro) SSH timed out twice (tailscale reports offline); Sources/BobMacCapture edits are only scopeSummary->destinationLabel renames (NotificationService, CapturePanelModel, CapturePanelView) plus Tests/BobMacCaptureTests global-destination constructor/label updates; Scripts/bundle.sh and just typecheck-tests still need to run when the Mac is reachable. fake-bob and the old @template:/template_header fixtures were intentionally left for retire-syntax; no epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-ey.3.1.2](bob-cli-ey.3.1.2.md) ◐ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.3.1.1/README.md) | [bob-cli-ey.3.1.1](bob-cli-ey.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@04904ee`](https://github.com/bobs-org/bob-mac-capture/commit/04904eed3b98544e5d75add5b1d0e0121e1d665a) | feat(mac-capture)!: decode grammar-2 directive wire and generate real fixtures | [bob-cli-ey.3.1.1](bob-cli-ey.3.1.1.md) | 2026-10-31 23:59:03 EDT |
