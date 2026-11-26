# Bead: bob-cli-q8.4 — capture-complete tie fields

[Bead Pages](../README.md) / [bob-cli-q8](README.md) / bob-cli-q8.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6f.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6f.linker.w0.md) · **Assignee:** `bob-cli-q8.4` · **Size:** small
**Created:** 2026-11-25 18:16:42 EST · **Closed:** 2026-11-25 20:34:12 EST
**Plan:** [202611/plain\_link\_dependency\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/plain_link_dependency_ties.md)

## Description

capture-complete: relation candidates carry dependency_tie in both directions (also_prerequisite stays as a deprecated alias), and & / * candidates carry plain_link.

## Notes

[2026-11-26T01:34:00Z · bob-cli-q8.4] PROPOSED FOLLOW-UP: just docs-check fails identically on the clean base tree with generated drift in docs/bob-ledger-tools.md and docs/index.md (npm run docs:gen regions); unrelated to this phase

[2026-11-26T01:34:12Z · bob-cli-q8.4] capture-complete carries dependency_tie (prerequisite|dependent, vault edges plus same-item typed &/*; also_prerequisite kept as deprecated alias) and plain_link on &/* rows (to|from|both, vault LINKS only). Human render shows prerequisite/dependent/linked. Verified: 8211 lib tests pass incl. 3 new tie/plain_link/render tests; cargo fmt clean; docs-gen regenerated; docs-check shows only pre-existing clean-tree drift (recorded as follow-up)

## Dependencies

- **Depends on:** [bob-cli-q8.1](bob-cli-q8.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q8.9](bob-cli-q8.9.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.4/README.md) | [bob-cli-q8.4](bob-cli-q8.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2880238`](https://github.com/bobs-org/bob-cli/commit/28802383d80b1665f59aa68b68406c25482adff8) | feat(capture-complete)!: report dependency tie on every candidate | [bob-cli-q8.4](bob-cli-q8.4.md) | 2026-11-25 20:35:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q8.2][1] | Check whether the later q8 phase already tracks the baseline docs inventory drift found during q8.2 verification | 1 |
| read-by | [agent:bob-cli-q8.4][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.4/README.md

<!-- sase:referenced-by:end -->
