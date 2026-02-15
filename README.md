# RickRoute

I wanted a better link-in-bio than Linktree. The default ones feel generic—they don’t really capture who you are. So I built this: a single-page link hub that actually feels like *me*—dark, a bit of depth, and room for my agency, portfolio, podcast, writing, and socials in one place.

**Feel free to use it for yourself.** Fork it, host it anywhere (GitHub Pages, Netlify, Vercel, or plain static hosting), and make it yours. No backend, no signup—just one `index.html` and your assets.

---

## What’s in the box

- Single responsive page (mobile → tablet → laptop)
- Profile photo, headline, and CTAs
- Card grid: featured links (e.g. agency, portfolio), social/contact sidebar, podcast embed, writing & Dev.to
- Dark theme with subtle grid and glass-style cards
- SEO: canonical URL, robots meta, Open Graph & Twitter Card meta, theme-color, Schema.org JSON-LD (Person), plus `robots.txt`, `sitemap.xml`, `humans.txt`, and `.well-known/security.txt` for crawlers and attribution

---

## How to make it yours

### 1. Your identity & copy

- **Header**: Update the name in the `<h1>`, the tagline paragraph, and the profile image `alt` text.
- **Profile photo**: Replace `profile-photo.jpeg` with your own (same filename or update the `src` in the `<img>`).
- **Favicon**: Replace `logo.ico` with your icon (or change the `href` in the `<link rel="icon">` tags).

### 2. SEO & metadata (make it yours for search & social)

All of these live in the `<head>` of `index.html`. Use your name, your site URL, and a **full URL** for any image you want in link previews (e.g. `https://yourdomain.com/profile-photo.jpeg`).

| What | Where | Change to |
|------|--------|-----------|
| **Page title** | `<title>` | Your name and tagline (e.g. `Jane Doe – Creator & Developer`) |
| **Description** | `<meta name="description">` | One short sentence for search results and previews (~150 chars) |
| **Author** | `<meta name="author">` | Your name |
| **Keywords** | `<meta name="keywords">` | Comma‑separated terms you care about (optional but useful) |
| **Canonical URL** | `<link rel="canonical" href="...">` | Your live page URL (e.g. `https://yourdomain.com`) |
| **Theme color** | `<meta name="theme-color">` | Hex of your main background (e.g. `#030304`) |
| **OG title** | `<meta property="og:title">` | Same as or similar to `<title>` |
| **OG description** | `<meta property="og:description">` | Same as `name="description"` or a variant for social |
| **OG image** | `<meta property="og:image">` | **Absolute URL** to your preview image (e.g. profile photo) |
| **OG URL** | `<meta property="og:url">` | Same as canonical URL |
| **OG site name** | `<meta property="og:site_name">` | Your name or site name |
| **Twitter title** | `<meta name="twitter:title">` | Same as OG title |
| **Twitter description** | `<meta name="twitter:description">` | Same as OG description |
| **Twitter image** | `<meta name="twitter:image">` | Same absolute URL as `og:image` |
| **Twitter image alt** | `<meta name="twitter:image:alt">` | Short description of the image (e.g. your name) |
| **JSON-LD (Person)** | `<script type="application/ld+json">` | Update `name`, `url`, `description`, `image` to your details |

**Tip:** For link previews to show your image on Twitter, LinkedIn, etc., `og:image` and `twitter:image` must be **absolute** URLs (e.g. `https://yoursite.com/profile-photo.jpeg`), not relative paths.

### 3. Crawler & root files (robots, sitemap, humans, security)

These files help search engines and tools discover and understand your site. Replace any placeholder domain (e.g. `https://rickroutes.onrender.com`) with your live URL.

| File | Purpose | What to change |
|------|---------|----------------|
| **robots.txt** | Tells crawlers what they may index and where the sitemap is. | `Sitemap:` line → your domain, e.g. `https://yourdomain.com/sitemap.xml`. |
| **sitemap.xml** | Lists the page(s) for search engines. | `<loc>` → your full page URL (e.g. `https://yourdomain.com/`). Optionally update `<lastmod>` when you change the page. |
| **humans.txt** | Credits who built the site (humanstxt.org). Optional, no SEO impact. | Name, site, Twitter, location, last update. Remove or rewrite to credit yourself/team. |
| **.well-known/security.txt** | Security contact for vulnerability reports (RFC 9116). | `Contact:` → your `mailto:` or HTTPS contact. `Expires:` → date when this file is stale (max 1 year, ISO 8601). `Canonical:` → `https://yourdomain.com/.well-known/security.txt`. Re-update `Expires` periodically. |

**Note:** `robots.txt` and `sitemap.xml` must be served from the site root (same origin as your page). On GitHub Pages / Netlify / Vercel, put them in the repo root so they’re at `https://yourdomain.com/robots.txt` and `https://yourdomain.com/sitemap.xml`.

### 4. Links & CTAs

- **Top buttons**: Change the “Book a Consultation” and “Portfolio” `<a href="...">` and button text to whatever you use (e.g. Calendly, portfolio URL).
- **Grid cards**: Each card is an `<a href="...">` or a `<div>` with `<a>` inside. Search for the label (e.g. “Excelevate”, “Portfolio”, “LinkedIn”, “Email”, “The Podcast”, “Writing”, “Dev.to”) and update the `href` and the visible text/subtitles.
- **Email block**: There are two `mailto:` links—Personal and Work. Edit the `href` and the short labels (e.g. “Personal”, “Work”) as needed.
- **Footer**: Update the copyright name and the GitHub / LinkedIn (or other) icon links in the footer.

### 5. Podcast / embed

- The podcast card has a Spotify iframe. Replace the `src` URL with your show’s embed URL from Spotify (or swap the iframe for another provider’s embed code).
- Adjust the card title and description text to match your show.

### 6. Deploy & share

- **Local**: Open `index.html` in a browser.
- **Online**: Push the repo to GitHub and turn on GitHub Pages, or drag the folder into Netlify/Vercel for instant deploy.

---

No build step, no dependencies to install—just edit the HTML (and swap in your images and `logo.ico`), then ship it. If you use it, a link back or a star is appreciated but not required. Have fun making it yours.
