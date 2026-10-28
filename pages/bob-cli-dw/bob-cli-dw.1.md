# Bead: bob-cli-dw.1 — Expose RecoveryAssessment for failed-close snapshot imports

[Bead Pages](../README.md) / [bob-cli-dw](README.md) / bob-cli-dw.1

**Status:** ○ open · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-dp.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dp.land.md) · **Assignee:** `bob-cli-dw.1` · **Size:** small
**Created:** 2026-10-28 15:35:24 EDT
**Plan:** [202610/backlog\_batch\_b6.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b6.md)

## Description

recovery-assessment-public: resolve bob-cli-dt in sase by exposing the shared failed-close assessment type through a public name and updating _failed_close_recovery_snapshots.py (and any other consumers) to import that public name. Do not suppress, whitelist, or pragma the private _RecoveryAssessment misuse. Read SASE symvision policy first. Verify with focused failed-close snapshot/recovery tests plus sase tool run check in the opened sase checkout. Independent clean witness 13ea2a464abef73b3eab4bfee9e624d7 already makes this KNOWN; later checks including 5d1634e22bc172fe358db97b9279961f still report it.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dw.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dw.1/README.md) | [bob-cli-dw.1](bob-cli-dw.1.md) | 0 |
