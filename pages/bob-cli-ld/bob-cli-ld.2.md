# Bead: bob-cli-ld.2 — Rust catalog row grammar and dual-format SUBOPEN reader

[Bead Pages](../README.md) / [bob-cli-ld](README.md) / bob-cli-ld.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c6.md) · **Assignee:** `bob-cli-ld.2` · **Size:** medium
**Created:** 2026-11-13 10:58:46 EST · **Closed:** 2026-11-13 12:05:03 EST
**Plan:** [202611/subprojects\_catalog\_section.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subprojects_catalog_section.md)

## Description

subopen-reader-rust: add the shared row grammar/parser, read SUBOPEN from the [!projects] callout with legacy-marker fallback in surface.rs, and publish shared parity vectors.

## Notes

[2026-11-13T17:00:15Z · bob-cli-ld.2] PROPOSED FOLLOW-UP: Triage clean-base workspace gate failures — just check fails with five deny-level clippy diagnostics in src/native/gmail/unarchive.rs introduced by commit 2ddfc944 (bob-cli-kx.3.1.3), reproduced identically on clean HEAD and reported on parent epic bob-cli-kx. just docs-check also reproduces identically with docs/reference/json-outputs.md at 6008/6000 (prior budget repair bob-cli-k3.2.1), docs/reference/plugins/bob-ledger-tools.md at 6136/6000 (editing-headroom tracker bob-cli-il; earlier proposal bob-cli-kx.3.1.3 note #1), and docs/reference/plugins/bob-navigation-hotkeys.md at 6055/6000 (prior budget tracker bob-cli-jz). No new task bead created.

[2026-11-13T17:05:03Z · bob-cli-ld.2] Added the Rust Projects row parser and catalog-first SUBOPEN reader with legacy fallback, damage handling, shared parity vectors, and updated docs. Focused reader tests, rustfmt, and diff checks pass. just check and just docs-check fail identically on clean HEAD; recorded both as a proposed follow-up. epic-symbols was empty.

## Dependencies

- **Depends on:** [bob-cli-ld.1](bob-cli-ld.1.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-ld.3](bob-cli-ld.3.md) ◐ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-ld.4](bob-cli-ld.4.md) ◐ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-ld.5](bob-cli-ld.5.md) ◐ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.2/README.md) | [bob-cli-ld.2](bob-cli-ld.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`86be434`](https://github.com/bobs-org/bob-cli/commit/86be4344ca1fb41169c74df637d25d74ef5624ee) | feat(projects): add dual-format SUBOPEN catalog reader | [bob-cli-ld.2](bob-cli-ld.2.md) | 2026-11-13 12:07:13 EST |
