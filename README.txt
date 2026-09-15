FAQ Document - Corrected Android PWA

1. Create a PUBLIC GitHub repository, for example: FAQ
2. Upload ALL files in this folder to the ROOT of the repository.
3. GitHub: Settings -> Pages -> Deploy from a branch -> main -> / (root) -> Save.
4. Wait for GitHub Pages to publish the site.
5. Open the GitHub Pages URL in Chrome on your Samsung phone.
6. IMPORTANT: open the site first and wait a few seconds so the service worker can install.
7. In Chrome, open the menu (three dots). Look for "Install app".
8. If Chrome still says "Add to Home screen", check Chrome has loaded the site over HTTPS and reload once. On some Samsung/Chrome versions, the wording may still be "Add to Home screen" even when the shortcut behaves as a standalone web app.

UPDATED: index.html now only auto-redirects to the Google Doc when it is opened as the INSTALLED app (i.e. launched from the home-screen icon in standalone mode). When you open the page as a normal browser tab (e.g. to install/reinstall it), it behaves like before and does NOT redirect, so you have time to use the browser menu to install it. Once installed, tapping the icon jumps straight to the Doc after a brief flash of the launcher screen.

Works in both Chrome and Samsung Internet - both are Chromium-based on Android and support installable PWAs (manifest.json + service worker) the same way. In Samsung Internet the menu option may be called "Add page to" -> "Home screen" (it may show as a regular shortcut or as an app depending on version) instead of Chrome's "Install app", but the result is the same standalone app.

To apply this update on your phone:
1. Upload this updated index.html to the same GitHub repository (overwrite the old one) - keep the other files (manifest.json, service-worker.js, icons) as they are.
2. Wait for GitHub Pages to redeploy (usually under a minute).
3. On your Z Fold 8, uninstall the existing app icon (long-press -> remove/uninstall).
4. Open the GitHub Pages URL again in your browser as a normal tab, wait a few seconds, then install it from the menu.
5. The new icon will now open straight into the Google Doc; opening the same URL as a plain browser tab will still show the launcher screen.

(If you don't uninstall/reinstall, the old cached version may keep showing the button - the service worker caches the page for offline use, so a plain reload isn't always enough.)

Google Document:
https://docs.google.com/document/d/1S45W0eeV3lBunJOKlvEaHh_CecS7swXFApMTvVD5HSA/edit?tab=t.0

Scheduled automatic opening at 07:00, 10:00, 14:40, 17:00 and 21:10 still requires Android automation such as Tasker. A PWA cannot force Chrome to open itself in the foreground at scheduled times.
