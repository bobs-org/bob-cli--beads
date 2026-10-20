# Bead: bob-cli-a7.3 — Contract, reference, and help text

[Bead Pages](../README.md) / [bob-cli-a7](README.md) / bob-cli-a7.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.9p` · **Assignee:** `bob-cli-a7.3` · **Size:** medium
**Created:** 2026-10-20 15:12:11 EDT · **Closed:** 2026-10-20 17:20:59 EDT
**Plan:** [202610/bare\_pomodoro\_names.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bare_pomodoro_names.md)

## Description

docs: teach `=name` as the primary spelling in the capture contract, syntax reference, and CLI help; regenerate references; pass the docs gate; propose the Mac Capture hint follow-up.

## Notes

[2026-10-20T21:20:46Z · bob-cli-a7.3] PROPOSED FOLLOW-UP: Mac Capture short-spelling hint — Bob emits a start_token (from named_start_token) on agenda entries, and the Mac renders it, falling back to =#slug on older Bob (CaptureAgendaPresentation.swift builds =#\(slug), headerTimeView styles hasPrefix("=#"), empty-state copy reads =#NAME starts one)

[2026-10-20T21:20:50Z · bob-cli-a7.3] PROPOSED FOLLOW-UP: docs-check material-builder tests fail on missing github-callouts/mkdocs modules — reproduces identically on clean base tree (verified via worktree at HEAD), environmental, unrelated to this phase

[2026-10-20T21:20:59Z · bob-cli-a7.3] Docs teach =name as primary spelling: capture.md grammar/named-start/atomically/linking/chaining/parse/complete/retired sections, capture-syntax.md index/headings/mnemonic/zsh note, CLI help + examples (=bugs, x =bugs, @sase:deep-fix=bugs) with regenerated cli refs. Verified: just check exit 0, help tests 77/77, docs-check passes lint/drift/zensical-build/URLs/lychee/search-smoke(110)/tutorial/media/token-coverage; 2 material-template failures are pre-existing environmental (missing github-callouts, reproduce on clean HEAD worktree). No epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-a7.1](bob-cli-a7.1.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a7.2](bob-cli-a7.2.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a7.3/README.md) | [bob-cli-a7.3](bob-cli-a7.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a0ac845`](https://github.com/bobs-org/bob-cli/commit/a0ac8451643ba867ce105627a8e346734ade961f) | docs(capture): teach =name primary start-token spelling | [bob-cli-a7.3](bob-cli-a7.3.md) | 2026-10-20 17:22:17 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a7.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a7.3/README.md

<!-- sase:referenced-by:end -->
