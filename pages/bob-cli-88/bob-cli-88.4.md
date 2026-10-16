# Bead: bob-cli-88.4 — bob-cli docs, optional decision record, and full deploy

[Bead Pages](../README.md) / [bob-cli-88](README.md) / bob-cli-88.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10m](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10m.md) · **Assignee:** `bob-cli-88.4` · **Size:** small
**Created:** 2026-10-16 07:28:58 EDT · **Closed:** 2026-10-16 08:55:11 EDT
**Plan:** [202610/emptied\_pomodoro\_cleanup.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/emptied_pomodoro_cleanup.md)

## Description

docs: document the plugin-side emptied-entry rule in bob-cli docs, write the decision record if accepted, then run the full plugin suite and deploy all plugins.

## Notes

[2026-10-16T12:24:07Z · bob-cli-88.4] PROPOSED FOLLOW-UP: record the shared emptied-Pomodoro keymap rule as a standing decision — the epic selected no decision record, so this documentation phase did not edit memory.

[2026-10-16T12:35:34Z · bob-cli-88.4--1] PROPOSED FOLLOW-UP: investigate six npm test failures reproduced on clean bob-plugins HEAD 86cebc9 (four unblocked-glyph tests, Keep counts once and saturates at 999 without reset, and forward conversion Depends-On round-trip); npm test reports 2846 passed, 6 failed.

