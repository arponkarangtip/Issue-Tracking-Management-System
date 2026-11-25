# Issue Tracker Pro — HTML/CSS/JS + Google Sheets Edition (v3)

## Setup & Deployment Instructions
1. Open https://sheets.new and create a new Google Sheet.
2. Click **Extensions -> Apps Script**, delete any default code, paste `backend/Code.gs`, and click **Save**.
3. Click **Deploy -> New deployment -> Web app** (**Execute as:** `Me`, **Who has access:** `Anyone`).
4. Copy the generated **Web app URL** (`https://script.google.com/macros/s/.../exec`).
5. Open `assets/js/gsheet-api.js` and paste the URL into `GSHEET_WEBAPP_URL`:
   ```javascript
   const GSHEET_WEBAPP_URL = "https://script.google.com/macros/s/YOUR_SCRIPT_ID/exec";
   ```
6. Open `index.html` in your browser (or deploy to GitHub Pages / Netlify / Vercel). The app connects to Google Sheets automatically in the background and initializes all 15 tables on first login.
7. Sign in with:
   - **Admin:** `admin@issuetracker.local` / `Admin@123`
   - **Intern:** `intern@issuetracker.local` / `Intern@123`
