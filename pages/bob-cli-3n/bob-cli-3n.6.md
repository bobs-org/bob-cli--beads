# Bead: bob-cli-3n.6 — Navigation-hotkeys dependency model, single-transaction writer, and api v1

[Bead Pages](../README.md) / [bob-cli-3n](README.md) / bob-cli-3n.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vl.md) · **Assignee:** `bob-cli-3n.6` · **Size:** medium
**Created:** 2026-10-02 16:54:35 EDT · **Closed:** 2026-10-02 20:15:46 EDT
**Plan:** [202610/task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links.md)

## Description

nav-model: add the Depends-On grammar and pure planner, a writer that prepares targets and then commits the parent in one transaction (status effects, commitment transfer, immediate recovery on removal, legacy fold), switch the existing picker paths and recovery edges to it, and add api v1.

## Notes

[2026-10-03T00:15:46Z · bob-cli-3n.6] nav-model done in bob-plugins workspace: contract Depends-On grammar (parse verdicts, canonical writer form), pure planDependencyEdit (line/field/target-ids/status/ADJ-8 recovery/notices), single-transaction writer (preparations first, one commit), picker/batch/counted rewired, recovery edges = line links + field-gated R8 legacy (no #^ref edges), frozen api v1. Verified: npm test 1262/1262 pass (incl. new test-navigation-dependencies.cjs 26 tests over DP/DW vectors, planner, one-undo-group, failed-prep-untouched, api), npm run validate 6/6, manifest 1.53.0, README row updated, bob plugins sync deployed (vault main.js in sync). No epic-symbol leftovers. Changes uncommitted in linked bob-plugins checkout; canonical ~/projects checkout still shows 1.52.0/drift.

## Dependencies

- **Depends on:** [bob-cli-3n.1](bob-cli-3n.1.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3n.4](bob-cli-3n.4.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3n.5](bob-cli-3n.5.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3n.7](bob-cli-3n.7.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.6/README.md) | [bob-cli-3n.6](bob-cli-3n.6.md) | 0 |
