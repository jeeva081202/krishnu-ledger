# Krishnu Cotton Sarees – Customer Ledger

Live app for GitHub Pages + Firebase (free).

## Files
| File | What it is |
|---|---|
| index.html | The full app |
| firebase-config.js | Paste your Firebase settings here (Step 2) |
| firestore.rules | Security rules – copy into Firebase (Step 4) |
| manifest.json, icon-*.png, apple-touch-icon.png | "Add to Home screen" app icon |
| logo.jpg, icon.jpg | Your logo |

> Do NOT upload `krishnu-data.json` (your customer data) to GitHub. Keep it on your phone/PC only.

## Step 1 – Create Firebase project (5 min)
1. Open https://console.firebase.google.com and sign in with your Gmail.
2. Click **Create a project** → name: `krishnu-ledger` → turn **off** Google Analytics → **Create project**.

## Step 2 – Get the config
1. On the project home page click the **</> (Web)** icon.
2. App nickname: `krishnu` → **Register app** (do NOT tick Firebase Hosting).
3. You'll see `const firebaseConfig = { apiKey: "...", ... }`.
4. Open `firebase-config.js` and replace each `PASTE_...` value with your values. Save.

## Step 3 – Turn on login and add the two users
1. Left menu **Build → Authentication → Get started**.
2. **Sign-in method → Email/Password → Enable → Save**.
3. **Users → Add user**: your email + a password. Add again for the owner's email + password.

## Step 4 – Create the database and lock it
1. **Build → Firestore Database → Create database**.
2. Location: **asia-south1 (Mumbai)** → **Start in production mode** → Create.
3. Open the **Rules** tab, delete everything, paste the contents of `firestore.rules`.
4. Replace `OWNER_EMAIL_HERE` with the owner's email (small letters) → **Publish**.

## Step 5 – Put it on GitHub Pages
1. https://github.com → **New repository** → name `krishnu-ledger` → Public → Create.
2. **Add file → Upload files** → drag in every file from this folder (not krishnu-data.json) → **Commit changes**.
3. Repo **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main** / **(root)** → Save.
4. After 1–2 minutes your link is: `https://YOUR-USERNAME.github.io/krishnu-ledger/`

## Step 6 – Allow your GitHub link in Firebase
Firebase → **Authentication → Settings → Authorized domains → Add domain** → `YOUR-USERNAME.github.io`

## Step 7 – Bring your old data in
1. Open the link, sign in.
2. **Admin → Restore from backup** → pick `krishnu-data.json` → **Restore**.

## Step 8 – Give it to the owner
Send the owner the link + their email/password. On the phone: open link in Chrome → ⋮ menu → **Add to Home screen**. It opens like an app with your logo.

## Every month
Admin → **Excel backup** and **Full backup (.json)**. Keep both safe.
