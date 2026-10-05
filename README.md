# Ruthreas — portfolio site

A static site. No build step, no server code, no external dependencies:
fonts and photographs are embedded in `index.html`.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole website |
| `404.html` | "Page not found" page (used automatically by Netlify, Vercel, GitHub Pages, Cloudflare Pages) |
| `favicon.svg`, `favicon.ico`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` | Browser and home-screen icons |
| `og-image.jpg` | Preview image shown when the link is shared |
| `site.webmanifest` | Icon and colour information for phones |
| `robots.txt` | Allows search engines to index the site |

## Hosting

Upload every file in this folder to the root of the site. Keep `index.html` at the top level.

- **Netlify:** app.netlify.com → Add new site → Deploy manually → drag this folder in.
- **Vercel / Cloudflare Pages:** create a project and upload this folder (no framework, no build command).
- **GitHub Pages:** put the files in a repository, then Settings → Pages → deploy from the main branch.
- **cPanel / Hostinger / GoDaddy:** upload the files into `public_html` with the file manager.
  If the 404 page does not appear on its own, add this line to `.htaccess`: `ErrorDocument 404 /404.html`

## After you have a domain

Link previews on WhatsApp and LinkedIn need the full address of the preview image.
In `index.html`, change

    <meta property="og:image" content="og-image.jpg">

to

    <meta property="og:image" content="https://YOUR-DOMAIN/og-image.jpg">

and add these two lines beside it:

    <meta property="og:url" content="https://YOUR-DOMAIN/">
    <link rel="canonical" href="https://YOUR-DOMAIN/">

## Editing content

Open `index.html` in a text editor and search for the comment markers:

- `<!-- 1 · OPENING -->` — title line and the three fields
- `<!-- 2 · IDENTITY -->` — introduction sentence and the three facts
- `<!-- 3 · WORK -->` — the three rows, organisations, and the "Now" line
- `<!-- 4 · THE ROOM -->` — headline, two captions, one sentence
- `<!-- TESTIMONIALS -->` — empty; add a section here when real quotes exist
- `<!-- 5 · CONTACT -->` — email, WhatsApp number, LinkedIn, Instagram

The WhatsApp links use `916384880470` (India code 91 + the number).

## Still to be supplied

- Role titles and dates for Edu Tantr and MACH IT (the site links to LinkedIn for now)
- Testimonials
