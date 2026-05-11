# Editor Guide: How to add and update content

This guide is for the deacon and any backup editor. You do NOT need to
know any code to edit the site. Everything happens in forms.

## Signing in

1. Go to `https://YOUR-SITE.netlify.app/admin` (or the custom domain
   if one is configured).
2. Click "Login with GitHub."
3. Sign in with your GitHub account.

If this is your first time, you may also need to authorize Decap CMS to
access the repository. Click "Authorize" when GitHub asks.

## What you'll see

The admin area has six sections in the sidebar:

- **Equipment** — Inventory items
- **Issues** — Current and past sound problems
- **Suggestion rules** — Troubleshooting tips
- **Board scenes** — Saved board states
- **Education articles** — Plain-language teaching content

Click any of them to see the existing entries and add new ones.

## Adding a new piece of equipment

1. Click **Equipment** in the sidebar.
2. Click **New Equipment**.
3. Fill in:
   - **Reference ID** — A short label with no spaces, e.g.
     `sm58-vocal-mics`. This becomes the URL.
   - **Friendly name** — What the equipment is, in plain words.
   - **Category** — Pick from the dropdown.
   - **Make / Model** — The brand and model name.
   - **Quantity** — How many we have.
   - **Status** — Active, retired, loaned, or missing.
   - **Where it lives** — Sound booth, mic locker, stage, etc.
   - **Photo** — Optional. Take a photo with your phone in good light.
   - **Public notes** — What anyone visiting the site should know.
   - **Internal notes** — Serial numbers, donor info, purchase records.
     **This field never shows on the public site.**
4. Click **Publish**. The change goes live in about 30 seconds.

## Logging a new issue

1. Click **Issues** → **New Issue**.
2. Fill in:
   - **Title** — A short summary.
   - **Affected equipment ref-id** — Optional. If the issue is about a
     specific piece of gear, put its ref-id here.
   - **Symptom** — Pick a value from the symptoms list (e.g.
     `cable-crackle`, `feedback`, `settings-drift`).
   - **Severity** — Low, medium, high.
   - **Status** — Open if new, Recurring if it keeps happening,
     Resolved if it's fixed.
   - **First seen / Last seen** — Dates.
   - **Attempted fixes** — What's already been tried.
   - **Plain description** — Tell the story.
   - **How reported** — `cms` if you logged it directly, `form-promoted`
     if it came from a volunteer's form submission.
3. Click **Publish**.

## Promoting a volunteer's form submission into an issue

1. Open your email (or the Netlify dashboard → Forms).
2. Find the volunteer's form submission.
3. In the admin area, click **Issues → New Issue**.
4. Fill in the form using the details from the submission. Set
   "How reported" to `form-promoted`.
5. Publish.
6. Delete the original form submission from Netlify (optional).

## Updating a suggestion rule

1. Click **Suggestion rules**.
2. Click the rule to edit.
3. **Important:** If the rule was previously `approved` and you change
   the advice meaningfully, demote it to `reviewed` and have the
   experienced sound reviewer re-approve it before publishing.
4. If you're just refreshing prices on replacement gear, update the
   `lastVerified` date to today.
5. Click **Publish**.

**Note**: The build will refuse to publish a rule with status `approved`
that's missing `reviewedBy`, `reviewedDate`, or `lastVerified`. If your
publish fails, check those fields.

## Adding a board scene

1. Photograph the board after a known-good service.
2. Click **Board scenes → New Scene**.
3. Pick the board type — digital or analog.
4. For digital: enter the scene number on the board.
5. For analog: also upload a labeled channel diagram if you have one.
6. Add per-channel notes (one line per channel).
7. Publish.

## Writing an article

1. Click **Education articles → New Article**.
2. Use the [content style guide](./content-style-guide.md) for voice.
3. Aim for 400–800 words.
4. Pick a `level` (beginner / intermediate) and an estimated reading
   time.
5. Set `updated` to today.
6. Publish.

## Editing existing content

Same as adding, but click an existing entry instead of "New." The form
loads with the current values; change what you need and publish.

## Photos

- Take photos in good light.
- Avoid photos with identifiable people in them.
- Crop to just the equipment when possible.
- Decap auto-resizes large photos, but the build will FAIL if any image
  exceeds 500 KB. Use phone "share → reduce size" or any image editor.

## What if I make a mistake?

Two ways to fix:

1. **Edit the entry** through the admin — usually faster.
2. **Roll back the commit** — open the GitHub repo, find the commit
   from your edit, and click "Revert." The site rebuilds with the
   previous state.

If you can't figure out how to fix something, contact the developer.

## Monthly routine

See the [review checklist](./review-checklist.md) for the monthly
content-maintenance pass.
