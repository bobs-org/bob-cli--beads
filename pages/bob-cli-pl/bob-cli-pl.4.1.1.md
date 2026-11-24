# Bead: bob-cli-pl.4.1.1 — Local home-card model, species, and presentation

[Bead Pages](../README.md) / [bob-cli-pl.4.1](bob-cli-pl.4.1.md) / bob-cli-pl.4.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.4--1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.4.md) · **Assignee:** `bob-cli-pl.4.1.1` · **Size:** medium
**Created:** 2026-11-24 09:51:08 EST · **Closed:** 2026-11-24 10:23:25 EST
**Plan:** [202611/local\_home\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/local_home_cards.md)

## Description

presentation: implement the pure local Area/Project card model, field and pennant species, DOM presentation, and deterministic model/DOM tests described below. Wire source fragments and exports, but leave production mounting to mount-foot.

## Notes

[2026-11-24T15:22:44Z · bob-cli-pl.4.1.1] Exported presentation contract for mount-foot:

- homeCardModel(input) -> null | model
  input: { path, frontmatter, sourceText?, clock?, ready?, hue?, ancestors?,
  resolveParent?(target, fromPath), ancestryBroken?, ancestryCyclic?,
  ancestryTruncated?, inbox?, isInboxNote?(path), themeHue?(name, raw) }
  model: { kind, path, stem, title: { text, source, range }, hue, material:
  { wash, muted, paper, hue }, terminal, inbox, root, crumbs, ancestry,
  subtitle, chips, ready, pills, where, managed, created, prj, sourcePending,
  lifecycle }
- homeCardBuildEl(doc, model, options?) -> Element | null
  options: { onOpenEditor({ filePath, key?, mode: "browse" }), onLink(target, event),
  onToggleCollapse(next), collapsed, reducedMotion }
- helpers: homeCardEligible, homeCardTitleModel, homeCardEligibleHeading,
  homeCardWalkAncestry, homeCardCollapseCrumbs, homeCardPrjTask,
  homeCardLifecycle, homeCardChips, homeCardReadyModel, homeCardWhereMarks,
  homeCardManagedMap, HOME_CARD_MAX_CRUMBS, HOME_CARD_CLASS, HOME_CARD_META_CLASS
- propertyCardHomeTitleRecognizer(title) — first-body H1, no followers
- species: area word Area tile field icon layers; project word Project tile pennant icon target
- propertyCardInventory({ ..., managed }) additive adapter grouping
- missing created stamp silent for kind === "area"
Fragments: 249b-plugin-home-card-model.js, 249c-plugin-home-card-dom.js, 374g-exports-home-card.js
No production host, mixin, or == registration in this phase.

[2026-11-24T15:22:51Z · bob-cli-pl.4.1.1] PROPOSED FOLLOW-UP: docs-check mount collision — BOB_CLI_DIR workspace npm run docs:check fails because bob-plugins docs/index.md collides with bob-cli docs/reference/plugins/index.md; reproduces from committed files, independent of this phase architecture.md species wording.

[2026-11-24T15:22:58Z · bob-cli-pl.4.1.1] PROPOSED FOLLOW-UP: vault sync blocked — bob plugins sync -p bob-ledger-tools refused overwrite of uncommitted deploy from bob-cli_10 (da688dd, 2026-11-24T13:11:12Z); research agent still running in workspace 10, so no -F. Land/mount-foot should sync after that deploy lands.

[2026-11-24T15:23:06Z · bob-cli-pl.4.1.1] PROPOSED FOLLOW-UP: event-link-times and frees-marks 25ms budgets failed once under full npm test load (74.7ms / 149ms) and passed in isolation; likely pre-existing load flake, not home-card code.

[2026-11-24T15:23:25Z · bob-cli-pl.4.1.1] Verified presentation-only home cards in bob-plugins: Area field/layers and Project pennant/target species; homeCardModel/homeCardBuildEl with injected callbacks; propertyCardHomeTitleRecognizer; additive inventory managed seam; area-silent missing created stamp. npm run build; 15/15 home-card unit tests plus identity/created/inventory/title/foot kit tests pass; npm run validate passes. npm test: 9233 pass, 4 fail — two stylesheet hex contracts fixed, two 25ms budgets failed once under suite load and passed isolated. docs-check mount collision and vault sync overwrite-refusal recorded as PROPOSED FOLLOW-UP. No production host, mixin, == registration, or ancestor close. epic-symbols: none.

## Dependencies

- **Blocks:** [bob-cli-pl.4.1.2](bob-cli-pl.4.1.2.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.4.1.1/README.md) | [bob-cli-pl.4.1.1](bob-cli-pl.4.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5717d51`](https://github.com/bobs-org/bob-plugins/commit/5717d5182523c2d357ec604b1476fc5e32c12e10) | feat(ledger-tools): add local Area and Project card presentation | [bob-cli-pl.4.1.1](bob-cli-pl.4.1.1.md) | 2026-11-24 10:27:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.4.1.1][1] | Confirm close status after finalizer keep on linked repo | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.4.1.1/README.md

<!-- sase:referenced-by:end -->
