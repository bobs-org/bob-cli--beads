# Bead: bob-cli-ct.5 — Link picker, link well, and panel wiring

[Bead Pages](../README.md) / [bob-cli-ct](README.md) / bob-cli-ct.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14k.md) · **Assignee:** `bob-cli-ct.5` · **Size:** medium
**Created:** 2026-10-26 15:37:27 EDT · **Closed:** 2026-10-26 17:45:08 EDT
**Plan:** [202610/ref\_link\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_link_copy.md)

## Description

mac-ui: fetch links beside code when the Copy card opens, draw the L row, the link picker rows, and the link well in light and dark, extend the design fixtures and docs, and run the Mac acceptance.

## Notes

[2026-10-26T21:44:53Z · bob-cli-ct.5] PROPOSED FOLLOW-UP: Review CI render artifacts for the new refs-copy-link-* design fixtures when macOS CI runs

[2026-10-26T21:44:57Z · bob-cli-ct.5] PROPOSED FOLLOW-UP: Run interactive Mac acceptance (Cmd-Y L Return in Highlights, digit/Option-A variants, HUD, pasteboard vs click URL) with a release-train bob

[2026-10-26T21:45:08Z · bob-cli-ct.5] mac-ui done in bob-mac-capture: panel fetches links beside code (token-guarded, cancelled on close, unsupported mapped), Copy card draws L row/LINKS picker/link well with light/dark+contrast tokens, design fixtures + panel-model tests added, portable-check 1693 pass, mac typecheck-tests + bundle build pass, docs-check pass

## Dependencies

- **Depends on:** [bob-cli-ct.4](bob-cli-ct.4.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ct.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ct.5/README.md) | [bob-cli-ct.5](bob-cli-ct.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@2764ec5`](https://github.com/bobs-org/bob-mac-capture/commit/2764ec5f4a8fe2574bb6e466bc451a13df5dc8f3) | feat(refs): wire Copy card link picker, link well, and panel loads | [bob-cli-ct.5](bob-cli-ct.5.md) | 2026-10-26 17:46:50 EDT |
