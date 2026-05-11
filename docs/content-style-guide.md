# Content Style Guide

This guide is for anyone writing or editing content on this site —
articles, suggestions, equipment notes, issue descriptions.

## Voice

- **Plain English. Sixth-to-eighth grade reading level.**
- **No jargon without definition.** First time you use a term like
  "gain staging" or "phantom power," explain it in plain words.
- **Short sentences. Short paragraphs.**
- **Direct address.** "If you hear feedback, do X" — not "in the event of feedback, one should..."

## Articles

- Aim for **400–800 words.** Anything longer should probably be two
  articles.
- Start with **what the volunteer will get out of reading it.**
- End with **what to do next** — link to the troubleshoot page or the
  related equipment.
- Add a **Last updated** date and bump it whenever you make a real change.

## Suggestion rules

Every suggestion has the same structure for safety:

1. **Check first** — safe checks that can't damage anything. List 3–5.
2. **Safe fix** — actions a volunteer with basic knowledge can take.
3. **Escalation trigger** — one clear sentence: when to stop and ask.
4. **Do NOT do** — list anything that could damage gear or make things
   worse. Be specific.
5. **Replacements** — only for symptoms where buying new gear is the
   answer. Always include price range, source URL, and lastVerified date.

**Confidence levels:**

- `high` — Reviewer is confident this is correct in our context.
- `medium` — Generally true but depends on situation; reviewer should
  flag any caveats in the body.
- `needs-review` — Default for AI-drafted rules; can't be `approved`
  in this state.

## Equipment

- **public_notes**: Anything visitors should know — what it's for, where
  it lives, any quirks.
- **internal_notes**: Serial numbers, purchase info, donor info,
  storage codes, anything sensitive. This field NEVER renders publicly.
- **Photos**: Take in storage when possible. Avoid photos with
  identifiable people. Re-export at ≤1600px width before uploading.

## Issues

- **Plain description**: Tell the story. When did it happen? What did
  you hear or see? What did you try? Past tense, conversational.
- **Attempted fixes**: A list of what's already been tried (and whether
  it worked).
- **Resolved issues stay public** so volunteers can search the archive.

## Review and freshness

- Run the [review checklist](/docs/review-checklist.md) monthly.
- Suggestions older than 12 months display a "stale" warning on the
  site. Re-verify and bump `lastVerified` to clear the warning.
- Equipment marked `retired` / `loaned` / `missing` is excluded from
  suggestion matching but stays in the archive.
