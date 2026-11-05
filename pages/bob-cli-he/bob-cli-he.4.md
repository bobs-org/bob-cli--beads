# Bead: bob-cli-he.4 — Mac Clip card shows provider and ages

[Bead Pages](../README.md) / [bob-cli-he](README.md) / bob-cli-he.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5r.linker.w0.md) · **Assignee:** `bob-cli-he.4` · **Size:** small
**Created:** 2026-11-05 10:29:53 EST · **Closed:** 2026-11-05 14:16:02 EST
**Plan:** [202611/percent\_c\_history\_agreement.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/percent_c_history_agreement.md)

## Description

mac-card: in bob-mac-capture, decode clip.history tolerantly, show provider and ages in the Clip card, and drop the Clipy wording from the panel docs.

## Notes

[2026-11-05T19:13:47Z · bob-cli-he.4] PROPOSED FOLLOW-UP: macOS CI Test step hangs at the 15-minute watchdog (stuck after WorkBadgeToneTests) on master, including the clean base commit 6e09f2c (run 42079206476) and this phase commit 9714a56 (run 42089082999); Lint and Build are green and all CaptureClipPresentationTests pass on macOS. Investigate the hanging test via the test-hang artifact.

[2026-11-05T19:16:02Z · bob-cli-he.4] Verified: swift build clean; full swift test 2177 passed/0 failed on Linux; all 12 CaptureClipPresentationTests (incl. 3 new provenance tests) pass on macOS CI with Lint and Build green; just docs-check passed. macOS CI Test step red via pre-existing 15-min watchdog hang after WorkBadgeToneTests, reproducing identically on clean base 6e09f2c (run 42079206476) vs this commit 9714a56 (run 42089082999); recorded as PROPOSED FOLLOW-UP. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-he.3](bob-cli-he.3.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-he.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-he.4.md) | [bob-cli-he.4](bob-cli-he.4.md) | 0 |
