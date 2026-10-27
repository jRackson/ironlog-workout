IRONLOG — iPhone workout tracker
=================================

Included:
- index.html: the app
- manifest.json: installable web app settings
- sw.js: offline cache
- icon-192.png and icon-512.png: home-screen icons

IMPORTANT: iOS does not install a web app by opening a ZIP or a local HTML file. To use the Home Screen icon and offline caching, the files must be served from an HTTPS website. You do not need an App Store account.

EASIEST SETUP (GitHub Pages, free):
1. On a computer, open https://github.com and sign in/create an account.
2. Create a new public repository named ironlog-workout (a public repository is the simplest option for free GitHub Pages; the app data itself remains local to each device).
3. Upload all five files from this folder into the repository root: index.html, manifest.json, sw.js, icon-192.png, icon-512.png.
4. In the repository, open Settings → Pages.
5. Under Build and deployment, choose Deploy from a branch; select main and /(root), then Save.
6. Wait for the Pages URL to appear. It will look like https://YOUR-USERNAME.github.io/ironlog-workout/ .
7. On your iPhone 13, open that URL in Safari (not an in-app browser).
8. Tap the Share button → Add to Home Screen → Add.
9. Launch IronLog from the new icon. Open it once while online so the offline cache can install. Then test by switching Airplane Mode on and reopening it.

Using the app:
- Home: start the next session or choose one of five days.
- Workout: weights and reps are pre-filled with your targets. Adjust to what you actually lifted and tick each set. Completing a set starts a rest timer. An unfinished workout is restored if you close the app.
- Plan: rename days, add/remove exercises, and set sets, rep range, weight, weight jump and rest.
- Progress: see next targets for every exercise, view sessions, volume estimate, best logged weights, and optional bodyweight entries.
- History: inspect completed sessions.
- More: turn automatic progression on/off, export/import a JSON backup.

PROGRESSIVE OVERLOAD (automatic):
Each exercise has a rep range (e.g. 6-10), a weight and a weight jump (e.g. 2.5 kg). After you tap Finish & save:
- Hit the rep target on every set -> next time the target is 1 rep higher.
- Every set reaches the top of the range -> weight goes up by the jump and reps reset to the bottom of the range.
- Missed the target -> same weight and target repeat.
- Below the bottom of the range two sessions in a row -> weight drops about 10%.
- Skipped or partly finished exercises are left unchanged.
Leave a weight blank in Plan if unsure: enter it in your first workout and IronLog uses it as the starting point.
Your existing plan and history are kept when you update.

UPDATING AN EXISTING INSTALL:
Replace index.html and sw.js in your GitHub repository (upload and commit), wait a minute, then open the app online and close/reopen it once or twice to load the new version.

DATA / PRIVACY:
Workout data is stored in the browser's local storage on the device; the hosted files do not receive your logs. Export a backup regularly. Avoid clearing Safari website data, which may erase local logs. The app is offline-first after the first successful online load. iOS can pause timers when the app is backgrounded or the phone locks, so keep the timer visible and use the iPhone Clock as a backup for long intervals.

The starter split is Push / Pull / Legs / Upper / Lower. It is a template and can be edited to match your preferred exact routine. The app is a prototype and has not been submitted to the App Store.
