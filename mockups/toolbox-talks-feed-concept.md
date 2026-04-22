# Working LMS Feed Mockup (Toolbox Talks)

This mockup is now **interactive** and reads from `toolbox_talks_library.json`.

## What works
- Loads live talk data from `../toolbox_talks_library.json`
- Renders a scrollable card feed
- Search input (title/category/CFR)
- Hazard-category filter chips
- Sort options (recommended, talk number, duration, title)
- Sidebar stats and simple “trending” logic

## How to view locally
From repo root:

```bash
python -m http.server 8000
```

Then open:

- `http://localhost:8000/mockups/toolbox-talks-feed-mockup.html`

> Note: Opening the HTML directly as a `file://` URL may block JSON loading in some browsers. If that happens, run the local server command above.

## Next implementation step
If you want this in your LMS app directly, the next step is to port this into framework components (React/Vue/etc.) and wire CTAs (`Start Talk`, `Save`, `Assign Crew`) to real endpoints.
