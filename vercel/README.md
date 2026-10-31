# CAMS Alarm Explorer — Vercel deployment

Developed by Mohamed Badr.

This folder is the complete website: one static page (`index.html`) plus `vercel.json`.
There is no build step. Your CAMS exports are never uploaded — users import the sheet
and it is read inside their own browser.

Keep CAMS exports (`.csv` / `.xlsx`) **out of this folder**, so they are never published.

## Deploy with the Vercel CLI (Windows, from VS Code)

Needs Node.js (https://nodejs.org) and a free Vercel account.

1. Open a terminal in VS Code (`Ctrl + ``) and go into this folder:

   ```
   cd G:\rashpetco\VScode\CAMS_Tool\vercel
   ```

2. Install the CLI and log in (a browser window opens to confirm):

   ```
   npm i -g vercel
   vercel login
   ```

3. Deploy:

   ```
   vercel --prod
   ```

   On the first run, answer the prompts:
   - Set up and deploy? **Y**
   - Which scope? your account
   - Link to existing project? **N**
   - Project name: `cams-alarm-explorer` (or any name)
   - In which directory is your code located? **./**
   - Modify settings? **N**

   It prints the live URL, e.g. `https://cams-alarm-explorer.vercel.app`.

## Updating later

Replace `index.html` with the new version, then run `vercel --prod` again in this folder.

## Alternative: deploy from GitHub

Push this folder to a GitHub repository, then on vercel.com choose
**Add New → Project → Import** that repository and click **Deploy**
(Framework preset: *Other*, no build command, output directory: root).
Every push to the repository redeploys automatically.
