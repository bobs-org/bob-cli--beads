# Bead: bob-cli-k7.2 — Umbrella rule and \`\_generated/\` fix in the Obsidian cycler

[Bead Pages](../README.md) / [bob-cli-k7](README.md) / bob-cli-k7.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1b8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1b8.md) · **Assignee:** `bob-cli-k7.2` · **Size:** small
**Created:** 2026-11-11 07:57:57 EST · **Closed:** 2026-11-11 08:57:46 EST
**Plan:** [202611/keep\_moving\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/keep_moving_link_marks.md)

## Description

umbrella-cycler: in the bob-plugins task-status-cycler, apply the umbrella rule in successorLeafProject using the planner's held note text, stop generated tag pages from making parent stems ambiguous, update LP/KM tests and docs, build, and sync.

## Notes

[2026-11-11T13:57:34Z · bob-cli-k7.2] PROPOSED FOLLOW-UP: docs:check lint fails on clean base too — 6 word-budget errors in untouched files (reference/json-outputs, mac-capture x4, navigation-hotkeys); needs budget raise or trims

[2026-11-11T13:57:46Z · bob-cli-k7.2] Umbrella rule + _generated fix in task-status-cycler (1.49.0, synced to vault). successorLeafProject now takes held note text: no marker line => leaf with no walk; marker => old R2 walk decides; missing text => neutral false. ResolveParent ignores _generated via projectParentPathIsIndexed. LeafProject wired with text at both plan call sites and planner. Tests: LP1-LP17 incl LP16 _generated case, KM6 umbrella end-to-end (no offer), KM33 screenshot project (4 Next rows), LP16 planner parity — 20/20 keep-moving, 251/251 across cycler+successor+pull-in+nav suites. Docs paragraph + description updated, version 1.49.0. docs:check lint fails identically on clean base (6 pre-existing word-budget errors, noted as follow-up).

## Dependencies

- **Depends on:** [bob-cli-k7.1](bob-cli-k7.1.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-k7.4](bob-cli-k7.4.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k7.2/README.md) | [bob-cli-k7.2](bob-cli-k7.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@87b28e1`](https://github.com/bobs-org/bob-plugins/commit/87b28e1a60ee4aceca1f9f7094ffe06129b81485) | feat(task-status-cycler): skip only umbrella projects, stop \_generated ambiguity | [bob-cli-k7.2](bob-cli-k7.2.md) | 2026-11-11 08:58:31 EST |
