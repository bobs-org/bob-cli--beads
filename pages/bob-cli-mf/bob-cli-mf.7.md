# Bead: bob-cli-mf.7 — Add-and-place ghosts and pointer drag

[Bead Pages](../README.md) / [bob-cli-mf](README.md) / bob-cli-mf.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.51.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.51.linker.w0.md) · **Assignee:** `bob-cli-mf.7` · **Size:** medium
**Created:** 2026-11-16 15:38:38 EST · **Closed:** 2026-11-16 22:11:06 EST
**Plan:** [202611/schema\_editor\_arrange\_and\_emoji.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_editor_arrange_and_emoji.md)

## Description

album-place-drag: show a ghost chip or row for choice-add and field-add that the move keys place before the single add op. Add shared pointer drag with grip handles, an insertion caret, autoscroll, and Esc cancel for album items.

## Notes

[2026-11-17T03:10:32Z · bob-cli-mf.7] PROPOSED FOLLOW-UP: two bank-setup unit tests fail identically on pristine base 86ddb9f (category.set now keeps ☕ emoji but tests expect bare label; Setup card model + selects-by-key tests) -r recording pre-existing failure found during phase verification

[2026-11-17T03:10:46Z · bob-cli-mf.7] PROPOSED FOLLOW-UP: real-Obsidian album UI e2e drag + ghost-add walkthrough with light/dark screenshots needs a host with the Obsidian Electron binary (none in this container; offline self-test skips) -r recording environment-limited phase verification

[2026-11-17T03:11:06Z · bob-cli-mf.7] Ghost placement + shared pointer drag land: choice-add/field-add paint a dashed ghost chip/row at the landing slot; Alt+J/K/Shift-ends/Alt+M move it with focus in the stage (no macOS glyph insertion) and the single add op carries the gap as position; shared drag controller in 241xb (grip, 2px caret, autoscroll, Esc, out-of-scope snap-back) feeds placeAtGap; 9 new unit tests pass, all 70 album/schema tests pass, build:check + inventory + bob-docs lint pass, deployed via bob plugins sync -p bob-ledger-tools. Pre-existing (identical on base 86ddb9f, noted as PROPOSED FOLLOW-UPs): 2 bank-setup tests, docs glossary drift, 11 unrelated suite failures + 4 perf flakes; real-Obsidian e2e needs an Obsidian host.

## Dependencies

- **Depends on:** [bob-cli-mf.6](bob-cli-mf.6.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mf.8](bob-cli-mf.8.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mf.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.7/README.md) | [bob-cli-mf.7](bob-cli-mf.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1ff96bd`](https://github.com/bobs-org/bob-plugins/commit/1ff96bd15c67be57865454137b605277bf5170f9) | feat(ledger-tools): add-and-place ghosts and pointer drag for the album Schema Card | [bob-cli-mf.7](bob-cli-mf.7.md) | 2026-11-16 22:13:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mf.7][1] | check notes history | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.7/README.md

<!-- sase:referenced-by:end -->
