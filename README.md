# getfitflame.com

Static website for the FitFlame iOS app, hosted on GitHub Pages with the custom domain in `CNAME`.

- `/` home page
- `/support/` contact form (Formspree) and FAQ
- `/privacy/` Privacy Policy, generated with Termly
- `/terms/` Terms of Use (applies alongside Apple's standard EULA)

No build step: edit the HTML and push to `main`.

The app links to `/privacy/`, `/terms/` and `/support/`, so keep those paths stable.

## Updating the Privacy Policy

The policy text comes from Termly but is converted to plain HTML between the `PRIVACY POLICY` /
`END PRIVACY POLICY` markers so it matches the site. After any Termly re-export, re-apply these fixes,
which correct generator boilerplate that doesn't match how FitFlame works:

- Payment Data: remove "we may collect ... payment instrument number and security code" (Apple handles payments).
- Social logins: describe Sign in with Apple (user ID + optional email), not Facebook/X and friends lists.
- Location Data: approximate (city-level) location only, no GPS.
- AI "How to Opt Out": Termly leaves the list empty; list Not Now, Settings → AI processing, and deleting fits.
- Minors: 13, not 18, to match the Terms of Use.
- Personal information list: add outfit photos.
- Typos from the generator inputs ("o save", double periods).

## Updating the Terms

The Terms come from Termly the same way (between the `TERMS AND CONDITIONS` markers). After a re-export,
re-apply these fixes:

- Email: Termly used `nick@fitflame.com`; the real address is `nick@getfitflame.com`.
- Address: remove the `__________` street placeholder (Chicago, IL only) and the "company registered in Illinois"
  claim until an LLC exists.
- Contribution license (sections 2 and 12): Termly grants an unlimited, perpetual right to sell and use uploads in
  ads. Replace with the limited "solely to operate and provide the Services" license, which matches the Privacy
  Policy, and state that contributions are private (not viewable by other users).
- Refunds: "All sales are final and no refund will be issued" contradicts Apple's refund process; point to Apple.
- User registration: no passwords or usernames; describe the automatic account and Sign in with Apple.
- Purchases: remove shipping fees and card details; Apple charges payment and taxes.
- User data: remove "we perform regular routine backups" (not guaranteed on our plan).
- Typos: "one (1) years", "informal negotiations binding arbitration".
