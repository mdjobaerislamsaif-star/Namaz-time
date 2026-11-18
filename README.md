# Namaz Time - installable app package

Files in this folder:

- `index.html` - the app (one file, calculates prayer times on the device)
- `manifest.webmanifest` - name, colors and icons, so phones can install it
- `sw.js` - makes it work offline after the first visit
- `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` - app icons

## 1. Put it online (free)

Upload the whole folder to any static host. It must be served over **https**.

- Netlify Drop: open app.netlify.com/drop and drag this folder in.
- GitHub Pages: create a repository, upload these files, turn on Pages in the repository settings.

You get a link like `https://your-name.netlify.app`.

## 2. Test the install

Open the link in Chrome on an Android phone. Open the menu and choose "Install app" (or "Add to Home screen"). The app should open full screen with its own icon. Turn on airplane mode and open it again to check offline use.

## 3. Play Store

Go to pwabuilder.com, enter your link, and follow its Android package steps. You need a Google Play developer account, and new personal accounts must run a closed test with at least 12 testers for 14 days before production access.

## Updating later

Change the files, then change `CACHE` in `sw.js` (for example `namaz-time-v2`) and upload again. Phones pick up the new version on the next visit.
