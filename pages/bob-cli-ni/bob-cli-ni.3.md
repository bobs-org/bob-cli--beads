# Bead: bob-cli-ni.3 — The bob-copy fence card

[Bead Pages](../README.md) / [bob-cli-ni](README.md) / bob-cli-ni.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5g.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5g.linker.w0.md) · **Assignee:** `bob-cli-ni.3` · **Size:** medium
**Created:** 2026-11-19 10:05:33 EST · **Closed:** 2026-11-19 12:41:56 EST
**Plan:** [202611/copy\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/copy_chips.md)

## Description

fence: render bob-copy fences as titled cards with a header Copy button and byte-exact payloads, and teach chipAt and the cursor-line command about fences.

## Notes

[2026-11-19T17:41:56Z · bob-cli-ni.3] Fence card shipped: bob-copy fences render as titled cards (header Copy button, byte-exact payloads) in Live Preview and Reading view via one code-block processor; chipAt resolves fence positions as block chips and the cursor command flashes the card. Verified: 55 unit tests pass (17 new fence tests), build:check, validate 12/12, docs:check, offline e2e self-test. Real-Obsidian e2e cases written (payload exactness, fold, body-click, callout fallback) but not runnable here (no Obsidian binary); they run on hosts with Obsidian. Commit febfc6b pushed to bob-plugins master (rebased over 0a4a91f); vault synced to 0.3.0 and enabled. Bryan: reload Obsidian on each host.

## Dependencies

- **Depends on:** [bob-cli-ni.2](bob-cli-ni.2.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-ni.5](bob-cli-ni.5.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ni.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ni.3/README.md) | [bob-cli-ni.3](bob-cli-ni.3.md) | 0 |
