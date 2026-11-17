# Bead: bob-cli-mf.3 — bob-emoji search upgrades and api v1

[Bead Pages](../README.md) / [bob-cli-mf](README.md) / bob-cli-mf.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.51.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.51.linker.w0.md) · **Assignee:** `bob-cli-mf.3` · **Size:** medium
**Created:** 2026-11-16 15:38:38 EST · **Closed:** 2026-11-16 16:03:36 EST
**Plan:** [202611/schema\_editor\_arrange\_and\_emoji.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_editor_arrange_and_emoji.md)

## Description

emoji-engine: normalize multi-token queries with tiered ranking, look up pasted glyphs, add catalog categories, CLDR keywords when chosen, and label suggestions. Expose a frozen versioned api on bob-emoji that keeps the editor :shortcode: menu.

## Notes

[2026-11-16T21:03:36Z · bob-cli-mf.3] emoji-engine done in bob-plugins: CLDR en+derived vendored at 7d2b9cb (LICENSE.cldr.txt, README pinned), generator merges category+keywords with VS16-insensitive dedupe and curated gaps (memory, find, automation/service, ready, seed); search rewritten with colon-strip, multi-token AND, tiers 0-6, alias preference, VS16 single-glyph first, within-tier boost/recents, Damerau fuzzy when <8; suggestForLabel with stop-words and light stemming; frozen api v1 (search/suggestForLabel/categories/browse/info/recents/remember) built even without EditorSuggest; docs updated (bob-emoji.md, plugin-apis.md Bob Emoji) and manifest 0.2.0; main.js 182KB->353KB (+171KB within 250KB budget); gates: build --check clean, 19 emoji tests pass, plugin-build+docs tests 60 pass, inventory check clean, docs-check passed, bob plugins sync -p bob-emoji deployed.

## Dependencies

- **Blocks:** [bob-cli-mf.6](bob-cli-mf.6.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mf.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.3/README.md) | [bob-cli-mf.3](bob-cli-mf.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@daceef0`](https://github.com/bobs-org/bob-plugins/commit/daceef0e0c6dfab253353bcb166bab5add273e7f) | feat(bob-emoji): search upgrades and api v1 with CLDR keywords | [bob-cli-mf.3](bob-cli-mf.3.md) | 2026-11-16 16:05:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mf.3][1] | Need phase scope | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.3/README.md

<!-- sase:referenced-by:end -->
