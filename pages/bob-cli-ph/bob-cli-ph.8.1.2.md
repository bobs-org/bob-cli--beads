# Bead: bob-cli-ph.8.1.2 — Tray and verbatim title on annotated preview drawer headers

[Bead Pages](../README.md) / [bob-cli-ph.8.1](bob-cli-ph.8.1.md) / bob-cli-ph.8.1.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.2` · **Size:** medium
**Created:** 2026-11-25 20:56:00 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

## Description

preview-tray: BlockDiffCard renders a Bob-annotated drawer header as SF Symbol tray plus the semibold verbatim title, muted when empty, with accessible labels and light/dark/increased-contrast render fixtures.

## Notes

[2026-11-26T04:34:37Z · bob-cli-ph.8.1.2--1] Gate diagnosis: mac typecheck failed for real — DrawerHeaderDesignTests.testRenderDrawerHeaders called throwing edgeRows() inside the VStack ViewBuilder (error at line 59) which cascaded to a key-path inference error at line 80. Fixed in c2dd7fbf by hoisting let edge = try edgeRows() above the builder; just typecheck-tests now PASS on all 4 macOS targets on rebased HEAD. Pre-existing script bug (not a product defect): /tmp/bob-cli-ph-8-1-2-gates.sh wraps the mac ssh in GNU timeout, which does not exist on macOS — reran those steps without timeout per AGENTS.md. Pushed c2dd7fbf (rebased onto b422fbdc draft-styling); docs-check passed in the gate run; macos-ci-check still to run.

## Dependencies

- **Depends on:** [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.2.md) | [bob-cli-ph.8.1.2](bob-cli-ph.8.1.2.md) | 0 |
