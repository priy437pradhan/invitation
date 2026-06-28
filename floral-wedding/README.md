# Digital Invitation Templates — pp.develper

Four ready-to-sell digital invitation websites. Each folder is **self-contained** — copy a
folder, swap the details/photos/music, deploy to Vercel, share the link.

## The four designs

| Folder | Best for | Look |
|---|---|---|
| `royal-wedding/` | Traditional Indian weddings | Maroon + gold, mandala that draws itself |
| `floral-wedding/` | Garden / modern weddings | Blush + sage, floral wreath |
| `birthday-pop/` | Kids & teens birthdays | Confetti, balloons, wobbling age badge |
| `birthday-elegant/` | Milestone birthdays (30/40/50) | Dark + gold, flickering candle |

## What every folder contains

```
folder-name/
├── index.html        ← the whole site (open this to preview)
├── images/
│   ├── cover.jpg      ← link-preview / share image (1200×630)
│   └── photo1-4.jpg   ← gallery photos
└── audio/
    └── music.mp3      ← background music (loops)
```

## How to preview

Just double-click `index.html` — it opens in any browser. (Music starts on the first tap,
because browsers block auto-playing sound.)

## Features in each template

- Animated hero (each design has its own signature animation)
- Live **countdown timer** to the event
- Event schedule / details with a **Google Maps** link
- Photo **gallery**
- **Guest RSVP** → sends to your WhatsApp
- **Pre-book this design** form (name, phone, date, design) → sends to your WhatsApp, **no
  confirmation step**
- Floating **WhatsApp chatbot** bubble (bottom-right) → opens a chat to **+91 70778 17064**
- **Background music** with a play/mute toggle (top-right)
- **Open Graph cover image** so the WhatsApp/Instagram link preview shows a nice thumbnail

## Customising for a client (per job)

Open `index.html` and edit:

1. **Names / age / title** — in the hero section (`<h1 ...>`).
2. **Date & countdown** — search for `EVENT_DATE = new Date("...")` near the bottom and set
   the real date/time. Also update the visible date text in the hero and details.
3. **Venue & map** — edit the schedule/details text and the `maps.google.com/?q=...` link.
4. **Photos** — drop the client's images into `images/` using the **same filenames**
   (`photo1.jpg` … `photo4.jpg`) and `cover.jpg`. Keep `cover.jpg` around 1200×630.
5. **Music** — replace `audio/music.mp3` with the client's track (same filename).
   Free, license-clean sources: Pixabay Music, YouTube Audio Library.
6. **WhatsApp number** — already set to `917077817064` (the `WHATSAPP` variable in the script
   and the footer). Change it if needed.

## Deploy to Vercel

1. Put the client's folder in its own GitHub repo (one repo per client = one clean link).
   ```
   cd folder-name
   git init
   git add .
   git commit -m "invite"
   git branch -M main
   git remote add origin https://github.com/YOUR-USER/CLIENT-REPO.git
   git push -u origin main
   ```
2. On vercel.com → **Add New → Project** → import that repo → **Deploy**.
   No build settings needed (it's a static site). You'll get a link like
   `client-name.vercel.app`.

## ⚠️ One step to make the share-preview image work

The cover image in the link preview needs the **real** Vercel URL. So:

1. Deploy first and copy your real link (e.g. `aarav-diya.vercel.app`).
2. In `index.html`, find `YOUR-LINK.vercel.app` (appears ~4 times near the top, in the
   `og:image`, `og:url`, and `twitter:image` tags) and replace it with your real domain.
3. Commit & push again.
4. Test the preview at **opengraph.xyz** before sending it to the customer (WhatsApp caches
   previews, so test on a fresh link).

## Note on the demo assets

The photos, cover images, and music in here are **original placeholders** I generated so the
folder works out of the box and nothing breaks. Replace them with the real client's photos and
song for each job.

---
pp.develper · Custom digital invitations · +91 70778 17064
