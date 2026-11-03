# Bead: bob-cli-gh.2 — Period calendar, scaffolds, note parser, and bob periods ensure/list

[Bead Pages](../README.md) / [bob-cli-gh](README.md) / bob-cli-gh.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.34.linker.w0` · **Assignee:** `bob-cli-gh.2` · **Size:** medium
**Created:** 2026-11-03 10:55:43 EST · **Closed:** 2026-11-03 11:58:24 EST
**Plan:** [202611/period\_notes\_and\_stats\_strips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_notes_and_stats_strips.md)

## Description

core: a new `periods` module in bob-cli with the ISO period calendar, ids, paths, labels, the four deterministic scaffolds (with v1 agent callouts), the note-anatomy parser and review-state machine, create-only `bob periods ensure` with one-week look-ahead, a basic `bob periods list`, CLI wiring, and the first `docs/periods.md`.

## Notes

[2026-11-03T16:58:24Z · bob-cli-gh.2] Core phase done: periods module (calendar/labels/scaffold/instructions/note/ensure/list/cli), bob periods ensure/list wired in Vault group, docs/periods.md + nav + CLI reference, moment fixture (7174 rows) + 7 scaffold goldens. Verified: cargo fmt clean, cargo clippy gate clean, full cargo test --workspace clean (4700+ lib, 2930+ cli), just docs-check clean (447 passed). days_table=yes honored (weekly scaffold keeps ## Days).

## Dependencies

- **Blocks:** [bob-cli-gh.3](bob-cli-gh.3.md) ◐ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gh.4](bob-cli-gh.4.md) ◐ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gh.6](bob-cli-gh.6.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gh.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gh.2/README.md) | [bob-cli-gh.2](bob-cli-gh.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`020a1f6`](https://github.com/bobs-org/bob-cli/commit/020a1f6da021513bc60abdcbda7a4d9ab606fb90) | feat(periods): add ISO period calendar, scaffolds, parser, ensure/list | [bob-cli-gh.2](bob-cli-gh.2.md) | 2026-11-03 11:59:22 EST |
