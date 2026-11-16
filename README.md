# getfitflame.com

Static website for the FitFlame iOS app, hosted on GitHub Pages with the custom domain in `CNAME`.

- `/` home page
- `/support/` contact form (Formspree) and FAQ
- `/privacy/` Privacy Policy
- `/terms/` Terms of Use (applies alongside Apple's standard EULA)

No build step: edit the HTML and push to `main`.

The app links to `/privacy/`, `/terms/` and `/support/`, so keep those paths stable. When the app starts
sharing data with a new service, update the provider table in the Privacy Policy and its date.
