# littleSteps — MVP front-end prototype

A single-file, no-build HTML prototype of the littleSteps MVP (see the PRD). It demonstrates the full user journey for all four personas. There is no backend: sign-in, family sync, push reminders and offline sync are simulated, and all data is kept in the browser's `localStorage`.

## Run / deploy

Open `index.html` in a browser, or serve the folder from any static host (GitHub Pages, Netlify, Vercel, S3). No build step, no dependencies.

**GitHub Pages:** Settings → Pages → Deploy from branch → `main` / root.

On a wide screen a **demo guide** panel appears beside the phone frame with shortcuts (night feed, lock screen, partner sync, second child, larger text, offline, language, night mode, reset).

## What's covered

| PRD area | In the prototype |
|---|---|
| Accounts & region | US (Apple / Google / email) or China (WeChat / phone + SMS); region fixed at sign-up; parental consent; EN / 简体中文 |
| Family sharing | Invite by 6-digit code, link or QR (7-day, single use, revocable); join with a code; remove members; "leave and keep a copy"; simulated partner log arriving in ~3 s |
| Child profile | Multiple children, colour tags, switcher on every screen, edit, archive (stops reminders and celebrations) |
| Quick-log home | Status cards (last feed, sleep, last diaper), handover line, reminders, big one-handed buttons, "log for both" with 2+ children |
| Feeding | Breast timer with suggested side, switch side, per-side totals; bottle pre-filled with last amount (ml / oz); solids |
| Sleep | One-tap timer, nap vs night by time of day, missed-sleep entry, adjust a forgotten timer |
| Live timers | Lock-screen preview (Live Activity mock) with Switch side and Stop; timers store start timestamps |
| Diapers, growth | One-tap diaper; weight / length / head with WHO percentiles and growth curves |
| Milestones | Age-grouped checklist, tick with date / photo / note, custom milestones, gentle celebration (fades in night mode / reduced motion) |
| Vaccines & checkups | Regional schedule (CDC or China NIP), due soon / overdue reminders, mark done with clinic, skip; checkup schedule; doctor visits |
| Timeline | Day view, daily totals, 7-day feeding and sleep trend; edit, delete, move to another child |
| Integrity rules | Undo for 5 s after every save; "please check" for implausible values (bottle > 400 ml, weight change > 20 % in a week); future times and end-before-start blocked; possible-duplicate detection with merge |
| Offline | Simulated offline mode (also follows the real network state); queued entries sync on reconnect |
| Night mode & a11y | Auto night mode after sunset, manual override, larger text; AA-contrast palette from the PRD; labelled controls |
| Data | CSV export, delete account, privacy summary, source and "not medical advice" on every chart and schedule |

## Prototype limits (replace before production)

- **Content is demo data.** Growth tables embed WHO LMS values for 0–12 months only; CDC 2 y+ and China WS/T 423-2022 tables are not included. Vaccine, checkup and milestone lists are summaries for the demo and must be replaced with the official versioned JSON content and reviewed.
- No real authentication, server, push notifications or cross-device sync.
- Photos are referenced by file name only and not stored.
