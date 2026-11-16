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
