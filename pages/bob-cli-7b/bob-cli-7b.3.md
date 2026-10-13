# Bead: bob-cli-7b.3 — Bob Mac Capture presents dropped and refused prerequisites

[Bead Pages](../README.md) / [bob-cli-7b](README.md) / bob-cli-7b.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7c.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7c.w0.md) · **Assignee:** `bob-cli-7b.3` · **Size:** medium
**Created:** 2026-10-13 08:12:08 EDT · **Closed:** 2026-10-13 09:49:03 EDT
**Plan:** [202610/capture\_link\_drops\_blocking\_deps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_link_drops_blocking_deps.md)

## Description

mac: decode `dropped_dependencies` and `link_guard`, add the dropped-dependency chip to the link, toggle, Ensure Next, and close presentations, and (per mac_guard_detail) render bob's not-linked sentence; verify through macOS CI.

## Notes

[2026-10-13T13:48:41Z · bob-cli-7b.3] Manual check for Bryan: type ^job:blocked (or @job:blocked) on a task Blocked by one open prerequisite; the live preview should show the dropped-dependency chip and Return should drop then link.

[2026-10-13T13:49:03Z · bob-cli-7b.3] Decoded dropped_dependencies and link_guard (drop_refused) additively; chips on link/toggle/Ensure Next/close; CaptureLinkGuardPresentation for kind link_guard and task_toggle without toggle_direction (mac_guard_detail=yes). Fixtures generated from workspace bob capture --dry-run -f json (cli-core). Linux has no Swift toolchain so just format-lint/build/test were not run here; macOS CI must cover them. Manual check recorded: ^job:blocked on a one-prereq Blocked task should preview the chip and link on Return. epic-symbols: none leftover. Memory left to publish (bob-cli-7b.4).

## Dependencies

- **Depends on:** [bob-cli-7b.1](bob-cli-7b.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7b.4](bob-cli-7b.4.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7b.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.3/README.md) | [bob-cli-7b.3](bob-cli-7b.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7b.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.3/README.md

<!-- sase:referenced-by:end -->