[2026-10-16T12:44:37Z · bob-cli-88.4--2] Docs verification: reviewed docs/task-dependencies.md and docs/task-status-hooks.md; the docs now describe the plugin keymap childless-entry cleanup rule, and git diff --check passes. No --epic-symbol entries for bob-cli-88.4. reports no remaining symbols. Clean-base bob-plugins suite at HEAD 86cebc9: 2846 passed, 6 failed; the follow-up investigation is already recorded in note #2. Deployment: Bob Plugins - sync - /home/bryan/projects/github/bobs-org/bob-plugins -> /home/bryan/bob

  ok block-id-prompt         copied manifest.json   +1 -1
             @ -1,7 +1,7 @
              {
                "id": "block-id-prompt",
                "name": "Block ID Prompt",
             -  "version": "1.33.0",
             +  "version": "1.32.0",
                "minAppVersion": "1.8.7",
                "description": "Prompt for custom block IDs and complete wiki block links to open t…
                "author": "Bryan",
             ↳ backed up to /home/bryan/.local/state/bob-cli/plugin-backups/20261016-084436/block-id-prompt/manifest.json
  ok block-id-prompt         copied main.js   +39 -316
             @ -3307,34 +3307,6 @
              
              function isDedicatedLinkBullet(lines, reference, removalRange) {
                const bounds = lineContentBounds(lines, reference.line);
             -  // Preferred path: judge the bare link token with the same decorations
             -  // `isDedicatedTaskLinkBullet` accepts (an optional checkbox, a run of
             -  // `🍅 ` markers, an optional `~~` strike opener, an optional `!`, and a
             -  // trailing ` #` move-only directive), so a single-link dedicated bullet
             -  // in those forms is removed whole instead of leaving a `- [ ]`, `- #`,
             -  // or `- 🍅` stub behind.
             -  if (
             -    reference &&
             -    Number.isInteger(reference.start) &&
             -    Number.isInteger(reference.end) &&
             -    reference.end > reference.start
             -  ) {
             -    const tokenStartCh = reference.start - bounds.start;
             -    const tokenEndCh = reference.end - bounds.start;
             -    if (
             -      tokenStartCh >= 0 &&
             -      tokenEndCh <= bounds.line.length &&
             -      bounds.line.slice(tokenStartCh, tokenEndCh) === reference.raw
             -    ) {
             -      return isDedicatedTaskLinkBullet(bounds.line, {
             -        startCh: tokenStartCh,
             -        endCh: tokenEndCh,
             -      });
             -    }
             -
             -    return false;
             -  }
             -
                const bodyBounds = listItemBodyBounds(bounds.line);
                if (!bodyBounds) {
                  return false;
             @ -3369,231 +3341,8 @
              
              function editContainsReference(edit, reference) {
                return edit.start <= reference.start && edit.end >= reference.end;
             -}
             -
             -// ---------------------------------------------------------------------------
             -// Emptied Pomodoro entries: every link-removing gesture also deletes the
             -// entries it empties, in the same write. An entry is emptied when the
             -// gesture's edits remove at least one line or Task Link token inside its
             -// block and no list-item child remains in the block afterwards (the
             -// childless rule: prose bullets keep the entry, exactly like
             -// `bob task reconcile`'s empty-Pomodoro rule; fenced example bullets never
             -// count). Entries that were already childless, such as freshly planned
             -// placeholders, are never touched.
             -// ---------------------------------------------------------------------------
             -
             -// Every Pomodoro entry in `section` that may be deleted: unfenced, of an
             -// eligible status (`statuses: "any"` for the selected-link deletion, which
             -// can hit an entry of any status; anything else means open-only), and
             -// holding at least one unfenced list-item child in the snapshot.
             -function collectEmptiedEntryCandidates(lines, section, fencedLines, statuses) {
             -  const candidates = [];
             -  for (let line = section.startLine; line <= section.endLine; line += 1) {
             -    if (fencedLines[line] || !isPomodoroEntryLine(lines[line])) {
             ... and 442 more diff lines
             ↳ backed up to /home/bryan/.local/state/bob-cli/plugin-backups/20261016-084436/block-id-prompt/main.js
  ok bob-ledger-tools        up to date
  ok bob-navigation-hotkeys  copied manifest.json   +1 -1
             @ -1,7 +1,7 @
              {
                "id": "bob-navigation-hotkeys",
                "name": "Bob Navigation Hotkeys",
             -  "version": "2.41.0",
             +  "version": "2.40.1",
                "minAppVersion": "1.8.7",
                "description": "Ctrl+Shift+P always opens the Task Card, a focused first screen wit…
                "author": "Bryan",
             ↳ backed up to /home/bryan/.local/state/bob-cli/plugin-backups/20261016-084436/bob-navigation-hotkeys/manifest.json
  ok bob-navigation-hotkeys  copied main.js   +81 -135
             @ -12829,8 +12829,8 @
              }
              
              // True when one or more matched link occurrences make up a bullet's entire
             -// body, with the same checkbox/marker/strike/embed/move-only decorations
             -// accepted by Task Links. Two matched links may be separated by whitespace.
             +// body (only whitespace, if anything, between adjacent occurrences). Two
             +// matched links on one otherwise-empty bullet still count as dedicated.
              function isDedicatedPomodoroLinkLine(lineText, occurrences) {
                const bounds = pomodoroBulletBodyBounds(lineText);
                const list = Array.isArray(occurrences) ? occurrences : [];
             @ -12838,18 +12838,13 @
                  return false;
                }
                const sorted = list.slice().sort((left, right) => left.start - right.start);
             -  const line = String(lineText || "");
             -  const before = /^(?:\[[^\]\n]\][ \t]+)?(?:🍅[ \t]+)*(~~)?!?$/u.exec(
             -    line.slice(bounds.start, sorted[0].start),
             -  );
             -  const after = /^(~~)?(?:[ \t]*#)?$/.exec(
             -    line.slice(sorted[sorted.length - 1].end, bounds.end),
             -  );
                if (
             -    !before || !after || Boolean(before[1]) !== Boolean(after[1])
             +    sorted[0].start !== bounds.start ||
             +    sorted[sorted.length - 1].end !== bounds.end
                ) {
                  return false;
                }
             +  const line = String(lineText || "");
                for (let index = 1; index < sorted.length; index += 1) {
                  if (line.slice(sorted[index - 1].end, sorted[index].start).trim() !== "") {
                    return false;
             @ -14743,9 +14738,7 @
              // used to resolve `[[target#^id]]` links to a vault path). Struck links and
              // links under a closed/cancelled entry are never candidates. A dedicated link
              // bullet (the link, its marker, and nothing else) is removed subtree and all;
             -// otherwise only the matched token is removed from its bullet. Every entry
             -// emptied by these removals is deleted in the same plan; untouched placeholders
             -// and entries retaining a non-fenced list item are preserved.
             +// otherwise only the matched token is removed from its bullet.
              function planDeferredPomodoroLinkCleanup(dailyContent, targets, options = {}) {
                const snapshot = String(dailyContent || "");
                const targetList = Array.from(targets || []).filter(
             @ -14859,105 +14852,70 @
                    endLineExclusive: block.endLineExclusive,
                  });
                }
             -  const removedBulletCount = subtreeCandidates.length;
                let removedEntryCount = 0;
             -  // Same open-ledger definition this cleanup already uses
             -  // (`collectOpenPomodoroRanges` / `isOpenPomodoroLedgerEntryLine`), not
             -  // `collectPomodoroEntries`' picker grammar, so a childless
             -  // `- [ ] Current (0900-0930)` entry is eligible.
             -  for (const range of openRanges) {
             -    const entryBlock = findCurrentBulletChildBlock(lines, range.entryLine);
             -    const childEndExclusive = Math.min(
             -      entryBlock.endLineExclusive,
             -      section.endLine + 1,
             -    );
             ... and 358 more diff lines
             ↳ backed up to /home/bryan/.local/state/bob-cli/plugin-backups/20261016-084436/bob-navigation-hotkeys/main.js
  ok bob-project-tasks       up to date
  ok bob-vim-surround        up to date
  ok task-status-cycler      copied manifest.json   +1 -1
             @ -1,7 +1,7 @
              {
                "id": "task-status-cycler",
                "name": "Task Status Cycler",
             -  "version": "1.42.0",
             +  "version": "1.41.0",
                "minAppVersi

… and 4230 more characters

## Dependencies

- **Depends on:** [bob-cli-88.1](bob-cli-88.1.md) ✓ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-88.2](bob-cli-88.2.md) ✓ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-88.3](bob-cli-88.3.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-88.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-88.4.md) | [bob-cli-88.4](bob-cli-88.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`298ebdf`](https://github.com/bobs-org/bob-cli/commit/298ebdf41b05000189bba7d5af8e64a1a717685e) | docs(task-cleanup): document emptied entry cleanup | [bob-cli-88.4](bob-cli-88.4.md) | 2026-10-16 08:56:10 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-88.4--3][1] | Confirm parent epic remains open and phase scope before closing only bob-cli-88.4 | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-88.4.md

<!-- sase:referenced-by:end -->
