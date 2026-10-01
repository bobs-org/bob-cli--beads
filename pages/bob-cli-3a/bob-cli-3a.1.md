# Bead: bob-cli-3a.1 — Display contract and pure mark model

[Bead Pages](../README.md) / [bob-cli-3a](README.md) / bob-cli-3a.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3y](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3y.md) · **Assignee:** `bob-cli-3a.1` · **Size:** medium
**Created:** 2026-10-01 11:19:39 EDT · **Closed:** 2026-10-01 11:43:33 EDT
**Plan:** [202610/fresh\_mark.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/fresh_mark.md)

## Description

mark-core: write the freshness-mark display contract and its M/N/C conformance vectors into docs/freshness.md. Then implement the pure, exported bob-ledger-tools helpers (source detection, resolution, model, consensus, tooltip, DOM builder) and the mark styles, and test them against the vectors verbatim.

## Notes

[2026-10-01T15:43:33Z · bob-cli-3a.1] mark-core done: docs/freshness.md §§11-12 + §5/§8/README updates; 7 pure helpers + DOM builder exported via module.exports.helpers with mark styles; new test file covers all M/N/C vectors verbatim (24 tests pass); full bob-plugins suite 1053 pass, validate 6/6, bob plugins sync ok; no epic-symbol leftovers

## Dependencies

- **Blocks:** [bob-cli-3a.2](bob-cli-3a.2.md) ◐ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3a.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3a.1/README.md) | [bob-cli-3a.1](bob-cli-3a.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`61785b7`](https://github.com/bobs-org/bob-cli/commit/61785b77522f1e88344426acdf8c50e21dc281ac) | feat(freshness): add freshness mark display contract and conformance vectors | [bob-cli-3a.1](bob-cli-3a.1.md) | 2026-10-01 11:45:51 EDT |
| bob-plugins | [`bob-plugins@dbe3bdd`](https://github.com/bobs-org/bob-plugins/commit/dbe3bdd0e7364523f89b6491b090938240751e12) | feat(ledger-tools): add pure freshness mark model, styles, and vector tests | [bob-cli-3a.1](bob-cli-3a.1.md) | 2026-10-01 11:46:24 EDT |
