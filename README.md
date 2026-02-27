## Draft version of the app, updating before pushing to main
- https://mbo.my.id/version-52pzt/
- Login: https://mbo.my.id/version-52pzt/sign-in
- Sign-up: https://mbo.my.id/version-52pzt/sign-up

## Current Phase
### Done
- Completed Figma-aligned UI updates for Sign Up and Log In (Draft / version-52pzt)
- Implemented and tested basic login + signup workflows to match the updated UI
- Verified /s/<slug> and /p/<slug> pages still load correctly using a test user (ex: tester)
### In Progress
- Preparing and organizing evidence screenshots + documenting final UI/workflow decisions in GitHub
- Defining username rules for signup (minimum 4 characters + unique)
### Next
- Implement username → slug behavior on account creation:
- validate handle (min 4 + unique)
- save handle to User.Username
- ensure the handle becomes the user’s slug for routing
- Re-test end-to-end signup/login using a new test user and confirm redirects + routing still work

## Semester Goals

### 1) UI Update (Auth Pages)
- Update Sign In / Sign Up pages in Bubble to match the Figma designs

### 2) Username → Slug Routing
- On account creation, set the user’s handle/username to become the **User slug**
- Preserve existing MVP paths using `/s/` and `/p/` for redirects

### 3) Research Function (Invite a Connection for Private Pages)
- Research and propose the most efficient approach to let users invite/request connections when a page is set to private
- Evaluate options such as:
     - a user-specific invitation link for existing accounts
     - a request-access workflow that allows a user to ask for connection without seeing the full private page
- Document the recommended approach with basic data flow + workflow steps (and any constraints/risks) before implementation
