# Bead: bob-cli-hg.6 — bob gmail save and list

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.6` · **Size:** large
**Created:** 2026-11-05 12:37:49 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

gmail-save: resolve URL/ID/note inputs to a confirmed thread, fetch it, write or refresh the mail note with inline images under the vault lock, honor headers mode, never_save, and the writer host, commit, journal, and list saved threads offline.

## Notes

[2026-11-06T04:45:57Z · bob-cli-hg.6] Planning audit: no prior phase notes or completed save/list implementation; shell, ids, body renderer, and note engine are landed. Validated four-medium-phase child epic proposal sase_plan_gmail_save_list.md: resolve-policy -> prepare-content -> save-transaction -> list-diagnostics, with its land agent to verify and close only hg.6. Upstream gog v0.44.0 inspection confirms attachment --inline writes a cache; proposal uses its narrowly allowlisted, readonly Discovery attachments.get with --no-cache to preserve the approved no-body-cache and dry-run contracts. No SASE memory edits or implementation changes. epic-symbols currently reports no entries.

## Dependencies

- **Blocks:** [bob-cli-hg.12](bob-cli-hg.12.md) ◐ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.14](bob-cli-hg.14.md) ◐ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.2](bob-cli-hg.2.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.4](bob-cli-hg.4.md) ✓ · ⧖ 2026-11-05
- **Depends on:** [bob-cli-hg.5](bob-cli-hg.5.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.7](bob-cli-hg.7.md) ◐ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.9](bob-cli-hg.9.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.md) | [bob-cli-hg.6](bob-cli-hg.6.md) | 0 |
