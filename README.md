# PATH — Study Companion

A mobile-friendly JEE study planner that runs as a static website.

## Features
- Daily tasks and habits
- Error notebook with review queue
- Doubt Manager: text, subject/chapter, priority/status, optional question photo, saved solution, and an Ask ChatGPT shortcut
- Study logs, progress dashboard, JSON backup/restore
- Local browser storage; no account or server required

## Publish / update on GitHub Pages
1. Download and extract this ZIP.
2. In your existing `path-study-app` GitHub repository, choose **Add file → Upload files**.
3. Upload/replace `index.html`, `sw.js`, `manifest.json`, `icon.svg`, `icon-192.png`, `icon-512.png`, and `README.md` from this folder. Keep filenames at repository root.
4. Commit changes to `main`. GitHub Pages should redeploy automatically.
5. Open your existing site in Safari and refresh. If the old version remains, close the tab and reopen it after a moment. On iPhone, if you installed the site on the Home Screen, you may need to remove the old shortcut and add it again to refresh its icon.

## Data safety
The app keeps data in localStorage under `pathDataV1`; this upgrade keeps that key and adds a `doubts` array, so existing tasks, errors, habits, and logs remain intact on the same browser/device. Before updating, use Progress → Export backup (.json) as a precaution. Imported older backups are supported; they start with an empty doubts list.

Question photos are resized to JPEG and stored in local browser storage. Very large collections of photos can eventually fill browser storage, so export backups regularly. The Ask ChatGPT button sends the doubt text in a prefilled ChatGPT prompt; it does not automatically upload the saved image. If the question is in the photo, attach it in the ChatGPT tab that opens.


## Handwritten mistake notes update
The Error notebook now includes a finger/stylus handwriting canvas. Draw equations or diagrams, then save the error; the drawing is stored with the mistake in local browser storage and appears inside its explanation. Existing entries without handwriting remain compatible. Export a backup before updating.
