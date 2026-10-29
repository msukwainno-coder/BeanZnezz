BEANZNEZZ — HTML/CSS/VANILLA JAVASCRIPT FRONTEND
================================================

WHAT IS INCLUDED
----------------
This ZIP contains a static, responsive frontend demonstration for BeanzNezz,
a dating and lifestyle platform intended for adults aged 18+ in Malawi.

Required root files:
  index.html
  signup.html
  login.html
  browse.html
  profile.html
  search.html
  likes.html
  matches.html
  messages.html
  notifications.html
  membership.html
  payment.html
  settings.html
  safety.html
  admin.html
  style.css
  script.js
  README.txt

HOW TO PREVIEW
--------------
1. Extract the ZIP.
2. Open index.html in a modern browser.
3. Navigate through the links in the header and footer.
4. Use fictional information only. Do not enter real passwords or sensitive
   personal details into this demonstration.
5. Some sample profile photos load from Unsplash, so an internet connection
   is needed for those images. The rest of the site is local static content.

GITHUB PAGES DEPLOYMENT
-----------------------
1. Sign in to GitHub and create a new repository.
2. Extract this ZIP on your device.
3. Upload all 18 files directly into the repository root. Do not upload a
   nested parent folder.
4. Open the repository's Settings.
5. Select Pages from the sidebar.
6. Under the build/deployment source, choose "Deploy from a branch".
7. Select the main branch and the /(root) folder, then save.
8. Wait for GitHub Pages to publish. Open the published URL shown in the
   Pages settings. The site's index.html is the entry point.

No build command or framework is required. Links are relative, and the CSS
and JavaScript are shared across pages.

IMPORTANT LIMITATIONS
---------------------
This is Stage 1 only: a static frontend. It is not a live dating service.
No account is securely created, no password is authenticated, no real
messages are sent, no payment is processed, and no administrator controls
are protected. Browser storage and client-side JavaScript can be modified
by a visitor and must never be treated as secure enforcement.

The demo includes:
- Responsive shared navigation and active-page styling.
- Registration validation and a login preview.
- A five-step profile wizard and public-preview layout.
- Sample profiles, search, age/location/gender filtering, likes, matches,
  notifications, and sample chat.
- A client-side illustration of one introductory message per match.
- Membership price cards and a payment demonstration.
- Settings previews, safety guidance, report/block previews, and an admin
  dashboard with sample figures.

BACKEND REQUIREMENTS BEFORE PRODUCTION
--------------------------------------
1. Authentication: secure signup/login, email/phone verification, password
   hashing, recovery, session management, logout, and abuse/rate limiting.
2. Database entities: users, profiles, profile photos, photo permissions,
   likes, matches, conversations, messages, membership plans, subscriptions,
   payments, payment events, reports, blocks, notifications, and admin audit
   logs. Add migrations, indexes, retention policies, and backups.
3. Authorization: enforce ownership and roles on every API request. Never
   trust browser-supplied user IDs, plan names, payment states, or permissions.
4. Privacy: keep legal name, date of birth, contact details, boundaries, and
   other sensitive fields private by default. Public profile APIs must return
   only fields explicitly intended for public display.
5. Private photos: store in private object storage and issue short-lived,
   authorized access links only after backend permission checks.
6. Membership entitlements: calculate active entitlements server-side based
   on verified subscription records. Never activate paid membership from a
   frontend click.
7. Introductory message rule: enforce one introductory message per match on
   the server, with atomic checks to prevent race conditions and browser
   JavaScript bypasses. Check entitlement for every subsequent send.
8. Super Elite privacy: exclude private/non-discoverable profiles from normal
   discovery and search at the database/API layer. Do not rely on CSS or
   client-side filtering.
9. Payments: integrate a trusted payment provider; verify provider callbacks
   or webhooks on the server; validate amount, currency, reference, status,
   replay protection, and idempotency before activating membership. Never
   collect raw card details in this static site.
10. Moderation: real report/block queues, review states, appeals, evidence
    access controls, abuse prevention, administrator roles, and immutable
    audit logging.
11. Security and operations: HTTPS, CSRF/XSS protections where applicable,
    input validation, output encoding, secure headers, logging, monitoring,
    incident response, backups, privacy policy, terms, and data deletion.
12. Testing: accessibility, responsive layouts, API authorization, payment
    verification, privacy leakage, abuse/rate limits, and recovery flows.

GITHUB PAGES NOTE
-----------------
GitHub Pages hosts static frontend files only. It does not provide the
authentication, database, secure photo access, payment verification,
messaging service, or server-side access controls needed for production.
Choose and deploy a backend service before inviting real members.
