# Bead: bob-cli-cc.9 — Code picker, preview well, and panel wiring

[Bead Pages](../README.md) / [bob-cli-cc](README.md) / bob-cli-cc.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.9` · **Size:** medium
**Created:** 2026-10-26 09:00:56 EDT · **Closed:** 2026-10-26 13:03:54 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

## Description

mac-ui: fetch the catalog when the card opens, draw the C and M rows, the code picker, and the fixed-height preview well in light and dark, add HUD strings, VoiceOver, design fixtures, and docs, and verify the Command-Y C Return gesture on the Mac.

## Notes

[2026-10-26T17:03:40Z · bob-cli-cc.9] PROPOSED FOLLOW-UP: docs-check still fails on clean tree for undocumented BOB_TEST_FIXTURE_PDF in src/native/highlights_ref/source_store.rs:185 (already noted on bob-cli-c9.6 / bob-cli-ce.6); Copy-card word budget is now 5998/6000.

[2026-10-26T17:03:54Z · bob-cli-cc.9] Wired Copy card C/M rows, code picker, preview well, and parallel bob ref code fetch in bob-mac-capture.

Verified:
- Linux portable-check pieces: swift format lint exit 0; swift test 1672 passed (RefsFetchingTests + RefsCodeTests included).
- Mac scratch /tmp/bob-mac-capture-cc9: just typecheck-tests PASS (BobMacCaptureTests, InstallHelper, CaptureCore, RefsCore); bundle.sh produced Bob Mac Capture.app; scratch deleted.
- docs/refs.md Copy card + docs/keyboard.md Copy card keys; assembled refs.md 5998/6000 words.
- sase bead epic-symbols: no leftover --epic-symbol entries.

Not verified: live Highlights ⌘Y C ↵ vs bob ref code paste (no GUI session). docs-check still fails on pre-existing BOB_TEST_FIXTURE_PDF lint (PROPOSED FOLLOW-UP).

## Dependencies

- **Blocks:** [bob-cli-cc.10](bob-cli-cc.10.md) ◐ · ⧖ 2026-10-26
- **Depends on:** [bob-cli-cc.8](bob-cli-cc.8.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.9/README.md) | [bob-cli-cc.9](bob-cli-cc.9.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land][1] | Check whether ref code/source_store test failures are already recorded | 1 |
| read-by | [agent:bob-cli-cc.9][2] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.9/README.md

<!-- sase:referenced-by:end -->
