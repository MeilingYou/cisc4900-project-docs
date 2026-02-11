# Task Tracker (CISC 4900) — Bubble Auth + Username/Slug Routing

**Last updated:** 2026-02-08  
**Scope this week:** Discovery + safe v2 UI iteration (sign-in_v2 / sign-up_v2) + workflow review (no breaking changes)

---

## Done (Week 2)

### Discovery + Evidence
- Identified where current auth pages live in Bubble (`sign-in`, `sign-up`) and documented current vs Figma gaps.
- Confirmed routing pages `s` and `p` use **Type of content = User** and rely on **Current page User’s Slug**.
- Preview-tested routing with real slug **tester** (`/s/tester`, `/p/tester`) and captured screenshots with URL visible.
- Captured evidence screenshots for:
  - current login/signup
  - figma login/signup
  - data fields (User.Username / User.Slug, Alter.Custom Slug)
  - workflows (login + signup)
  - page settings for `s` and `p`

### Documentation
- Wrote/updated Discovery Notes (Week 2) and maintained evidence checklist.
- Drafted an implementation plan outline (focus: safe v2 iteration + username/slug requirements).
- Set up repo structure (Docs / Evidence / Deliverables / Timelog) and updated README/Changelog entries.

### v2 Page Iteration (Safe UI Changes)
- Reviewed `sign-in_v2` and `sign-up_v2` as the safe sandbox for UI changes.
- Located the correct input groups in the Element Tree (email/password groups) to avoid editing the original pages.
- Started updating v2 labels/placeholders toward Figma:
  - `sign-in_v2`: Email label → “Username or Email”
  - `sign-up_v2`: identified the “Name” input to replace with “@Username/Handle”
  - Confirm Password wording aligned toward Figma
- Ran quick Development previews after edits to confirm layout didn’t break and navigation links still work.

---

## In Progress (Week 2 Day 3)

### v2 UI Completion (Match Figma exactly)
- Finish updating `sign-in_v2` UI text to match Figma:
  - Title text (“Log In” vs “Login”) — verify exact Figma wording
  - Input labels/placeholders
  - Button text
  - Secondary links placement/text
- Finish updating `sign-up_v2` UI text to match Figma:
  - Replace “Name” with “@Username/Handle”
  - Confirm Password label/placeholder wording
  - Terms of Service checkbox + link
  - “Spam or abusive accounts will be removed” footer note
  - Add the info icon near username and plan the toggle behavior (popup/group)

### Workflow Review (No changes yet)
- Re-open workflow Step 2 redirects for sign-in and sign-up and document:
  - where user is sent after login/signup
  - what data (if any) is sent to the destination page

---

## Blocked / Needs Confirmation
  - Where should the handle be stored:
    - `User.Username` (existing field) vs a new field
  - How to set the URL slug:
    - auto-slug from Username vs workflow step vs backup URL field
  - Should the **right-side informational panel** stay or be removed to match Figma exactly?

---

## Next Tests (After workflow updates)
- Test new signup with a fresh user:
  - handle min length (4+)
  - handle uniqueness (no duplicates)
  - slug generation matches expected `/s/<slug>` and `/p/<slug>`
- Test login flow:
  - email login still works
  - if username login is required, test the lookup approach + error messages
- Confirm redirects go to the correct page after login/signup.

---

## Links / Evidence Notes
- Evidence is stored in `/Evidence/` with screenshots for:
  - current vs figma auth pages
  - workflow screenshots (login/signup)
  - page settings for `s` and `p`
  - routing test using slug `tester`
