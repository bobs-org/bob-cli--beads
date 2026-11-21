# Bead: bob-cli-o6.2 — Identity kit: species tile, kicker, title row, rail, tokens, and title ownership

[Bead Pages](../README.md) / [bob-cli-o6](README.md) / bob-cli-o6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1eh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1eh.md) · **Assignee:** `bob-cli-o6.2` · **Size:** large
**Created:** 2026-11-20 11:49:16 EST · **Closed:** 2026-11-20 12:47:17 EST
**Plan:** [202611/property\_card\_title\_block.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_title_block.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:46d23740114adb12f11c021c | attached via sase artifact create --bead |
| related | file:explicit:81e02cfaafb6ccf00d465f0c | attached via sase artifact create --bead |
| related | file:explicit:d0db68c8b8e4d000bccb5052 | attached via sase artifact create --bead |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

identity-kit: add the shared species registry, glyph tiles, kicker/title/subtitle row, docked rail with optional children strip, data-card-kind tokens and the temporal accent, and generalized title ownership (inline-title hide, Live Preview block hide with reveal-on-selection-touch, Reading source hide) to the bob-ledger-tools kit, with unit tests and a preview matrix; no card adopts it yet.

## Notes

[2026-11-20T17:46:43Z · bob-cli-o6.2] IDENTITY KIT API (bob-ledger-tools 1.144.0; all on module.exports.helpers via src/374-exports-property-card.js). Fragments 240f-240i after 240d. Species (240f): PROPERTY_CARD_KIND_ATTR ("data-card-kind"), PROPERTY_CARD_KINDS, propertyCardSpecies(kind) -> frozen {kind, word, tile, icon, band, temporal}, propertyCardAccessibleName(kind, title), propertyCardApplyIdentity(card, {kind, title}). Builders (240g): propertyCardBuildGlyphTile(doc, {kind, emoji?, icon?, band?, value?}) (leaf value carries data-value-length so CSS shrinks a 4-char year), propertyCardBuildTitleBlock(doc, {kind, title, kicker, pill, subtitle, tile, onLink}) -> {element, tile, kicker, heading, pill, subtitle, actions}, propertyCardBuildRail(doc, {prev, parent, next, children, label, onNavigate}) -> {element, items:{prev,parent,next}, children}. Links handle click and middle-click (auxclick button 1): preventDefault, then the injected handler with the raw event; never internal-link. Range and recognizers (240h, pure): propertyCardCleanInlineText, propertyCardCleanHeadingText, propertyCardTitleSourceRangeFromLines(lineAt, lineCount, recognizer), propertyCardTitleSourceRange(text, recognizer), propertyCardSelectionTouches(selection|state, range), propertyCardPeriodScaffoldTitle(subject) (bob labels.rs format), propertyCardAlbumTitleRecognizer(title), propertyCardDayTitleRecognizer(subject, {alias, today}), propertyCardPeriodTitleRecognizer(subject, {alias, today}). The period heading also accepts the bob scaffold title and the intention subject.label, not only the alias. Ownership (240i): PROPERTY_CARD_OWNS_TITLE_CLASS, PROPERTY_CARD_TITLE_SOURCE_CLASS, PROPERTY_CARD_TITLE_SOURCE_ATTR, propertyCardTitleScopeDenied, propertyCardTitleFieldCreate/Reduce/Decorations/Attributes, propertyCardTitleOwnershipExtension, propertyCardTitleEnsureEffect, propertyCardOwnTitleInEditor(view, {path, recognizer, defer?}), propertyCardReadingLineText, propertyCardOwnTitleInReading(scope, {path, recognizer}), propertyCardOwnTitle(scope, {path, recognizer, view}), propertyCardTitleReleaseAll, propertyCardHostRegisterTitleOwnership(plugin). Handles are release functions with .generation. Editor own returns null in Source mode and when the kit field is not installed (no host opted in), so adopters treat null as fall back to native. Re-owning the same path and key returns the same handle, and re-dispatches the same generation only if the field dropped it (Source round trip). Reading own bumps the generation on every call, like propertyCardOwnKeys, so keep the latest handle. Host: createPropertyCardHost({titleOwnership: true}) registers the field once per plugin (flag _propertyCardTitleOwnershipRegistered). Only opted-in hosts call propertyCardTitleReleaseAll on dispose. CSS: kit section at the end of styles.css. --bob-property-card-ink (accent 70% toward --text-normal) colors the species word, pill, and current chip so kicker contrast is at least 4.5:1. --bob-day-accent uses an rgb(0 191 188) fallback, not #00bfbc, because the Reading Board and Stats stylesheet contract tests forbid hex in trailing sections. The album header band applies only when content follows the title block (:not(:last-child)).

[2026-11-20T17:46:52Z · bob-cli-o6.2] PROPOSED FOLLOW-UP: bob-plugins test-command-mode-sheet-sequence-dom "production sheet render and clicks use real DOM APIs" timed out at 30 s in a full npm test run on athena under heavy load (load average 184 on 64 cores). It passed twice in isolation on the identity-kit tree and once on a clean 36dcf7c archive. No open flake bead tracks this timeout (bob-cli-f1, closed, covered the missing-Chromium skip). Separately, the frees-marks "200-link / 2000-task build stays within the 25 ms budget" check failed in both full runs (254 ms, 495 ms). It passes in isolation on both trees, and bob-cli-io already tracks it.

[2026-11-20T17:47:17Z · bob-cli-o6.2] Identity kit shipped in bob-ledger-tools 1.144.0, uncommitted in linked bob-plugins until this turn finalizes (commit: feat(ledger-tools): add property-card identity kit and title ownership). It adds fragments 240f-240i, the titleOwnership host option, the CSS kit section, the purple-to-violet walk-rail fix, exports, two unit suites, scripts/preview-title-block.cjs, and an architecture.md "Title block kit" subsection. Rebased on origin/master 36dcf7c (ledger-tools 1.143.0); the title-slot phase had not landed. Verified: npm run build and build:check are clean. The new suites pass: identity 8/8, title-ownership 18/18. Full npm test passed except load-only timing flakes (load average 184): the frees-marks 25 ms budget (bob-cli-io) and a command-mode sheet-sequence 30 s timeout (follow-up noted). Both pass in isolation on this tree and on clean 36dcf7c. npm run docs:check passed twice (BOB_CLI_DIR set to the bob-cli workspace). preview-property-cards -b 36dcf7c: 24/24 pixel-identical. The record-rail fixture uses blue, so the violet fix changes no capture. preview-intention-card: 24/24 sha256-identical to a 36dcf7c archive render. preview-title-block: 56 captures, all assertions pass (one aria-level=1 per card; species contrast at least 5.5:1 light and 7.7:1 dark; stripe contrast at least 4.2:1). I inspected every PNG and fixed two defects found that way: the record fold overlapping the emoji at 375px, and a stray album header rule when nothing follows the title block. Artifacts: report file:explicit:46d23740114adb12f11c021c, index file:explicit:d0db68c8b8e4d000bccb5052, grayscale sheet file:explicit:81e02cfaafb6ccf00d465f0c. bob plugins sync -p bob-ledger-tools (dry run, then real) had no refusal; the vault main.js and styles.css are byte-identical to the checkout. No epic symbols. No memory edits.

## Dependencies

- **Blocks:** [bob-cli-o6.4](bob-cli-o6.4.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-o6.5](bob-cli-o6.5.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.2.md) | [bob-cli-o6.2](bob-cli-o6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6278b78`](https://github.com/bobs-org/bob-plugins/commit/6278b78c8f0987071d189245dd40eca426c55e12) | feat(ledger-tools): add property-card identity kit and title ownership | [bob-cli-o6.2](bob-cli-o6.2.md) | 2026-11-20 12:48:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.5.1.1][1] | Check open o6 phases for fragment coordination before editing 240g/styles.css | 1 |
| read-by | [agent:bob-cli-oj.5.1.2][2] | Coordination precondition: which o6 phases are open and which fragments they touch | 1 |
| read-by | [agent:bob-cli-oj.5.1.3][3] | bob-cli-o6 precondition: check open phases editing fragments I will touch | 1 |
| read-by | [agent:bob-cli-oj.6][4] | Need o6 child phase statuses to avoid editing fragments an open o6 phase is changing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md

<!-- sase:referenced-by:end -->
