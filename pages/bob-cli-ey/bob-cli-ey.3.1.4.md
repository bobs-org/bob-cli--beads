# Bead: bob-cli-ey.3.1.4 — Read clips in live preview and render the Clip card

[Bead Pages](../README.md) / [bob-cli-ey.3.1](bob-cli-ey.3.1.md) / bob-cli-ey.3.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.3.md) · **Assignee:** `bob-cli-ey.3.1.4` · **Size:** medium
**Created:** 2026-10-31 23:33:00 EDT · **Closed:** 2026-11-01 01:43:36 EST
**Plan:** [202610/mac\_directives.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_directives.md)

## Description

clip-preview: authorize live clipboard reads only from the current Bob parse, refresh on activation and pasteboard counter changes, render all clip modes and not_read, and complete the Mac preview documentation and regression coverage.

## Notes

[2026-11-01T06:43:36Z · bob-cli-ey.3.1.4] clip-preview landed in bob-mac-capture: live preview omits --no-clip only for the current draft whose accepted parse reports a clip directive span on compatible grammar (bare %, escaped/literal %c, stale drafts, missing/lower grammar keep --no-clip); Clip card per batch item (kind/count headers, exact lines, snippet destination, attachment summaries+thumbnails, history dividers, not_read placeholder); activation refresh + <=1Hz pasteboard-counter poll with stops on hide/focus-loss/draft-removal/teardown; literal-clipboard caption and livePreviewUsesLiteralClipboard deleted; docs updated. Verified: athena just portable-check 1877 tests 0 failures, just docs-check passed, just check-scripts passed, fake-bob bash -n ok, retirement sweep clean, epic-symbols empty. macOS targets unverified (ssh to mac timed out; hosted tests run in macOS CI).

## Dependencies

- **Depends on:** [bob-cli-ey.3.1.3](bob-cli-ey.3.1.3.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.3.1.4/README.md) | [bob-cli-ey.3.1.4](bob-cli-ey.3.1.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.3.1.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.3.1.4/README.md

<!-- sase:referenced-by:end -->
