# The Walling Legacy

A polished, mobile-responsive, **dependency-free static website** plus a careful evidence audit. Prepared October 25, 2026. The design uses HTML and CSS only; there is no tracking, remote JavaScript, build step, paid font or runtime dependency.

## Contents

- `index.html` — complete one-page illustrated website with accessible navigation, family tree, historical narrative, evidence statuses, visual archive, land narrative, veteran-housing vision and source ledger.
- `assets/` — four locally stored, rights-reviewed historical photo/artwork files. They are required for the illustrated layout; upload this folder unchanged.
- `RESEARCH.md` — 15-claim confidence matrix, era-by-era military scope, records to order, image-rights register, and publication cautions.

## Preview locally

Double-click `index.html` or run a local static server with `python3 -m http.server 8000` in this folder and visit http://localhost:8000. The file also works directly through a `file:` URL.

## Push to GitHub

1. Create a new empty GitHub repository, e.g. `walling-legacy` (keep it private until the family has reviewed the sensitive genealogical claims).
2. Upload `index.html`, `RESEARCH.md`, and `README.md` to the repository root, or from this folder run:

   ```bash
   git init
   git add index.html RESEARCH.md README.md assets
   git commit -m "Initial sourced Walling legacy site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USER/walling-legacy.git
   git push -u origin main
   ```

3. Replace `YOUR-USER` with your GitHub account; authenticate through your usual GitHub flow. No git commands were run on your behalf.

## Deploy on Cloudflare Pages

1. In Cloudflare dashboard, go to **Workers & Pages → Create application → Pages → Connect to Git** (menu wording may vary).
2. Select the GitHub repository and the `main` branch.
3. Choose **no framework** / static HTML. Leave **build command blank** (or use `exit 0` if the UI requires one) and set **build output directory** to `/` or the repository root as the interface expects.
4. Deploy. Since `index.html` sits in the root, Cloudflare Pages serves it at the generated `*.pages.dev` address.
5. Optional: add a custom domain from the Pages project's Custom domains settings and follow the DNS verification steps.
6. Keep the deployed preview access-restricted or private until title, family tree and permission checks have been completed. Cloudflare deployments from a public Pages address are otherwise publicly accessible.

## Before publishing to the Walling family

- Ask them to review names, relationships, service records and imagery, explicitly offering a correction mechanism.
- Complete the high-priority record orders in `RESEARCH.md`, most importantly the Gabriel–Jesse link, Robert M. Walling's kinship and the present legal property owner.
- Four site images are now included with attribution: original Walling Pond photograph (CC BY-SA 3.0) and three contextual public-domain illustrations. See `RESEARCH.md` for dates, creator and full rights register. They do **not** establish identities of ancestors or military uniforms for the family.
- Original newspaper pages are linked; the site-created newspaper-style graphics are **summaries, not reproduced clippings**. Get reuse clearance before installing page screenshots or crops. The 2012 ODFW image remains available separately under CC BY-SA 2.0 if desired.
- Verify that the pond listing and zoning are still current, and keep the veterans project language conditional.

## Design system

Deep forest green (`#10251f`), warm historical paper (`#f8f5ed`), and muted gold (`#d6b16a`); large editorial serif headlines and neutral system UI annotations. Responsive break at 760px. The pond is an original abstract CSS visualization, not a survey or photo.
