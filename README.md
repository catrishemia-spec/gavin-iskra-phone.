# A Little World for Gavin Iskra

A responsive React + Vite interactive phone experience. The website begins at a lock screen and opens into seven working app-like spaces: Messages, Letters, Gallery, Music, Notes, Calendar, and Secret.

## Run locally

1. Install Node.js (LTS).
2. In this folder, run `npm install`.
3. Run `npm run dev` and open the local URL Vite prints.
4. For a production build, run `npm run build` (output is in `dist/`).

## Deploy to Vercel

1. Upload this folder to a GitHub repository.
2. In Vercel, choose **Add New → Project** and import the repository.
3. Vercel should detect Vite. Use build command `npm run build` and output directory `dist`.
4. Deploy.

## Customize the gift

Most editable content is in `src/main.jsx` near the top:

- `initialMessages`: sample conversation bubbles.
- `letters`: the letters (including the opening letter).
- `photos`: image URLs, captions, dates, and notes. Replace the sample Unsplash URLs with photos you have permission to use; local assets can be placed in `public/` and referenced as `/your-photo.jpg`.
- `tracks`: playlist titles. The player intentionally does not pretend to play audio. To enable actual playback, add a real audio file and wire an `<audio>` element to it; no audio source is included by default.
- `notes`: sticky-note content.
- Calendar currently uses October 2026 sample dates; edit the calendar component/data for real dates.

The chat lets you add messages during the current session; notes can be added during the current session. These are intentionally local UI interactions, not a cloud chat or shared messaging service. No login or database is required.

## Notes

- The design is original and only broadly inspired by modern smartphone interfaces.
- The first screen unlocks on tap/click or an upward touch swipe. The visible unlock button also supports mouse/touch.
- Includes responsive mobile layout, keyboard-accessible buttons, visible focus states, and reduced-motion support.
- Google Fonts and the gallery's sample images use external URLs, so replace them with local assets if you want the site to work fully offline.
