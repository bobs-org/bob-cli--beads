# Bead: bob-cli-dw.5 — Stop claiming Cancel-row and reconcile apply the same canceled-link cleanup

[Bead Pages](../README.md) / [bob-cli-dw](README.md) / bob-cli-dw.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-dp.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dp.land.md) · **Assignee:** `bob-cli-dw.5` · **Size:** small
**Created:** 2026-10-28 15:35:24 EDT · **Closed:** 2026-10-28 15:46:44 EDT
**Plan:** [202610/backlog\_batch\_b6.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b6.md)

## Description

cancel-reconcile-docs: resolve bob-cli-dj in bob-cli docs/task-status-hooks.md Canceled Task References. Lines ~157-161 correctly describe reconcile deleting the complete list item (including struck forms, authored prose, and sibling links). Lines ~184-189 describe the Ctrl+Shift+P Cancel row using deferral-prune dedicated-bullet/token semantics, then falsely claim struck links are untouched either way and that reconcile re-derives the same cleanup. The nav implementation matches the Cancel-row paragraph; reconcile matches the complete-item paragraph, so reconcile can later delete a struck link or mixed-prose bullet the immediate cancel kept. Correct the parity claim to state both behaviors. Verify with docs-check / just check. Do not change cancel or reconcile code in this phase unless a doc-only fix is impossible to state accurately.

## Notes

[2026-10-28T19:46:44Z · bob-cli-dw.5] Verified docs/task-status-hooks.md Canceled Task References already states both behaviors (52bff016): Cancel-row/cancel-label uses dedicated-bullet/token prune and keeps struck links; reconcile deletes the complete list item including struck forms and mixed-prose bullets. Corrected the leftover 'same rule' claim in docs/projects.md Cancelling a task so reconcile is later healing, not the same cleanup. just docs-check passed (lint, build, links, search, tutorial, unit tests). No --epic-symbol leftovers. Did not change cancel or reconcile code.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dw.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dw.5.md) | [bob-cli-dw.5](bob-cli-dw.5.md) | 0 |
