# Bead: bob-cli-1e.4 — Verify quota recovery and run the fallback if version history holds

[Bead Pages](../README.md) / [bob-cli-1e](README.md) / bob-cli-1e.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0en](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0en.md) · **Assignee:** `bob-cli-1e.4` · **Size:** medium
**Created:** 2026-08-27 08:13:36 EDT · **Closed:** 2026-08-27 08:38:19 EDT
**Plan:** [202608/unsync\_old\_lib.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/unsync_old_lib.md)

## Description

verify: confirm sync cycles go green, and if attachment version history keeps the vault over 1 GB, execute the documented fresh-remote-vault rebuild with exclusions configured before the first sync.

## Notes

[2026-08-27T12:38:19Z · bob-cli-1e.4] Verified: sync still red (Vault limit exceeded) after 3+ poll cycles since service restart. Confirmed this matches the anticipated version-history cause, not a new failure: old_lib fully drained from remote (0 live entries, 0 MB), remote live total 114.5 MB (matches backup baseline ~115 MB projection), ignoreFolders=['old_lib'] verified in config.json, local old_lib intact at 660 files / 814 MB. Per Q1 answer, user chose Wait over the fresh-remote-vault rebuild fallback: re-check daily, sync (including bob nightly) stays broken for up to ~2 weeks while old_lib attachment version history expires naturally on the Standard plan, no data risk, no re-onboarding. Did not execute ob sync-create-remote/sync-setup rebuild steps per that decision.

## Dependencies

- **Depends on:** [bob-cli-1e.3](bob-cli-1e.3.md) ✓ · ⧖ 2026-08-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1e.4](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.bob-cli-1e.4.md) | [bob-cli-1e.4](bob-cli-1e.4.md) | 0 |
