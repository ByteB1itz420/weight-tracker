# scale.

A quiet weight tracker. No account, no server, no tracking - every entry lives in your browser's localStorage on your device and never leaves it unless you export it yourself.

**Try it:** open `index.html` in any browser, or visit the hosted deployment. That's the whole setup.

## What you get

- **One-tap daily log** - date pre-fills to today, weight pre-fills to your last entry. Logging the same date again updates it.
- **Trend chart** - your daily line, a 7-entry moving average (so one noisy day doesn't fool you), and your goal as a dashed line. Last 30 / Last 90 / All ranges.
- **Cut / bulk read** - compares your last two 7-entry averages and tells you whether you're cutting, bulking, or holding, with pace per 7 entries.
- **Stats** - start, current, change, left to goal, 7-entry average, overall average, and a week-by-week line (this calendar week vs last week, Monday to Sunday).
- **Goal tracking** - set a goal weight (and optional date) on first run; edit it any time. Progress bar fills as you close in.
- **Full control of your log** - tap any entry's weight to edit it inline, tap x to delete it (with an explicit confirm). Works on every point, not just the latest.
- **Portable data** - export to JSON or CSV, import JSON back. Moving devices is one export and one import.
- **Seed links** - a full log can travel as base64url JSON in a link's `#seed=` hash. The hash is never sent to any server; one tap on the banner loads it. Handy for restoring a backup or sharing a log with yourself.
- **Light / dark / system theme** with a manual toggle.

## Run it yourself

It's a single static `index.html` with zero dependencies and no build step.

```bash
# any static server works
npx serve .
# or just double-click index.html
```

Deploy by dropping the file on any static host (Vercel, Netlify, GitHub Pages, a Raspberry Pi).

## Privacy

There is no backend. Nothing is sent anywhere: no analytics, no cookies, no accounts. Your data lives in `localStorage` under one key; "Reset everything" in the footer wipes it. Export before you clear your browser data - clearing site data clears your log.
