# Implementation Plan (Week 2)

## Goal
Update `sign-in_v2` / `sign-up_v2` to match Figma and implement **handle → slug** behavior without breaking existing `/s/` and `/p/` routes.

## Reference
Current-state screenshots + findings are documented in `Docs/discovery.md` (source of truth for “what exists”).

## Work Strategy
- Make changes in **Development only**.
- Use **v2 pages** for iteration until supervisor approves switching/replacing original pages.

---

## Milestone 1: UI matches Figma (v2 pages only)

### Tasks
- **Login (v2):** change label/placeholder to **“Username or Email”**
- **Sign Up (v2):** replace **Name** input with **@Username/Handle** input; update **Confirm Password** wording

### Done when
- v2 pages visually match Figma for **fields, labels, and button text**

### Test
- Preview v2 pages and verify **layout + navigation links** still work

---

## Milestone 2: Handle validation (before writing anything)

### Rules
- Minimum **4** characters
- **Unique** (no duplicate handles)

### Implementation approach
- Add checks in signup workflow **before saving** handle

### Done when
- Duplicate handle is blocked with a clear message
- Short handle is blocked with a clear message

---

## Milestone 3: Set handle and confirm slug behavior

### Tasks
- After signup, store handle in the agreed field (**User.Username** or new field)
- Confirm whether slug is automatically derived or needs a workflow action / backend step

### Open question
- Does Bubble allow direct “set slug,” or do we set a field and let slug derive from it?

### Done when
- New user account results in correct URL behavior for the user’s profile/system pages

---

## Milestone 4: Routing regression test

### Must not break
- `/s/tester`
- `/p/tester`

### Done when
- Existing slugs still load correct pages using **Current page User** context

---

## Milestone 5: Login decision (requires supervisor confirmation)

### If required now
“Username or Email” login will need either:
- email login only (UI text updated but behavior unchanged), OR
- username lookup → login flow (custom step)

### Blocked until
- Supervisor confirms whether username login is required in Week 2–3 scope

---

### Sign Up (v2) — Username Info Icon / Tooltip
- Add an info (“i”) icon next to the @Username input on `sign-up_v2` (per Figma).
- Workflow: When info icon is clicked → Toggle/Show/Hide the tooltip element.
---

## Acceptance Checklist
- [ ] v2 UI matches Figma
- [ ] handle validation works (min length + unique)
- [ ] new user handle is stored correctly
- [ ] `/s/` and `/p/` still work
- [ ] login works at least by email (username login only if approved)
