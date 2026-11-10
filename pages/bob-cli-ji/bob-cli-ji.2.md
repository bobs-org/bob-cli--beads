# Bead: bob-cli-ji.2 — bob gcal note command, event selection and read-only modes

[Bead Pages](../README.md) / [bob-cli-ji](README.md) / bob-cli-ji.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3z.linker.w0.md) · **Assignee:** `bob-cli-ji.2` · **Size:** medium
**Created:** 2026-11-10 05:59:46 EST · **Closed:** 2026-11-10 07:57:59 EST
**Plan:** [202611/private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/private_gcal_event_notes.md)

## Description

select: add the `bob gcal note` command skeleton and its option pre-pass. Select an event by title query across a 90-day window, `-D`, a pasted Google Calendar URL, or `-i`/`-C`. Add the TTY picker and the This event / All events scope prompt, widen the organizer fields, and add the list (`-l`, `-a`) and show modes with their JSON contract, help, and catalog row.

## Notes

[2026-11-10T12:57:49Z · bob-cli-ji.2] PROPOSED FOLLOW-UP: docs-check reference word budget over (json-outputs 6071 base words, plus mac-capture capture-previews/keyboard/protocol) fails identically on clean base tree; needs budget raise or reference page trims

[2026-11-10T12:57:59Z · bob-cli-ji.2] Implemented bob gcal note select phase: CLI skeleton with alphabetical options and pre-pass for -30/TEXT, 90-day selection with -D/URL/-i/-C, TTY picker and This/All scope prompt, organizer widening to displayName/email with JSON {name,self}, list (-l/-a) and show modes with human tables and schema_version 1 JSON (notes vs events, orphans, candidates, no text in listings). Added gcal-note catalog writes row, docs/gcal-notes.md Command+JSON, json-outputs row, completion kinds for calendar/event-id, and tests/gcal_note_cli.rs (10 tests). Verified: cargo fmt --check clean, cargo clippy unused clean, cargo test lib 6331 pass, gcal_note_cli/gcal_cli/gcal_list/gcal_notes all pass, just docs-gen clean. just docs-check fails identically on base (4 reference pages over 6000-word cap), recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-ji.1](bob-cli-ji.1.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.4](bob-cli-ji.4.md) ✓ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.2/README.md) | [bob-cli-ji.2](bob-cli-ji.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a2809a1`](https://github.com/bobs-org/bob-cli/commit/a2809a1dc48db0d2ac384f44d3e5fce7c8635715) | feat(gcal): add bob gcal note selection and read-only modes | [bob-cli-ji.2](bob-cli-ji.2.md) | 2026-11-10 08:11:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.2][1] | Need the phase scope and design file | 2 |
| read-by | [agent:research.40.cld][2] | Check phase progress and notes for guide accuracy | 1 |
| read-by | [agent:research.40.mus][3] | research guide on adding metadata to private event tasks | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.cld/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.mus/README.md

<!-- sase:referenced-by:end -->
