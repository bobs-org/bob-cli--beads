# Bead: bob-cli-52.3 — URL-intent classifier, routing policy, and offline library verdict

[Bead Pages](../README.md) / [bob-cli-52](README.md) / bob-cli-52.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.3` · **Size:** small
**Created:** 2026-10-07 08:11:17 EDT · **Closed:** 2026-10-07 09:02:26 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

intent: a new `url_routing` module with the strict bare-URL classifier, display formatting, the `highlights.url_routing` config policy (per-entry-point toggles and `exclude_hosts`), an offline library verdict that agrees exactly with create's dedupe, and a doctor routing row.

## Notes

[2026-10-07T12:59:32Z · bob-cli-52.3] PROPOSED FOLLOW-UP: lib test native::completion::kinds::tests::every_value_arg_has_a_decision fails identically on clean base (ref create:audio missing kinds decision)

[2026-10-07T12:59:37Z · bob-cli-52.3] PROPOSED FOLLOW-UP: lib test native::highlights_ref::create::tests::listen_filter_renders_card_and_encoded_play_link fails identically on clean base

[2026-10-07T12:59:41Z · bob-cli-52.3] PROPOSED FOLLOW-UP: cli test highlights::create::ingest_characterizes_url_failure_modes fails identically on clean base

[2026-10-07T13:02:26Z · bob-cli-52.3] Closed by explicit `sase stitch create -B close` after create_commit landed df9d504 ("feat(url-routing): add intent classifier, routing policy, and offline library verdict"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-52.3` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-52.4](bob-cli-52.4.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.5](bob-cli-52.5.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.6](bob-cli-52.6.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.3/README.md) | [bob-cli-52.3](bob-cli-52.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`df9d504`](https://github.com/bobs-org/bob-cli/commit/df9d504fb937a9ba80bf7ec51f6d8ead285fac62) | feat(url-routing): add intent classifier, routing policy, and offline library verdict | [bob-cli-52.3](bob-cli-52.3.md) | 2026-10-07 09:01:44 EDT |
