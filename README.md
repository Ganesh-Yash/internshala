# internshala

A tiny, dependency-free **Internship Tracker** — keep every internship application (company, role, source, date, status, stipend, link, notes) in one place.

It is a single `index.html` file. There is no build step, no framework, no backend and no account: everything is stored in your browser's `localStorage`, so your data never leaves your device.

## Features

- Add, edit and delete applications
- Status pipeline: Wishlist → Applied → Shortlisted → Interview → Offer / Rejected
- Live counters (total, in progress, offers, rejected)
- Search across company, role, source, stipend and notes, plus a status filter
- "Days since applied" hint for applications that are still in progress
- Export / import your data as JSON (for backups or moving to another device)
- Responsive layout with automatic light/dark theme

## Getting started

Open `index.html` in any modern browser — that's it.

If you prefer serving it over HTTP (for example to test on a phone on the same network):

```bash
# Python 3
python3 -m http.server 8000

# or Node.js
npx serve .
```

Then visit <http://localhost:8000>.

## Project structure

```
.
├── index.html   # the whole app: markup, styles and script
├── .gitignore
└── README.md
```

## Notes on data

- Data is saved under the `localStorage` key `internshala.applications.v1`.
- Clearing site data in your browser will delete it — use **Export JSON** for a backup.
- **Import JSON** merges by `id`: existing entries are updated, new ones are added.

## License

MIT
