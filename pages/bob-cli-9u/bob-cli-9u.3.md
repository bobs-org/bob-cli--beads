# Bead: bob-cli-9u.3 — Emphasis-aware quote preview in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-9u](README.md) / bob-cli-9u.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4z.linker.w0.md) · **Assignee:** `bob-cli-9u.3` · **Size:** small
**Created:** 2026-10-19 11:48:19 EDT · **Closed:** 2026-10-19 11:58:46 EDT
**Plan:** [202610/underline\_emphasis.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/underline_emphasis.md)

## Description

mac-preview: a pure RefsCore excerpt that keeps late emphasis inside the 4-line inspector preview, a plain-text quote tooltip, and bold runs instead of raw `**` in the Copy card picker.

## Notes

[2026-10-19T15:58:46Z · bob-cli-9u.3] mac-preview done in bob-mac-capture: RefsQuoteExcerpt.preview (leadThreshold=140, leadInWords=8) + RefsQuoteEmphasis.plainText in RefsCore with 10 new RefsInspectorTests; inspector quoteView shows excerpt with plain-text tooltip and full-quote VoiceOver; picker line1/line2/alternate render bold via shared RefsQuoteText helper; payloads/tooltips keep raw **. Verified: just portable-check exit 0 (1404 tests pass), Mac scratch-copy just typecheck-tests PASS, scratch deleted. No epic-symbol leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9u.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9u.3/README.md) | [bob-cli-9u.3](bob-cli-9u.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9u.3][1] | check notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9u.3/README.md

<!-- sase:referenced-by:end -->
