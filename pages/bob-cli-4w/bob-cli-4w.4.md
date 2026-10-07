# Bead: bob-cli-4w.4 — bob ref find and the library CLI plumbing

[Bead Pages](../README.md) / [bob-cli-4w](README.md) / bob-cli-4w.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.4` · **Size:** medium
**Created:** 2026-10-06 20:15:52 EDT · **Closed:** 2026-10-06 22:15:00 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

find: add the Library help group, shared output plumbing and JSON envelope, `docs/ref.md`, and batch identity lookup with verdicts, optional intake checks, and human, Markdown, and JSON output.

## Notes

[2026-10-07T02:14:52Z · bob-cli-4w.4] PROPOSED FOLLOW-UP: lib tests completion::kinds every_value_arg_has_a_decision (ref create:audio) and highlights_ref::create listen_filter_renders_card fail identically on the clean base tree (known bob-cli-4j/4u/40 failures); find phase leaves them alone

[2026-10-07T02:15:00Z · bob-cli-4w.4] bob ref find ships: Library help group, shared output plumbing (REF_SCHEMA_VERSION=1 envelope, chips, markdown), docs/ref.md, batch lookup with in_library/in_intake/possible/not_found verdicts in human/Markdown/JSON. Verified: 20 new find CLI tests + 2 output unit tests pass; full cli suite 1067 green; fmt+clippy clean with no new warnings; 2 lib failures reproduce identically on base (recorded as follow-up). No epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-4w.1](bob-cli-4w.1.md) ✓ · ⧖ 2026-10-06
- **Depends on:** [bob-cli-4w.3](bob-cli-4w.3.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.5](bob-cli-4w.5.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.4/README.md) | [bob-cli-4w.4](bob-cli-4w.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`87498c7`](https://github.com/bobs-org/bob-cli/commit/87498c7bd7b4da89e0a95c1a693e7aa209d4463c) | feat(ref-library): add bob ref find library-membership verdicts | [bob-cli-4w.4](bob-cli-4w.4.md) | 2026-10-06 22:20:45 EDT |
