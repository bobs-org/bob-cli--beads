# Bead: bob-cli-3n.11 — Publish glossary, decision record, and final docs

[Bead Pages](../README.md) / [bob-cli-3n](README.md) / bob-cli-3n.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vl.md) · **Assignee:** `bob-cli-3n.11` · **Size:** small
**Created:** 2026-10-02 16:54:40 EDT · **Closed:** 2026-10-02 22:33:32 EDT
**Plan:** [202610/task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links.md)

## Description

publish: add glossary:task-dependency-link, amend glossary:task-link, add the Depends-On decision record and mark task-status-is-derived, republish memory, sweep docs for stale transclusion wording, and record follow-ups and Bryan's checklist.

## Notes

[2026-10-03T02:30:46Z · bob-cli-3n.11] PROPOSED FOLLOW-UP: remove R8 legacy-child reading in Rust and nav once hooks report legacy_dependency_children: 0 across a week of runs

[2026-10-03T02:30:50Z · bob-cli-3n.11] PROPOSED FOLLOW-UP: reverse Blocks stage for dependents (epic Q4 deferral)

[2026-10-03T02:30:53Z · bob-cli-3n.11] PROPOSED FOLLOW-UP: task-line mini-badge showing open/total dependency count

[2026-10-03T02:30:57Z · bob-cli-3n.11] PROPOSED FOLLOW-UP: v2 path codec for notes whose paths cannot encode as dependency ids (ADJ-9)

[2026-10-03T02:31:00Z · bob-cli-3n.11] PROPOSED FOLLOW-UP: bob-plugins still ships scripts/migrate-task-dependency-identities.mjs and its README Dependency identity migration section though nav-gestures was to delete the embed-emitting migration scripts

[2026-10-03T02:33:32Z · bob-cli-3n.11] Published glossary:task-dependency-link, amended glossary:task-link, added decision task-deps-are-depends-on-links and marked task-status-is-derived superseded-in-part by it; sase memory init regenerated (CLAUDE.md/AGENTS.md rosters list the new record and term); docs sweep fixed stale dependency wording in docs/plan.md and docs/freshness.md, bob-plugins README already describes the new contract; just all passes (fmt, clippy, cargo test green)

## Dependencies

- **Depends on:** [bob-cli-3n.10](bob-cli-3n.10.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.11/README.md) | [bob-cli-3n.11](bob-cli-3n.11.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f21e856`](https://github.com/bobs-org/bob-cli/commit/f21e856cae4893f482a9a8baeb0417b5ea1501d0) | docs(memory): publish task-deps-are-depends-on-links decision and glossary | [bob-cli-3n.11](bob-cli-3n.11.md) | 2026-10-02 22:35:21 EDT |
