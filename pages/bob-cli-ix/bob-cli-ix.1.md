# Bead: bob-cli-ix.1 — Claim \`Nx\` in both parsers

[Bead Pages](../README.md) / [bob-cli-ix](README.md) / bob-cli-ix.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3s.linker.w0.md) · **Assignee:** `bob-cli-ix.1` · **Size:** large
**Created:** 2026-11-09 05:24:37 EST · **Closed:** 2026-11-09 06:55:09 EST
**Plan:** [202611/sized\_pomodoro\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/sized_pomodoro_close.md)

## Description

grammar: add the shared size lexer and `PomodoroCloseSpec.size`, claim sized whole-item, chain, and link closes plus their teaching errors in the execution and editor parsers, extend `capture-parse` spans/JSON and the close-outcome aliases, and make `bob capture` refuse sized specs until execution lands.

## Notes

[2026-11-09T10:31:55Z · bob-cli-ix.1] PROPOSED FOLLOW-UP: Reconcile the sized-close execution grammar revision — the parent plan says to bump 19 to 20, but src/native/capture_language/mod.rs already declares 21 after record-update parsing (12641768); tests/cli/capture/record.rs and parse.rs assert 21. The grammar phase will preserve the current revision. The execution phase and epic land agent must choose the next monotonic revision instead of lowering it to 20.

[2026-11-09T11:28:17Z · bob-cli-ix.1] PROPOSED FOLLOW-UP: execute-phase GRAMMAR_REVISION — the later execute phase still instructs setting GRAMMAR_REVISION to 20; current grammar is 21. Reconcile with then-current revision instead of bumping or lowering 21 from this grammar phase.

[2026-11-09T11:55:09Z · bob-cli-ix.1--1] Closed by explicit `sase stitch create -B close` after create_commit landed 070d2aac ("feat(capture)!: claim the sized Nx close in the capture grammar"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-ix.1` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-ix.2](bob-cli-ix.2.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ix.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ix.1.md) | [bob-cli-ix.1](bob-cli-ix.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`070d2aa`](https://github.com/bobs-org/bob-cli/commit/070d2aacbfb2ee7b481eabe3db0ecd5c417fd00f) | feat(capture)!: claim the sized Nx close in the capture grammar | [bob-cli-ix.1](bob-cli-ix.1.md) | 2026-11-09 06:54:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ix.1--1][1] | Confirm assigned phase is complete so this recovery turn can close it | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ix.1.md

<!-- sase:referenced-by:end -->
