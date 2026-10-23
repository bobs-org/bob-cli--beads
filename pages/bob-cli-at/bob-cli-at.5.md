# Bead: bob-cli-at.5 — Bob Mac Capture core decoding and open-PDF presentation

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.5` · **Size:** medium
**Created:** 2026-10-23 11:44:16 EDT · **Closed:** 2026-10-23 15:28:05 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

mac-core: in the linked bob-mac-capture repo, RefsCore decodes the new scan fields tolerantly. Those are `generated_at`, `summary.held`, `held[]` (lossy rows), and `notes[].marker_write`. Add a bounded receipt reader that resolves the path like bob: `XDG_STATE_HOME`, else `~/.local/state`. Add a pure `RefsPDFUpdates` classifier that takes a response plus optional open-tab file names. It splits entries into refreshed-open, refreshed-quiet, reading holds, busy holds, and changed holds, and supplies dedupe keys. Add the exact copy deck for notifications, footer clauses, and the busy banner, using the Refs state vocabulary. Unit-test it all and run `just portable-check`.

## Notes

[2026-10-23T19:28:05Z · bob-cli-at.5--5] Verified RefsCore scan decoding, bounded receipt reader, PDF update classifier, and presentation tests with passing just portable-check; macOS targets remain unverified on Linux.

## Dependencies

- **Depends on:** [bob-cli-at.4](bob-cli-at.4.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-at.6](bob-cli-at.6.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-at.5.md) | [bob-cli-at.5](bob-cli-at.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@9fb67f3`](https://github.com/bobs-org/bob-mac-capture/commit/9fb67f324f7500a63a184add96b4b03f4254f74f) | feat(refs): decode scan receipts and present PDF updates | [bob-cli-at.5](bob-cli-at.5.md) | 2026-10-23 15:28:44 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-at.5--5][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-at.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-at.5.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.land/README.md

<!-- sase:referenced-by:end -->
