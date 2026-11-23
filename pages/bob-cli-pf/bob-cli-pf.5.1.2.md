# Bead: bob-cli-pf.5.1.2 — Add guarded property rename and reorder

[Bead Pages](../README.md) / [bob-cli-pf.5.1](bob-cli-pf.5.1.md) / bob-cli-pf.5.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.5.md) · **Assignee:** `bob-cli-pf.5.1.2` · **Size:** medium
**Created:** 2026-11-23 12:39:51 EST · **Closed:** 2026-11-23 14:06:53 EST
**Plan:** [202611/property\_editor\_parity.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_parity.md)

## Description

rename-reorder: implement the inline rename stage and source-order moves with attached comments, stable focus, filter lockout, undo, and reduced-motion-aware feedback.

## Notes

[2026-11-23T19:06:26Z · bob-cli-pf.5.1.2] PROPOSED FOLLOW-UP: 298p filter input missing bob-text role — scripts/test-prose-field-roles.cjs fails at plugins/bob-ledger-tools/src/298p-plugin-property-editor-selection-filter.js:536 on clean HEAD 25d8fe61 (5.1.1 leftover); 298q rename input is annotated

[2026-11-23T19:06:34Z · bob-cli-pf.5.1.2] PROPOSED FOLLOW-UP: Full npm test still flakes tracked timing nodes bob-cli-km (event-link-times 95.0ms/25ms), bob-cli-io (frees-marks 102ms/25ms), and bob-cli-pg (taskLinks typed p95 12.00ms/12ms); isolated serial reruns pass (6.4ms, 20.1ms, 11.00ms)

[2026-11-23T19:06:53Z · bob-cli-pf.5.1.2] Landed r rename stage and Alt+J/K source-order prop.move in 298q (496 lines) wrapping 298p. 11/11 focused rename-reorder tests plus 68 related property-editor tests pass. npm run build, build:check, and docs:check pass. npm test: 9092 pass / 3 fail / 5 skip; test:perf 25 pass / 1 fail. Failures are clean-tree: 298p bob-text gap (5.1.1 leftover) and tracked flakes bob-cli-km, bob-cli-io, bob-cli-pg (all three pass isolated). bob plugins sync deployed bob-ledger-tools. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-pf.5.1.1](bob-cli-pf.5.1.1.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pf.5.1.3](bob-cli-pf.5.1.3.md) ◐ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.2/README.md) | [bob-cli-pf.5.1.2](bob-cli-pf.5.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@76565b6`](https://github.com/bobs-org/bob-plugins/commit/76565b6d71da6be7f6fb8313cbddcb8d986320bc) | feat(property-editor): add guarded rename and source-order reorder | [bob-cli-pf.5.1.2](bob-cli-pf.5.1.2.md) | 2026-11-23 14:08:54 EST |
