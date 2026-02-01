# Bubble Discovery Notes (Pre-Start)

Date: 1/30/2026 - 2/1/2026
Goal: Identify where login/signup UI and account creation logic live in Bubble so implementation can be planned safely.

---

## Access / Environment Notes
- I do not have permission to duplicate the Bubble app (shared access).
- Work will be done in Development and/or by building new pages (e.g., login_v2/signup_v2) if required.
- IMPORTANT: I will not deploy changes to Live unless approved by the project owner/supervisor.
---

## Pages
### Login page
- Page name in Bubble: sign-in
- Type of content (page settings): Likely none / blank (TBD)
- Notes about layout/structure:
  - Current layout appears split: left side is the login form panel; right side contains informational content (“System Maps” / “Emergency Profiles”).
  - Left panel includes branding/logo (“ONE”), title “Login”, input fields, primary login button, and links.
  - Current input fields shown: Email, Password (needs to become “Username or Email” per Figma).

### Signup page
- Page name in Bubble: sign-up
- Type of content (page settings): Likely none / blank (TBD)
- Notes about layout/structure:
  - Similar split layout: left side is sign-up form panel; right side informational content.
  - Current input fields shown: Name, Email, Password, Re-enter Password
  - Terms checkbox exists but wording may differ from Figma.


## Data Model (Username / Slug)
### Where username/custom slug is stored
- Data type: TBD (most likely User, but could be Profile/Account)
- Notes / questions:
  - Task requirement: username should become the slug for the account URL on account creation.
  - Existing MVP users: their current custom slug would be treated as their username.
  - Need to confirm where MVP “custom slug” currently lives and whether it’s already on User or stored elsewhere.

---

## URL / Routing Behavior
### After signup redirect
- Redirect action found in signup workflow: TBD (likely Navigation → Go to page)
- Destination page name: TBD
- Data sent (if any): TBD (ex: Current User / Profile)
- Expected URL format (based on task): username becomes slug for account URL
- Current URL behavior observed: TBD
  - Need to verify whether profile/account page uses “Type of content” and how slugs are currently configured.

---

## Differences vs Figma (Quick Gap List)
- Login:
  - Figma requires input “Username or Email” + Password.
  - Current Bubble shows Email + Password (needs update).
- Sign Up:
  - Figma requires @Username, Email, Password, Confirm Password.
  - Current Bubble shows Name, Email, Password, Re-enter Password (needs update; replace Name with @Username).
- Text/wording:
  - Figma uses “Terms of Service” and includes “*Spam or abusive accounts will be removed”.
  - Current Bubble wording may differ (needs verification).
- Layout:
  - Figma shows a centered auth form design on dark background.
  - Current Bubble uses a split layout with additional right-side informational content (needs decision: keep or remove).

---

## Evidence Captured / To Capture
- Bubble current screenshots (before):
  - login_current.png (captured)
  - signup_current.png (captured)
- Figma reference screenshots:
  - login_figma.png (captured)
  - signup_figma.png (captured)

---

## Next Steps (Pre-Start)
1) Confirm Bubble page names (login/signup) from page dropdown and update this doc.
2) In Workflow tab:
   - Identify exact login and signup events and list actions in order.
3) In Data tab:
   - Find where username/custom_slug is stored (User vs Profile vs Account) and record exact field names.
4) Confirm required URL format with supervisor (e.g., /user/slug or /@slug).
5) Decide implementation approach:
   - Modify existing pages vs create login_v2/signup_v2 pages for review.
6) Define slug rules:
   - allowed characters, uniqueness check, case handling, and migration for MVP users.
