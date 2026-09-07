# tendays.app

The public website for TENdays: home page, the account-deletion page Google Play
requires, and the privacy notice. Plain HTML and CSS, no build step, hosted on
GitHub Pages from the `main` branch of this repository, with the custom domain
`tendays.app` (the `CNAME` file).

Colours, radii and fonts come from the TENdays Design Manual, the same tokens
the app uses (`src/theme/tokens.ts` in the app repo). Fonts load from Google
Fonts: Bricolage Grotesque (display) and Instrument Sans (body).

## Editing

Edit the HTML files directly and push to `main`; GitHub Pages redeploys within a
minute or two. Every page repeats the same header and footer, so a change to
those is a change in each file.

- `index.html` — home page
- `delete-account/index.html` — the URL given to Google Play's Data safety form
- `privacy/index.html` — interim notice until the solicitor-reviewed policy lands
- `assets/style.css` — the one stylesheet
- `assets/mark.svg` — the ten-dots mark (2 × 5, last dot Bunting red)

## DNS (GoDaddy)

For the apex `tendays.app`, four A records pointing at GitHub Pages:
185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153.
For `www`, a CNAME to `tendays-app.github.io`. Mail records (Resend) are
untouched. GitHub issues the HTTPS certificate once the records resolve.
