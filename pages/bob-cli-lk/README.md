# Bead: bob-cli-lk — Fix Gmail archiving: follow merges, reopen on replies, stable confirm digests

[Bead Pages](../README.md) / bob-cli-lk

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e1.md) · **Assignee:** `bob-cli-lk.land`
**Created:** 2026-11-14 11:42:09 EST
**Plan:** [202611/gmail\_archive\_merge\_and\_reply\_reopen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_merge_and_reply_reopen.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_archive_merge_and_reply_reopen.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_merge_and_reply_reopen.md

<!-- sase:links:end -->

## Description

No bob-labelled thread sits in the Inbox unexplained. A merge-retired linker follows its resolved target's status. Any hold that remains is shown as a review row and a doctor count. A reply after close reopens the task and links the reply. A pending -c confirmation survives edits that only shift lines.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-lk.1](bob-cli-lk.1.md) | Follow merge edges and surface remaining holds | ✓ closed | medium | 2026-11-14 | 1 | 1 |
| [bob-cli-lk.2](bob-cli-lk.2.md) | Line-shift-proof archive confirmation identity | ✓ closed | small | 2026-11-14 | 1 | 1 |
| [bob-cli-lk.3](bob-cli-lk.3.md) | Reopen closed Gmail Tasks when a reply arrives | ◐ in_progress | large | 2026-11-14 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-lk: Fix Gmail archiving: follow merges, reopen on replies, stable confirm digests [in_progress]"]
    n1["bob-cli-lk.1: Follow merge edges and surface remaining holds [closed]"]
    n2["bob-cli-lk.2: Line-shift-proof archive confirmation identity [closed]"]
    n3["bob-cli-lk.3: Reopen closed Gmail Tasks when a reply arrives [in_progress]"]
    n4["bob-cli-lk.3.1: Reopen closed Gmail Tasks on counted replies [in_progress]"]
    n5["bob-cli-lk.3.1.1: Prepare closed-thread replies and resumable activity cursors [closed]"]
    n6["bob-cli-lk.3.1.2: Plan task reopening, restore, and the exact-message log [in_progress]"]
    n7["bob-cli-lk.3.1.3: Integrate reply reopening with sync durability and archiving [in_progress]"]
    n8["bob-cli-lk.3.1.4: Finish reply-reopen reports, documentation, and regression coverage [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n3 --> n4
    n4 --> n5
    n4 --> n6
    n4 --> n7
    n4 --> n8
    n1 -.-> n2
    n1 -.-> n3
    n5 -.-> n6
    n5 -.-> n7
    n6 -.-> n7
    n7 -.-> n8
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lk.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.1/README.md) | [bob-cli-lk.1](bob-cli-lk.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-lk.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.2/README.md) | [bob-cli-lk.2](bob-cli-lk.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-lk.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.md) | [bob-cli-lk.3](bob-cli-lk.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-lk.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.1.1.md) | [bob-cli-lk.3.1.1](bob-cli-lk.3.1.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-lk.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.3.1.2/README.md) | [bob-cli-lk.3.1.2](bob-cli-lk.3.1.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-lk.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.3.1.3/README.md) | [bob-cli-lk.3.1.3](bob-cli-lk.3.1.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-lk.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.3.1.4/README.md) | [bob-cli-lk.3.1.4](bob-cli-lk.3.1.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-lk.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.3.1.land/README.md) | [bob-cli-lk.3.1](bob-cli-lk.3.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-lk.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lk.land/README.md) | [bob-cli-lk](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`47fac4b`](https://github.com/bobs-org/bob-cli/commit/47fac4b0ff0fe82fb1396e949d217fc8e2b3af2f) | feat(gmail): follow merge edges and surface remaining archive holds | [bob-cli-lk.1](bob-cli-lk.1.md) | 2026-11-14 13:35:49 EST |
| bob-cli | [`7ffc825`](https://github.com/bobs-org/bob-cli/commit/7ffc8251782f87288e97421fd3b63058e5332f91) | fix(gmail): make archive confirmation line-shift proof | [bob-cli-lk.2](bob-cli-lk.2.md) | 2026-11-14 14:22:23 EST |
| bob-cli | [`b112a61`](https://github.com/bobs-org/bob-cli/commit/b112a61805a529fa8e69ba0a86cd9114b10ccc49) | feat(gmail): prepare closed-thread replies with resumable activity cursors | [bob-cli-lk.3.1.1](bob-cli-lk.3.1.1.md) | 2026-11-14 15:05:13 EST |
