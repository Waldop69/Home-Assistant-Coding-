# Knights of Columbus Council 1016 — Website

A static HTML/CSS/JS website for Knights of Columbus Council 1016, built to be
uploaded directly to GoDaddy web hosting (or any standard web host) — no build
step or server required.

## Pages

- `index.html` — Home
- `newsletter.html` — Monthly newsletter + archive
- `calendar.html` — Calendar of events (Google Calendar embed + list view)
- `join.html` — Membership / how to join
- `fourth-degree.html` — Fourth Degree Knights / Assembly info
- `history.html` — History of the Knights of Columbus and Council 1016
- `links.html` — Parish, diocese, and other Catholic organization links
- `insurance.html` — Council insurance agent / Field Agent contact
- `dues.html` — Pay annual membership dues online (PayPal button)

Shared styles live in `assets/css/style.css`, shared nav-toggle script in
`assets/js/main.js`. Newsletter PDFs go in `assets/newsletters/`.

## Before you go live — replace the placeholders

Every page has yellow-dashed `placeholder` boxes and `[bracketed]` text
marking content you need to personalize:

- Real council address, phone number, and email throughout the footer
- Officer names/contacts (Grand Knight, Financial Secretary, Membership
  Director, Faithful Navigator, Field Agent)
- Meeting schedule and location
- Real parish, diocese, and state council links (`links.html`)
- Council founding year and history (`history.html`)
- Fourth Degree Assembly name/number and Honor Guard contact
  (`fourth-degree.html`)
- Google Calendar embed URL (`calendar.html`) — create a public Google
  Calendar, then Settings → "Integrate calendar" → copy the embed `src`
- Monthly newsletter PDFs in `assets/newsletters/` (see that folder's README)
- PayPal business email, dues amount, and return URLs in `dues.html` (see
  the "Setting This Up" section on that page for step-by-step instructions)

## Deploying to GoDaddy

1. In your GoDaddy account, make sure you have **Web Hosting** (cPanel or
   GoDaddy's file manager) attached to your domain — the drag-and-drop
   Website Builder won't accept these files.
2. Connect via GoDaddy's **File Manager** (in your hosting dashboard) or an
   FTP client (e.g. FileZilla) using the FTP credentials from your hosting
   account.
3. Upload the entire contents of this repository (all `.html` files plus the
   `assets/` folder) into your hosting account's public web root — usually
   `public_html/`.
4. Visit your domain to confirm the site loads, then click through every
   page/link to check for typos and broken links.

## Local preview

No build tools needed — just open `index.html` directly in a browser, or
run a simple local server from this folder:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
