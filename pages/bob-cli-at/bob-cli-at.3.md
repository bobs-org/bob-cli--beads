# Bead: bob-cli-at.3 — Coordinated marker writes, holds, and human reporting

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.3` · **Size:** medium
**Created:** 2026-10-23 11:44:15 EDT · **Closed:** 2026-10-23 13:48:39 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

executor: when the policy is on, wrap each marker-write PDF's whole v1/v2 write sequence in one coordinated accessor. That covers scan (human and JSON), `ref sync -w`, and create-time ingest. Inside the accessor, re-check the PDF first. Same digest: write as today. Changed digest with the same marker: write to the freshly located annotation and record saved-first. Changed marker: hold `marker_changed`. Add the `editor_active` reading hold for unattended scans only, plus the new `-a, --attended` scan flag, and the `coordination_timeout` hold with the per-PDF budget and scan cap. Add `ScanWriteOutcome::Held` and the marker-write report (mode, saved-first, status transition, wait time). Holds exit 0. Add the yellow `held` concise line, the summary count, and the verbose and `ref sync` lines. JSON mode counts holds as neither notes nor failures for now. With the key off, output stays byte-identical. Document the contract and the config key, then run `just docs-gen` for the flag.

## Notes

[2026-10-23T17:48:39Z · bob-cli-at.3] Coordinated marker writes wrap each PDF v1/v2 sequence when the policy is on: re-check digest/marker, saved-first, marker_changed/editor_active/coordination_timeout holds, -a/--attended, yellow held lines and summary counts. JSON holds count as neither notes nor failures; key-off output stays byte-identical. Verified with just fmt, just docs-check, and just check (clippy rustc_gate + cargo test --no-fail-fast, including 14 lib and 6 CLI marker_write tests). No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-at.1](bob-cli-at.1.md) ✓ · ⧖ 2026-10-23
- **Depends on:** [bob-cli-at.2](bob-cli-at.2.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-at.4](bob-cli-at.4.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.3/README.md) | [bob-cli-at.3](bob-cli-at.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cd4bc7a`](https://github.com/bobs-org/bob-cli/commit/cd4bc7a0cb23cb6d1eb13fc2c66da7d17d6a9eb7) | feat(highlights): coordinate PDF marker writes with holds and human reporting | [bob-cli-at.3](bob-cli-at.3.md) | 2026-10-23 13:49:27 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-at.3][1] | Need the phase scope and design file | 4 |
| read-by | [agent:bob-cli-at.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.land/README.md

<!-- sase:referenced-by:end -->
