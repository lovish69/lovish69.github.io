# Deploy with Lovish — portfolio

A responsive, dependency-free portfolio built from Lovish Barber's public GitHub profile and repository READMEs. No build step, paid hosting, API key, or backend required.

## Preview
Open index.html in a browser, or run `python3 -m http.server 3000` in this folder.

## Publish on GitHub Pages
Your account already has a `lovish69.github.io` repository. Inspect and back up its existing files first; do not overwrite work you want to keep. You can use that repository or create a separate public repository named `portfolio`.

1. Upload **the contents of this folder** to the repository root, not a nested portfolio folder. Make sure `index.html` and `CNAME` are at the root. `.nojekyll` is optional for this plain HTML site.
2. Commit to `main`.
3. Open repository **Settings → Pages**.
4. Under Build and deployment, choose **Deploy from a branch**, then **main**, **/(root)**, and Save.
5. Recommended: verify ownership first in your personal GitHub **Settings → Pages → Add a domain**. Enter `deploywithlovish.tech` and add the exact TXT record GitHub supplies at your authoritative DNS provider. Keep that TXT record after verification.
6. In the repository's **Settings → Pages → Custom domain**, enter `deploywithlovish.tech` and Save **before pointing DNS to GitHub**. Only one Pages repository should claim this domain.

## Connect Namecheap
In Namecheap: **Domain List → Manage → Advanced DNS → Host Records**.
These instructions apply when Namecheap BasicDNS, PremiumDNS, or FreeDNS manages DNS. If you use custom nameservers, edit the records at that provider instead. Do not switch nameservers without understanding existing email/website dependencies.

Add these records, with TTL set to Automatic:

| Type | Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | lovish69.github.io |

The CNAME target is **lovish69.github.io**, not deploywithlovish.github.io and not a repository URL. Do not include `https://` or a path.

Remove only conflicting website records for `@` and `www` (old parking records, URL redirects, or other A/AAAA/CNAME records pointing elsewhere). Preserve unrelated TXT, MX, and email records. Do not add wildcard DNS records.

After DNS propagates and GitHub's DNS check passes, enable **Enforce HTTPS** in the repository's Pages settings. DNS propagation and certificate availability can each take up to 24 hours. Test both `https://deploywithlovish.tech` and `https://www.deploywithlovish.tech`.

Official reference: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Update your content
- Edit text, styles, and the `projects` array inside `index.html`.
- Project data is curated, not live-synced; update the array when your work changes.
- Project summaries reflect public repository descriptions, not independent verification of deployments.
- The interactive hero is a perspective-rendered 3D cloud network drawn with Canvas. It supports dragging, keyboard arrow rotation, service selection, and pause/resume. It is illustrative, not a live monitoring panel.
- No CDN or external 3D library is required. Service buttons provide an accessible alternative to clicking the canvas. Project cards tilt on fine-pointer devices, with reduced-motion preferences respected.
- Email comes from your public GitHub profile. Confirm it before publishing.
- LinkedIn uses the intended profile path from your GitHub README, whose original URL was malformed; confirm the corrected URL before publishing.
- Education, internship details, and certifications were added from the user-supplied résumé. The internship employer was not specified, so none is named. The user confirmed the three certifications are earned, and their public Credly wallet lists them. Badge images, displayed expiry dates, and public-profile links were added from Credly. Network+ via Udemy is labeled coursework, not a CompTIA-issued certification. Percentage-based impact claims and case-count metrics were omitted.
- The original résumé PDF and phone number are intentionally not published in this package.
- The site includes project category filters, responsive layouts, keyboard focus styles, reduced-motion support, contact links, and a clipboard button with a text fallback.

## Status
The files are ready to publish. No changes have been made to your GitHub account, Namecheap account, or live DNS.

## Expanded portfolio sections
The page now includes the delivery lifecycle, three repository-based project deep dives with simplified architecture diagrams, an expanded toolkit, and a learning section. No employment or certification claims have been added.

## Résumé content review before publication
AWS Solutions Architect – Associate, AWS Cloud Practitioner, and CompTIA Security+ were confirmed by the user and found on their public Credly profile. The internship organization is still unspecified. Education dates are reproduced from the résumé; the 2025–2027 MCA is shown as in progress.

## Public credentials
Profile: https://www.credly.com/users/lovish-barber.1481ab50/badges/credly
The portfolio links to the public wallet, not the private edit page or individual badge assertions. AWS certifications expire 30 Jan 2028; Security+ ce expires 22 Nov 2027, as displayed on the public profile when checked. AWS Educate Networking is displayed separately as a training badge. Badge images are embedded so previews do not depend on external image access.
