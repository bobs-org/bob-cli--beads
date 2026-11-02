# Bead: bob-cli-fw.2 — Mac Capture merge card shows what bob picked

[Bead Pages](../README.md) / [bob-cli-fw](README.md) / bob-cli-fw.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.173](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.173.md) · **Assignee:** `bob-cli-fw.2` · **Size:** small
**Created:** 2026-11-02 09:55:54 EST · **Closed:** 2026-11-02 11:10:15 EST
**Plan:** [202611/merge\_next\_planned\_default.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merge_next_planned_default.md)

## Description

mac: decode the new merge fields, mark the implied source (`Current`) and absorbed rows (`Next`), add a tinted `Same as =*plan#fix` caption with a `#name` teaching hint, and document the merge card and protocol row.

## Notes

[2026-11-02T16:10:15Z · bob-cli-fw.2] Mac Capture decodes source_role, absorbed[].role, and explicit; Current/Next capsules and Same as caption render from those fields. portable-check (2017 tests), just docs-check, and a Mac scratch bundle.sh + typecheck-tests all passed.

## Dependencies

- **Depends on:** [bob-cli-fw.1](bob-cli-fw.1.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fw.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fw.2/README.md) | [bob-cli-fw.2](bob-cli-fw.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@a58e4f0`](https://github.com/bobs-org/bob-mac-capture/commit/a58e4f09fc987f7e0056336f94870082fc00c2ca) | feat(capture): show implied merge picks on the merge card | [bob-cli-fw.2](bob-cli-fw.2.md) | 2026-11-02 11:11:38 EST |
