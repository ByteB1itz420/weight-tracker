# scale. - a quiet weight tracker

Public, no-account weight tracking web app. Anyone opens it, sets a goal, starts logging. All data stays on the visitor's device (localStorage); import/export JSON keeps logs portable. No backend, no tracking, no personal data in the bundle.

## Features
- First-run onboarding: current weight, goal weight, optional goal date (start weight becomes entry #1)
- One-tap daily log (date pre-filled today, weight pre-filled with last entry; same-date update)
- Trend chart (hand-rolled SVG, zero deps): daily line + 7-entry moving average + dashed goal line; ranges Last 30 / Last 90 / All
- Cut / bulk read: direction + pace from the last two 7-entry averages
- Stats: start, current, change, left to goal + progress bar; goal editable anytime
- Log list with per-entry delta and two-tap delete
- Export JSON / CSV, import JSON (accepts full state or a bare entries array)
- Light / dark / system theme with manual toggle

## Stack
Single static index.html, zero dependencies. Static hosting on Vercel.
## Seed links
One-tap restore links carry a full log as base64url JSON in the URL hash (#seed=...). Hash is never sent to the server and is stripped after load/dismiss.
