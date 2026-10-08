# LifeKit Website — v1.0.0

This is the public download website for the LifeKit Android app.

## Folder structure

```text
LifeKitWebsite/
├── index.html
├── privacy.html
├── style.css
├── script.js
├── README.md
├── assets/
│   ├── logo.svg
│   ├── favicon.svg
│   ├── screenshot-1.svg
│   ├── screenshot-2.svg
│   └── screenshot-3.svg
└── download/
    └── LifeKit-v1.0.0.apk
```

## BEFORE UPLOADING

1. Copy your tested APK into `download`.
2. The APK must be named exactly `LifeKit-v1.0.0.apk`.
3. Optional: replace the three SVG screenshot placeholders with real screenshots from your phone. Keep the filenames:
   - `screenshot-1.svg` (or change the HTML if using PNG/JPG)
   - `screenshot-2.svg`
   - `screenshot-3.svg`

## IMPORTANT

The website does NOT need the Flutter project or Dart source code.

Only this website folder is uploaded to GitHub/Vercel.

## GitHub

1. Create a new repository, for example `lifekit-website`.
2. Upload the CONTENTS of this folder.
3. Make sure `index.html` is in the repository root.
4. Make sure the APK is inside:
   `download/LifeKit-v1.0.0.apk`

## Vercel

1. Sign in to Vercel with GitHub.
2. Add New Project.
3. Import the `lifekit-website` repository.
4. For this plain HTML/CSS/JS site, no framework is required.
5. Deploy.
6. Open the generated `.vercel.app` address.
7. Test the Download APK button from a phone.

## Updating the APK later

For LifeKit v1.1.0:

1. Put the new APK in `download`.
2. Update the download links in `index.html` from:
   `download/LifeKit-v1.0.0.apk`
   to:
   `download/LifeKit-v1.1.0.apk`
3. Update the visible version text.
4. Update the privacy policy if the app's data practices changed.
5. Commit/push to GitHub.
6. Vercel will redeploy automatically.

## Do not upload

Do not upload:
- Flutter build cache
- `.dart_tool`
- `android/.gradle`
- your Android Studio project
- signing keys
- API keys
- passwords
- `.env` files

This repository should contain the public website and the release APK only.
