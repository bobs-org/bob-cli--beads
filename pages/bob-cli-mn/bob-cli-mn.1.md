# Bead: bob-cli-mn.1 — bob capture-rewrite keeps / literal after album routes

[Bead Pages](../README.md) / [bob-cli-mn](README.md) / bob-cli-mn.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1d8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1d8.md) · **Assignee:** `bob-cli-mn.1` · **Size:** medium
**Created:** 2026-11-17 06:44:44 EST · **Closed:** 2026-11-17 07:10:09 EST
**Plan:** [202611/album\_slash\_record\_list.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_slash_record_list.md)

## Description

bob_rewrite: teach capture-rewrite's / → # alias (and its typing-tip proof) to stay literal when the / is glued to a single-@ album route, via one more bounded album-head read; add Rust unit and CLI tests, update docs/capture.md, the CLI help, and the capture-alias glossary strand.

## Notes

[2026-11-17T12:10:09Z · bob-cli-mn.1] capture-rewrite keeps / literal after album routes. Verified: unit tests (AlbumValid/AlbumInvalid stay /, Unclaimed/DiscoveryIncomplete/no-policy still #, @eat/ still collapses, @eat# tip is null while @dev# still teaches /); CLI tests (album vault @eat/ unchanged with null tip, @notes/ still @notes#, @eat# null tip, missing vault @eat/ still @eat# and does not create the directory); live BOB_DIR probe of @eat/, @eat#, and @dev/; just lint, just docs-check, and cargo fmt --check. Glossary capture-alias updated; docs-gen refreshed CLI help and glossary.md.

## Dependencies

- **Blocks:** [bob-cli-mn.2](bob-cli-mn.2.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mn.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mn.1.md) | [bob-cli-mn.1](bob-cli-mn.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f692478`](https://github.com/bobs-org/bob-cli/commit/f6924787fa43424d6fb217261adf264debbf2272) | feat(capture): keep / literal after album routes | [bob-cli-mn.1](bob-cli-mn.1.md) | 2026-11-17 07:26:42 EST |
