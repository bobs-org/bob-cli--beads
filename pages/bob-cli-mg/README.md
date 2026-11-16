# Bead: bob-cli-mg — Period closing balance for WF Checking on period notes

[Bead Pages](../README.md) / bob-cli-mg

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.50.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.50.linker.w0.md) · **Assignee:** `bob-cli-mg.land`
**Created:** 2026-11-16 15:40:33 EST
**Plan:** [202611/wf\_checking\_period\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/wf_checking_period_close.md)

## Description

Every week, quarter, ISO-year, and all-time note shows the checking account's exact posted balance at the end of that period (or, honestly labeled, as of the last imported day). bob computes the balance live from bank evidence, and it is never written into notes. Daily notes stay untouched.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-mg.1](bob-cli-mg.1.md) | Historical balance resolver and check findings | ✓ closed | medium | 2026-11-16 | 1 | 1 |
| [bob-cli-mg.2](bob-cli-mg.2.md) | balances\[\] in bob bank report, human line, and docs | ◐ in_progress | small | 2026-11-16 | 1 | 0 |
| [bob-cli-mg.3](bob-cli-mg.3.md) | Bank Charts header balance readout in bob-ledger-tools | ◐ in_progress | medium | 2026-11-16 | 1 | 0 |
| [bob-cli-mg.4](bob-cli-mg.4.md) | Bank Closing vocabulary and decision record | ◐ in_progress | small | 2026-11-16 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-mg: Period closing balance for WF Checking on period notes [in_progress]"]
    n1["bob-cli-mg.1: Historical balance resolver and check findings [closed]"]
    n2["bob-cli-mg.2: balances[] in bob bank report, human line, and docs [in_progress]"]
    n3["bob-cli-mg.3: Bank Charts header balance readout in bob-ledger-tools [in_progress]"]
    n4["bob-cli-mg.4: Bank Closing vocabulary and decision record [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mg.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mg.1/README.md) | [bob-cli-mg.1](bob-cli-mg.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-mg.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mg.2/README.md) | [bob-cli-mg.2](bob-cli-mg.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-mg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mg.3/README.md) | [bob-cli-mg.3](bob-cli-mg.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-mg.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mg.4/README.md) | [bob-cli-mg.4](bob-cli-mg.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-mg.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mg.land/README.md) | [bob-cli-mg](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e49dbd4`](https://github.com/bobs-org/bob-cli/commit/e49dbd465daac7888ff45eb00e2f4e00c1beed6e) | feat(bank): add historical posted-balance resolver and check findings | [bob-cli-mg.1](bob-cli-mg.1.md) | 2026-11-16 16:34:25 EST |
