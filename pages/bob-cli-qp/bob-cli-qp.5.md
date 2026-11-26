# Bead: bob-cli-qp.5 — Reading-state readouts from the shared snapshot

[Bead Pages](../README.md) / [bob-cli-qp](README.md) / bob-cli-qp.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6l.linker.w0.md) · **Assignee:** `bob-cli-qp.5` · **Size:** medium
**Created:** 2026-11-26 14:22:08 EST · **Closed:** 2026-11-26 16:15:33 EST
**Plan:** [202611/ref\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_cards.md)

## Description

ref-readouts: subscribe cards to the shared snapshot. Patch the lane chip, Today pill, annotations, reread lineage, identifiers, and diagnostics into existing rows with no layout shift. Spy tests prove there are no spawns.

## Notes

[2026-11-26T21:15:11Z · bob-cli-qp.5] PROPOSED FOLLOW-UP: test-ledger-tools-frees-marks.cjs 25ms CPU budget flaked once under the full suite (26.7ms) and passes isolated on both this tree and the clean base; looks environmental, unrelated to ref readouts.

[2026-11-26T21:15:33Z · bob-cli-qp.5] ref-readouts done: 249u filled (lane chip for every status incl. snoozed/conflict/legacy, priority glyph + TODAY pill on open lanes, vN with earlier[] tooltip, arXiv/DOI copy chips, annotation counts with Highlights jump, foot lint with diagnostics + missing-PDF drop, read tone, per-path subscribe/unsubscribe); host paints + digest in signature; 16-test suite green; build, build:check, docs:check, inventory, perf green; full unit green except one environmental frees-marks CPU-budget flake (passes isolated, recorded as follow-up). No memory edits. Vault sync refused by sibling ws-10 in-progress deploy (no -F per repo rules); deploy pending for land/go-live.

## Dependencies

- **Depends on:** [bob-cli-qp.3](bob-cli-qp.3.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qp.4](bob-cli-qp.4.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qp.7](bob-cli-qp.7.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qp.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qp.5/README.md) | [bob-cli-qp.5](bob-cli-qp.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@0d8ccd6`](https://github.com/bobs-org/bob-plugins/commit/0d8ccd662ba098449af1ec39907da7bd35e037ee) | feat(ref-card): add reading-state readouts to ref note cards | [bob-cli-qp.5](bob-cli-qp.5.md) | 2026-11-26 16:16:35 EST |
