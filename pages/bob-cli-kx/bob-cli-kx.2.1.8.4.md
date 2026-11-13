# Bead: bob-cli-kx.2.1.8.4 — Reports, help, docs, and final verification

[Bead Pages](../README.md) / [bob-cli-kx.2.1.8](bob-cli-kx.2.1.8.md) / bob-cli-kx.2.1.8.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.1.land.md) · **Assignee:** `bob-cli-kx.2.1.8.4` · **Size:** medium
**Created:** 2026-11-12 23:51:16 EST · **Closed:** 2026-11-13 06:46:20 EST
**Plan:** [202611/gmail\_archive\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_landing_repairs.md)

## Description

surfaces: Fix quiet digest leaks, hollow kept/let-go rows, and paused row detail; rewrite remaining read-only claims in help and docs; document the journal schema, vocabulary, and exit codes; refresh the C1-C20 table; run the docs and full gates. Implement section 4.

## Notes

[2026-11-13T11:46:00Z · bob-cli-kx.2.1.8.4] PROPOSED FOLLOW-UP: docs-check offline lychee reports File not found for target/docs/reference/mac-capture/event-notes (single broken link, mac-capture mount infra); reproduces identically on clean base plus only the environment_ignore fix, so unrelated to this phase

[2026-11-13T11:46:20Z · bob-cli-kx.2.1.8.4] Section 4 surfaces done: digest kept only for dry-run/paused (human+JSON), live kept/let-go rows filled with note/sorted messages/tasks and no dangling arrow, paused rows carry gate reason plus decision shown in human output, -n serializes archive_skipped, doctor shows missing-modify hint alongside journal warnings, help/docs rewritten with journal schema/vocabulary/exit codes and refreshed C1-C20 table. Verified: report unit tests (22 pass incl 5 new surfaces tests), gmail_archive_apply (25), gmail_archive_preview (4), gmail_transport (4), gmail_sync (41), gmail_shell (69), just lint, cargo fmt, just docs-gen, docs-check lint green. just check lib has only the two plan-listed known failures (gcal sync_args owned bob-cli-l2, subprocess_runner flake owned bob-cli-kl); docs-check lychee mac-capture/event-notes failure proven identical on clean base (recorded as PROPOSED FOLLOW-UP).

## Dependencies

- **Depends on:** [bob-cli-kx.2.1.8.3](bob-cli-kx.2.1.8.3.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2.1.8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.8.4/README.md) | [bob-cli-kx.2.1.8.4](bob-cli-kx.2.1.8.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a8dd820`](https://github.com/bobs-org/bob-cli/commit/a8dd82047ee1ca2ea15d5747ab168dc57447198e) | feat(gmail)!: archive surfaces reports help docs and verification \[bob-cli-kx.2.1.8.4\] | [bob-cli-kx.2.1.8.4](bob-cli-kx.2.1.8.4.md) | 2026-11-13 06:49:00 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.8.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.8.4/README.md

<!-- sase:referenced-by:end -->
