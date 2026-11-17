# Bead: bob-cli-mf.6 — Shared Emoji Slot in the album card

[Bead Pages](../README.md) / [bob-cli-mf](README.md) / bob-cli-mf.6

**Status:** ✓ closed · **Resolution:** (unrecorded) · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.51.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.51.linker.w0.md) · **Assignee:** `bob-cli-mf.6` · **Size:** medium
**Created:** 2026-11-16 15:38:38 EST
**Plan:** [202611/schema\_editor\_arrange\_and\_emoji.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_editor_arrange_and_emoji.md)

## Description

album-emoji-slot: build the shared Emoji Slot (glyph well, preview chip, and in-card panel served by the bob-emoji api, with a plain fallback). Wire it into album choice add/edit and field-add initial choices with duplicate badges, IME guards, and a strict Esc ladder.

## Notes

[2026-11-17T00:02:47Z · bob-cli-mf.6] PROPOSED FOLLOW-UP: Capture and inspect the six real Obsidian Emoji Slot screenshots (empty, filtered, and browse states in light and dark themes) with scripts/obsidian-album-ui-e2e.cjs on a host with Obsidian and Xvfb; this environment lacks both, though the capture hooks and self-test are in place.

[2026-11-17T00:58:21Z · bob-cli-mf.6--3] PROPOSED FOLLOW-UP: Triage the 16 failures shared by the original and clean pre-Emoji full suites: “Setup card model preserves Category-card order and maps category gestures to guarded ops”; “Setup card selects by key, protects focused typing, and stages shared New category input”; “perf — one build over a 200-link ledger stays under 25 ms”; “200-link / 2000-task build stays within the 25 ms budget”; both “200-link / 50-target Live Preview build memoizes targets and stays near the 25 ms budget” cases; “mobile, non-desktop, or missing status bar mounts nothing and keeps type undefined”; “walkMode api is versioned and the top-level api version is unchanged”; “walkMode degrades with a null plugin”; “walkMode.setAttention validates type and value”; “a chip click opens the cached target and never re-resolves”; “toggle hides the chip and rail for the session”; “priority notice stylesheet scopes Obsidian notice overrides and uses theme tokens”; “walkMode.links matches the first destination [n and ]n would open”; “obsidian-block-marks-e2e --self-test”; and “production CSS computes no animation or transition under reduced motion”. Deltas: clean-base-only “stage ranker filters 1,000 synthetic tasks under 16 ms per keystroke” passed alone; original-only MN click passed in focused relation tests; clean-base-only “SV fixture is copied byte-for-byte from bob-cli” points to missing offer_close/vectors.json. No Emoji Slot regression reproduced.

[2026-11-17T02:32:35Z · bob-cli-mf.6--5] FINAL VERIFICATION — npm run build:check passed. The focused Emoji Slot suite reported 103 tests: 101 passed, 0 failed, 2 skipped. BOB_CLI_DIR workspace-aligned npm run docs:check passed all implemented gates (447 passed, 1 skipped for the Obsidian-dependent plugin-sync documentation check). Clean pre-Emoji base 866bb77c859d19046784324c58fd4e97ec86b00d npm test reported 7,043 passed and 18 failed; note #2 records the 16 shared failures, the clean-base-only stage-ranker budget and missing offer_close fixture, and the original-only MN click result. No Emoji Slot regression reproduced. Approved bob plugins sync -F -n -p bob-ledger-tools succeeded: 3 files copied, 0 skipped, 0 unchanged; installed Bob Ledger Tools v1.124.0. Real screenshot limitation: six Obsidian captures (empty, filtered, browse in light and dark themes) remain unavailable because this environment has neither Obsidian nor Xvfb; the proposed screenshot follow-up remains recorded. sase bead epic-symbols bob-cli-mf.6 returned no entries. Parent bob-cli-mf remains open.

## Dependencies

- **Depends on:** [bob-cli-mf.3](bob-cli-mf.3.md) ✓ · ⧖ 2026-11-16
- **Depends on:** [bob-cli-mf.5](bob-cli-mf.5.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mf.7](bob-cli-mf.7.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mf.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mf.6.md) | [bob-cli-mf.6](bob-cli-mf.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mf.6--5][1] | Verify the phase close and appended verification record | 2 |
| read-by | [agent:research.53.gem][2] | Understand concurrent agent deploying bob-plugins alongside ei | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mf.6.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.53.gem/README.md

<!-- sase:referenced-by:end -->
