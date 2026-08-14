# Bead: bob-cli-n.1 — Authoritative Obsidian link protocol in bob-cli

[Bead Pages](../README.md) / [bob-cli-n](README.md) / bob-cli-n.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.00w.f0.f0.w0.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.00w.f0.f0.w0.w0.md) · **Assignee:** `bob-cli-n.1` · **Size:** medium
**Created:** 2026-08-14 11:05:26 EDT · **Closed:** 2026-08-14 11:29:07 EDT
**Plan:** [202608/obsidian\_link\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/obsidian_link_completion.md)

## Description

link_protocol: extend bob-cli's editor-facing parse and completion contracts with a shared, vault-aware Obsidian wikilink scanner, note/alias/heading/block discovery, byte-exact replacements, deterministic ranking, additive JSON metadata, documentation, and exhaustive Rust coverage while preserving existing capture behavior and the lexical no-I/O guarantee of capture-parse.

## Notes

[2026-08-14T15:28:58Z · bob-cli-n.1] PROPOSED FOLLOW-UP: Investigate transient capture_clip_failures_leave_vault_untouched Text file busy flake - one just test run failed running BOB_CLIPBOARD_CMD with os error 26; isolated rerun and subsequent just test passed.

[2026-08-14T15:29:07Z · bob-cli-n.1] Implemented bob-cli Obsidian wikilink scanner/index, semantic capture-parse spans, wikilink note/heading/block capture-complete contexts with cursor_after and warnings, docs, and tests. Verified just fmt; just lint (passes with existing unrelated clippy warnings in plugins.rs/projects.rs); just test; just install-smoke; git diff --check; large temp vault 1500 notes returned 20 capped candidates in cold 111ms/warm 119ms, 3416-byte JSON.

[2026-08-14T15:32:37Z · bob-cli-n.1] Reconfirmed before commit: just fmt; just lint; just test; just install-smoke; git diff --check; large generated 1500-note vault returned 20 capped candidates in 121ms cold/124ms warm with a 2677-byte JSON response.

## Dependencies

- **Blocks:** [bob-cli-n.2](bob-cli-n.2.md) ✓ · ⧖ 2026-08-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-n.1/README.md) | [bob-cli-n.1](bob-cli-n.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d5eaf97`](https://github.com/bobs-org/bob-cli/commit/d5eaf976403f6ef5eb5afe6f788303c530fba4a2) | feat(capture): add Obsidian wikilink editor protocol | [bob-cli-n.1](bob-cli-n.1.md) | 2026-08-14 11:35:50 EDT |
