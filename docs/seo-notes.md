# SEO notes for the redesign draft (not served)

Prepared with the October 2026 redesign draft. Not yet applied live.

## Already ranking, do not break

- nivelatolabs.com ranks #1 for "Nivelato Labs" and for "Nivelato".
- The homepage title "Nivelato Labs - Software that measures up" is the ranking title. The draft keeps it exactly.

## Draft implements

- Per-page titles and meta descriptions, canonical URLs, Open Graph and Twitter cards on Home, Products, and About.
- Organization and WebSite JSON-LD on the homepage, AboutPage JSON-LD on About.
- sitemap.xml and robots.txt at the site root, listing the new Home / Products / About / PhoneBench structure that is intended to earn sitelinks.
- AGENTS.md and llms.txt at the site root for agent discoverability.

## Recommendation: noindex the app subdomains

As of the October 2026 audit, about 10 pages and subdomains are indexed, including app., dashboard., login., and beta. subdomains. An internal dashboard page and Spanish app UI text are indexed, which dilutes the brand results and exposes surfaces that are not marketing pages.

Recommended fix (separate live change, needs its own go-ahead, NOT done in this draft):

1. Serve an X-Robots-Tag: noindex header (or a robots meta tag where the surface serves HTML) on app., dashboard., login., and beta.
2. Give each of those subdomains a robots.txt with Disallow: / as a second layer.
3. After the headers are live, request removal of the already indexed URLs in Google Search Console.

## Recommendation: Google Business Profile

There is no knowledge panel yet. Claiming a Google Business Profile for Nivelato Labs would support one. This is a recommendation only; no profile was created by this draft.
