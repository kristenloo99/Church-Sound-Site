# Handoff Checklist

This is the script for the live handoff session between the developer
and the deacon (and separately, between the developer and the backup
editor).

Plan for **90 minutes** with the deacon, **45 minutes** with the
backup editor.

## Before the session

The developer should confirm:

- [ ] Repo is created under church-owned GitHub credentials, not personal.
- [ ] Netlify site is created under church-owned credentials.
- [ ] The deacon and backup editor have GitHub accounts and have
      accepted the repo collaborator invitation.
- [ ] Decap CMS is configured with the GitHub backend (no Netlify
      Identity, no Git Gateway).
- [ ] `data/reviewers.yml` has been updated with real reviewer names.
- [ ] At least 10 suggestion rules have been reviewed and set to
      `status: approved` by the experienced reviewer.
- [ ] Real equipment list, board scene photos, and one real issue have
      been entered.
- [ ] The site has been Lighthouse-scored ≥ 90 on mobile.
- [ ] The internal-fields sweep has been performed — verify no serial
      numbers, donor info, or internal notes leak to public pages.

## Session script

### Part 1: Tour (15 min)

Walk the deacon through the public site on his phone:

- [ ] Home page → 6 big buttons.
- [ ] Tap "Reset the Board" → show the scene-recall instructions.
- [ ] Tap "Troubleshoot" → tap one symptom → show the suggestion block.
- [ ] Tap "Report a Problem" → fill out the form (don't submit).
- [ ] Tap "Inventory" → tap one item.
- [ ] Tap "Issue Log" → tap one item.
- [ ] Tap "Learn" → tap signal-flow → show the article.

### Part 2: Admin login (10 min)

- [ ] Deacon opens `/admin` on his laptop.
- [ ] Signs in with GitHub for the first time.
- [ ] Authorizes Decap.
- [ ] Lands on the admin home.

### Part 3: Live edits (45 min)

Deacon performs each of the following, with developer watching:

- [ ] **Add equipment** — pick a real piece of gear not yet entered.
- [ ] **Log a new issue** — pick a real current problem.
- [ ] **Promote a form submission** — developer submits a test form
      while the deacon watches, then deacon promotes it into the CMS.
- [ ] **Update a suggestion's lastVerified date** — pick one.
- [ ] **Upload a scene photo** — take a fresh phone photo of the
      board, upload, confirm it shows up on `/board-reset`.
- [ ] **Edit an article** — change one sentence, republish, confirm
      the live site updates within 3 minutes.

### Part 4: Rollback drill (10 min)

- [ ] Deacon deliberately makes a "bad" edit to a non-critical entry.
- [ ] Publishes it.
- [ ] Confirms it appears on the live site.
- [ ] Opens the GitHub repo, finds the commit, clicks "Revert" through
      the GitHub web UI.
- [ ] Confirms the site recovers.

### Part 5: Calendar + contact info (10 min)

- [ ] Deacon adds a monthly recurring reminder for the review checklist.
- [ ] Developer hands over a one-page "who to contact" sheet:
      reviewer, developer, church office.
- [ ] Screencast of the session is uploaded to the repo at
      `docs/handoff-screencast.mp4` (or a link to a video service).

## After the session: the one-week solo test

- [ ] Deacon operates the site for one full week with NO developer help.
- [ ] At least one real edit per day during that week.
- [ ] Developer is on standby but does not respond unless asked.
- [ ] At end of week, deacon signs off:
      "I can maintain this site without you."
- [ ] If the deacon can NOT sign off, sprint is NOT done. Identify the
      gaps and either fix them or schedule a follow-up session.

## Backup editor session (separate, 45 min)

Same as Parts 1–3 above, with the backup editor instead of the deacon.
Backup editor doesn't need the rollback drill or the one-week solo test,
but should complete one real edit before leaving.
