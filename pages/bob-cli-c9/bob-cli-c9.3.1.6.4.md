# Bead: bob-cli-c9.3.1.6.4 — Docs, cleanup, test hardening, and acceptance evidence

[Bead Pages](../README.md) / [bob-cli-c9.3.1.6](bob-cli-c9.3.1.6.md) / bob-cli-c9.3.1.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.land.md) · **Assignee:** `bob-cli-c9.3.1.6.4` · **Size:** small
**Created:** 2026-10-25 19:48:33 EDT · **Closed:** 2026-10-25 21:38:47 EDT
**Plan:** [202610/ref\_reread\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_reread_landing_fixes.md)

## Description

contract_docs: correct help and docs, remove stale interim markers, add producer, inline-filing, and byte-snapshot tests, and run the full acceptance checks.

## Notes

[2026-10-26T01:38:47Z · bob-cli-c9.3.1.6.4] contract_docs done. Help: -f row no longer duplicates clap possible-values; Recapture covers -N as later-overwrite selector plus legacy-only and new-day no-force cases; fixed hint spacing; alphabetical order kept. Docs: same-day snapshot -f rereads as <dated-root>__vN; narrated-hint and newest-reading -L attach documented; ref-sync gains ref-<root-slug>-vN/-2/Title-(vN) rules; ref.md gains single-source __vN naming. Cleanup: removed stale allow(dead_code) and single_sources/collections_acceptance interim comments in force.rs, duplicate.rs, recapture.rs. Tests (5 new, all pass): jobs-worker and Keep-pull producer retries never mint __vN; inline -f reread files lib PDF + earlier: note + ^ref-v2 task in one run; local-PDF and URL byte snapshots of note/PDF/sidecar/audio/task line. Verified: just check exit 0 (fmt, clippy gate, full suite), just docs-gen exit 0 (no golden drift), just docs-check exit 0, epic-symbols clean, no Cargo.toml/CHANGELOG/memory changes.

## Dependencies

- **Depends on:** [bob-cli-c9.3.1.6.3](bob-cli-c9.3.1.6.3.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.6.4/README.md) | [bob-cli-c9.3.1.6.4](bob-cli-c9.3.1.6.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`516d7b9`](https://github.com/bobs-org/bob-cli/commit/516d7b98fe31311470d6cce1bd61dc3d81ce0665) | fix(ref): contract docs, cleanup, and reread test hardening | [bob-cli-c9.3.1.6.4](bob-cli-c9.3.1.6.4.md) | 2026-10-25 21:39:53 EDT |
