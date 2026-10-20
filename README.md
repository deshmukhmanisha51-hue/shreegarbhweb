# Shreegarbha Ayurved

Bilingual clinic site. English routes sit at the root. Marathi routes use the `/mr` prefix.

## Scripts

```bash
npm install
npm run dev
npm run build
npm run preview
```

## Environment

Copy `.env.example` to `.env`. `VITE_SITE_URL` defaults to `https://example.com` until the production domain is set. `VITE_WHATSAPP_E164` overrides the published WhatsApp number. GA4, GTM, Search Console, and Meta Pixel stay off while their variables are empty. Analytics events run only after a measurement ID is set and the visitor accepts cookies. Event parameters are categories such as page and language. Names, phone numbers, and message text are not sent.

`npm run build` writes an `index.html` for each English and Marathi route so link previews can read the title and description, and writes `public/sitemap.xml` and `public/robots.txt` from `VITE_SITE_URL`. A local video is added to structured data only when `public/media/video/<name>.json` includes a `title` and `description` beside a real video file.

## Media

Place files in:

- `public/media/logo/` — `logo.svg`, `logo.png`, or `logo.webp`
- `public/media/doctor/`
- `public/media/clinic/`
- `public/media/botanical/`
- `public/media/video/` — `name.mp4` or `name.webm`, with optional `name.webp` (or jpg/png) poster and `name.vtt` captions

Instagram post permalinks go in `instagramPosts` in `src/config/site.ts`. An empty list shows the profile card and does not load embed scripts.
- `public/media/suon/` — `logo.svg`, `logo.png`, or `logo.webp`
