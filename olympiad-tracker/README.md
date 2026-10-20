# Olympiad Tracker v3 — Offline-first PWA

## What's included
- Dashboard, hierarchical topic management, focus timer, study planner, problem attempts, analytics, local JSON backups.
- Personalized 20-week schedule (200 dated session slots) focused on AC then advanced physics, and geometry then algebra; astronomy mostly deferred until after regional.
- Eight original starter deep lessons with derivations, worked examples, and hidden hints; 18 short-break drills with expandable hints and answers.
- Mobile shortcut buttons for one-tap **Physics** or **Maths** timer start. Save sessions explicitly.
- Local-only IndexedDB: no cloud sync; upload/download backups for transfer.

## Fedora 44
Unzip; `cd olympiad-tracker`; run `python3 -m http.server 8080 --bind 127.0.0.1`; visit `http://127.0.0.1:8080` in Chromium or Chrome. Open browser menu > Install (if supported). The service worker can cache offline assets after the first online local visit.

## Android installation
This is a PWA, **not an APK**. To use on Android, upload the **contents** of `olympiad-tracker` to a new GitHub repository. Set **Settings > Pages > Deploy from branch > main / root**. Open resulting HTTPS URL in Chrome on Android. Choose menu > Add to Home screen / Install app. Load the app online once, then use offline. Public GitHub Pages hosts app source publicly (not browser's local study records). Do not upload exported backups to a public repo.

## Local data and upgrades
Existing data in IndexedDB is retained on a normal in-place app update. Topic additions are versioned. Timer status survives reload, but because elapsed time uses wall clock, manual changes to the device clock may affect it. The stopwatch is a study log, not a precision clock. When upgrading GitHub Pages, refresh online while connected and then reopen the installed PWA; cached updates might take a reload.

## Caveats
- Week dates and competition windows are provisional, not confirmed national deadlines.
- Not tested on physical Android/Fedora devices. Static syntax and headless browser checks are not full interaction tests.
- No automatic device synchronization or push reminders.
- A scheduled session is an assignment, not an automatically completed study log. Start/stop/save the timer separately.
- Lessons contain 8 detailed original starter modules; other weekly topics have a topic-specific plan rather than full textbook-length treatment.
