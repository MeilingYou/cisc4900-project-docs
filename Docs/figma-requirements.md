# Figma Requirements — Login & Sign Up Pages

Date: 2026-1-31
Source: Figma screenshots provided (Login / Sign Up)

Purpose: This document captures the UI requirements from Figma that the Bubble Login and Sign Up pages must match (layout, fields, text, and key elements).

---

## Global Styling / Layout (Both Pages)
- Overall theme: dark background, light text
- Branding:
  - “ONE” logo at the top-left
  - Bottom-left text: “MULTIPLIED BY ONE HUB”
- Form layout:
  - Single main auth form area (card/panel) with a clear title at top
  - Inputs stacked vertically with consistent spacing
  - Primary CTA button below inputs
  - Secondary links beneath button
- Color accents:
  - Primary button uses a strong pink/red accent
  - Links use a bright green accent (Sign Up / Log In / Forgot Password / Terms of Service)

---

## Login Page (Figma)

### Page Title
- Title text: **Login**

### Inputs (in order)
1) **Username or Email**
2) **Password**

### Primary Button
- Button label: **Login**

### Secondary Text / Links (below button)
- Text: **Already have an account?**  
  - Link: **Sign Up**
- Link: **Forgot Password?**

### Notes
- “Sign Up” and “Forgot Password?” appear as green links in the design.
- Keep spacing clean and consistent between title → inputs → button → links.

---

## Sign Up Page (Figma)

### Page Title
- Title text: **Sign Up**

### Info icon next to @Username: 
- Clicking/tapping the icon toggles a short explanation that the @Username will be used as the user’s URL slug (for `/s/<username>` and `/p/<username>` pages).

### Inputs (in order)
1) **@Username**
2) **Email**
3) **Password**
4) **Confirm Password**

### Primary Button
- Button label: **Sign Up**

### Secondary Text / Links (below button)
- Text: **Already have an account?**  
  - Link: **Log In**

### Terms / Consent
- Checkbox with text: **By signing up, you agree to our Terms of Service**
  - Link: **Terms of Service** (green link)

### Additional Note
- Footer note text: **\*Spam or abusive accounts will be removed**

### Notes
- A small info/icon appears near the username area in the design (confirm whether this is required for v1).
- Keep field order exactly as shown and align spacing with the login page styling.

---

## Implementation Reminders (for Bubble)
- Login placeholder should accept **“Username or Email”** (not email-only).
- Signup must include a **Username** field (with “@Username” placeholder).
- Text should match Figma exactly (including “Terms of Service” wording and the spam/abuse note).

