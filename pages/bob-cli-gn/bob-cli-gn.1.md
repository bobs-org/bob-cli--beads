# Bead: bob-cli-gn.1 — bob records attachment origins and ships \`bob attachments\`

[Bead Pages](../README.md) / [bob-cli-gn](README.md) / bob-cli-gn.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.17n](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.17n.md) · **Assignee:** `bob-cli-gn.1` · **Size:** medium
**Created:** 2026-11-03 14:53:40 EST · **Closed:** 2026-11-03 15:58:48 EST
**Plan:** [202611/image\_zoom\_origins.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/image_zoom_origins.md)

## Description

origins: add the `.bob/attachments/<host>.jsonl` origin journal, have `%c` record every attachment it copies, add `bob attachments import` and `bob attachments origin`, allowlist the journal in the vault, and document the contract.

## Notes

[2026-11-03T20:58:38Z · bob-cli-gn.1] PROPOSED FOLLOW-UP: HEAD commit a95d5d8f (bob-cli-gj stitch) shipped a duplicate `note_pull: None` in one CaptureItemResult literal (src/native/capture/plan.rs), so the tree did not compile; removed the trailing duplicate (value unchanged) to unblock this phase — owning epic should confirm

[2026-11-03T20:58:48Z · bob-cli-gn.1] origins phase done and verified: .bob/attachments/<host>.jsonl journal with attachment.import events, bob attachments import (10-path, %c-identical copy, journal cleanup on append failure) and origin (hash-then-saved candidates, this-host-present pick, present/missing/changed/elsewhere) in human+json, %c recording via capture with byte-identical capture JSON and dry-run writing nothing, vault allowlist verified trackable + merge=union (left for vault-sync to commit), docs/attachments.md + nav/registry/privacy-baseline wired, just check green (fmt, clippy gates, full cargo test workspace exit 0: lib 4772, cli 2953, all other bins ok), just docs-gen + just docs-check green

## Dependencies

- **Blocks:** [bob-cli-gn.2](bob-cli-gn.2.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gn.3](bob-cli-gn.3.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gn.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gn.1.md) | [bob-cli-gn.1](bob-cli-gn.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0b4cebd`](https://github.com/bobs-org/bob-cli/commit/0b4cebdf90cdd8fb8bb69ed60e07b2936c480906) | feat(attachments): record attachment origins and ship bob attachments | [bob-cli-gn.1](bob-cli-gn.1.md) | 2026-11-03 16:32:51 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gn.1--1][1] | Need phase scope check for stale landing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gn.1.md

<!-- sase:referenced-by:end -->
