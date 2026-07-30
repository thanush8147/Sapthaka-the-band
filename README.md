# Your Music Studio Website (offline, single-file)

## How to open it
Just double-click **index.html** — it opens in your browser and works with
**zero internet connection**. No install, no server, no build step. You can
put this whole folder on a USB drive, a laptop, anywhere, and it still works.

## Folder structure
```
studio-site/
├── index.html                 <- the whole website (open this)
├── README.md                  <- this file
└── assets/
    ├── images/
    │   ├── crew/               <- crew member photos go here
    │   └── gallery/             <- past-event / behind-the-scenes photos
    ├── audio/                   <- your music sample(s) (.mp3 recommended)
    └── video/                   <- past-event video clips (.mp4 recommended)
```

## What to customize (everything is marked with comments in index.html)
Open index.html in any text editor (Notepad, VS Code, etc.) and search for
the word **CUSTOMIZE** — every spot that needs your real info has a comment
right above it. In short, you'll replace:

1. **Studio name** — in the `<title>` tag and the `.logo` div in the header, and the footer line.
2. **Hero section** — headline, sub-line, and the two button links.
3. **Crew** — one `.crew-card` block per person: photo path, name, role, short bio.
   Drop photos into `assets/images/crew/` and point the `src=` at the filename.
4. **Music samples** — one `.track` block per song: title, tag line, and the
   `<audio src="...">` path. Drop your audio file(s) into `assets/audio/`.
5. **Upcoming events** — one `.event` block per event: date, event name,
   venue, and the RSVP/ticket link (or leave it as `#` if there's nothing to
   link yet).
6. **Gallery** — one `.gallery-item` block per photo or video. Photos use
   `data-type="image"`, videos use `data-type="video"`. Drop files into
   `assets/images/gallery/` or `assets/video/` and update the paths.
7. **Careers** — one `.career` block per open role, with a `mailto:` link so
   applicants can email you directly (no server or form backend needed).
8. **Contact & social** — your email, phone, address, and every social link
   (Instagram, YouTube, Facebook, Spotify icons are pre-built — just replace
   the `href="#"` with your real profile URLs. Delete any icon block you
   don't use, or duplicate one for a platform not listed).

## Adding more items
Anywhere you see a comment like `<!-- Duplicate a .track block ... -->`,
just copy the block above it, paste it below, and edit the copy. The layout
adjusts automatically (crew cards and gallery tiles reflow into a grid;
tracks and events stack in a list).

## Notes
- All fonts are system fonts (no Google Fonts, no internet needed) so text
  always renders correctly offline.
- All icons are hand-drawn SVG, not an icon font/CDN — also offline-safe.
- The audio/video tags use your local files directly — no upload step
  required, they just need to sit in the matching `assets/` folder.
- If you later want this live on the internet (a real domain), the exact
  same folder can be uploaded as-is to any static host (Netlify, GitHub
  Pages, Hostinger, etc.) with no changes.
