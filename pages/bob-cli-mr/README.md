# Bead: bob-cli-mr — Backlog triage T1: bob-plugins red gates, closed-prerequisite reopen, highlights-scan lock window

[Bead Pages](../README.md) / bob-cli-mr

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1dh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1dh.md) · **Assignee:** `bob-cli-mr.land`
**Created:** 2026-11-17 11:16:43 EST
**Plan:** [202611/backlog\_triage\_t1\_red\_gates\_closed\_prereqs\_scan\_lock.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t1_red_gates_closed_prereqs_scan_lock.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/backlog_triage_t1_red_gates_closed_prereqs_scan_lock.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t1_red_gates_closed_prereqs_scan_lock.md

<!-- sase:links:end -->

## Description

bob-plugins npm test has no deterministic reds, capture never reopens a closed or archived prerequisite, a writing highlights scan holds bob_sync.lock only while it writes, and the lander chains the next five-bead triage epic until every open task bead is closed.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-mr.1](bob-cli-mr.1.md) | Fix the deterministic bob-plugins npm test reds | ✓ closed | medium | 2026-11-17 | 1 | 1 |
| [bob-cli-mr.2](bob-cli-mr.2.md) | Never promote closed or archived prerequisites | ✓ closed | medium | 2026-11-17 | 1 | 1 |
| [bob-cli-mr.3](bob-cli-mr.3.md) | Narrow the highlights-scan bob\_sync.lock window | ✓ closed | large | 2026-11-17 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-mr: Backlog triage T1: bob-plugins red gates, closed-prerequisite reopen, highlights-scan lock window [in_progress]"]
    n1["bob-cli-mr.1: Fix the deterministic bob-plugins npm test reds [closed]"]
    n2["bob-cli-mr.2: Never promote closed or archived prerequisites [closed]"]
    n3["bob-cli-mr.3: Narrow the highlights-scan bob_sync.lock window [closed]"]
    n4["bob-cli-mr.3.1: Narrow the full highlights scan lock window [closed]"]
    n5["bob-cli-mr.3.1.1: Share full-scan planning and capture validation inputs [closed]"]
    n6["bob-cli-mr.3.1.2: Apply prepared scans inside a bounded mutation window [closed]"]
    n7["bob-cli-mr.3.1.3: Prove scan interleavings and document the new lock window [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n3 --> n4
    n4 --> n5
    n4 --> n6
    n4 --> n7
    n1 -.-> n2
    n2 -.-> n3
    n5 -.-> n6
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mr.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mr.1/README.md) | [bob-cli-mr.1](bob-cli-mr.1.md) | 1 |
| [bbugyi200.athena.bob-cli-mr.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.2.md) | [bob-cli-mr.2](bob-cli-mr.2.md) | 1 |
| [bbugyi200.athena.bob-cli-mr.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.md) | [bob-cli-mr.3](bob-cli-mr.3.md) | 0 |
| [bbugyi200.athena.bob-cli-mr.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mr.3.1.1/README.md) | [bob-cli-mr.3.1.1](bob-cli-mr.3.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-mr.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.1.2.md) | [bob-cli-mr.3.1.2](bob-cli-mr.3.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-mr.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.1.3.md) | [bob-cli-mr.3.1.3](bob-cli-mr.3.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-mr.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.1.land.md) | [bob-cli-mr.3.1](bob-cli-mr.3.1.md) | 2 |
| [bbugyi200.athena.bob-cli-mr.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mr.land/README.md) | [bob-cli-mr](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b0a9c89`](https://github.com/bobs-org/bob-plugins/commit/b0a9c89d9f38a6219ef126c3d2a6719e86f572ea) | fix(navigation): clear deterministic npm test reds for walkMode guards, Platform shadowing, and block-marks dates | [bob-cli-mr.1](bob-cli-mr.1.md) | 2026-11-17 11:29:56 EST |
| bob-cli | [`b0bddbb`](https://github.com/bobs-org/bob-cli/commit/b0bddbb98247331181bd0c9f6aa3ed07e6f6541e) | fix(capture): never promote closed or archived prerequisites | [bob-cli-mr.2](bob-cli-mr.2.md) | 2026-11-17 12:04:33 EST |
| bob-cli | [`1e8f77a`](https://github.com/bobs-org/bob-cli/commit/1e8f77af0541ab29fdec657e9139a0c95a10f597) | feat(scan): share prepared full-scan planning and validation inputs | [bob-cli-mr.3.1.1](bob-cli-mr.3.1.1.md) | 2026-11-17 12:59:58 EST |
| bob-cli | [`3236cee`](https://github.com/bobs-org/bob-cli/commit/3236ceefaa690c2c9aa8d935db0de7b1a2c11ce1) | feat(scan): apply prepared full scans inside a bounded lock window | [bob-cli-mr.3.1.2](bob-cli-mr.3.1.2.md) | 2026-11-17 14:53:36 EST |
| bob-cli | [`6c409ab`](https://github.com/bobs-org/bob-cli/commit/6c409ab287f79994ac5fc257c0d47f9fc4ed273c) | test(ref): prove narrow scan lock-window interleavings | [bob-cli-mr.3.1.3](bob-cli-mr.3.1.3.md) | 2026-11-17 15:56:23 EST |
| bob-cli | [`0e83df4`](https://github.com/bobs-org/bob-cli/commit/0e83df4cd5797841998afffe227b14052c01f2d7) | feat(scan): finish highlights scan lock-window landing repairs | [bob-cli-mr.3.1](bob-cli-mr.3.1.md) | 2026-11-17 17:23:08 EST |
| bob-mac-capture | [`bob-mac-capture@bfbedda`](https://github.com/bobs-org/bob-mac-capture/commit/bfbedda918ab3884fcba3b16a6206437f3b913fa) | docs(refs): correct last-scan receipt wording for narrow lock window | [bob-cli-mr.3.1](bob-cli-mr.3.1.md) | 2026-11-17 17:23:46 EST |
