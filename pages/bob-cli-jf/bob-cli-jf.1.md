# Bead: bob-cli-jf.1 — Restore bob-mac-capture master and stop linked clones from mutating their host repo

[Bead Pages](../README.md) / [bob-cli-jf](README.md) / bob-cli-jf.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-jf](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-jf.md) · **Assignee:** `bob-cli-jf.1.land`
**Created:** 2026-11-10 06:47:59 EST
**Plan:** [202611/bob\_mac\_capture\_history\_restore.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_mac_capture_history_restore.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bob_mac_capture_history_restore.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_mac_capture_history_restore.md

<!-- sase:links:end -->

## Description

bobs-org/bob-mac-capture master again holds only Mac history (29147289 plus the genuine Mac commits pushed since), no checkout on athena, apollo, or the Mac still carries the bob-cli history that was pushed onto it, `just docs-check` passes again, and SASE can no longer rewrite or push a host checkout when a linked or sidecar path has no Git directory of its own.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-jf.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-jf.1.land/README.md) | [bob-cli-jf.1](bob-cli-jf.1.md) | 0 |
