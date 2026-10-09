# Bead: bob-cli-5x.1 — bob ref scan gains a JSON report and a writer lock

[Bead Pages](../README.md) / [bob-cli-5x](README.md) / bob-cli-5x.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z1.md) · **Assignee:** `bob-cli-5x.1` · **Size:** medium
**Created:** 2026-10-09 12:26:28 EDT · **Closed:** 2026-10-09 12:49:07 EDT
**Plan:** [202610/bob\_refs\_scan\_keymap.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_scan_keymap.md)

## Description

cli-scan-json: add `-f/--format human|json` to `bob ref scan` with a versioned envelope that names every created and updated note, a pure-JSON stdout (hook chatter goes to stderr), coded hard-failure envelopes, and an exclusive lock that serializes writing scans; document it and cover it with CLI tests.

## Notes

[2026-10-09T16:49:00Z · bob-cli-5x.1] INTERFACE SAMPLE: real `bob ref scan -f json` success envelope from the CLI test (synthetic vault, BOB_NOW pinned; keys and order are the contract for refs-scan-ui fixture parity):
{"ok":true,"schema_version":1,"command":"ref scan","generated_at":"2026-10-06T12:00:00","mode":"write","write_pdfs":false,"hook":{"status":"none","command":null},"intake":[],"summary":{"pdfs":2,"created":1,"updated":1,"unchanged":0,"markers":0,"tasks":0,"failures":0},"notes":[{"action":"create","path":"ref/chat/fresh_report.md","title":"Fresh Report","ref_type":"chat","source_pdf":"lib/chat/fresh_report.pdf","marker":false},{"action":"update","path":"ref/chat/standing_memo.md","title":"Standing Memo Revised","ref_type":"chat","source_pdf":"lib/chat/standing_memo.pdf","marker":false}],"failures":[]}
Error envelope shape (dirty_targets case): {"ok":false,"schema_version":1,"command":"ref scan","generated_at":"2026-10-06T12:00:00","mode":"write","write_pdfs":false,"intake":[],"error":{"code":"dirty_targets","message":"refusing to modify dirty vault files","hint":"commit, stash, or clean those paths, then scan again","paths":["ref/chat/memo.md"]}}

[2026-10-09T16:49:07Z · bob-cli-5x.1] cli-scan-json done and verified: -f/--format human|json on bob ref scan with versioned schema-1 envelopes (success + coded hard-failure shapes), pure single-line JSON stdout with hook chatter on stderr, exclusive scan.lock writer lock (0600/0700, 250ms x 120s wait, BOB_REF_SCAN_LOCK_WAIT_SECONDS override, dry runs skip it), docs in highlights-ref-sync.md (JSON output + Writer lock + scan_busy row) and ref.md pointer. just check gate green: cargo fmt --check clean, cargo clippy --all-targets --all-features clean, full cargo test --no-fail-fast 16 binaries ok including 11 new tests (success/partial/dry-run/dirty/busy x2/human-busy/hook-output/hook-fail/help-conflict) and all pre-existing scan tests unchanged. No epic-symbol entries remain.

## Dependencies

- **Blocks:** [bob-cli-5x.4](bob-cli-5x.4.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5x.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5x.1/README.md) | [bob-cli-5x.1](bob-cli-5x.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7fe88b7`](https://github.com/bobs-org/bob-cli/commit/7fe88b72f4d32df7e4bdf1af1a22a038cfd314a4) | feat(refs): add JSON scan report and writer lock to bob ref scan | [bob-cli-5x.1](bob-cli-5x.1.md) | 2026-10-09 12:50:42 EDT |
