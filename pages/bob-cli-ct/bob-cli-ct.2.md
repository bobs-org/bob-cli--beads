# Bead: bob-cli-ct.2 — bob ref links read surface

[Bead Pages](../README.md) / [bob-cli-ct](README.md) / bob-cli-ct.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14k.md) · **Assignee:** `bob-cli-ct.2` · **Size:** medium
**Created:** 2026-10-26 15:37:26 EDT · **Closed:** 2026-10-26 16:52:17 EDT
**Plan:** [202610/ref\_link\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_link_copy.md)

## Description

links-cmd: add the read-only `bob ref links <REF> [N]` command (human, json, markdown, raw; page filter) with bob-computed label, site, and Markdown forms, golden-tested, with completion, catalog, help, and docs.

## Notes

[2026-10-26T20:32:35Z · bob-cli-ct.2] PROPOSED FOLLOW-UP: just docs-check published-URLs gate still red on the preexisting /bob-command-mode/ link in docs/guides/run-bob-from-obsidian.md (tracked by bob-cli-cs; same failure as bob-cli-ct.1). Lint, generated-drift, and Zensical build passed after the links-cmd docs landed.

[2026-10-26T20:52:17Z · bob-cli-ct.2--1] Verified bob ref links REF [N] (human/json/markdown/raw, page filter, computed label/site/markdown) with goldens, completion, catalog, help, and docs. sase tool run check passed (fmt, clippy, full cargo test). No leftover --epic-symbol entries. Recorded preexisting just docs-check published-URLs failure (bob-cli-cs).

## Dependencies

- **Depends on:** [bob-cli-ct.1](bob-cli-ct.1.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-ct.3](bob-cli-ct.3.md) ◐ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-ct.4](bob-cli-ct.4.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ct.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ct.2.md) | [bob-cli-ct.2](bob-cli-ct.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`82716a6`](https://github.com/bobs-org/bob-cli/commit/82716a6444e15457cbf432fd08636e2dcce0ea86) | feat(ref): add bob ref links read surface | [bob-cli-ct.2](bob-cli-ct.2.md) | 2026-10-26 16:53:14 EDT |
