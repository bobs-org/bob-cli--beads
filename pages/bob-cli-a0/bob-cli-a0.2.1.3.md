# Bead: bob-cli-a0.2.1.3 — Enforce Bob's documentation contract

[Bead Pages](../README.md) / [bob-cli-a0.2.1](bob-cli-a0.2.1.md) / bob-cli-a0.2.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.2.md) · **Assignee:** `bob-cli-a0.2.1.3` · **Size:** medium
**Created:** 2026-10-19 19:05:38 EDT · **Closed:** 2026-10-19 20:01:47 EDT
**Plan:** [202610/docs\_toolchain.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_toolchain.md)

## Description

lint: port the editorial checks and add root registration, nav completeness, portability, media provenance, privacy, and budget ratchets with negative fixtures for every rule.

## Notes

[2026-10-20T00:01:47Z · bob-cli-a0.2.1.3] Verified bob-docs lint on the real site (exit 0), 77 pytest cases covering typing/registry, front matter, budgets, hygiene, test pins, portability, nav omission/empty tab, privacy baseline (new/duplicate/code hits), media, forged vs verified source, malformed YAML, shell prompts, and generated-page metadata/privacy; capture.md grammar (++N, !!!) and completion.md $SHELL transcripts survive; lint --fix only lowers ceilings and removes obsolete privacy rows; strict Zensical build still passes.

## Dependencies

- **Depends on:** [bob-cli-a0.2.1.2](bob-cli-a0.2.1.2.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.2.1.5](bob-cli-a0.2.1.5.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.2.1.6](bob-cli-a0.2.1.6.md) ◐ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.3/README.md) | [bob-cli-a0.2.1.3](bob-cli-a0.2.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e37cd4a`](https://github.com/bobs-org/bob-cli/commit/e37cd4a5c849e3922b830cf5fbe36926bb6ffddd) | feat(docs): add bob-docs lint for the documentation contract | [bob-cli-a0.2.1.3](bob-cli-a0.2.1.3.md) | 2026-10-19 20:12:29 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.2.1.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.3/README.md

<!-- sase:referenced-by:end -->
