FAQ Document - Corrected Android PWA

1. Create a PUBLIC GitHub repository, for example: FAQ
2. Upload ALL files in this folder to the ROOT of the repository.
3. GitHub: Settings -> Pages -> Deploy from a branch -> main -> / (root) -> Save.
4. Wait for GitHub Pages to publish the site.
5. Open the GitHub Pages URL in Chrome on your Samsung phone.
6. IMPORTANT: open the site first and wait a few seconds so the service worker can install.
7. In Chrome, open the menu (three dots). Look for "Install app".
8. If Chrome still says "Add to Home screen", check Chrome has loaded the site over HTTPS and reload once. On some Samsung/Chrome versions, the wording may still be "Add to Home screen" even when the shortcut behaves as a standalone web app.

The app intentionally opens a small launcher screen instead of immediately redirecting. This improves PWA installability and makes it behave more like an app.

Google Document:
https://docs.google.com/document/d/1S45W0eeV3lBunJOKlvEaHh_CecS7swXFApMTvVD5HSA/edit?tab=t.0

Scheduled automatic opening at 07:00, 10:00, 14:40, 17:00 and 21:10 still requires Android automation such as Tasker. A PWA cannot force Chrome to open itself in the foreground at scheduled times.
