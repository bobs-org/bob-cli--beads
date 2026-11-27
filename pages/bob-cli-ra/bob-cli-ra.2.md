# Bead: bob-cli-ra.2 — Matcher hardening, key notices, and the links footer copy

[Bead Pages](../README.md) / [bob-cli-ra](README.md) / bob-cli-ra.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6o.linker.w0.md) · **Assignee:** `bob-cli-ra.2` · **Size:** medium
**Created:** 2026-11-27 15:01:37 EST · **Closed:** 2026-11-27 17:41:02 EST
**Plan:** [202611/tree\_note\_link\_walks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/tree_note_link_walks.md)

## Description

nav: stop matching step links inside inline code, count authored step links only on nav lines on tree routes, pass the tree fields through resolveNavLinks and walkMode.links, give `[n`/`]n`/`[N`/`]N` useful notices, and teach the `n` walker-footer panel parents, lanes, wraps, and singletons.

## Notes

[2026-11-27T21:32:44Z · bob-cli-ra.2] NAV API SHAPE: walkMode.links stays v7 and additively returns route, kind, lane, parent (navGroups step.parent), and stepNone; tree step overrides use nav lines while calendar/record retain body matching.

[2026-11-27T22:41:02Z · bob-cli-ra.2--3] Verified on bob-plugins HEAD dca84529: npm run build succeeded; npm run build:check passed; all four focused navigation/footer tests passed (144 tests); npm run docs:gen completed; npm run docs:check exited 0. Synced bob-navigation-hotkeys and bob-ledger-tools from this checkout; both syncs succeeded with files unchanged. bob plugins list -f json --no-pull and direct manifest comparison confirmed clean deployed versions bob-navigation-hotkeys 2.107.17 and bob-ledger-tools 1.173.0, both stamped at source HEAD dca84529. sase bead epic-symbols bob-cli-ra.2 reported no --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-qq.10.5](../bob-cli-qq/bob-cli-qq.10.5.md) ✓ · ⧖ 2026-11-27
- **Depends on:** [bob-cli-ra.1](bob-cli-ra.1.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-ra.4](bob-cli-ra.4.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ra.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ra.2.md) | [bob-cli-ra.2](bob-cli-ra.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5b34a69`](https://github.com/bobs-org/bob-plugins/commit/5b34a69caf800c6c8d8ab3f6ae202c570c0f1407) | feat(navigation): harden tree walk matching and footer copy | [bob-cli-ra.2](bob-cli-ra.2.md) | 2026-11-27 16:41:06 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ra.3][1] | Need nav phase status for rail dependency | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ra.3/README.md

<!-- sase:referenced-by:end -->
