# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.1 — Keep explicit non-default ports in URL dedupe keys and display URLs

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.1` · **Size:** small
**Created:** 2026-10-25 10:04:06 EDT · **Closed:** 2026-10-25 10:14:55 EDT
**Plan:** [202610/backlog\_batch10\_port\_help\_doctor\_mermaid\_startpending.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch10_port_help_doctor_mermaid_startpending.md)

## Description

port-dedupe-ports: resolve bob-cli-c3 by keeping url.port() in dedupe_key_for and display_url with unit tests for non-default, spelled-out default, and absent ports.

## Notes

[2026-10-25T14:14:47Z · bob-cli-an.6.6.6.5.6.5.5.6.6.1] Baseline: dead `Some(port) != url.port_or_known_default()` comparison in `dedupe_key_for` (clip_url.rs:90) and `display_url` (intent.rs:119); `port()` already strips scheme-default ports so the condition was never true. Key-shape check: all identity consumers (sources.rs scan, ref_library/identity.rs, intent.rs classify) recompute keys at read time via validate_and_clean/dedupe_key_for — no stored keys, no migration needed; spelled-out default ports still normalize identically on both sides. Fix: keep `if let Some(port) = url.port()` in both places. Tests: new `dedupe_key_keeps_explicit_non_default_ports` (non-default kept, :443/:80 dropped, cross-port distinctness) and `display_keeps_explicit_non_default_ports` (display + classifier carry port); sibling bob-cli-7u spelling tests still green. Limitations: none known; target task bob-cli-c3 left open for the lander per working rules. just check: exit 0, 18 ok suites, 0 failures.

[2026-10-25T14:14:55Z · bob-cli-an.6.6.6.5.6.5.5.6.6.1] Fixed dead port comparison in dedupe_key_for and display_url to keep url.port(); new unit tests cover non-default/spelled-out-default/absent ports; just check green (18 suites ok, 0 failures); sibling 7u tests green; bob-cli-c3 left open for lander

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.1/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7e8ffed`](https://github.com/bobs-org/bob-cli/commit/7e8ffedd292dc901ba7d14f57fcd72a0b09a6bcf) | fix(url-routing): keep explicit non-default ports in dedupe and display URLs | [bob-cli-an.6.6.6.5.6.5.5.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.1.md) | 2026-10-25 10:16:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.1][1] | check full description notes decisions | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.1/README.md

<!-- sase:referenced-by:end -->
