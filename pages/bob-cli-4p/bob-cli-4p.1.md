# Bead: bob-cli-4p.1 — Priority marks in bob-ledger-tools

[Bead Pages](../README.md) / [bob-cli-4p](README.md) / bob-cli-4p.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0xf](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0xf.md) · **Assignee:** `bob-cli-4p.1` · **Size:** medium
**Created:** 2026-10-06 13:50:51 EDT · **Closed:** 2026-10-06 14:06:57 EDT
**Plan:** [202610/priority\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/priority_marks.md)

## Description

ledger-marks: build the display-only priority mark in bob-ledger-tools. That covers the canonical-field parser, the lenient ladder-config reader, the mark model and tooltip, a single CSS-mask glyph set, the Live Preview decoration, the rendered-view post-processor, CSS-only Tasks-result replacement, the repair flag, the session toggle, and the additive `api.priorityMarks` v1 namespace. Also write the bob-cli display contract with conformance vectors, then test, build, and sync.

## Notes

[2026-10-06T18:06:57Z · bob-cli-4p.1] ledger-marks done: parser/ladder/model/element in 135, Live Preview + post-processor + toggle + api.priorityMarks v1 in 265, CSS-mask glyph set + repair flag, docs/projects.md Priority marks contract with PM1-PM17 verbatim. Verified: npm run build ok, npm test 1904/1904 pass (incl. 17 new priority-marks tests), npm run validate 6/6, bob plugins sync deployed (4 copied), cargo fmt clean, epic-symbols none. Live Obsidian checklist pending for Bryan. One deviation: priorityMarksRefresh is lazy-ensured (not eager) to preserve the surfaces suite's single-eager-effect stub invariant.

## Dependencies

- **Blocks:** [bob-cli-4p.2](bob-cli-4p.2.md) ◐ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4p.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4p.1/README.md) | [bob-cli-4p.1](bob-cli-4p.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c2aec57`](https://github.com/bobs-org/bob-cli/commit/c2aec5703ce28e437881b1ce4633e9a8e706e5c0) | docs(projects): add Priority marks contract with conformance vectors | [bob-cli-4p.1](bob-cli-4p.1.md) | 2026-10-06 14:09:27 EDT |
