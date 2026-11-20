# Bead: bob-cli-nh.7.1.4 — Real Obsidian acceptance and final plugin deployment

[Bead Pages](../README.md) / [bob-cli-nh.7.1](bob-cli-nh.7.1.md) / bob-cli-nh.7.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.7.md) · **Assignee:** `bob-cli-nh.7.1.4` · **Size:** medium
**Created:** 2026-11-19 18:17:37 EST · **Closed:** 2026-11-20 07:51:15 EST
**Plan:** [202611/intention\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/intention_card.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:1919355ed6090b82b47ff817 | attached via sase artifact create --bead |
| related | file:explicit:38d3354dfd6b6e7aaf8351d0 | attached via sase artifact create --bead |
| related | file:explicit:691e7f45a1092f0a1693d13e | attached via sase artifact create --bead |
| related | file:explicit:6bf0fea689b815ec8b6d63d1 | attached via sase artifact create --bead |
| related | file:explicit:7dfdbceb0f90c18729a2cf7c | attached via sase artifact create --bead |
| related | file:explicit:862d25860568f44cb4a82bd5 | attached via sase artifact create --bead |
| related | file:explicit:930bbfc65a8ad11998092e33 | attached via sase artifact create --bead |
| related | file:explicit:f841eb68bf723f242b173ab0 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

acceptance: add the isolated intention-card CDP runner and offline wrapper, prove mounting, both yesterday gestures, field edits/Undo, navigation/YAML, stale drafts, and fail-open behavior with a current real bob binary. Run regression and docs gates, inspect screenshots, deploy and verify provenance, and provide closeout evidence for bob-cli-nh.7 without closing ancestors.

## Notes

[2026-11-20T12:50:17Z · bob-cli-nh.7.1.4] ACCEPTANCE EVIDENCE (closeout input for bob-cli-nh.7): Added scripts/obsidian-intention-card-e2e.cjs (+ -lib, -workflows) and offline wrapper scripts/test-obsidian-intention-card-e2e.cjs (in test:unit). Real run under xvfb-run with owned Obsidian 1.x Electron, scratch Git vault/profile, never the live vault; bob built from bob-cli d15432aa (clean), BOB_BIN sha256 b0bcf62b4f4c2a4440c0c0854350877073cb9fbeae278f9c6875a424c9f5b99a (bob 0.5.0); test clock 2026-11-20 America/New_York, plugin today agreed at start/end. Final verdict PASS 65/65 mandatory checks, 0 console exceptions/errors, 11 real writer applies (stdin + results recorded), 37 screenshots all inspected (light/dark, 375px). Proven: Reading + Live Preview placement after H1/nav and above ^gtd, exactly 7 owned keys hidden with unrelated rows visible, restore on unmount/mode change/malformed metadata/plugin disable and recovery; empty/malformed/Source/embed fail open; empty-note ==; open->intention:0, closed->Reflection; [n==r and ==[r end with caret at end of yesterday textarea, no literal r, no writes; add/replace/paste-normalized/soft-cap/Alt+K reorder/Ctrl+D remove/u Undo with byte checks of body + unowned frontmatter and fresh bob reads; multiline reflection Ctrl+Enter save-close; summary explainer, edited provenance, stamp-restoring Undo across reopen; ]/[/= navigation incl. missing day disabled, missing year ensure hint, ISO boundary walk 2026-01-01 -> 2025-12-31/2026-W01/2025-W52/2025-Q4/2026-Q1/2026; palette Edit intentions + Reflect on yesterday; Command Mode rows; Ctrl+Shift+P fallback + task priority; YAML Done returns to subject/selection; invalid YAML stays in Source with notice; two-pane stale refusal keeps draft with no writer call then explicit retry saves; body-only edit survives save; emulated old bob keeps card + Source recovery. Artifacts: report file:explicit:1919355ed6090b82b47ff817; screenshots file:explicit:7dfdbceb0f90c18729a2cf7c; contact sheet file:explicit:f841eb68bf723f242b173ab0; painter previews file:explicit:8ce152c821eec94009654f19 (sheets file:explicit:691e7f45a1092f0a1693d13e, file:explicit:6bf0fea689b815ec8b6d63d1).

[2026-11-20T12:50:35Z · bob-cli-nh.7.1.4] DEFECTS FOUND BY REAL ACCEPTANCE AND FIXED (bob-plugins, bob-ledger-tools 1.140.0 -> 1.141.0): (1) Live Preview crash: the card was a block decoration from a ViewPlugin (CodeMirror RangeError "Block decorations may not be specified via plugins") so a daily note with intentions could not open in LP; now an inline widget at the end of the line before the first unrelated block, built lazily, and the toDOM ReferenceError (undefined plugin) fixed. (2) Reading view: the card rendered intention Markdown with the note sourcePath, re-entering its own post-processor in a repaint loop; render containers are now marked and rejected, each card owns a MarkdownRenderChild unloaded with it; the card anchored inside the H1 wrapper (above the nav line) and sizer-level inserts were pruned by Obsidian, so it now appends inside the last H1/nav section with a bounded retry when sections attach late. (3) Editor: stages never received focus/caret; pasted newlines were stripped instead of becoming spaces with a note; stages opened on missing/needs-update subjects; stale refusals never fetched a fresh fingerprint so retry failed again; Undo ignored the path-scoped record after reopen; generation churn from the card own pane save surfaced as a false field-stale error on body-only edits; malformed YAML read as ok+warning let Done reopen the card and the editor treat it as empty; `y` opened Live Preview instead of raw Source. All fixed in new fragment 297ca plus small call-site edits (297c 977 lines). (4) Polish: Reading-view SUMMARY/REFLECTION titles inherited huge h2 sizing, chip/text misalignment from <p> margins, raw status words, duplicated stale text, bare Edit label. Unit coverage: scripts/test-ledger-tools-intention-card-acceptance.cjs (10 tests). The editor real-writer unit test now runs only with explicit BOB_BIN (it auto-discovered a stale target/debug/bob lacking periods update and failed on the clean base).

[2026-11-20T12:50:39Z · bob-cli-nh.7.1.4] GATES AND DEPLOYMENT: npm run build:check, docs:inventory:check, npm run validate (12/12) pass. Focused intention/host/ownership/registry/YAML suites 99/99 with BOB_BIN. npm test: all pass except intermittent CPU-budget timing tests (see follow-up; same class reproduced on clean base). BOB_CLI_DIR=<bob-cli_11> npm run docs:check: lint, generated drift, strict build pass; published-URLs fails identically on clean base (follow-up). Regression real runs: Record Card e2e PASS 144/144 (file:explicit:930bbfc65a8ad11998092e33); album UI 120/121 and bank UI 73/78 with failures identical on clean base (bob-cli-nq, bob-cli-m6, bob-cli-m7, queue-card pair). Isolated startup smoke PASS (file:explicit:38d3354dfd6b6e7aaf8351d0). Deployed: bob plugins sync --repo <linked bob-plugins> --no-pull (dry run then real; 3 files copied, no refusal); .bob-deploy.json source_head ea47caf dirty=dirty (commit happens at this turn finalize) and manifest/main.js/styles.css stamp==source==vault sha256; vault manifest 1.141.0; edit-intentions + reflect-on-yesterday present; bob plugins list synced 1.141.0. Post-sync deployed-vault smoke gate PASS, failures [] (file:explicit:862d25860568f44cb4a82bd5). Land agent: a re-sync from the committed checkout will rewrite the stamp to the landed commit (descendant deploy, no -F).

[2026-11-20T12:50:51Z · bob-cli-nh.7.1.4] PROPOSED FOLLOW-UP: Fix the two docs-check published-URL obligations — with BOB_CLI_DIR=bob-cli d15432aa and bob-plugins ea47caf (clean base and this branch identical): docs/develop/plugins/architecture.md:74 -> /develop/validation/ and docs/reference/glossary.md:301 -> /bob-copy-chips/ have no built page; noted by bob-cli-nh.7.1.3 but no open bead tracks it.

[2026-11-20T12:50:55Z · bob-cli-nh.7.1.4] PROPOSED FOLLOW-UP: Move load-sensitive CPU-budget tests out of the parallel test:unit stage — test-ledger-tools-event-link-times.cjs ("one build over a 200-link ledger stays under 25 ms"), test-ledger-tools-frees-marks.cjs ("200-link / 2000-task build stays within the 25 ms budget"), and test-navigation-dependencies-stage-performance.cjs ("200/400/1000-task ... without cubic growth") intermittently fail npm test under parallel load and pass 3/3 alone; the frees-marks failure reproduced on the clean bob-plugins base. Serial test:perf stage (like the block-id-prompt index perf file) would make npm test deterministic.

[2026-11-20T12:51:00Z · bob-cli-nh.7.1.4] PROPOSED FOLLOW-UP: Bank UI e2e queue-card-live and queue-card-reading fail with "missing import command" on the clean bob-plugins base and this branch alike (with BOB_BIN from bob-cli d15432aa); invalid-fence and walk-learn-* are tracked by bob-cli-m6/bob-cli-m7, but no open bead tracks the queue-card pair (bob-cli-nh.6 called it intervening bank queue drift).

[2026-11-20T12:51:04Z · bob-cli-nh.7.1.4] PROPOSED FOLLOW-UP: Document in bob-cli docs/periods.md that an empty-op `bob periods update -n` on malformed frontmatter returns ok:true with empty fields and a frontmatter_invalid (or intentions_*) warning, so clients must treat those warnings as refusals (the card editor and YAML Done now do); alternatively consider failing the dry run closed like writes.

[2026-11-20T12:51:15Z · bob-cli-nh.7.1.4] Verified: real-Obsidian intention-card acceptance PASS 65/65 (bob from bob-cli d15432aa, report file:explicit:1919355ed6090b82b47ff817, 37 screenshots + 24 previews inspected); plugin defects found by the run fixed with unit coverage; build:check, docs inventory, validate pass; npm test green apart from intermittent CPU-budget flakes reproduced on base; docs:check URL failures identical on base; Record Card regression 144/144, album/bank failures identical on base; bob-ledger-tools 1.141.0 deployed with stamp/source/vault hashes matching and deployed-vault smoke gate PASS. Follow-ups recorded as notes; ancestors left open.

## Dependencies

- **Depends on:** [bob-cli-nh.7.1.3](bob-cli-nh.7.1.3.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.7.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.7.1.4/README.md) | [bob-cli-nh.7.1.4](bob-cli-nh.7.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b1a655a`](https://github.com/bobs-org/bob-plugins/commit/b1a655af0228ca2589c04ee46109da9335e22551) | feat(ledger-tools): prove the intention card in real Obsidian and fix what it found | [bob-cli-nh.7.1.4](bob-cli-nh.7.1.4.md) | 2026-11-20 07:55:43 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.7.1.4][1] | Check notes left by previous agents on this phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.7.1.4/README.md

<!-- sase:referenced-by:end -->
