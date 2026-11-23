# Bead: bob-cli-pf.2.1.3 — Guarded props commands, capability, completion, and contract

[Bead Pages](../README.md) / [bob-cli-pf.2.1](bob-cli-pf.2.1.md) / bob-cli-pf.2.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.md) · **Assignee:** `bob-cli-pf.2.1.3` · **Size:** medium
**Created:** 2026-11-22 14:47:18 EST · **Closed:** 2026-11-22 20:38:06 EST
**Plan:** [202611/props\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/props_cli.md)

## Description

cli-integration: wire show and update into the CLI, lock and atomically apply fresh plans, register catalog and completion, document the protocol, and verify the complete command in isolated vaults.

## Notes

[2026-11-23T01:37:56Z · bob-cli-pf.2.1.3] PROPOSED FOLLOW-UP: parallel-run ETXTBSY flakes in fake-script harnesses — native::highlights_ref::spotify short_links_resolve_through_validated_redirects (lib) and gmail_transport permission_and_partial_thread_failures + fake_injects_a_reply (Text file busy, os error 26 on the fake curl/gog script) fail under full-suite load and pass in isolation; same family as the gcal_ack flake tracked on bob-cli-pf.2.1.2 note #2. Consider serializing fake-script setup or retrying ETXTBSY.

[2026-11-23T01:38:06Z · bob-cli-pf.2.1.3] cli-integration done: src/native/props/cli.rs implements bob props show/update (confined NOTE resolver, read-only show/dry-run, lock+replan+atomic apply, no git/sync); wired NativeCommand::PropsShow/Update, Vault group between periods and query, completion tree+kinds, catalog props-show row + props-update exclusion + props_v1 feature. tests/cli/props.rs: 12 tests green. docs/props.md + contracts.yml registration + docs-gen outputs. Gates: fmt clean, full clippy gate clean, docs-check 447 passed, lib 7946 passed, cli binary 4035 passed, other 33 binaries green (2 gmail_transport ETXTBSY flakes pass in isolation, recorded as follow-up).

## Dependencies

- **Depends on:** [bob-cli-pf.2.1.2](bob-cli-pf.2.1.2.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.2.1.3/README.md) | [bob-cli-pf.2.1.3](bob-cli-pf.2.1.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.2.1.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.2.1.3/README.md

<!-- sase:referenced-by:end -->
