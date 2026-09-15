FAQ Document - Corrected Android PWA

1. Create a PUBLIC GitHub repository, for example: FAQ
2. Upload ALL files in this folder to the ROOT of the repository.
3. GitHub: Settings -> Pages -> Deploy from a branch -> main -> / (root) -> Save.
4. Wait for GitHub Pages to publish the site.
5. Open the GitHub Pages URL in Chrome on your Samsung phone.
6. IMPORTANT: open the site first and wait a few seconds so the service worker can install.
7. In Chrome, open the menu (three dots). Look for "Install app".
8. If Chrome still says "Add to Home screen", check Chrome has loaded the site over HTTPS and reload once. On some Samsung/Chrome versions, the wording may still be "Add to Home screen" even when the shortcut behaves as a standalone web app.

UPDATED: index.html now auto-redirects to the Google Doc about 0.4 seconds after opening (just enough of a pause for Chrome to still treat it as a proper installed app). You'll see a brief flash of the launcher screen, then it jumps straight to the Doc. No tap needed.

To apply this update on your phone:
1. Upload this updated index.html to the same GitHub repository (overwrite the old one) - keep the other files (manifest.json, service-worker.js, icons) as they are.
2. Wait for GitHub Pages to redeploy (usually under a minute).
3. On your Z Fold 8, uninstall the existing app icon (long-press -> remove/uninstall).
4. Open the GitHub Pages URL again in Chrome, wait a few seconds, then use "Install app" from the Chrome menu again.
5. The new icon will now open straight into the Google Doc.

(If you don't uninstall/reinstall, the old cached version may keep showing the button - the service worker caches the page for offline use, so a plain reload isn't always enough.)

Google Document:
https://docs.google.com/document/d/1S45W0eeV3lBunJOKlvEaHh_CecS7swXFApMTvVD5HSA/edit?tab=t.0

Scheduled automatic opening at 07:00, 10:00, 14:40, 17:00 and 21:10 still requires Android automation such as Tasker. A PWA cannot force Chrome to open itself in the foreground at scheduled times.
