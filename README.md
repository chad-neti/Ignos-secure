# Ignis Secure Limited - Website (Phase 1)

Static HTML/CSS site for Ignis Secure Limited, Fire & Security Specialists, West London.
No frameworks and no build step. Deploy the repository root as-is to any static host
(Cloudflare Pages, Netlify or Vercel).

## Pages live in this phase

| URL | Page |
|---|---|
| `/` | Home |
| `/fire-alarm-installation/` | Fire Alarm Installation (service page) |
| `/fire-alarm-installation-uxbridge/` | Local page #1: Uxbridge |
| `/blog/how-often-should-a-fire-alarm-be-serviced/` | Blog post #1 |

All other services (maintenance, CCTV, access control, electrical) appear on the home
page as plain text cards with phone CTAs only. Per the SEO plan, nothing links to an
unbuilt page. Future towns in "Areas We Cover" are plain text; only Uxbridge is linked.

## IMPORTANT: placeholders to replace before launch

Search and replace these across ALL files. They are deliberate placeholders:

| Placeholder | Where | Replace with |
|---|---|---|
| `01895 000 000` and `+441895000000` | every page (tel links, schema) | the real phone number, identical everywhere (NAP consistency) |
| `info@ignissecure.co.uk` | every page | the real email address |
| `https://www.ignissecure.co.uk` | canonicals, schema, sitemap, robots | the real domain, once chosen. Pick www or non-www and 301 the other |

Also still to do:

- [ ] Add the real business address to the `LocalBusiness` schema in `index.html`
      and to the footer, matching the Google Business Profile character for character
- [ ] Add `openingHours` and `sameAs` (Google Business Profile URL) to the
      `LocalBusiness` schema once available
- [ ] The contact form uses Netlify Forms (`data-netlify="true"`). If hosting
      elsewhere, swap the form to Formspree or Web3Forms and update the `action`
- [ ] Add GA4 and verify the site in Google Search Console
- [ ] Submit `sitemap.xml` in Search Console and request indexing for all 4 pages
- [ ] Update `lastmod` dates in `sitemap.xml` when pages change

## Structure

```
index.html                                   Home
fire-alarm-installation/index.html           Service page
fire-alarm-installation-uxbridge/index.html  Local page
blog/how-often-should-a-fire-alarm-be-serviced/index.html
assets/css/style.css                         All styling (design tokens at the top)
assets/js/main.js                            Mobile nav toggle only
assets/img/                                  Logo (WebP + PNG fallback), favicon
robots.txt, sitemap.xml
```

## Adding the next location page

1. Copy the structure (not the text) of `fire-alarm-installation-uxbridge/index.html`
2. Write at least 60-70% unique content for the new town
3. Add the URL to `sitemap.xml`
4. Convert the town's plain-text entry in "Areas We Cover" (home page and footers)
   into a link, sitewide
5. Request indexing in Search Console
