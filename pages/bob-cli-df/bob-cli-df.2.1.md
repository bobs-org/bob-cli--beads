# Bead: bob-cli-df.2.1 — Quarantine artifact-link collisions and keep unrelated writes available

[Bead Pages](../README.md) / [bob-cli-df.2](bob-cli-df.2.md) / bob-cli-df.2.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.2.md) · **Assignee:** `bob-cli-df.2.1.land`
**Created:** 2026-10-27 21:43:18 EDT
**Plan:** [202610/artifact\_link\_collision\_quarantine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_collision_quarantine.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/artifact_link_collision_quarantine.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/artifact_link_collision_quarantine.md

<!-- sase:links:end -->

## Description

Preserve the earliest durable artifact-link payload, retain conflicting replays as visible quarantine evidence, and allow unrelated reads, writes, and outbox publication to complete.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.2.1.land/README.md) | [bob-cli-df.2.1](bob-cli-df.2.1.md) | 0 |
