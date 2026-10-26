# Bead: bob-cli-ce.2 — bob \_\_catalog --protocol 1

[Bead Pages](../README.md) / [bob-cli-ce](README.md) / bob-cli-ce.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5c.linker.w0.md) · **Assignee:** `bob-cli-ce.2` · **Size:** medium
**Created:** 2026-10-26 10:35:52 EDT · **Closed:** 2026-10-26 11:11:31 EDT
**Plan:** [202610/bob\_colon\_command\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_colon_command_mode.md)

## Description

catalog: add the hidden, versioned JSON command catalog to bob-cli. A static table sits beside SUBCOMMANDS, positional args and about text come from the clap tree, coverage tests classify every public leaf, and a contract docs page documents it.

## Notes

[2026-10-26T15:11:31Z · bob-cli-ce.2] Verified hidden bob __catalog --protocol 1: 52 entries (pomodoro_actions=yes), coverage unit tests, CLI handshake tests (schema_version 1, --protocol=1, protocol 2 JSON exit 2, missing protocol usage exit 2, no ANSI, BOB_DIR missing + XDG untouched), contract page docs/command-catalog.md registered, just docs-check passed, just all passed. epic-symbols: no leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-ce.3](bob-cli-ce.3.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-ce.5](bob-cli-ce.5.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ce.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.2/README.md) | [bob-cli-ce.2](bob-cli-ce.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0bec19d`](https://github.com/bobs-org/bob-cli/commit/0bec19d89ec994ac957c22f024aeefc09eeb36f9) | feat(catalog): add hidden bob \_\_catalog --protocol 1 handshake | [bob-cli-ce.2](bob-cli-ce.2.md) | 2026-10-26 11:12:33 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ce.2][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.2/README.md

<!-- sase:referenced-by:end -->
