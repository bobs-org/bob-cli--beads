# Bead: bob-cli-3n.12.3 — Fix dependency chips and align the Depends-On recognisers

[Bead Pages](../README.md) / [bob-cli-3n.12](bob-cli-3n.12.md) / bob-cli-3n.12.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.land.md) · **Assignee:** `bob-cli-3n.12.3` · **Size:** medium
**Created:** 2026-10-02 23:24:08 EDT · **Closed:** 2026-10-02 23:59:32 EDT
**Plan:** [202610/task\_dep\_links\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_fixes.md)

## Description

chips-compat-fix: pin api v1 ref.line as 0-based and fix the chip off-by-one and stale widget meta, restrict chips to real Depends-On lines, fix Reading view, hover, and the lookup cache, align the ledger-tools, cycler, and block-id-prompt recognisers with new DP vectors, and add the missing tests.

## Notes

[2026-10-03T03:59:17Z · bob-cli-3n.12.3] PROPOSED FOLLOW-UP: Nav reader still accepts blockquoted Depends-On lines (writer round-trip) while Rust and the DP29 contract verdict say not-a-line — decide one side in nav-writer-fix or docs-memory-fix

[2026-10-03T03:59:32Z · bob-cli-3n.12.3] chips-compat-fix done: §9 pins 0-based ref.line; chips send 0-based refs (Live Preview + Reading derived line 2 in test, hidden when underivable); widget eq covers line+interactive; ownership-gated Live Preview (DP19/DP20) and Reading own-text match; Reading label/separators hidden, status box, done strike, ✓×N collapse; hover passes chip el + row; lookup index on freshness memo; DP24-DP29 added and all four recognisers aligned (Rust DP test green); bip refuses malformed Ctrl+Shift+Enter; cycler counted notice + handler tests; manifests 1.19.0/1.21.0/1.19.0 README rows updated; npm test 1305/1305, validate 6/6, just all green, three plugins deployed

## Dependencies

- **Blocks:** [bob-cli-3n.12.7](bob-cli-3n.12.7.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3n.12.8](bob-cli-3n.12.8.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.3/README.md) | [bob-cli-3n.12.3](bob-cli-3n.12.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a069239`](https://github.com/bobs-org/bob-cli/commit/a069239a5ec36929933b9bdbfa096e27a7d9ed58) | docs(deps): pin api v1 ref.line as 0-based and add DP24-DP29 recogniser vectors | [bob-cli-3n.12.3](bob-cli-3n.12.3.md) | 2026-10-03 00:00:51 EDT |
| bob-plugins | [`bob-plugins@330fc58`](https://github.com/bobs-org/bob-plugins/commit/330fc58b6f5ae549d412d9e13e81ee7ed86402d7) | fix(deps): 0-based chip refs, owned-line chips, Reading view, hover, memo-bound lookup, aligned recognisers | [bob-cli-3n.12.3](bob-cli-3n.12.3.md) | 2026-10-03 00:03:29 EDT |
