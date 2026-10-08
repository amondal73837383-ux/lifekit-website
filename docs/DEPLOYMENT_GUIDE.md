# LifeKit — Complete Deployment Guide

## PART A — Prepare the website on Windows

You already have the tested APK:

C:\LifeKit2\lifekit\build\app\outputs\flutter-apk\LifeKit-v1.0.0.apk

### 1. Extract this ZIP

Extract the LifeKitWebsite ZIP somewhere easy, for example:

C:\LifeKitWebsite

### 2. Copy the APK

Open:

C:\LifeKit2\lifekit\build\app\outputs\flutter-apk\

Copy:

LifeKit-v1.0.0.apk

Paste it into:

C:\LifeKitWebsite\download\

Final result:

C:\LifeKitWebsite\download\LifeKit-v1.0.0.apk

### 3. Optional — add real screenshots

Take screenshots from your tested LifeKit app.

Put them in:

C:\LifeKitWebsite\assets\

The current website contains three placeholder screenshot panels. You can keep them for the first launch or replace them with real screenshots after deployment.

If you use PNG files, edit the three `<img src="...">` paths in index.html accordingly.

---

# PART B — Test the website locally

The website is static and can be opened directly.

Double-click:

index.html

Test:
- navigation
- Download button
- Privacy Policy
- mobile layout

For the APK download, make sure the APK is in the exact `download` folder.

---

# PART C — GitHub upload

Use your browser.

1. Open GitHub.
2. Sign in.
3. Create a NEW repository.
4. Repository name:
   `lifekit-website`
5. Public is recommended for the simple public website.
6. Create the repository.

### Upload

Upload the CONTENTS of:

C:\LifeKitWebsite

The GitHub repository root should look like:

index.html
privacy.html
style.css
script.js
README.md
assets/
download/

VERY IMPORTANT:
`index.html` must be at the root, not inside another `LifeKitWebsite` folder.

The APK must be:

download/LifeKit-v1.0.0.apk

Commit the changes.

---

# PART D — Vercel deployment

1. Open Vercel.
2. Sign in using GitHub.
3. Select Add New → Project.
4. Find `lifekit-website`.
5. Import it.

Because this is plain HTML/CSS/JavaScript:
- Framework Preset: leave as the automatically detected/static option.
- Build Command: leave empty if Vercel allows it.
- Output Directory: leave empty/default.
- Install Command: not needed.

Click DEPLOY.

Wait for deployment to finish.

Vercel will give you a public address similar to:

https://lifekit-website.vercel.app

Your exact address may be different.

---

# PART E — Test the live website

Open the Vercel URL on your Android phone.

Test:

1. Home page loads.
2. Features appear.
3. Screenshots appear.
4. Privacy Policy opens.
5. Download APK button works.
6. APK downloads completely.
7. APK installs.
8. LifeKit opens.

Also test the website from another phone if possible.

---

# PART F — Updating LifeKit

Suppose you build:

LifeKit-v1.1.0.apk

Replace the old APK in:

download/

Then update every occurrence of:

LifeKit-v1.0.0.apk

to:

LifeKit-v1.1.0.apk

Also change:
- version text
- release notes if you add them
- privacy policy if app behavior changed

Commit the changes to GitHub.

Vercel normally redeploys automatically.

---

# PART G — Future custom domain

Do NOT buy a domain yet if you want to keep the first launch at ₹0.

Use the Vercel address first.

Later, if you buy a domain such as:

lifekit.example

you can connect it from the Vercel project settings.

---

# PART H — What NOT to upload

Never upload these to the public website repository:

- passwords
- API keys
- `.env`
- Android signing private keys
- keystore passwords
- Firebase private service-account files
- database credentials
- Flutter `.dart_tool`
- Android build cache

The website repository is public-facing.

---

# PART I — Monetization

The current website does not include:
- advertisements
- AdMob
- subscriptions
- payments
- donations
- affiliate links

Do not add monetization until you decide exactly what model you want.

When you add advertising, analytics, payments, accounts or cloud sync, update the app's privacy disclosures accordingly.

---

# PART J — Final launch checklist

[ ] APK tested on your phone
[ ] APK tested on another Android phone
[ ] APK copied to website/download/
[ ] index.html is repository root
[ ] Download link tested
[ ] Privacy Policy tested
[ ] Mobile website tested
[ ] Vercel deployment successful
[ ] APK downloaded from live website
[ ] APK installed from live website
[ ] LifeKit opens after installation
