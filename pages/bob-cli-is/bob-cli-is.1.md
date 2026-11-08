# Bead: bob-cli-is.1 — Bob capture-rewrite close-outcome alias

[Bead Pages](../README.md) / [bob-cli-is](README.md) / bob-cli-is.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3r.linker.w0.md) · **Assignee:** `bob-cli-is.1` · **Size:** medium
**Created:** 2026-11-08 11:42:40 EST · **Closed:** 2026-11-08 12:28:45 EST
**Plan:** [202611/close\_outcome\_x\_s\_typing\_aliases.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/close_outcome_x_s_typing_aliases.md)

## Description

bob-close-alias: add an x/s branch to the expand_sigil_alias rule in bob-cli capture-rewrite. It locates a close slot on the draft before the key, then checks the swapped selection with the close lexer. Ships with unit and CLI tests, capture-rewrite help, and capture docs as a non-breaking feat(capture).

## Notes

[2026-11-08T17:28:30Z · bob-cli-is.1] PROPOSED FOLLOW-UP: just check clippy fails on the clean tree in src/native/gmail/sync/file.rs — bind_instead_of_map at L327 and needless_return at L163/L184 from 1cf8d96b; cargo fmt --check, cargo test --workspace, and just docs-check are green

[2026-11-08T17:28:45Z · bob-cli-is.1] Verified: expand_sigil_alias aliases lowercase x→! and s→* in whole-item, lead-chain, past second-=, and link-close slots with --cursor; letters stay literal in capture/capture-parse, inline logs, child bullets, templates, wikilinks, and without --cursor. cargo fmt --check, cargo test --workspace (5689 lib tests + CLI), and just docs-check passed. just check clippy fails on clean-tree gmail/sync/file.rs (see PROPOSED FOLLOW-UP). epic-symbols empty. No memory edits.

## Dependencies

- **Blocks:** [bob-cli-is.3](bob-cli-is.3.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-is.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-is.1/README.md) | [bob-cli-is.1](bob-cli-is.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-is.1][1] | Need notes and remaining work from earlier agents | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-is.1/README.md

<!-- sase:referenced-by:end -->
