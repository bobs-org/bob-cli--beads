# Bead: bob-cli-kx.3.1.5 — Render the mail banner and Move-back action

[Bead Pages](../README.md) / [bob-cli-kx.3.1](bob-cli-kx.3.1.md) / bob-cli-kx.3.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.md) · **Assignee:** `bob-cli-kx.3.1.5` · **Size:** medium
**Created:** 2026-11-13 08:02:47 EST · **Closed:** 2026-11-13 12:04:31 EST
**Plan:** [202611/gmail\_archive\_receipts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_receipts.md)

## Description

mail_banner: implement the Bob Mail banner button over Bob-owned receipt data and bob gmail unarchive, preserving thin-client ownership and safe rendered text.

## Notes

[2026-11-13T16:16:20Z · bob-cli-kx.3.1.5] mail_banner code complete: 046-archive-banner.js (pure core) + 055-plugin-archive-banner.js (Reading + Live Preview hosts, coalesced list snapshot, exact unarchive argv, pending guard), docs/bob-mail.md Archived mail section, styles, 23 new node tests. Verified: node suites 98/98 pass (banner, mail, compose, plugin-build, mail-link-marks, docs inventory/check), build:check + validate-manifests + docs:inventory clean, docs-check.sh fails only on 3 pre-existing word-budget overruns in untouched bob-cli reference docs (json-outputs, ledger-tools, navigation-hotkeys; last touched by 2ddfc944). Deploy blocked: vault bob-mail stamp is a dirty build from reaped workspace bob-cli_11 (base 01ff42d, 13:27Z); deployed main.js/manifest/styles.css are byte-identical to landed a563fc7 so -F -p bob-mail discards no uncommitted bob-mail work. Awaiting Bryan approval for the force deploy.

[2026-11-13T17:04:31Z · bob-cli-kx.3.1.5--1] Gate-authorized force-deploy done: bob plugins sync -p bob-mail -F succeeded from linked bob-plugins checkout; vault main.js/styles.css byte-identical to built tree and resync reports 3 unchanged. Verified: banner suite 23/23, unit 6476 pass/0 fail/2 skipped, npm run validate clean, build current. epic-symbols empty. Note: banner work still uncommitted in linked bob-plugins tree (HEAD a563fc7) for land agent to land; upstream cccfdbb touches task-status-cycler only, no bob-mail impact.

## Dependencies

- **Depends on:** [bob-cli-kx.3.1.4](bob-cli-kx.3.1.4.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-kx.3.1.6](bob-cli-kx.3.1.6.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.3.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.1.5.md) | [bob-cli-kx.3.1.5](bob-cli-kx.3.1.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.3.1.5--1][1] | Need phase scope and design to finish force-deploy per gate decision | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.1.5.md

<!-- sase:referenced-by:end -->
