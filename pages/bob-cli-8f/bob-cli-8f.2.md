# Bead: bob-cli-8f.2 — RefsCore decoding, fetcher, card state machine, and copy

[Bead Pages](../README.md) / [bob-cli-8f](README.md) / bob-cli-8f.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7y.md) · **Assignee:** `bob-cli-8f.2` · **Size:** medium
**Created:** 2026-10-16 10:04:17 EDT · **Closed:** 2026-10-16 12:30:45 EDT
**Plan:** [202610/refs\_link\_to\_today.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_link_to_today.md)

## Description

mac_core: in bob-mac-capture's portable RefsCore/CaptureCore targets, decode the `ref today` envelope (reusing CaptureCommandSuccess). Add BobRefsFetcher.linkToToday with preview and write lanes, plus the pure RefsTodayLinkCard state machine (ranking, selection-to-selector mapping, stale-preview drop, running/failed/refused phases) and its key map. Add RefsTodayLinkPresentation for every string, row meta, lane chip, preview line, toast, notification, and announcement. Add a fake-bob `ref today` arm with real-bob fixtures and tests.

## Notes

[2026-10-16T16:30:00Z · bob-cli-8f.2] Portable API for mac_ui: BobRefsFetcher.linkToToday(notePath:selector:dryRun:) is concrete only; the UI phase adds the RefsFetching requirement. RefsTodayLinkCard(item:) starts loading; feed the initial automatic dry run (including transport problems wrapped as RefsTodayLinkResponse(ok:false,error:...)) into applyListing. editQuery/select/handle return preview, submit, reload, cancel, or none. For every preview effect, snapshot card.previewRequest BEFORE debounce/await, then call applyPreview(response, for: token); its selector and generation reject stale results including A→B→A and post-submit/cancel responses. Preview transport failures can use the same error envelope plus token. Write failures call fail(problem); stale_pomodoro returns reload and applyListing preserves the query. Row clicks call select(index:) then handle(.submit). RefsTodayLinkPresentation owns row copy/time math/progress, lane chip, preview text, refusal headlines, toast, notifications and announcement. Real CLI fixture provenance is recorded in Tests/Fixtures/refs-today-README.md. No protocol/AppKit changes or memory edits in this phase.

[2026-10-16T16:30:45Z · bob-cli-8f.2] Implemented portable ref-today schema decoding with CaptureCommandSuccess reuse; preview/write fetch lanes and timeouts; pure ranked card state, selector mapping, IME/key handling, stale generation rejection, refusal/failure/reload paths; centralized row/preview/toast/notification/accessibility copy and time math; fake-bob arm and seven scrubbed real CLI fixtures. Verified on athena: just portable-check passed all 1,274 portable tests; after final regression additions and copy consolidation, focused RefsTodayLinkTests + RefsFetchingTests passed 38 tests, with targeted Swift format lint clean. git diff --check and bash -n fake-bob passed. No new Sendable warnings from the response graph. sase bead epic-symbols reports no leftovers. Only portable targets/fixtures changed; no memory edits. API integration notes recorded for mac_ui. Closed only this phase.

## Dependencies

- **Depends on:** [bob-cli-8f.1](bob-cli-8f.1.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8f.3](bob-cli-8f.3.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8f.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8f.2/README.md) | [bob-cli-8f.2](bob-cli-8f.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@ef6522b`](https://github.com/bobs-org/bob-mac-capture/commit/ef6522bb4142b2ac5b755e81f6d4671fba7b3d54) | feat(refs): add portable Link to Today card core | [bob-cli-8f.2](bob-cli-8f.2.md) | 2026-10-16 12:31:27 EDT |
