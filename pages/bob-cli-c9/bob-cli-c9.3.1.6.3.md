# Bead: bob-cli-c9.3.1.6.3 — Route guards, audio, vault ordering, redirects, and parser edges

[Bead Pages](../README.md) / [bob-cli-c9.3.1.6](bob-cli-c9.3.1.6.md) / bob-cli-c9.3.1.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.land.md) · **Assignee:** `bob-cli-c9.3.1.6.3` · **Size:** medium
**Created:** 2026-10-25 19:48:33 EDT · **Closed:** 2026-10-25 21:11:26 EDT
**Plan:** [202610/ref\_reread\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_reread_landing_fixes.md)

## Description

route_guards: overwrite exact-output permission, narrated-reading hint, no audio auto-discovery on rereads, library-PDF -f -L refusal, vault-note preflight ordering, redirect guard, parser raw-argv fixes, and typed overwrite fallbacks.

## Notes

[2026-10-26T01:11:26Z · bob-cli-c9.3.1.6.3] route_guards done: exact-output overwrite keeps permission for URL/collection/Markdown; plain reread prints narrated hint via shared helper with no audio inheritance; library-PDF refusal wins under -f even with -L/-P while -L alone still attaches; vault preflight runs before parent (refusal before missing-parent, same-day reread, new-day ordinary); redirect guard checks final_url for PDF/curl, arXiv, and clip adapter outside family (exit 1, nothing written); parser finds subcommand after top-level opts and treats clustered -df=reread as explicit; typed overwrite fallbacks replace string matching (collection exact uses typed next stem). Verified: 9 new CLI tests + 1 force unit test pass, 5 existing focused tests pass (library refusal, listen attach, overwrite fresh/filed, vault same-day, reread-listen), cargo fmt clean, clippy gate clean, no epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-c9.3.1.6.2](bob-cli-c9.3.1.6.2.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-c9.3.1.6.4](bob-cli-c9.3.1.6.4.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.6.3/README.md) | [bob-cli-c9.3.1.6.3](bob-cli-c9.3.1.6.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d96ed41`](https://github.com/bobs-org/bob-cli/commit/d96ed412085581c4b49456c6672bd26db4fc9592) | feat(highlights-ref): add route guards for create/clip overwrite, redirect, and narrated hints | [bob-cli-c9.3.1.6.3](bob-cli-c9.3.1.6.3.md) | 2026-10-25 21:12:26 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.3.1.6.3][1] | Need full scope notes and epic symbols | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.6.3/README.md

<!-- sase:referenced-by:end -->
