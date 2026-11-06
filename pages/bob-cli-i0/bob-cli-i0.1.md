# Bead: bob-cli-i0.1 — install\_ui package core, state store, and script test harness

[Bead Pages](../README.md) / [bob-cli-i0](README.md) / bob-cli-i0.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.199](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.199.md) · **Assignee:** `bob-cli-i0.1` · **Size:** medium
**Created:** 2026-11-06 15:11:24 EST · **Closed:** 2026-11-06 15:32:41 EST
**Plan:** [202611/install\_all\_wait\_and\_whats\_new.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/install_all_wait_and_whats_new.md)

## Description

ui-core: create the stdlib Python 3.9 `scripts/lib/install_ui/` package (entry point, term.py, state.py, watermark subcommands), the bash 3.2-safe `scripts/lib/install_ui.sh` loader, bob-cli watermark recording in `just install`, and a unittest suite with portability gates wired into `just check-scripts`.

## Notes

[2026-11-06T20:32:41Z · bob-cli-i0.1] just check-scripts passes (42 install_ui unit tests: term fixtures vs install_all banner/duration, state concurrent appends/corrupt JSON/unwritable dir/trim/lock contention, 3.9 syntax + bash 3.2 lint, loader discovery/cache/BOB_INSTALL_UI=0). mark-installed records full HEAD SHA, dirty flag, and path in installed.json; watermark --json reads it; just install sources install_ui.sh and calls install_ui_mark_installed after a successful cargo+completion install.

## Dependencies

- **Blocks:** [bob-cli-i0.2](bob-cli-i0.2.md) ◐ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-i0.3](bob-cli-i0.3.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-i0.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-i0.1/README.md) | [bob-cli-i0.1](bob-cli-i0.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`10be962`](https://github.com/bobs-org/bob-cli/commit/10be96258b86bdf3ad8bdc6cabd5ae34e71e7bf0) | feat(install): add install\_ui core, watermarks, and script tests | [bob-cli-i0.1](bob-cli-i0.1.md) | 2026-11-06 15:33:58 EST |
