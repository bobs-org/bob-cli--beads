# Bead: bob-cli-q8.8 — The ⌃B / ⌃⇧B / ⌃L chords, ↵ conversions, and the armed release

[Bead Pages](../README.md) / [bob-cli-q8](README.md) / bob-cli-q8.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6f.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6f.linker.w0.md) · **Assignee:** `bob-cli-q8.8` · **Size:** medium
**Created:** 2026-11-25 18:16:43 EST · **Closed:** 2026-11-26 00:47:10 EST
**Plan:** [202611/plain\_link\_dependency\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/plain_link_dependency_ties.md)

## Description

nav-tie-keys: wire the Ctrl chords and ↵ conversions in all four stages with strict modifier helpers. A ↵ release takes two presses. Batches and counted sessions refuse conversions, and the label stage guards its plain row. Add the footers and docs, then deploy with bob plugins sync.

## Notes

[2026-11-26T05:46:53Z · bob-cli-q8.8] PROPOSED FOLLOW-UP: full bob-plugins test:unit shows 27 failures that reproduce identically on the clean base at 2ba3315 (blocks/dependency stage views, DW20-22, PDL8-10, task-reqs/vectors fixture parity, vim/scaffold) — pre-existing/environmental under host load, unrelated to nav-tie-keys; needs triage as task bead(s)

[2026-11-26T05:47:10Z · bob-cli-q8.8] nav-tie-keys done: strict Ctrl modifiers (469 split, 470 under cap), 451 tie-chord fragment dispatched from 450, Enter conversions (Depends/Blocks one-press, Links/Linked-from two-press arm/disarm), counted/marked and in-batch refusals, label-stage plain-row guard, stage-flag leak fix, contextual footers in all four stages, new test-navigation-tie-chords.cjs (14 tests pass; tie suites 46/46), bob-cli + bob-plugins docs updated, build:check + both docs-checks green, bob plugins sync deployed (vault main.js verified). Full test:unit 27 failures reproduce identically on clean base at 2ba3315 — recorded as PROPOSED FOLLOW-UP. Glossary task-relation one-sentence rule added; memory_decision_record left untouched per decisions.

## Dependencies

- **Depends on:** [bob-cli-q8.7](bob-cli-q8.7.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.8/README.md) | [bob-cli-q8.8](bob-cli-q8.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`57adf61`](https://github.com/bobs-org/bob-cli/commit/57adf61701d1bb6baa1bf73fb0576249dbf4ac79) | docs(task-relation): plain-link exclusivity for dependency ties | [bob-cli-q8.8](bob-cli-q8.8.md) | 2026-11-26 00:48:33 EST |
