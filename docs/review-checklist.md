# Monthly Review Checklist

Run this once a month. Set a calendar reminder. The whole pass takes
about 30 minutes.

## 1. Stale suggestions (10 min)

- [ ] Open `/admin` → Suggestion rules.
- [ ] For each rule with a yellow "aging" or red "stale" banner on the
      public site:
  - [ ] Re-verify the price range on replacement products.
  - [ ] Check that all source URLs still work.
  - [ ] Bump `lastVerified` to today's date.
- [ ] If a rule's advice no longer feels right, demote it from
      `approved` to `reviewed` and get the experienced sound reviewer
      to re-check it.

## 2. Open issues (5 min)

- [ ] Open `/admin` → Issues.
- [ ] For each issue marked `open` for more than 30 days:
  - [ ] Is it still open? If fixed, mark it `resolved` and add a
        resolution note in the body.
  - [ ] If it keeps coming back, mark it `recurring`.

## 3. Form submissions (5 min)

- [ ] Open Netlify dashboard → Forms → `report-issue`.
- [ ] Triage new submissions:
  - [ ] Spam? Delete.
  - [ ] Already handled? Mark and delete.
  - [ ] Worth tracking? Promote to a new issue in `/admin` and link to
        equipment if applicable.

## 4. Inventory accuracy (5 min)

- [ ] Walk through the sound booth. Does every active equipment item on
      the site actually exist? Update `status` for anything that's been
      loaned, retired, or gone missing.

## 5. Board scenes (5 min)

- [ ] When was the last scene photo updated? If the board has been
      reconfigured (added channels, changed routing), upload a new
      scene photo.

## 6. Backup access check (annually)

- [ ] Once a year, confirm the backup editor can still log in.
- [ ] Confirm the GitHub repo and Netlify account are still owned by
      church-controlled credentials, not personal accounts.
