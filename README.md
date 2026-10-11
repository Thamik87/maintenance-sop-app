# Maintenance SOP Builder — prototype v0.1

A mobile-first, offline-capable web app prototype for collecting maintenance work records and drafting repeatable SOPs.

## Included
- Work order number, asset number, claimed fault
- Safety / LOTO notes, tools, parts, lessons learned, outcome
- Chronological steps with description, notes, multiple photos per step
- Browser speech recognition where supported; phone keyboard microphone is a fallback
- Local draft library using IndexedDB
- JSON export/import backup
- Print / Save as PDF from the browser
- Service worker cache for offline use after the app has first been loaded from a web server
- GitHub Actions workflow to publish to GitHub Pages

## Important limitations
- This is a prototype, not a certified safety system or approved document-control system.
- Data is stored in the current browser profile on the current device. Clearing browser data may erase records. Export backups regularly.
- Photos can consume significant browser storage. If saving fails, reduce photo count/size and export backups.
- Voice recognition varies by browser/device and may use an online speech service. It is not guaranteed offline.
- AI summarization is not implemented in this version. Review and edit notes manually; never send company-sensitive content to an external AI without authorization.
- Do not use this prototype as a substitute for approved LOTO procedures, permits, verification, or formal SOP approval.

## Publish from your Android phone
1. Create a repository on GitHub. A private repository is fine for storing the source, but remember that the published Pages site may be public depending on your GitHub plan and repository settings. Do not upload company-sensitive source/data.
2. Upload the contents of this folder to the repository root, including the hidden `.github/workflows/deploy-pages.yml` file. GitHub mobile web may make uploading hidden files awkward; use GitHub's web interface or a browser in Desktop site mode.
3. In repository **Settings → Pages**, select **GitHub Actions** as the build/deployment source if prompted.
4. Open **Actions** and wait for the “Deploy Maintenance SOP Builder to GitHub Pages” workflow to finish successfully.
5. Open the Pages URL shown by the workflow in Android Chrome. Use Chrome's menu → **Add to Home screen**.
6. Load the site once while online. Then test airplane mode, creating a test record, adding a step/photo, saving, exporting/importing a backup, and printing to PDF.

## Before using real plant records
Get company IT/security approval for hosting, personal-device storage, maintenance photos, and any voice service. GitHub Pages is generally public hosting; do not publish real company data there. For real use, host the app on an approved private HTTPS location.
