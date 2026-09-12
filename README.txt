Gaming Network Helper — PWA Package
========================================

Files
-----
index.html               Main app.
manifest.webmanifest     PWA/app metadata.
sw.js                    Service worker for offline caching.
icon-192.png             192×192 app icon.
icon-512.png             512×512 app icon.
privacy-policy.html      Privacy policy page for publishing.
README.txt               This setup guide.

GitHub Pages
------------
1. Create a GitHub repository.
2. Put all files in the repository root.
3. Enable GitHub Pages from Settings → Pages.
4. Select the branch/folder that contains these files.
5. Open the published HTTPS URL.
6. Test the app and confirm the manifest/service worker load.

Important
---------
- GitHub Pages must be served over HTTPS for PWA installation/service-worker
  functionality.
- Before Play Store submission, replace the contact placeholder in
  privacy-policy.html with a real developer contact address.
- The current index.html performs its network test against
  https://speed.cloudflare.com. Browser/network policies can affect the test.
- The app does not implement auto-aim, injection, game-file modification,
  memory modification, or bypass features.

PWABuilder / Android
--------------------
Use the HTTPS GitHub Pages URL as the starting point in PWABuilder.
Run its validation checks, review the generated Android package settings,
and provide your final privacy-policy URL when required.

If you change app files, update CACHE_NAME in sw.js (for example v2) when
you want browsers to clearly recognize a new service-worker cache version.
