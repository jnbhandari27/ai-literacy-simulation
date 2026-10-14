# AI Literacy Simulation — hosting guide

A single static page (`index.html`). No build step, no backend, no analytics, nothing is stored.

## Deploy on Vercel (about 2 minutes)

**Option 1 — command line**
1. Unzip this folder and open a terminal inside it.
2. Run `npx vercel --prod` (first run asks you to log in; accept the defaults, leave "build command" and "output directory" blank).
3. Vercel prints a URL like `https://your-project.vercel.app` — that is the link to put in the Google Form.

**Option 2 — GitHub**
1. Push this folder to a new GitHub repository.
2. On vercel.com choose Add New → Project → import the repo → Deploy (no settings needed).

Any other static host (Netlify, GitHub Pages, Cloudflare Pages) works the same way.

## Completion code

The page ends by showing the code `CALIB-4729` (set at the top of the `<script>` as `COMPLETION_CODE`).
In the Google Form, make the code question *Required* and add response validation:
Text → Contains → `CALIB-4729`.
If you change the code in `index.html`, change the validation to match and redeploy.

## Before you circulate

- Open the live URL on a phone and a laptop and click through once.
- Do not switch on Vercel Web Analytics for this project — the page tells respondents nothing they tap is stored.
- `vercel.json` adds a no-index header so the page stays out of search results.
