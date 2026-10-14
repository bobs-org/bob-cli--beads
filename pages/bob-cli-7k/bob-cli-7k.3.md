# Bead: bob-cli-7k.3 — App building blocks for the Copy card and HUD (not yet wired)

[Bead Pages](../README.md) / [bob-cli-7k](README.md) / bob-cli-7k.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.19.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.19.linker.w0.md) · **Assignee:** `bob-cli-7k.3` · **Size:** medium
**Created:** 2026-10-14 09:32:31 EDT · **Closed:** 2026-10-14 10:18:46 EDT
**Plan:** [202610/refs\_ctrl\_y\_copy\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_ctrl_y_copy_card.md)

## Description

refs-copy-components: in the app target, add the checked pasteboard write, the single-flight exact-path ref-show cache, the RefsCopyCardView, and the glass copy HUD with design fixtures, without wiring ⌃Y yet.

## Notes

[2026-10-14T14:18:24Z · bob-cli-7k.3] PROPOSED FOLLOW-UP: just typecheck-tests fails on Mac CLT — Scripts/typecheck-tests.sh unsets SDKROOT then swiftc cannot load stdlib for arm64-apple-macosx26.0; reproduces identically on clean master 060d77b after Build complete; with SDKROOT set, XCTest stub typecheck of BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, and RefsCoreTests all PASS

[2026-10-14T14:18:46Z · bob-cli-7k.3] Verified refs-copy-components in bob-mac-capture without wiring ⌃Y: checked pasteboard write (setString/writeObjects + org.nspasteboard.source), unstructured single-flight exact-path showRow cache (LRU 32, no failure cache, no refs.first fallback), RefsCopyCardView + copy-card visual tokens, glass copy HUD (nonactivatingPanel, static frame math). Mac ./Scripts/bundle.sh compiled the new sources. Athena just portable-check exit 0 (1139 tests). Manual SDKROOT typecheck of all four test targets PASS. just typecheck-tests fails identically on clean master 060d77b (stdlib after unset SDKROOT) — recorded as PROPOSED FOLLOW-UP. epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-7k.2](bob-cli-7k.2.md) ✓ · ⧖ 2026-10-14
- **Blocks:** [bob-cli-7k.4](bob-cli-7k.4.md) ✓ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7k.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.3/README.md) | [bob-cli-7k.3](bob-cli-7k.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7e7d8d6`](https://github.com/bobs-org/bob-mac-capture/commit/7e7d8d628446cda13fa2a903ef2570c5010aa5d1) | feat(refs): add Copy card view, glass HUD, and checked pasteboard | [bob-cli-7k.3](bob-cli-7k.3.md) | 2026-10-14 10:20:24 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7k.3][1] | Need notes, remaining work, and close-out evidence | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.3/README.md

<!-- sase:referenced-by:end -->
