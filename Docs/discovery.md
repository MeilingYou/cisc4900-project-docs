# Bubble Discovery Notes (Week 2)

**Date:** 1/30/2026 – 2/8/2026  
---

## Access / Environment Notes
- I do not have permission to duplicate the Bubble app (shared access).
- Work will be done in **Development** and/or by building **temporary v2 pages** (e.g., `login_v2/signup_v2`) if needed.
- I will not deploy changes to Live unless approved by the project owner/supervisor.

---

## Pages

### Login page
- **Page name in Bubble:** `sign-in`
- **Type of content (page settings):** TBD (need to confirm)
- **Current layout/structure:** Split layout. Left side is the login form panel; right side contains informational content (“System Maps” / “Emergency Profiles”).
- **Current input fields shown:** Email, Password  
  - **Planned change:** Email field becomes **“Username or Email”** (per Figma)

### Signup page
- **Page name in Bubble:** `sign-up`
- **Type of content (page settings):** TBD (need to confirm)
- **Current layout/structure:** Similar split layout. Left side is sign-up form panel; right side informational content.
- **Current input fields shown:** Name, Email, Password, Re-enter Password  
  - **Planned change (per Figma):** Replace **Name** with **@Username (handle)**; use **Confirm Password** wording

---

## Data Model (Handle / Username / Slug)

### Confirmed fields found
- **Data type: User**
  - **Username** (text)
  - **Slug** (built-in field)
- **Data type: Alter**
  - **Custom Slug** (text)

### Supervisor-confirmed requirements
- “Username” is the **handle** used in the URL slug (does not need to match display/account name).
- URL format: **`domain/page/username`**
- Old paths must be preserved using **`/s/`** and **`/p/`** so automatic redirects still work when updating domain.
- Auth pages should **match Figma** and **replace existing login/signup**.
- Handle must be **unique**; suggested **minimum 4 characters**.

---

## URL / Routing Behavior
Confirmed:
- Page s → Type of content: User
- Page p → Type of content: User
- Routing uses the User’s Slug (because the page context is “Current page User”, and the URL is /s/<slug> and /p/<slug>)

---

## Differences vs Figma (Quick Gap List)

### Login
- **Figma:** Username or Email + Password  
- **Current:** Email + Password (update needed)

### Sign Up
- **Figma:** @Username, Email, Password, Confirm Password  
- **Current:** Name, Email, Password, Re-enter Password (replace Name with @Username)

### Text / Layout
- Figma includes “Terms of Service” + “*Spam or abusive accounts will be removed” (verify exact wording)
- Supervisor: “Match Figma. Replace old login signup.”
- Current: split layout with right-side info content (will be updated to match Figma)

---

## Evidence Captured / To Capture

### Captured
- `Evidence/login_current.png`
- `Evidence/signup_current.png`
- `Evidence/login_figma.png`
- `Evidence/signup_figma.png`
- `Evidence/data_user_username_slug.png`
- `Evidence/data_alter_custom_slug.png`
- `Evidence/test_s_tester.png`
- `Evidence/test_p_tester.png`
- `Evidence/page_s_type_of_content.png`
- `Evidence/page_p_type_of_content.png`
- `Evidence/workflow_login.png`
- `Evidence/workflow_signup.png`
- `page_list_showing_v2_pagespng`
- 

---

## Next Steps (Week 2)
1) Confirm pages `s` and `p` settings to preserve `/s/` and `/p/` paths.
2) Review login/signup workflows and document actions in order.
3) Implement handle rules in signup:
   - minimum length **4**
   - **unique** across accounts
4) Update login/signup UI to match Figma and replace existing pages (in Development; use v2 pages only if needed for safety/review).
