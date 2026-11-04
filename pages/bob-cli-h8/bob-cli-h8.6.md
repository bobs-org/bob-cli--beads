# Bead: bob-cli-h8.6 — Make the highlights overwrite tests timezone-independent

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.6` · **Size:** small
**Created:** 2026-11-04 16:39:09 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

highlights-tz-tests: the two highlights::overwrite_local failures (bob-cli-h6) assert a hardcoded -0400 offset, while CI stamps in UTC. Pin the zone for those bob subprocesses, sweep sibling assertions, and confirm the overwrite-refreshes-captured rule in docs. Then close h6 and the no-longer-reproducing bob-cli-fh.

## Dependencies

- **Blocks:** [bob-cli-h8.11](bob-cli-h8.11.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.6/README.md) | [bob-cli-h8.6](bob-cli-h8.6.md) | 0 |
